---
title: "T-代数"
---

## T-代数

[F-代数](./f-algebra)とは、組$\lang A, f : F(A) \to A \rang$のことであった。ここでは自己関手としてモナドを取るT-代数を考える。

すなわちモナド$\lang T : \mathbf C \to \mathbf C, \mu : T^2 \Rightarrow T, \eta : 1_\mathbf C \Rightarrow T \rang$におけるT-代数とは、組$\lang A, f : T(A) \to A \rang$であって、$f \circ \mu_A = f \circ T(f)$かつ$f \circ \eta_A = \mathrm{id}_A$を満たすものをいう。

[![](https://storage.googleapis.com/zenn-user-upload/e79043ee88e9-20251113.png)](https://q.uiver.app/#q=WzAsOCxbMCwxLCJUKFQoQSkpIl0sWzAsMCwiXFxtYXRoYmYgQyJdLFsxLDEsIlQoQSkiXSxbMSwyLCJBIl0sWzAsMiwiVChBKSJdLFsyLDEsIkEiXSxbMywxLCJUKEEpIl0sWzMsMiwiQSJdLFsyLDMsImYiXSxbMCwyLCJcXG11X0EiXSxbMCw0LCJUKGYpIiwyXSxbNCwzLCJmIiwyXSxbMCwzLCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbNSw2LCJcXGV0YV9BIl0sWzYsNywiZiJdLFs1LDcsIlxcbWF0aHJte2lkfV9BIiwyXSxbNSw3LCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJvZmZzZXQiOi0zLCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

## 自由T-代数

モナド$T : \mathbf C \to \mathbf C$と圏$`\mathbf C$の対象$C \in \mathrm{ob}(\mathbf C)$を考えたとき、$\lang T(A), \mu_A \rang$はT-代数である。

### 証明

T-代数の条件は、$\mu_A \circ \mu_{T(A)} = \mu_A \circ T(\mu_A)$かつ$\mu_A \circ \eta_{T(A)} = \mathrm{id}_{T(A)}$を満たすことであるが、これはモナドの条件によって満たされている。

[![](https://storage.googleapis.com/zenn-user-upload/45c4df11ca89-20251113.png)](https://q.uiver.app/#q=WzAsOCxbMCwxLCJUKFQoVChBKSkpIl0sWzAsMCwiXFxtYXRoYmYgQyJdLFsxLDEsIlQoVChBKSkiXSxbMSwyLCJUKEEpIl0sWzAsMiwiVChUKEEpKSJdLFsyLDEsIlQoQSkiXSxbMywxLCJUKFQoQSkpIl0sWzMsMiwiVChBKSJdLFsyLDMsIlxcbXVfQSJdLFswLDIsIlxcbXVfe1QoQSl9Il0sWzAsNCwiVChcXG11X0EpIiwyXSxbNCwzLCJcXG11X0EiLDJdLFswLDMsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs1LDYsIlxcZXRhX3tUKEEpfSJdLFs2LDcsIlxcbXVfQSJdLFs1LDcsIlxcbWF0aHJte2lkfV9BIiwyXSxbMTMsNywiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsib2Zmc2V0IjotMywibGV2ZWwiOjEsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

## T-代数の圏

ここでF-代数が圏を成すことを思い出して、T-代数全体が成す圏を考える。
これはアイレンベルク-ムーア圏(*Eilenberg-Moore category*)と呼び、伝統的に$\mathbf C^T$と表記される。

$\mathbf C^T$は、T-代数$\lang A, a : T(A) \to A \rang$を対象に持ち、$f : A \to B$であって$f \circ a = b \circ T(f)$を満たす$\mathbf C$の射を射として持つような圏である。

[![](https://storage.googleapis.com/zenn-user-upload/11cf1545e1f3-20251117.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDXlQiXSxbMCwxLCJcXGxhbmcgQSwgYSBcXHJhbmciXSxbMCwyLCJcXGxhbmcgQiwgYiBcXHJhbmciXSxbMSwwLCJcXG1hdGhiZiBDIl0sWzEsMSwiVChBKSJdLFsyLDEsIkEiXSxbMiwyLCJCIl0sWzEsMiwiVChCKSJdLFsxLDIsImYiXSxbNCw1LCJhIl0sWzUsNiwiZiJdLFs0LDcsIlQoZikiLDJdLFs3LDYsImIiLDJdLFs0LDYsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

## T-代数の自由-忘却随伴

モナド$T$における自由T-代数を作る関手$F^T : \mathbf C \to \mathbf C^T$と、T-代数（自由T-代数とは限らない）を$\mathbf C$に移す忘却関手$U^T : \mathbf C^T$は、随伴関手$F^T \dashv U^T$である。

[![](https://storage.googleapis.com/zenn-user-upload/3de9d3d8174a-20251117.png)](https://q.uiver.app/#q=WzAsOSxbMiwwLCJcXG1hdGhiZiBDXlQiXSxbMiwxLCJcXGxhbmcgVChBKSwgXFxtdV9BIFxccmFuZyJdLFsyLDIsIlxcbGFuZyBUKEIpLCBcXG11X0IgXFxyYW5nIl0sWzEsMSwiQSJdLFsxLDIsIkIiXSxbMSwwLCJcXG1hdGhiZiBDIl0sWzAsMCwiXFxtYXRoYmYgQ15UIl0sWzAsMSwiXFxsYW5nIEEsIGEgXFxyYW5nIl0sWzAsMiwiXFxsYW5nIEIsIGIgXFxyYW5nIl0sWzEsMiwiVChmKSJdLFszLDQsImYiXSxbNSwwLCJGXlQiXSxbNiw1LCJVXlQiXSxbNyw4LCJmIiwyXV0=)

$F^T : \mathbf C \to \mathbf C^T$の定義は次の通り。

$$
\begin{aligned}
F^T(A) &\coloneqq \lang T(A), \mu_A \rang \\
F^T(f) &\coloneqq T(f)
\end{aligned}
$$

また$U^T : \mathbf C^T \to \mathbf C$の定義は次の通り。

$$
\begin{aligned}
U^T(\lang A, a \rang) &\coloneqq A \\
U^T(f) &\coloneqq f
\end{aligned}
$$

### 証明

任意の$\mathbf A \in \mathrm{ob}(\mathbf C)$, $\lang B, b \rang \in \mathrm{ob}(\mathbf C^T)$について以下の自然同型が成り立つことを示す。

$$
\hom_{\mathbf C^T}(F^T(A), \lang B, b \rang) \simeq \hom_\mathbf C(A, U^T \lang B, b \rang)
$$

左から右については、$h : F^T(A) \to \lang B, b \rang$を$h \circ \eta_A : A \to B$に対応させる。
すなわち対応関係$\phi : \hom_{\mathbf C^T}(F^T(-), -) \Rightarrow \hom_\mathbf C(-, U^T(-))$を以下のように定義する。

$$
\phi_{A, \lang B, b \rang} \coloneqq h \mapsto h \circ \eta_A
$$

$\phi$は以下の図式を可換にするため、自然変換である。

[![](https://storage.googleapis.com/zenn-user-upload/f09f70f1f292-20251120.png)](https://q.uiver.app/#q=WzAsNSxbMCwxLCJcXGhvbV97XFxtYXRoYmYgQ15UfShGXlQoQSksIFxcbGFuZyBCLCBiIFxccmFuZykiXSxbMCwwLCJcXG1hdGhiZntTZXR9Il0sWzAsMiwiXFxob21fXFxtYXRoYmYgQyhBLCBVXlQoXFxsYW5nIEIsIGIgXFxyYW5nKSkiXSxbMSwxLCJcXGhvbV97XFxtYXRoYmYgQ15UfShGXlQoQScpLCBcXGxhbmcgQicsIGInIFxccmFuZykiXSxbMSwyLCJcXGhvbV9cXG1hdGhiZiBDKEEnLCBVXlQoXFxsYW5nIEInLCBiJyBcXHJhbmcpKSJdLFswLDIsIlxccGhpX3tBLCBcXGxhbmcgQiwgYiBcXHJhbmd9IiwyXSxbMyw0LCJcXHBoaV97QScsIFxcbGFuZyBCJywgYicgXFxyYW5nfSJdLFsyLDQsIlxcaG9tX1xcbWF0aGJmIEMoZiwgVV5UKGcpKSIsMl0sWzQsMCwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzAsMywiXFxob21fe1xcbWF0aGJmIENeVH0oRl5UKGYpLCBnKSJdXQ==)

#### 証明

$\phi_{A', \lang B', b' \rang} \circ \hom_{\mathbf C^T}(F^T(f), g) \simeq \hom_\mathbf C(f, U^T(g)) \circ \phi_{A, \lang B, b \rang}$は次のようにして確かめられる。

[$\hom$関手](./hom-functor)の射は射の合成と対応づけることを思い出すと、上の可換図式は次の式になる。

$$
\begin{aligned}
g \circ h \circ F^T(f) \circ \eta_A = U^T(g) \circ h \circ \eta_A \circ f
\end{aligned}
$$

圏$\mathbf C$の射として書くと、次の図式になる。$T(f) \circ \eta_{A'} = \eta_A \circ f$はモナドのunitの条件によって保障されているので、図式全体が可換であることが分かる。

[![](https://storage.googleapis.com/zenn-user-upload/dedf22dcd125-20251121.png)](https://q.uiver.app/#q=WzAsMTAsWzIsMywiQiciXSxbMiwyLCJCIl0sWzIsMSwiVChBKSJdLFsxLDMsIkIiXSxbMSwyLCJUKEEpIl0sWzEsMSwiVChBJykiXSxbMCwzLCJUKEEpIl0sWzAsMiwiQSJdLFswLDEsIkEnIl0sWzAsMCwiXFxtYXRoYmYgQyJdLFsxLDAsImciXSxbNCwwLCI9IiwxXSxbMywwLCJVXlQoZyk9ZyIsMl0sWzIsMSwiaCJdLFs0LDEsImgiLDFdLFs1LDEsIj0iLDFdLFs1LDIsIkZeVChmKT1UKGYpIl0sWzQsMywiaCIsMV0sWzcsMywiPSIsMV0sWzYsMywiaCIsMl0sWzUsNCwiVChmKSIsMV0sWzcsNCwiXFxldGFfQSIsMV0sWzgsNCwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxXSxbOCw1LCJcXGV0YV97QSd9Il0sWzcsNiwiXFxldGFfQSIsMl0sWzgsNywiZiIsMl1d)

右から左については、$h' : A \to U^T(\lang B, b \rang)$を$b \circ T(h') : T(A) \to B$に対応させる。
すなわち対応関係$\phi^{-1} : \hom_\mathbf C(-, U^T(-)) \Rightarrow \hom_{\mathbf C^T}(F^T(-), -)$を以下のように定義する。

$$
\phi^{-1}_{A, \lang B, b \rang} \coloneqq h' \mapsto b \circ T(h')
$$

$\phi^{-1}$は以下の図式を可換にするため、自然変換である。

[![](https://storage.googleapis.com/zenn-user-upload/58a3982c1a1d-20251121.png)](https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntTZXR9Il0sWzAsMSwiXFxob21fXFxtYXRoYmYgQyhBLCBVXlQoXFxsYW5nIEIsIGIgXFxyYW5nKSkiXSxbMSwxLCJcXGhvbV9cXG1hdGhiZiBDKEEnLCBVXlQoXFxsYW5nIEInLCBiJyBcXHJhbmcpKSJdLFswLDIsIlxcaG9tX3tcXG1hdGhiZiBDXlR9KEZeVChBKSwgXFxsYW5nIEIsIGIgXFxyYW5nKSJdLFsxLDIsIlxcaG9tX3tcXG1hdGhiZiBDXlR9KEZeVChBJyksIFxcbGFuZyBCJywgYicgXFxyYW5nKSJdLFsxLDIsIlxcaG9tX1xcbWF0aGJmIEMoZiwgVV5UKGcpKSJdLFszLDQsIlxcaG9tX3tcXG1hdGhiZiBDXlR9KEZeVChmKSwgZykiLDJdLFsxLDMsIlxccGhpXnstMX1fe0EsIFxcbGFuZyBCLCBiIFxccmFuZ30iLDJdLFsyLDQsIlxccGhpXnstMX1fe0EnLCBcXGxhbmcgQicsIGInIFxccmFuZ30iXV0=)

#### 証明

同様にhom関手を計算すれば上の図式は以下の式になる。

$$
b \circ T(U^T(g) \circ h' \circ f) = g \circ b \circ T(h') \circ F^T(f)
$$

関手の条件により、$T(U^T(g) \circ h' \circ f) = T(U^T(g)) \circ T(h') \circ T(f)$なので、以下の可換図式が成り立つ。

[![](https://storage.googleapis.com/zenn-user-upload/2e0d5028c769-20251121.png)](https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIlQoQScpIl0sWzAsMiwiVChBKSJdLFsxLDMsIlQoQicpIl0sWzAsMywiVChCKSJdLFsxLDIsIlQoQikiXSxbMSwxLCJUKEEpIl0sWzIsMSwiVChCKSJdLFsyLDIsIkIiXSxbMiwzLCJCJyJdLFsxLDYsIkZeVChmKSA9IFQoZikiXSxbMSwyLCJUKGYpIiwyXSxbMSw1LCI9IiwxXSxbMiwzLCI9IiwxXSxbMiw1LCJUKGgnKSIsMV0sWzIsNCwiVChoJykiLDJdLFszLDksImIiLDJdLFs1LDMsImciXSxbNCwzLCJVXlQoZykgPSBnIiwyXSxbNSw4LCJiIiwxXSxbNSw5LCI9IiwxXSxbNiw1LCJUKGgnKSIsMV0sWzYsNywiVChoJykiXSxbNiw4LCI9IiwxXSxbNyw4LCJiIl0sWzgsOSwiZyJdXQ==)

### 自然同型

最後に$\phi_{A, \lang B, b' \rang} \circ \phi^{-1}_{\lang B, b' \rang} = \mathrm{id}_{\hom_\mathbf C(A, U^T(\lang B, b \rang))}$および$\phi^{-1}_{A, \lang B, b' \rang} \circ \phi_{\lang B, b' \rang} = \mathrm{id}_{\hom_{\mathbf C^T}(F^T(A), \lang B, b \rang)}$を示す。

$\phi$, $\phi^{-1}$の定義を再掲する。

$$
\begin{aligned}
\phi_{A, \lang B, b \rang} &\coloneqq h \mapsto h \circ \eta_A \\
\phi^{-1}_{A, \lang B, b \rang} &\coloneqq h' \mapsto b \circ T(h') \\
\end{aligned}
$$

それぞれ式変形を行えば同型を確かめられる。

$b \circ T(h') = h' \circ a$はF-代数の条件、$a \circ \eta_A = \mathrm{id}_A$ はモナドの条件である。

$$
\begin{aligned}
\phi_{A, \lang B, b \rang}(\phi^{-1}_{A, \lang B, b \rang}(h')) &= b \circ T(h') \circ \eta_A \\
&= h' \circ a \circ \eta_A \\
&= h' \circ \mathrm{id}_A \\
&= h'
\end{aligned}
$$

$b \circ T(h) = h \circ \mu_A$はT-代数の条件、$\mu_A \circ T(\eta_A) = \mathrm{id}_{T(A)}$はモナドの条件である。

$$
\begin{aligned}
\phi^{-1}_{A, \lang B, b \rang}(\phi_{A, \lang B, b \rang}(h)) &= b \circ T(h \circ \eta_A) \\
&= b \circ T(h) \circ T(\eta_A) \\
&= h \circ \mu_A \circ T(\eta_A) \\
&= h \circ \mathrm{id}_{T(A)} \\
&= h
\end{aligned}
$$
