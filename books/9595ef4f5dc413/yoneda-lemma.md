---
title: "米田の補題"
free: false
---

米田の補題(*Yoneda lemma*)とは、局所的に小さな圏$\mathbf{C}$において対象$A$を固定した$\hom$関手から関手$F: \mathbf{C} \to \mathbf{Set}$への自然変換と集合$F(A)$とが同型であるという定理である。

## 定義

局所的に小さな圏$\mathbf{C}$と$\mathbf{C}$の対象$A$を任意に固定したhom関手$\hom_C(A, \_)$, 関手$F: \mathbf{C} \to \mathbf{Set}$およびこれら関手の間の自然変換$\hom_C(A, \_) \Rightarrow F$のすべての集合$\hom_{\mathrm{Set}^C}(\hom_C(A, \_), F)$を考える。

このとき集合の圏に米田写像(*Yoneda map*)と呼ばれる同型写像$y: \hom_{\mathrm{Set}^C}(\hom_C(A, \_), F) \to F(A)$が存在する。これは$A$および$F$について自然である。

すなわち以下が成り立つ：

$$
\hom_{\mathrm{Set}^C}(\hom_C(A, \_), F) \simeq F(A)
$$

[![yoneda_lemma](https://storage.googleapis.com/zenn-user-upload/07a82eed7035-20250202.png)](https://q.uiver.app/#q=WzAsMTQsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkEiXSxbMywwLCJcXG1hdGhiZntTZXR9Il0sWzMsMSwiXFxob21fQyhBLCBYKSJdLFswLDIsIlgiXSxbMSwyLCJZIl0sWzUsMSwiXFxob21fQyhBLCBZKSJdLFszLDIsIkYoWCkiXSxbNSwyLCJGKFkpIl0sWzYsMiwiRihBKSJdLFs2LDEsIlxcbWF0aHJte1xcaG9tX3tcXG1hdGhiZntTZXR9XntcXG1hdGhiZntDfX19KFxcaG9tX0MoQSwgXFxfKSwgRil9Il0sWzgsMCwiXFxtYXRoYmZ7U2V0fV5cXG1hdGhiZntDfSJdLFs4LDEsIlxcaG9tX0MoQSwgXFxfKSJdLFs4LDIsIkYiXSxbNCw1LCJmIiwyXSxbMyw2LCJcXGhvbV9DKEEsIGYpIFxcY29sb25lcXEgZyBcXG1hcHN0byBmIFxcY2lyYyBnIl0sWzEsNCwiZyIsMl0sWzMsNywiXFxldGFfWCIsMl0sWzYsOCwiXFxldGFfWSJdLFs3LDgsIkYoZikiLDJdLFsxMiwxMywiXFxldGEiXSxbMTAsOSwieSJdXQ==)

上図において$\eta$は適当な$\hom_{\mathrm{Set}^C}(\hom_C(A, \_), F)$の要素である。

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

いま、米田写像$y: \hom_{\mathbf{Set}^{\mathbf{C}}}(\hom_C(A, \_) \Rightarrow F) \to F(A)$を以下の通り定める。
これは自然変換$\tau$を、そのうちの（圏$\mathbf{C}$の対象）$A$に対応する要素$\tau_A$で$\mathrm{id}_A$を送ったものに対応づけるものである。

$$
\def\defineas{\overset{\mathrm{def}}{=}}
\begin{aligned}
y \defineas \tau \mapsto \tau_A(\mathrm{id}_A)
\end{aligned}
$$

![apply_id](https://storage.googleapis.com/zenn-user-upload/d25f12526243-20231214.png)

可換図式より、適当な射$h: A \to Y$を考えたとき、$\eta_Y(h) = F(h)(\eta_A(\mathrm{id}_A))$が得られる。

また、逆向きの写像$w: F(A) \to \hom_{Set^C}(\hom_C(A, \_), F)$を以下の通り定める。
これは圏$\mathbf{Set}$の対象$F(A)$を自然変換$\hom_C(A, \_) \Rightarrow F$に対応づけるものである。

$$
\def\defineas{\overset{\mathrm{def}}{=}}
\begin{aligned}
w \defineas a \mapsto g \mapsto F(g)(a)
\end{aligned}
$$

[![yonedamap_inverse](https://storage.googleapis.com/zenn-user-upload/6c9adf106450-20250202.png)](https://q.uiver.app/#q=WzAsMTEsWzQsMywiXFxob21fe1xcbWF0aHJte1NldH1eQ30oXFxob21fQyhBLCBcXF8pLCBGKSJdLFszLDIsImEiXSxbMywzLCJnIFxcbWFwc3RvIEYoZykoYSkiXSxbMywwLCJcXG1hdGhiZntTZXR9Il0sWzQsMiwiRihBKSJdLFs0LDEsIlxcaG9tX0MoQSwgQSkiXSxbNiwyLCJGKFgpIl0sWzYsMSwiXFxob21fQyhBLCBYKSJdLFswLDAsIlxcbWF0aGJme0N9Il0sWzAsMSwiQSJdLFsxLDEsIlgiXSxbNSw3LCJcXGhvbV9DKEEsIGcpIl0sWzksMTAsImciXSxbNCw2LCJGKGcpIl0sWzUsNCwidyhhKV9BIl0sWzcsNiwidyhhKV9YIl0sWzQsMCwidyJdLFsxLDIsInciLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtYXBzIHRvIn19fV0sWzIsMCwiXFxpbiIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs0LDEsIlxcaW4iLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

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
この双対も米田の補題と呼ばれる。

局所的に小さな圏$\mathbf{C}$と$\mathbf{C}$の対象$A$を任意に固定した反変hom関手$\hom_C(\_, A)$, 反変関手$F: \mathbf{C}^{\mathrm{op}} \to \mathbf{Set}$および自然変換$\hom_C(\_, A) \Rightarrow F$のすべての集合$\hom_{\mathrm{Set}^{C^\mathrm{op}}}(\hom_{C}(\_, A) \Rightarrow F)$を考える。

このとき$A$および$F$について自然な同型写像$y: \hom_{\mathrm{Set}^{C^\mathrm{op}}}(\hom_C(\_, A) \Rightarrow F) \to F(A)$が存在する。

[![covariant_yoneda_lemma](https://storage.googleapis.com/zenn-user-upload/c25f89e86cf3-20250202.png)](https://q.uiver.app/#q=WzAsMTQsWzgsMCwiXFxtYXRoYmZ7U2V0fV57Q157XFxtYXRocm17b3B9fX0iXSxbOCwxLCJcXGhvbV9DKFxcXywgQSkiXSxbOCwyLCJHIl0sWzYsMSwiXFxob21fe1xcbWF0aHJte1NldH1ee0Nee1xcbWF0aHJte29wfX19fShcXGhvbV9DKFxcXywgQSksIEYpIl0sWzYsMiwiRyhBKSJdLFszLDEsIlxcaG9tX3tDXntcXG1hdGhybXtvcH19fShYLCBBKSJdLFs1LDEsIlxcaG9tX3tDXntcXG1hdGhybXtvcH19fShZLCBBKSJdLFszLDIsIkcoWCkiXSxbNSwyLCJHKFkpIl0sWzAsMSwiQSJdLFswLDIsIlgiXSxbMSwyLCJZIl0sWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMSwyLCJcXGVwc2lsb24iXSxbMyw0LCJ5Il0sWzgsNywiRyhmKSJdLFs2LDUsIlxcaG9tX3tDXntcXG1hdGhybXtvcH19fShmLCBBKSBcXGNvbG9uZXFxIGcgXFxtYXBzdG8gZyBcXGNpcmMgZiIsMl0sWzUsNywiXFxlcHNpbG9uX1giLDJdLFs2LDgsIlxcZXBzaWxvbl9ZIl0sWzksMTAsImciLDJdLFsxMCwxMSwiZiIsMl1d)

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
