---
title: "米田の補題"
free: false
---

$$
\begin{aligned}
\hom_{\mathbf{Set}^\mathbf C}(\hom_\mathbf C(A, \_), F) &\simeq F(A) \\
\hom_{\mathbf{Set}^\mathbf{C^{\mathrm{op}}}}(\hom_\mathbf C(\_, A), F) &\simeq F(A) \\
\end{aligned}
$$

米田の補題(*Yoneda lemma*)とは、局所的に小さな圏$\mathbf{C}$において対象$A$を固定した$\hom$関手から集合値関手$F: \mathbf{C} \to \mathbf{Set}$または$F : \mathbf{C}^\mathrm{op} \to \mathbf{Set}$への自然変換全体の集合と集合$F(A)$とが同型であるという定理である。

$F$として反変関手を取ったものは、$\mathbf C$の反対圏を取れば全く同じ議論ができるため、同様に米田の補題として扱う。

## 定理

局所的に小さな圏$\mathbf{C}$と$\mathbf{C}$の対象$A$を任意に固定したhom関手$\hom_\mathbf C(A, \_)$, 関手$F: \mathbf{C} \to \mathbf{Set}$およびこれら関手の間の自然変換$\hom_\mathbf C(A, \_) \Rightarrow F$のすべての集合$\hom_{\mathbf{Set}^{\mathbf C}}(\hom_\mathbf C(A, \_), F)$を考える。

このとき集合の圏に米田写像(*Yoneda map*)と呼ばれる同型写像$y: \hom_{\mathbf{Set}^\mathbf C}(\hom_\mathbf C(A, \_), F) \to F(A)$が存在する。これは$A$および$F$について自然である。

すなわち以下が成り立つ：

$$
\hom_{\mathbf{Set}^\mathbf C}(\hom_\mathbf C(A, \_), F) \simeq F(A)
$$

https://q.uiver.app/#q=WzAsNSxbMSwxLCJGKEEpIl0sWzAsMSwiXFxob20oXFxob20oQSwgXFxfKSwgRikiXSxbMSwyLCJ4Il0sWzAsMiwiXFxldGEiXSxbMCwwLCJcXG1hdGhiZntTZXR9Il0sWzAsMSwieV57LTF9IiwwLHsib2Zmc2V0IjotMn1dLFsyLDAsIlxcaW4iLDMseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMSwwLCJ5IiwwLHsib2Zmc2V0IjotMn1dLFszLDEsIlxcaW4iLDMseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMywyLCIiLDMseyJvZmZzZXQiOi0yLCJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtYXBzIHRvIn19fV0sWzIsMywiIiwzLHsib2Zmc2V0IjotMiwic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibWFwcyB0byJ9fX1dXQ==

あるいは反変 hom 関手 $\hom_\mathbf C(\_, A)$ と反変関手 $F : \mathbf C^\mathrm{op} \to \mathbf{Set}$ およびこれらの関手の間の自然変換 $\hom_\mathbf C(\_, A) \Rightarrow F$ のすべての集合 $\hom_{\mathbf{Set}^{\mathbf C^\mathrm{op}}}(\hom_\mathbf C(\_, A), F)$ を考える。

このとき集合の圏に米田写像と呼ばれる同型写像 $y : \hom_{\mathbf{Set}^{\mathbf C^\mathrm{op}}}(\hom_\mathbf C(\_, A), F) \to F(A)$ が存在する。これは $A$ および $F$ について自然である。

すなわち以下が成り立つ：

$$
\hom_{\mathbf{Set}^\mathbf{C^{\mathrm{op}}}}(\hom_\mathbf C(\_, A), F) \simeq F(A)
$$

https://q.uiver.app/#q=WzAsNSxbMSwxLCJGKEEpIl0sWzAsMSwiXFxob20oXFxob20oXFxfLCBBKSwgRikiXSxbMSwyLCJ4Il0sWzAsMiwiXFxldGEiXSxbMCwwLCJcXG1hdGhiZntTZXR9Il0sWzAsMSwieV57LTF9IiwwLHsib2Zmc2V0IjotMn1dLFsyLDAsIlxcaW4iLDMseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMSwwLCJ5IiwwLHsib2Zmc2V0IjotMn1dLFszLDEsIlxcaW4iLDMseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMywyLCIiLDMseyJvZmZzZXQiOi0yLCJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtYXBzIHRvIn19fV0sWzIsMywiIiwzLHsib2Zmc2V0IjotMiwic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibWFwcyB0byJ9fX1dXQ==

## 証明

反変関手の米田の補題を使って証明する。

簡単のために、対象 $A$ を固定した hom 関手 $\hom_\mathbf C(\_, A) : \mathbf C^\mathrm{op} \to \mathbf{Set}$ を $H_A$ と書くことにする。詳しくは[米田埋め込み](./yoneda-embedding) を参照。

まず $y \colon \hom_{\widehat{\mathbf C}}(H_A, F) \to F(A)$ については以下のように定義する。

$$
\eta \mapsto \eta_A(\mathrm{id}_A)
$$

$\eta$ は $\hom(\_, A)$ から $F$ への自然変換 なので、これを $\eta_A(\mathrm{id}_A)$ に対応づける。$\eta$ の $A$ 成分は $\eta_A : \hom(A, A) \to F(A)$ という写像なので、これに $\mathrm{id}_A$ を渡してやれば$F(A)$ の元 $\eta_A(\mathrm{id}_A)$ が得られる。

次に、逆向きの写像 $y^{-1} \colon F(A) \to \hom_{\widehat{\mathbf C}}(H_A, F)$ については以下のように定義する。

$$
x \mapsto \{g \colon (A \to X) \mapsto F(g)(x)\}_{X \in \mathbf C}
$$

$y^{-1}$ が写す先 $\hom_{\widehat{\mathbf C}}(H_A, F)$ は自然変換なので、$\mathbf C$ の元で添え字づけられた $\mathbf{Set}$ の射の族になる。
代表として $X \in \mathrm{ob}(\mathbf C)$ を使うと、自然変換の $X$ 成分 $\hom(X, A) \to F(X)$ に対応づければよいことになる。

$g : X \to A$ を $F$ で写すと $F(g) : F(A) \to F(X)$ が得られる ($F$ は反変関手である) ので、これで $x \in F(A)$ を写せば $F(X)$ の元が得られる。

$\{g : (X \to A) \mapsto F(g)(x)\}_{X \in \mathbf C}$ が自然変換であることを確かめるには、$F(-)(x) \circ (- \circ f) = F(f) \circ F(-)(x)$ を示せればよい。

https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXGhvbShYLCBBKSJdLFsxLDAsIlxcaG9tKFksIEEpIl0sWzAsMSwiRihYKSJdLFsxLDEsIkYoWSkiXSxbMCwyLCJGKC0pKHgpIiwyXSxbMiwzLCJGKGYpIiwyXSxbMCwxLCJcXGhvbShmLCBBKSA9IC0gXFxjaXJjIGYiXSxbMSwzLCJGKC0pKHgpIl1d

射 $s : X \to A \in \hom_\mathbf C(X, A)$ を取って計算する。$F$ は反変関手なので $F(s \circ f) = F(f) \circ F(s)$ であることに注意する。

$$
\begin{aligned}
&s \overset{- \circ f}{\mapsto} s \circ f \overset{F(-)(x)}{\mapsto} F(s \circ f)(x) \\
&= (F(f) \circ F(s))(x) \\
&= F(f)(F(s)(x)) \\
\\
&s \overset{F(-)(x)}{\mapsto} F(s)(x) \overset{F(f)}{\mapsto} F(f)(F(s)(x))
\end{aligned}
$$

これで $\{g : (X \to A) \mapsto F(g)(x)\}_{X \in \mathbf C}$ が自然変換であることがわかった。

最後に $y$ と $y^{-1}$ が全単射であることを確認する。

$$
\begin{aligned}
y^{-1}(y(\eta)) &= y^{-1}(\eta_A(\mathrm{id}_A)) \\
&= \{g \mapsto F(g)(\eta_A(\mathrm{id}_A))\}_{X \in \mathbf C}
\end{aligned}
$$

$\eta$ は自然変換なので、$F(g) \circ \eta_A = \eta_X \circ \hom(g, A)$ が成り立つ。

https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXGhvbShBLCBBKSJdLFsxLDAsIlxcaG9tKFgsIEEpIl0sWzAsMSwiRihBKSJdLFsxLDEsIkYoWCkiXSxbMCwyLCJcXGV0YV9BIiwyXSxbMiwzLCJGKGcpIiwyXSxbMCwxLCJcXGhvbShnLCBBKSA9IC0gXFxjaXJjIGciXSxbMSwzLCJcXGV0YV9YIl0sWzAsMywiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d

$$
\begin{aligned}
y^{-1}(y(\eta)) &= \{g \mapsto F(g)(\eta_A(\mathrm{id}_A))\}_{X \in \mathbf C} \\
&= \{g \mapsto \eta_X (\mathrm{id}_A \circ g)\}_{X \in \mathbf C} \\
&= \{g \mapsto \eta_X (g)\}_{X \in \mathbf C} \\
&= \{\eta_X\}_{X \in \mathbf C} \\
&= \eta
\end{aligned}
$$

逆向き：

$$
\begin{aligned}
y(y^{-1}(x)) &= y(\{g : (X \to A) \mapsto F(g)(x)\}_{X \in \mathbf C}) \\
&= (g : (A\to A) \mapsto F(g)(x))(\mathrm{id}_A) \\
&= F(\mathrm{id}_A)(x) \\
&= \mathrm{id}_{F(A)}(x) \\
&= x
\end{aligned}
$$

これで米田写像の全単射を示せた。

最後に米田の補題が $F$ および $A$ について自然であることを示す。

まず $y$ が $F$ について自然であることを示す。
すなわち $y \colon \hom(H_A, -) \Rightarrow \mathrm{ev}_A$ が自然変換であることを示す。
ここで $\mathrm{ev_A} : \widehat{C} \to \mathbf{Set}, F \mapsto F(A)$ である。

https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXGhvbShIX0EsIEYpIl0sWzEsMCwiXFxob20oSF9BLCBHKSJdLFswLDEsIkYoQSkiXSxbMSwxLCJHKEEpIl0sWzAsMSwiXFxob20oSF9BLCBcXGV0YSkiXSxbMiwzLCJcXGV0YV9BIiwyXSxbMCwyLCJ5X0YiLDJdLFsxLDMsInlfRyJdXQ==

自然変換 $\alpha \in \hom(H_A, F)$ を取って計算する。

$$
\begin{aligned}
&\alpha \overset{\eta \circ -}{\mapsto} \eta \circ \alpha \overset{y_G}{\mapsto} (\eta \circ \alpha)_A(\mathrm{id}_A) \\
&= \eta_A(\alpha_A(\mathrm{id}_A)) \\
\\
&\alpha \overset{y_F}{\mapsto} \alpha_A(\mathrm{id}_A) \overset{\eta_A}{\mapsto} \eta_A(\alpha_A(\mathrm{id}_A))
\end{aligned}
$$

これで図式の可換性を確認できた。

次に $y$ が $A$ について自然であることを示す。
すなわち $y \colon \hom(H_-, F) \Rightarrow F$ が自然変換であることを示す。

https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXGhvbShIX0EsIEYpIl0sWzEsMCwiXFxob20oSF9CLCBGKSJdLFswLDEsIkYoQSkiXSxbMSwxLCJGKEIpIl0sWzAsMSwiXFxob20oSF9mLCBGKSJdLFsyLDMsIkYoZikiLDJdLFswLDIsInlfQSIsMl0sWzEsMywieV9CIl1d

自然変換 $\beta \in \hom(H_A, F)$ を取って計算する。
ここで $(H_f)_B = \hom(B, f) = (f \circ -)$  である。

$$
\begin{aligned}
&\beta \overset{y_A}{\mapsto} \beta_A(\mathrm{id}_A) \overset{F(f)}{\mapsto} F(f)(\beta_A(\mathrm{id}_A)) \\
\\
&\beta \overset{\hom(H_f, F)}{\mapsto} \beta \circ H_f \overset{y_B}{\mapsto} (\beta \circ H_f)_B(\mathrm{id}_B) \\
&= \beta_B((H_f)_B(\mathrm{id}_B)) \\
&= \beta_B(f \circ \mathrm{id}_B) = \beta_B(f)
\end{aligned}
$$

$\beta$ は自然変換であるから、$\beta_B \circ \hom(f, A) = F(f) \circ \beta_A$ が成り立つ。

https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXGhvbShBLCBBKSJdLFsxLDAsIlxcaG9tKEIsIEEpIl0sWzAsMSwiRihBKSJdLFsxLDEsIkYoQikiXSxbMCwyLCJcXGJldGFfQSIsMl0sWzIsMywiRihmKSIsMl0sWzAsMSwiXFxob20oZiwgQSkgPSAtIFxcY2lyYyBmIl0sWzEsMywiXFxiZXRhX0IiXSxbMCwzLCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=

この等式の両辺に $\mathrm{id}_A$ を適用すると、$F(f)(\beta_A(\mathrm{id}_A)) = \beta_B(f)$ が得られる。

$$
\begin{aligned}
F(f)(\beta_A(\mathrm{id}_A)) &= \beta_B(\hom(f, A)(\mathrm{id}_A)) \\
&= \beta_B(\mathrm{id}_A \circ f) \\
&= \beta_B(f)
\end{aligned}
$$

これで $y$ が $A$ について自然であることを確認できた。

## Haskellでの米田写像の実装

Haskellでは、米田写像とその逆射の実装も簡単だ。

```Haskell
yonedaMap :: (forall x. (a -> x) -> f x) -> f a
yonedaMap tau = tau id

yonedaMap' :: Functor f => f a -> (forall x. (a -> x) -> f x)
yonedaMap' a = \f -> fmap f a

contrayonedaMap :: (forall x. (x -> a) -> f x) -> f a
contrayonedaMap tau = tau id

contrayonedaMap' :: Contravariant f => f a -> (forall x. (x -> a) -> f x)
contrayonedaMap' a = \f -> contramap f a
```

https://play.haskell.org/saved/R4ovaKvY

適当な関手`Hom`, `Contrahom`と自然変換を実装すれば、より圏論の表記に近づけた実装もできる。

```Haskell
newtype Hom a x = Hom (a -> x)
newtype Contrahom a x = Contrahom (x -> a)
type f ~> g = forall a. f a -> g a

yonedaMap :: (Hom a ~> f) -> f a
yonedaMap tau = tau (Hom id)

yonedaMap' :: Functor f => f a -> (Hom a ~> f)
yonedaMap' a = \(Hom f) -> fmap f a

contrayonedaMap :: (Contrahom a ~> f) -> f a
contrayonedaMap tau = tau (Contrahom id)

contrayonedaMap' :: Contravariant f => f a -> (Contrahom a ~> f)
contrayonedaMap' a = \(Contrahom f) -> contramap f a
```

https://play.haskell.org/saved/EDjwLqf4
