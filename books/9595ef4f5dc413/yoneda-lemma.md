---
title: "米田の補題"
free: false
---

米田の補題(*Yoneda lemma*)とは、局所的に小さな圏$\mathbf{C}$において$\hom$関手から関手$F: \mathbf{C} \to \mathbf{Set}$への自然変換と集合$F(A)$とが同型であるという定理である。

## 補題

局所的に小さな圏$\mathbf{C}$と$\mathbf{C}$の対象$A$を任意に固定したhom関手$\hom_C(A, \_)$, 関手$F: \mathbf{C} \to \mathbf{Set}$および自然変換$\hom_C(A, \_) \Rightarrow F$のすべての集合$\mathrm{Nat}(\hom_C(A, \_) \Rightarrow F)$を考える。

このとき集合の圏に米田写像(*Yoneda map*)と呼ばれる同型写像$y: \mathrm{Nat}(\hom_C(A, \_) \Rightarrow F) \to F(A)$が存在する。これは$A$および$F$について自然である。

![yoneda_lemma](https://storage.googleapis.com/zenn-user-upload/64f7ba3a772c-20231212.png)

https://q.uiver.app/#q=WzAsMTEsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkEiXSxbMywwLCJcXG1hdGhiZntTZXR9Il0sWzMsMSwiXFxob21fQyhBLCBYKSJdLFswLDIsIlgiXSxbMSwyLCJZIl0sWzUsMSwiXFxob21fQyhBLCBZKSJdLFszLDIsIkYoWCkiXSxbNSwyLCJGKFkpIl0sWzYsMiwiRihBKSJdLFs2LDEsIlxcbWF0aHJte1xcbWF0aHJte05hdH19Il0sWzQsNSwiZiIsMl0sWzMsNiwiXFxob21fQyhBLCBmKSBcXGNvbG9uZXFxIGcgXFxtYXBzdG8gZiBcXGNpcmMgZyJdLFsxLDQsImciLDJdLFszLDcsIlxcZXRhX1giLDJdLFs2LDgsIlxcZXRhX1kiXSxbNyw4LCJGKGYpIl0sWzEwLDksInkiXV0=

## 証明

hom関手の定義の再掲。$\hom_C(A, \_)$は、圏$\mathbf{C}$の射$f: X \to Y$を、圏$\mathbf{Set}$の射$g \mapsto f \circ g$に対応させるものだった。
これは圏$\mathbf{C}$の射$A \to X$を射$A \to Y$に写すような写像である。

$$
\def\defineas{\overset{\mathrm{def}}{=}}
\begin{aligned}
\hom_C(A, f) \defineas g \mapsto f \circ g
\end{aligned}
$$

自然変換の可換性により以下が成り立つ。

$$
\begin{aligned}
\eta_Y \circ \hom_C(A, f) = F(f) \circ \eta_X
\end{aligned}
$$

いま、米田写像$y: \mathrm{Nat}(\hom_C(A, \_) \Rightarrow F) \to F(A)$を以下の通り定める。
これは自然変換$\tau$を、そのうちの（圏$\mathbf{C}$の対象）$A$に対応する要素$\tau_A$で$\mathrm{id}_A$を送ったものに対応づけるものである。

$$
\def\defineas{\overset{\mathrm{def}}{=}}
\begin{aligned}
y \defineas \tau \mapsto \tau_A(\mathrm{id}_A)
\end{aligned}
$$

![apply_id](https://storage.googleapis.com/zenn-user-upload/d25f12526243-20231214.png)

可換図式より、適当な射$h: A \to Y$を考えたとき、$\eta_Y(h) = F(h)(\eta_A(\mathrm{id}_A))$が得られる。

また、逆向きの写像$w: F(A) \to \mathrm{Nat}(\hom_C(A, \_) \Rightarrow F)$を以下の通り定める。
これは圏$\mathbf{Set}$の対象$F(A)$を自然変換$\hom_C(A, \_) \Rightarrow F$に対応づけるものである。

$$
\def\defineas{\overset{\mathrm{def}}{=}}
\begin{aligned}
w \defineas a \mapsto g \mapsto F(g)(a)
\end{aligned}
$$

![yonedamap_inverse](https://storage.googleapis.com/zenn-user-upload/16790ed42d57-20231226.png)

https://q.uiver.app/#q=WzAsMTEsWzQsMywiXFxtYXRocm17TmF0fV97XFxob21fQyhBLCBcXF8pIFxcUmlnaHRhcnJvdyBGfSJdLFszLDIsImEiXSxbMywzLCJnIFxcbWFwc3RvIEYoZykoYSkiXSxbMywwLCJcXG1hdGhiZntTZXR9Il0sWzQsMiwiRihBKSJdLFs0LDEsIlxcaG9tX0MoQSwgQSkiXSxbNiwyLCJGKFgpIl0sWzYsMSwiXFxob21fQyhBLCBYKSJdLFswLDAsIlxcbWF0aGJme0N9Il0sWzAsMSwiQSJdLFsxLDEsIlgiXSxbNSw3LCJcXGhvbV9DKEEsIGcpIl0sWzksMTAsImciXSxbNCw2LCJGKGcpIl0sWzUsNCwidyhhKV9BIl0sWzcsNiwidyhhKV9YIl0sWzQsMCwidyJdLFsxLDIsInciLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtYXBzIHRvIn19fV0sWzIsMCwiXFxpbiIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs0LDEsIlxcaW4iLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=

$w(y(\eta))$と$y(w(a))$を計算すると、$y$と$w$はそれぞれの逆射であることが確認できる。

$$
\begin{aligned}
w(y(\eta)) &= w(\eta_A(\mathrm{id}_A))   \\
&= g \mapsto F(g)(\eta_A(\mathrm{id}_A)) \\
&= g \mapsto \eta_X(g) \\
&= \eta
\end{aligned}
$$

$$
\begin{aligned}
y(w(a)) &= y(g \mapsto F(g)(a)) \\
&= F(\mathrm{id}_A)(a)   \\
&= \mathrm{id}_{F(A)}(a) \\
&= a
\end{aligned}
$$

以上で米田写像$y$は全単射であることが証明できた。

## 双対

上の補題では共変hom関手を用いたが、反変hom関手を用いれば双対を得ることができる。
この双対も米田の補題と呼ばれ、余米田の補題とは区別されるが、それは後のページに回すことにする。

局所的に小さな圏$\mathbf{C}$と$\mathbf{C}$の対象$A$を任意に固定した反変hom関手$\hom_C(\_, A)$, 反変関手$F: \mathbf{C} \to \mathbf{Set}$および自然変換$\hom_C(\_, A) \Rightarrow F$のすべての集合$\mathrm{Nat}(\hom_{C}(\_, A) \Rightarrow F)$を考える。

このとき$A$および$F$について自然な同型写像$y: \mathrm{Nat}(\hom_C(\_, A) \Rightarrow F) \to F(A)$が存在する。

## Haskellでの米田写像の実装

Haskellでは、米田写像とその逆射の実装も簡単だ。

```Haskell
yonedaMap :: (forall x. (a -> x) -> f x) -> f a
yonedaMap tau = tau id

yonedaMap' :: Functor f => f a -> (forall x. (a -> x) -> f x)
yonedaMap' a = \f -> fmap f a

coyonedaMap :: (forall x. (x -> a) -> f x) -> f a
coyonedaMap tau = tau id

coyonedaMap' :: Contravariant f => f a -> (forall x. (x -> a) -> f x)
coyonedaMap' a = \f -> contramap f a
```

https://play.haskell.org/saved/a4gbhdpa

適当な関手`Hom`, `Cohom`と自然変換を実装すれば、より圏論の表記に近づけた実装もできる。

```Haskell
newtype Hom a x = Hom (a -> x)
newtype Cohom a x = Cohom (x -> a)
type f ~> g = forall a. f a -> g a

yonedaMap :: (Hom a ~> f) -> f a
yonedaMap tau = tau (Hom id)

yonedaMap' :: Functor f => f a -> (Hom a ~> f)
yonedaMap' a = \(Hom f) -> fmap f a

coyonedaMap :: (Cohom a ~> f) -> f a
coyonedaMap tau = tau (Cohom id)

coyonedaMap' :: Contravariant f => f a -> (Cohom a ~> f)
coyonedaMap' a = \(Cohom f) -> contramap f a
```

https://play.haskell.org/saved/DQDNx0fn
