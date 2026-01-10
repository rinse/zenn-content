---
title: "圏論のHaskellへの応用"
free: false
---

## Hask圏

Haskellの型を対象、関数を射、関数合成を射合成に対応させた圏を、Hask圏と呼ぶ。

Hask圏の定義は曖昧で、例えばbottomなどが恣意的に使われ、しばしばHaskellのサブセットを想定する。

https://wiki.haskell.org/Hask

## "実用的な"Hask圏の性質

- Hask圏は[始対象と終対象](./initial-objects)を持つ
    * `Void`が始対象、`()`が終対象である
- Hask圏は[完備かつ余完備](./complete)である
    * すなわち任意の型どうしの直積・直和が存在する
- Hask圏は[局所小](./largeness-of-categories)である
- `Functor`のインスタンスは[自己関手](./endo-functor)である
- `Monad`のインスタンスは[モナド](./monad)である
- WriterモナドはReaderモナドの[左随伴](./adjunction-hom-functor)
    * `(a,) -| (a ->)`が成り立つ
    * ここで随伴を定める自然同型は、カリー化と非カリー化である
    * この[随伴から導かれるモナド](./adjunctions-derive-monads)はStateモナドであり、
      同様に導かれるコモナドはStoreコモナドである。

## 諸概念のHaskell上での表現

いくつかの圏論的な概念をHaskellで書いていく。

### 関手

Preludeの`Functor`型クラスは自己関手$F : \mathbf{Hask} \to \mathbf{Hask}$である。

ここで定義する型クラスは、$\mathbf{C}$から$\mathbf{D}$への関手を表す型クラスである。

```Haskell
class Functor c d f | f -> c, f -> d where
  map :: c a b -> d (f a) (f b)
```

これにより`Contravariant`を特別に用意することなく、反変関手を表現できる。

```Haskell
type Hask = (->)

instance Functor Hask Hask Maybe where
  map _ Nothing = Nothing
  map f (Just a) = Just (f a)

instance Functor Op Hask Predicate where
  map (Op f) (Predicate pred) = Predicate $ pred . f
```

https://play.haskell.org/saved/mbQP5kUM

### 随伴関手

かなりお気に入り。

`f a -> b`と`a -> g b`の同型か、unit - counit恒等式のどちらかが定義されれば、他方は自動的に定義される。

```Haskell
class (Functor f, Functor g) => f -| g where
  hom  :: (f a -> b) -> a -> g b
  hom' :: (a -> g b) -> f a -> b
  unit :: a -> g (f a)
  counit :: f (g a) -> a
  
  hom  f = fmap f . unit
  hom' f = counit . fmap f
  unit   = hom id
  counit = hom' id
```

Haskellでの有名な随伴として`Reader`モナドと`Writer`モナドが存在する。

```Haskell
type Writer w = (,) w
type Reader r = (->) r

instance Writer a -| Reader a where
  hom  f b = \a -> f (a, b)
  hom' f (b, a) = f a b
```

そしてこの随伴関手対から得られるモナドは、`State`モナドに一致する。
次の通り`State`を定義すると、コンストラクタとデコンストラクタがそのまま同型射になる。

```Haskell
newtype State s a = State
  { runState :: s -> (s, a)
  }

iso :: State s a -> Reader s (Writer s a)
iso = runState

iso' :: Reader s (Writer s a) -> State s a
iso' = State
```

またこの随伴関手対から得られるコモナドは、`Store`コモナドに一致する。

```Haskell
newtype Store s a = Store
  { runStore :: (s, s -> a)
  }

iso :: Store s a -> Writer s (Reader s a)
iso = runStore

iso' :: Writer s (Reader s a) -> Store s a
iso' = Store
```

https://play.haskell.org/saved/eND2RxdK

### 随伴関手から得られるモナド

すでに`Writer -| Reader`から`State`モナドを得られることを確認したが、
一般に、随伴$F \dashv G$からモナド$G \circ F$を得られる。

まず関手の合成を次のように定義する。関手の合成は関手である。

```Haskell
newtype (g :. f) a = Composition
  { unComposition :: g (f a)
  }

instance (Functor f, Functor g) => Functor (g :. f) where
  fmap f (Composition a) = Composition $ (fmap .fmap) f a
```

そうすると`f -| g`からモナド`g :. f`のインスタンスが得られることを確認できる。

```Haskell
instance f -| g => Applicative (g :. f) where
  pure = Composition . unit
  (<*>) = ap

instance f -| g => Monad (g :. f) where
  Composition m >>= f = Composition $
    let f' = unComposition . f
        gfgfb = (fmap . fmap) f' m
     in fmap counit gfgfb
```

同じようにして、コモナドのインスタンスも得られる。

https://play.haskell.org/saved/0iwJUq4y

### 自然変換

自然変換$\eta : F \Rightarrow G$を次のように書ける。
`=>`は予約されているので、苦肉の策で`~>`を使っている。

```Haskell
type f ~> g = forall a. f a -> g a
```

例えば`maybeToList`を次のように書ける。

```Haskell
maybeToList :: Maybe ~> []
maybeToList Nothing = []
maybeToList (Just a) = [a]
```

https://play.haskell.org/saved/4VEy6T7g

### 米田の補題

[米田の補題](./yoneda-lemma)とは、$A$を固定した米田埋め込みから集合値関手$F$への自然変換全体の集合が$F(A)$と同型になるという定理だった。

$$
F(A) \simeq \hom_{\mathbf{Set}^\mathbf{C^{\mathrm{op}}}}(\hom_{\mathbf C}(-, A), F)
$$

Haskellでは上の等式の右辺を、米田埋め込みと自然変換を使って次のように定義できる。

```Haskell
newtype Y a b = Y (b -> a)
type f ~> g = forall a. f a -> g a

newtype Yoneda f a = Yoneda (Y a ~> f)
```

`Yoneda f a`と`f a`の間の同型射は次の写像で与えられる。

```Haskell
yoneda :: Yoneda f a -> f a
yoneda (Yoneda f) = f (Y id)

yoneda' :: Contravariant f => f a -> Yoneda f a
yoneda' a = Yoneda $ \(Y f) -> contramap f a
```

`Yoneda f`は定義に照らして自明に（反変）関手を実装する。

```Haskell
instance Contravariant (Yoneda f) where
  contramap f (Yoneda g) = Yoneda $ \(Y h) -> g (Y (f . h))
```

https://play.haskell.org/saved/U3Gtc4aH

### 余米田の補題

[余米田の補題](./coyoneda-lemma)とは、米田の補題を右Kan拡張で表したときに、同じものを左Kan拡張で表したものであった。

$$
F(A) \simeq \int^{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C}(A, C) \times F(C)
$$

Haskellでは一般的に次のように表される。

```Haskell
data Coyoneda f b = forall a. Coyoneda (a -> b) (f a)
```

分かりやすさと実装上の都合で少し式を変形しているので、それを追っていこう。
まず変数名から合わる。Haskellコードでは`b`を固定していて、コエンドの変数として`a`を利用している。
次に`f`が共変関手を想定しているので、これに合わせてopの取り方を変える。
最後にhom集合のopを取れば、Haskellコードに対応する式が得られる。

$$
\begin{aligned}
F(B) &\simeq \int^{A \in \mathbf C^\mathrm{op}} \hom_{\mathbf C}(B, A) \times F(A) \\
&\simeq \int^{A \in \mathbf C} \hom_{\mathbf C^\mathrm{op}}(B, A) \times F(A) \\
&\simeq \int^{A \in \mathbf C} \hom_{\mathbf C}(A, B) \times F(A) \\
\end{aligned}
$$

同型射は次のように得られる。

```Haskell
coyoneda :: Functor f => Coyoneda f a -> f a
coyoneda (Coyoneda f a) = fmap f a

coyoneda' :: f a -> Coyoneda f a
coyoneda' = Coyoneda id
```

また`Coyoneda f`は定義に照らして自明に関手を実装する。
ここで`f`が共変関手になるように式変形を行っていたのが活きる。

```Haskell
instance Functor (Coyoneda f) where
  fmap f (Coyoneda g a) = Coyoneda (f . g) a
```

https://play.haskell.org/saved/kjk4Pb7e
