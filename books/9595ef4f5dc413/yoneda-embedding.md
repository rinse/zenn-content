---
title: "米田埋め込み"
free: false
---

## 米田の補題の特殊化

[米田写像](yoneda-lemma)とは、局所的に小さな圏 $\mathbf{C}$ において対象 $A$ を固定した hom 関手 $\hom_{\mathbf{C}}(\_, A): \mathbf{C}^\mathrm{op} \to \mathbf{Set}$ から集合値関手 $F: \mathbf{C}^\mathrm{op} \to \mathbf{Set}$ への自然変換全体の集合 $\hom_{\mathrm{Set}^{\mathbf C^\mathrm{op}}}(\hom_\mathbf C(\_, A), F)$ と集合 $F(A)$ との間にある同型射のことであった。

ここで集合値関手 $F$ に圏 $\mathbf{C}$ の対象 $B$ を固定した hom 関手 $\hom_{\mathbf{C}}(\_, B)$ をとることを考えると、米田の補題により米田写像 $y: \hom_{\mathrm{Set}^{\mathbf C^\mathrm{op}}}(\hom_{\mathbf{C}}(\_, A), \hom_{\mathbf{C}}(\_, B)) \simeq \hom_{\mathbf{C}}(A, B)$ が得られる。

ここで米田写像の $y$ は、より具体的には以下のような写像になる。

$$
\begin{aligned}
y \colon \hom_{\mathrm{Set}^{\mathbf C^\mathrm{op}}}(\hom_{\mathbf{C}}(\_, A), \hom_{\mathbf{C}}(\_, B)) &\to \hom_{\mathbf{C}}(A, B) \\
\phi &\mapsto \phi_A(\mathrm{id}_A) \\
\end{aligned}
$$

逆射は以下の通りだ。

$$
\begin{aligned}
y^{-1} \colon \hom_{\mathbf{C}}(A, B) &\to \hom_{\mathrm{Set}^{\mathbf C^\mathrm{op}}}(\hom_{\mathbf{C}}(\_, A), \hom_{\mathbf{C}}(\_, B)) \\
f &\mapsto (f \circ -)
\end{aligned}
$$

$(f \circ -) : \hom_\mathbf C(\_, A) \Rightarrow \hom_\mathbf C(\_, B)$ が自然変換であるというのは、以下のようにして確認できる。

すなわち $X$ 成分が以下のような写像であって、これは $X$ 成分について自然である。

$$
\begin{aligned}
(f \circ -)_X : \hom_\mathbf C(X, A) &\to \hom_\mathbf C(X, B) \\
(g : X \to A) &\mapsto f \circ g
\end{aligned}
$$

自然性は次のように確認できる。

$$
(f \circ -)_Y \circ \hom(a, A) = \hom(a, B) \circ (f \circ -)_X
$$

hom 関手の定義より、$a : Y \to X$ のとき $\hom(a, A) = (g \colon X \to A) \mapsto g \circ a$, $\hom(a, B) = (g \colon X \to B) \mapsto g \circ a$ であるから、適当な射 $h : X \to A \in \mathbf{C}$ の行き先を調べると

$$
\begin{aligned}
(f \circ (h \circ a)) &= ((f \circ h) \circ a) \\
\end{aligned}
$$

となり、可換性を確かめられる。

https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXGhvbV9cXG1hdGhiZiBDKFgsIEEpIl0sWzEsMCwiXFxob21fXFxtYXRoYmYgQyhZLCBBKSJdLFswLDEsIlxcaG9tX1xcbWF0aGJmIEMoWCwgQikiXSxbMSwxLCJcXGhvbV9cXG1hdGhiZiBDKFksIEIpIl0sWzAsMiwiKGYgXFxjaXJjIC0pX1giLDJdLFswLDEsIlxcaG9tKGEsIEEpID0gLSBcXGNpcmMgYSJdLFsxLDMsIihmIFxcY2lyYyAtKV9ZIl0sWzIsMywiXFxob20oYSwgQikgPSAtIFxcY2lyYyBhIiwyXSxbMCwzLCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=

## 定義

局所的に小さな圏 $\mathbf{C}$ の対象 $A \in \mathrm{ob}(\mathbf{C})$ を固定した [hom 関手](hom-functor) $\hom_\mathbf C(\_, A): \mathbf C^\mathrm{op} \to \mathbf{Set}$ を考える。

この hom 関手を $H_A$ と書くと、この関手を得る操作を関手$H_-: \mathbf{C} \to \mathbf{Set}^{\mathbf{C}^\mathrm{op}}$と捉えることができる。すなわち：

- 圏 $\mathbf{C}$ の任意の対象 $A$ をhom関手 $H_A = \hom_C(\_, A)$ に写す
- 圏 $\mathbf{C}$ の任意の射 $f: A \to B$ を、米田写像によって自然変換 $(f \circ -) \colon H_A \Rightarrow H_B$ に写す

この関手 $H_-: \mathbf{C} \to \mathbf{Set}^{\mathbf{C}^\mathrm{op}}$ を米田埋め込み(*Yoneda embedding*)と呼ぶ。

また共変 hom 関手 $\hom_\mathbf C(A, \_)$ を使えば、$H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^{\mathbf{C}}$ を得られる。この $H^-$ も米田埋め込みと呼ぶ。

$H^-$, $H_-$ は定義からそれぞれ $\hom(\_, \_) : \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf{Set}$ と同等のものなので以下が成り立つ。

$$
H_- \simeq H^-
$$

## 米田埋め込みは忠実充満

米田埋め込み $H^-$ および $H_-$ は[忠実充満関手](full-and-faithful-functors)である。

関手 $F: \mathbf{C} \to \mathbf{D}$ が忠実充満であるとは、局所的に小さな圏 $\mathbf{C}$ の任意の二対象 $X$, $Y$ について集合の圏上の射 $\hom_\mathbf{C}(X, Y) \to \hom_\mathbf{D}(F(X), F(Y))$ が単射かつ全射であることをいうのだった。

これを米田埋め込み $H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^\mathbf{C}$ に当てはめると、局所的に小さな圏 $\mathbf{C^{\mathrm{op}}}$ の任意の二対象 $X$, $Y$ について集合の圏上の射 $\hom_{\mathbf{C}^\mathrm{op}}(X, Y) \to \hom_{\mathbf{Set}^{\mathbf{C}}}(H^X, H^Y)$ が単射かつ全射になればよい。

ところで、自然変換 $\hom_C(A, \_) \Rightarrow \hom_C(B, \_)$ と圏 $\mathbf{C}$ の射 $B \to A$（あるいは同じことだが圏 $\mathbf{C}^{\mathrm{op}}$ の射 $A \to B$）の間には米田写像があるのだった。米田写像は同型写像であるから、米田埋め込みは忠実充満関手である。

## 表記

米田埋め込みは、$Y$, $y$, $よ$（ひらがな！）などと書かれることがある。

https://ncatlab.org/nlab/show/Yoneda+embedding#ReferencesNotation
