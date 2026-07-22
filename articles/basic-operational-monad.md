---
title: "Operationalモナドの基礎【Haskell】"
emoji: "🧩"
type: "tech"
topics: ["Haskell", "Monad", "CategoryTheory"]
published: true
---

## はじめに

Operational モナドとは、特定のアクションを備えたモナドの構造を表現するモナドである。

作成したモナドから、アクションを実装する任意のモナドへの自然変換を定義でき、OOP のインターフェースのように利用できる。

Operational モナドは、2つのコンポーネントから成り立つ。

- `Coyoneda` 構成
  * カインド `Type -> Type` を持つ任意の型構築子から関手を作る
- 自由モナド
  * 任意の関手をモナドに持ち上げる

これらにより、例えば以下のような命令から

```Haskell
data CommandF a where
  PutStrLnF :: String -> CommandF ()
  GetLineF  :: CommandF String
```

以下のようなアクションを備えたモナド `Command` を得られる。(`liftOperational` の定義は後述)

```Haskell
putStrLn' :: String -> Command ()
putStrLn' = liftOperational . PutStrLnF

getLine' :: Command String
getLine' = liftOperational GetLineF
```

`Command` はモナドなので、命令によって備えたアクションと、一般のモナドが持つアクションを利用できる。

```Haskell
helloWorld :: Command ()
helloWorld = do
  putStrLn' "Hello, Operational Monad!"
  getLine' >>= putStrLn'
  replicateM_ 3 $
    putStrLn' "Operational monads are fun!"
```

命令と、別のモナドが備えるアクションとの変換表を作成すると、`Command` モナドをそのモナドとして実行できるようになる。 (`interpretOperational` の実装は後述)

この変換表を複数作成できるため、`Command` モナドは複数の解釈を持てる。

```Haskell
interpretCommandFAsIO :: CommandF a -> IO a
interpretCommandFAsIO (PutStrLnF s) = putStrLn s
interpretCommandFAsIO GetLineF = getLine

runCommandAsIO :: Command a -> IO a
runCommandAsIO = interpretOperational interpretCommandFAsIO
```

## 自由モナド

この記事では、自由モナドを次のように定義する。`f` はモナドに備えさせたいアクションを一層分だけ表す関手である。

```Haskell
data Free f a
  = Pure a
  | Bind (f (Free f a))

instance Functor f => Functor (Free f) where
  fmap f (Pure a) = Pure (f a)
  fmap f (Bind next) = Bind (fmap (fmap f) next)

instance Functor f => Applicative (Free f) where
  pure = Pure
  Pure f <*> x = fmap f x
  Bind next <*> x = Bind (fmap (<*> x) next)

instance Functor f => Monad (Free f) where
  Pure a >>= f = f a
  Bind next >>= f = Bind (fmap (>>= f) next)
```

`Free f` は `f` の層を重ねたデータである。
`Pure` は計算の結果を、`Bind` は `f` の一層と、その中に配置された後続の計算を表す。
一つの層に含まれる後続の計算の数は `f` によって異なり、この例の `CommandF` では一つの命令とその後続に対応する。
`Functor`、`Applicative`、`Monad` のインスタンスは、この構造を保ったまま計算をつなげる。

`f` の値を自由モナドのアクションへ持ち上げる関数が `liftF` である。

```Haskell
liftF :: Functor f => f a -> Free f a
liftF = Bind . fmap Pure
```

実際に、標準入出力の命令を表す関手からモナドを作ってみよう。
自由モナドへ直接渡す `CommandF` は、それぞれの命令に後続の計算を持たせて定義する。

```Haskell
data CommandF cont
  = PutStrLn String cont
  | GetLine (String -> cont)

instance Functor CommandF where
  fmap f (PutStrLn s cont) = PutStrLn s (f cont)
  fmap f (GetLine cont) = GetLine $ \s -> f $ cont s
```

型引数 `cont` は命令の後に続く計算である。
`PutStrLn` は文字列を出力した後、値を受け取らずに `cont` へ進む。
`GetLine` は入力された文字列を `String -> cont` に渡して次の計算へ進む。

この関手を `Free` に渡すと、標準入出力のアクションを備えた `Command` モナドが得られる。

```Haskell
type Command = Free CommandF

putStrLn' :: String -> Command ()
putStrLn' s = liftF (PutStrLn s ())

getLine' :: Command String
getLine' = liftF (GetLine id)
```

このように自由モナドを直接使う場合、各命令は後続の計算を保持し、それを写す `Functor` を実装する必要がある。
命令が増えるたびに同じような継続と `fmap` の処理を書くことになる。

一方、GADT版の `CommandF` は、型引数を各命令の戻り値として使うため、継続を直接は持たず `Functor` も実装できない。
次に、この違いを `Coyoneda` で吸収する。

## Coyonedaで任意の型構築子を関手にする

「はじめに」で述べた一つ目のコンポーネントは、任意のカインド `Type -> Type` の型を関手へ持ち上げることであった。
この役割を担う `Coyoneda` は、存在型を使って次のように定義できる。

```Haskell
{-# LANGUAGE GADTs #-}

data Coyoneda f a where
  Coyoneda :: (x -> a) -> f x -> Coyoneda f a
```

`Coyoneda f a` は、ある型 `x` に対する `f x` と、その `x` を結果の型 `a` へ変換する関数を組にして持つ。
`x` が具体的に何であるかは、`Coyoneda` の外側からは分からない。

この型は、`f` に何の制約も課さずに `Functor` を実装できる。

```Haskell
instance Functor (Coyoneda f) where
  fmap f (Coyoneda g x) = Coyoneda (f . g) x
```

`fmap` が操作するのは変換関数 `x -> a` だけであり、`f x` には触れない。
変換を実行せずに関数合成として蓄積するため、内側の `f` が `Functor` である必要はない。

`f a` は、恒等関数と組み合わせるだけで `Coyoneda f a` へ持ち上げられる。

```Haskell
liftCoyoneda :: f a -> Coyoneda f a
liftCoyoneda = Coyoneda id
```

反対に `Coyoneda f a` を `f a` へ戻すには、蓄積した関数を `fmap` で適用する必要がある。

```Haskell
lowerCoyoneda :: Functor f => Coyoneda f a -> f a
lowerCoyoneda (Coyoneda f x) = fmap f x
```

`liftCoyoneda` によって、GADT版の `CommandF` のように `Functor` ではない命令の型も `Coyoneda CommandF` という関手へ持ち上げられる。
この `Coyoneda` 構成が、Operationalモナドを構成する一段目の変換である。

ここで、任意の型構築子から `Coyoneda f` を作ること自体と、余米田の補題は区別する必要がある。
`f` が関手である場合、`liftCoyoneda` と `lowerCoyoneda` は `f` と `Coyoneda f` の同型の両方向に対応する。
この同型を与えるのが余米田の補題である。
圏論的には、共変関手 $F$ に対して次の同型が成り立つ。

$$
F(A) \simeq \int^{X \in \mathbf{C}} \hom(X, A) \times F(X)
$$

右辺の $\hom(X, A)$ が `x -> a`、$F(X)$ が `f x` に対応している。
より詳しい対応については、圏論勉強ノートの[余米田の補題の Haskell での表現](https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/haskell#余米田の補題)を参照してほしい。

## Operationalモナドを作る

ここまでに、次の二つの変換を用意した。

1. `Coyoneda` 構成によって任意の型構築子 `f` から関手 `Coyoneda f` を作る
2. `Free` によって任意の関手をモナドへ持ち上げる

これらを合成したものを `Operational` と呼ぶ。

```Haskell
type Operational f = Free (Coyoneda f)
```

この構成により、`f` が `Functor` でなくても `Operational f` はモナドになる。

次に、`f` が表す一つの命令を `Operational f` のアクションへ持ち上げる関数を定義する。

```Haskell
liftOperational :: f a -> Operational f a
liftOperational = liftF . liftCoyoneda
```

`liftCoyoneda` が `f a` を `Coyoneda f a` へ、`liftF` がそれを `Free (Coyoneda f) a` へ持ち上げる。
`liftF` 自体には `Functor` 制約があるが、渡している `Coyoneda f` は常に関手なので、`liftOperational` の型には `Functor f` が現れない。

したがって、利用者はアクションの定義 `f` に `Functor` を実装することなく、`liftOperational` によってOperationalモナドのアクションを追加できる。

## 命令を定義する

Operationalモナドの利用者が定義するのは、モナドに備えさせたい命令と、それらをアクションとして公開する関数である。

標準出力と標準入力を抽象化する `Command` インターフェースを作る例を考える。
まず、命令とその戻り値をGADTで定義し、`Operational` に渡す。

```Haskell
data CommandF a where
  PutStrLnF :: String -> CommandF ()
  GetLineF  :: CommandF String

type Command = Operational CommandF
```

各命令を `liftOperational` で持ち上げると、`Command` が備えるアクションになる。

```Haskell
putStrLn' :: String -> Command ()
putStrLn' = liftOperational . PutStrLnF

getLine' :: Command String
getLine' = liftOperational GetLineF
```

`Command` を使う側から見ると、`putStrLn'` と `getLine'` は OOP のインターフェースに定義された抽象的なメソッドのように解釈できる。
利用者はこれらが最終的にどのモナドで実行されるかを知らなくても、`do` 記法で処理を記述できる。

```Haskell
helloWorld :: Command ()
helloWorld = do
  putStrLn' "Hello, Operational Monad!"
  getLine' >>= putStrLn'
  replicateM_ 3 $
    putStrLn' "Operational monads are fun!"
```

この時点では命令を組み立てただけであり、標準入出力はまだ実行されていない。
`helloWorld` は `Command` インターフェースだけに依存した、実行前のプログラムを表す値である。
命令の具体的な意味は、次に定義するインタプリタによって決まる。

## インタプリタを作る

インタプリタは、Operationalモナドが備える抽象的なアクションと、実行先のモナドが備える具体的なアクションとの変換表である。

まず、`CommandF` の各命令を `IO` の操作へ対応付ける。
GADTのパターンマッチによって、それぞれの命令が返す型に応じた処理を書くことができる。

```Haskell
interpretCommandFAsIO :: CommandF a -> IO a
interpretCommandFAsIO (PutStrLnF s) = putStrLn s
interpretCommandFAsIO GetLineF = getLine
```

次に、`Coyoneda` の変換を一般化する。
命令 `f x` を `m x` へ変換した後、`Coyoneda` に蓄積されていた `x -> a` を `fmap` で適用すればよい。
引数の変換はすべての `x` に対して使えなければならないため、ここでは `RankNTypes` 拡張を使う。

```Haskell
{-# LANGUAGE RankNTypes #-}

interpretCoyoneda
  :: Functor m
  => (forall x. f x -> m x)
  -> Coyoneda f a
  -> m a
interpretCoyoneda interpret (Coyoneda f x) =
  fmap f (interpret x)
```

自由モナドのインタプリタも同様に一般化できる。

```Haskell
interpretFree
  :: Monad m
  => (forall x. f x -> m x)
  -> Free f a
  -> m a
interpretFree _ (Pure a) = pure a
interpretFree interpret (Bind next) =
  interpret next >>= interpretFree interpret
```

### 自由モナドの解釈は畳み込みである

ここで、モノイドとモナドの対応関係に注目したい。
正確には、モナドは自己関手の圏において、関手の合成を積としたモノイド対象である。
この対応のもとでは、自由モナドは自由モノイドに対応する。

Haskellにおける代表的な自由モノイドはリストである。
`[a]` は `a` の値を生成元とする自由モノイドであり、各生成元をモノイド `w` の値へ写す関数を与えると、`foldMap` によってリスト全体を `w` へ畳み込める。

```Haskell
foldMap :: Monoid w => (a -> w) -> [a] -> w
```

自由モナドに対する `interpretFree` も同じ役割を持つ。
各生成元に相当する `f` の一層をモナド `m` のアクションへ写す変換を与えると、`Free f` 全体を `m` へ畳み込める。

```Haskell
interpretFree
  :: Monad m
  => (forall x. f x -> m x)
  -> Free f a
  -> m a
```

対応関係を並べると次のようになる。

| モノイド | モナド |
| --- | --- |
| モノイド `w` | モナド `m` |
| 生成元の型 `a` | アクションを表す関手 `f` |
| 自由モノイド `[a]` | 自由モナド `Free f` |
| 生成元の解釈 `a -> w` | アクションの解釈 `forall x. f x -> m x` |
| `foldMap` | `interpretFree` |

`interpretFree` の実装を見ると、`Pure` は `pure` に、`Bind` は解釈先のモナドの `(>>=)` によって再帰的に畳み込まれている。
圏論的には、`f` から `m` への変換を、それを延長する `Free f` から `m` へのモナド準同型へ一意に持ち上げている。

したがって、自由モナドにおける「解釈」とは、自由モナドで組み立てた構造を別のモナドへ畳み込むことにほかならない。
`interpretFree` は、リストに対する `foldMap` のモナド版と捉えることができる。

この二つを組み合わせると、任意の `Operational f` を実行するインタプリタになる。

```Haskell
interpretOperational
  :: Monad m
  => (forall x. f x -> m x)
  -> Operational f a
  -> m a
interpretOperational interpret =
  interpretFree (interpretCoyoneda interpret)
```

`Command` から `IO` への自然変換は、命令の変換表 `interpretCommandFAsIO` を渡すだけで定義できる。

```Haskell
runCommandAsIO :: Command a -> IO a
runCommandAsIO = interpretOperational interpretCommandFAsIO

main :: IO ()
main = runCommandAsIO helloWorld
```

実行結果は次のようになる。

```text
Hello, Operational Monad!
This is a standard input.
This is a standard input.
Operational monads are fun!
Operational monads are fun!
Operational monads are fun!
```

一つ目の `This is a standard input.` は標準入力として入力した文字列で、二つ目は `putStrLn'` による出力である。

変換の型を並べると、それぞれの役割が分かりやすい。

```Haskell
interpretCommandFAsIO :: CommandF a -> IO a
interpretCoyoneda     :: Functor m => (forall x. f x -> m x) -> Coyoneda f a -> m a
interpretFree         :: Monad m => (forall x. f x -> m x) -> Free f a -> m a
interpretOperational  :: Monad m => (forall x. f x -> m x) -> Operational f a -> m a
```

`CommandF` は関手ではないため、`interpretCommandFAsIO` 自体は厳密には自然変換ではない。
`interpretCoyoneda` によって `Coyoneda CommandF` から `IO` への変換へ持ち上げ、さらに `interpretFree` を適用すると、`Command` から `IO` への自然変換 `runCommandAsIO` が得られる。

同じ `Command` に別の変換表を与えることもできる。
例えば、入力を固定して出力に印を付けるモック用の解釈は次のように定義できる。

```Haskell
interpretCommandFAsMockIO :: CommandF a -> IO a
interpretCommandFAsMockIO (PutStrLnF s) =
  putStrLn ("[mock output] " <> s)
interpretCommandFAsMockIO GetLineF =
  pure "This is a mock input."

runCommandAsMockIO :: Command a -> IO a
runCommandAsMockIO =
  interpretOperational interpretCommandFAsMockIO
```

`helloWorld` 自体を変更せず、`runCommandAsIO` と `runCommandAsMockIO` のどちらで実行するかを選べる。
これは、一つのインターフェースに複数の実装を与えられるようなものだ。

ユーザーがインターフェースごとに書く必要があるのは、命令のGADT、命令を持ち上げる関数、そして命令の意味を決める変換表だけである。
`Coyoneda` や自由モナドを処理する部分は、別のDSLでもそのまま再利用できる。

## なぜ Yoneda ではなく Coyoneda なのか

米田の補題と余米田の補題は、関手 `f` に対してどちらも `f a` と同型な表現を与える。
それならば、`Coyoneda` の代わりに `Yoneda` を使うこともできそうに見える。

共変関手に対する `Yoneda` は、Haskellでは次のように表せる。

```Haskell
newtype Yoneda f a =
  Yoneda (forall x. (a -> x) -> f x)

instance Functor (Yoneda f) where
  fmap f (Yoneda g) =
    Yoneda (\h -> g (h . f))
```

`Yoneda f` も、`f` に制約を課さず `Functor` を実装できる。
しかし、`f a` を `Yoneda f a` へ持ち上げるには `fmap` が必要になる。

```Haskell
liftYoneda :: Functor f => f a -> Yoneda f a
liftYoneda x =
  Yoneda (\f -> fmap f x)

lowerYoneda :: Yoneda f a -> f a
lowerYoneda (Yoneda f) = f id
```

`Coyoneda` とは、制約が必要になる向きが逆である。

| 表現 | `f a` から持ち上げる | `f a` へ戻す |
| --- | --- | --- |
| `Coyoneda f a` | 制約なし | `Functor f` が必要 |
| `Yoneda f a` | `Functor f` が必要 | 制約なし |

Operationalモナドで必要なのは、命令 `f a` をモナドへ**持ち上げる**向きである。
その向きに `Functor f` 制約が付かないからこそ、`CommandF` のようなGADTをそのまま命令セットにできる。

YonedaとCoyonedaは関手に対して同じ表現力を持つが、同型のどちら向きに制約が現れるかは異なる。
Operationalモナドでは、インターフェースの命令を関手へ持ち上げる時点で `Functor f` を要求しないことが重要である。
Coyonedaが使われる理由は、この実装上の都合にある。

## まとめ

Operationalモナドは、特定のアクションを備えたモナドの構造を、実装から切り離して表現する。
その構成は、次の二つのコンポーネントに分けられる。

1. `Coyoneda` 構成が、命令セット `f` から `Functor` 制約なしで関手を作る
2. `Free` が、その関手をモナドへ持ち上げる

その結果、次の性質が得られる。

- 命令をGADTで定義し、各アクションの戻り値を型で直接表現できる
- プログラムを、命令の実装から独立した値として記述できる
- 命令から任意のモナドへの変換表を与えると、プログラムの解釈が得られる
- 複数の変換表を用意すれば、同じプログラムに複数の解釈を与えられる

OOPのインターフェースとの対応でいえば、命令のGADTと持ち上げ関数がインターフェース、命令の変換表が実装、Operationalモナドで書いた値がインターフェースだけに依存するプログラムに相当する。
Coyonedaは、このインターフェースを `Functor` の実装なしで自由モナドへ接続する役割を担っている。

::: details コード全文

```Haskell
{-# LANGUAGE GADTs #-}
{-# LANGUAGE RankNTypes #-}

import Control.Monad (replicateM_)

data Free f a
  = Pure a
  | Bind (f (Free f a))

instance Functor f => Functor (Free f) where
  fmap f (Pure a) = Pure (f a)
  fmap f (Bind next) = Bind (fmap (fmap f) next)

instance Functor f => Applicative (Free f) where
  pure = Pure
  Pure f <*> x = fmap f x
  Bind next <*> x = Bind (fmap (<*> x) next)

instance Functor f => Monad (Free f) where
  Pure a >>= f = f a
  Bind next >>= f = Bind (fmap (>>= f) next)

liftF :: Functor f => f a -> Free f a
liftF = Bind . fmap Pure

data Coyoneda f a where
  Coyoneda :: (x -> a) -> f x -> Coyoneda f a

instance Functor (Coyoneda f) where
  fmap f (Coyoneda g x) = Coyoneda (f . g) x

liftCoyoneda :: f a -> Coyoneda f a
liftCoyoneda = Coyoneda id

lowerCoyoneda :: Functor f => Coyoneda f a -> f a
lowerCoyoneda (Coyoneda f x) = fmap f x

type Operational f = Free (Coyoneda f)

liftOperational :: f a -> Operational f a
liftOperational = liftF . liftCoyoneda

data CommandF a where
  PutStrLnF :: String -> CommandF ()
  GetLineF  :: CommandF String

type Command = Operational CommandF

putStrLn' :: String -> Command ()
putStrLn' = liftOperational . PutStrLnF

getLine' :: Command String
getLine' = liftOperational GetLineF

helloWorld :: Command ()
helloWorld = do
  putStrLn' "Hello, Operational Monad!"
  getLine' >>= putStrLn'
  replicateM_ 3 $
    putStrLn' "Operational monads are fun!"

interpretCoyoneda
  :: Functor m
  => (forall x. f x -> m x)
  -> Coyoneda f a
  -> m a
interpretCoyoneda interpret (Coyoneda f x) =
  fmap f (interpret x)

interpretFree
  :: Monad m
  => (forall x. f x -> m x)
  -> Free f a
  -> m a
interpretFree _ (Pure a) = pure a
interpretFree interpret (Bind next) =
  interpret next >>= interpretFree interpret

interpretOperational
  :: Monad m
  => (forall x. f x -> m x)
  -> Operational f a
  -> m a
interpretOperational interpret =
  interpretFree (interpretCoyoneda interpret)

interpretCommandFAsIO :: CommandF a -> IO a
interpretCommandFAsIO (PutStrLnF s) = putStrLn s
interpretCommandFAsIO GetLineF = getLine

runCommandAsIO :: Command a -> IO a
runCommandAsIO = interpretOperational interpretCommandFAsIO

interpretCommandFAsMockIO :: CommandF a -> IO a
interpretCommandFAsMockIO (PutStrLnF s) =
  putStrLn ("[mock output] " <> s)
interpretCommandFAsMockIO GetLineF =
  pure "This is a mock input."

runCommandAsMockIO :: Command a -> IO a
runCommandAsMockIO =
  interpretOperational interpretCommandFAsMockIO

main :: IO ()
main = runCommandAsIO helloWorld
```

:::
