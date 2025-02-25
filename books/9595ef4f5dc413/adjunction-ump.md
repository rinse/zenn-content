---
title: "随伴関手 普遍性"
free: false
---

随伴関手は普遍射を用いて定義できる。

## 左随伴を得る

圏$\mathbf{C}$, 圏$\mathbf{D}$とそれらの間の関手$G: \mathbf{C} \to \mathbf{D}$を考える。

圏$\mathbf{D}$の任意の対象から$G$への普遍射が存在するとき、ある関手$F: \mathbf{D} \to \mathbf{C}$が存在して、$F \dashv G$を満たす。すなわち$F$は$G$の左随伴である。

### 普遍射の定義の確認

圏$\mathbf{D}$の各対象$D$から関手$G$への[普遍射](./universal-mapping-property.md)を$\lang C_D, \eta_D \rang$と書くことにする。
このとき任意の射$f : D \to G(C)$について、$\=f : C_D \to C$が一意に存在して、$f = G(\=f) \circ \eta_D$を満たす。

![](https://storage.googleapis.com/zenn-user-upload/2e5ff0fdf620-20250224.png)

### 関手を定義する

いま、2つ目の普遍射$\lang C_{D'}, \eta_{D'} \rang$を考える。
このとき普遍性によって、任意の$f : D \to D'$について、圏$\mathbf{D}$において$G(\=f) \circ \eta_D = \eta_D \circ f$を満たす圏$\mathbf{C}$の射$\=f : C_D \to C_{D'}$が一意に存在する。

![](https://storage.googleapis.com/zenn-user-upload/5d83bc5a8015-20250224.png)

この対応付けを使って関手$F : \mathbf{D} \to \mathbf{C}$を定義する。

- $F(D) \overset{\mathrm{def}}{=} C_D$
- $F(f) \overset{\mathrm{def}}{=} \=f$

![](https://storage.googleapis.com/zenn-user-upload/ae22defdb9c9-20250224.png)

### 随伴の確認

このとき$F \dashv G$が成り立つことを確認する。すなわち以下が成り立つことを確認する。

$$
\hom_C(F(\_), \_) \simeq \hom_D(\_, G(\_))
$$

まず$F$の定義と普遍性より、任意の$f : D \to G(C)$について、一意な$\=f : F(D) \to C$が存在する。

これを$\Phi : \hom_D(\_, G(\_)) \Rightarrow \hom_C(F(\_), \_)$と定義する。

![](https://storage.googleapis.com/zenn-user-upload/f52a1d850fd5-20250224.png)

また圏$\mathbf{C}$の任意の$g : F(D) \to C$について、圏$\mathbf{D}$の射$G(g) \circ \eta_D : D \to G(C)$が存在する。$G(g) \circ \eta_D$は、$\eta_D$が$C_D = F(D)$に対応することから一意である。

この$g$から$G(g) \circ \eta_D$への対応付けを$\Psi : \hom_C(F(\_), \_) \Rightarrow \hom_D(\_, G(\_))$として定義する。

![](https://storage.googleapis.com/zenn-user-upload/e1addf599e2f-20250224.png)

https://q.uiver.app/#q=WzAsMzIsWzAsMSwiXFxtYXRoYmYgQyJdLFsxLDIsIkQiXSxbMiwyLCJHKENfRCkiXSxbMiwzLCJHKEMpIl0sWzEsMSwiXFxtYXRoYmYgRCJdLFswLDIsIkNfRCJdLFswLDMsIkMiXSxbMiwxLCJcXG1hdGhjbGFwe15cXGZvcmFsbCBELCBeXFxleGlzdHMgXFxsYW5nIENfRCwgXFxldGFfRCBcXHJhbmd9Il0sWzYsMSwiXFxsYW5nIENfe0QnfSwgXFxldGFfe0QnfSBcXHJhbmciXSxbNSwyLCJEIl0sWzUsMywiRCciXSxbNiwyLCJHKENfRCkiXSxbNiwzLCJHKENfe0QnfSkiXSxbNCwxLCJcXG1hdGhiZntDfSJdLFs1LDEsIlxcbWF0aGJme0R9Il0sWzQsMiwiRihEKSBcXG92ZXJzZXR7XFxtYXRocm17ZGVmfX17PX0gQ19EIl0sWzQsMywiRihEJykgXFxvdmVyc2V0e1xcbWF0aHJte2RlZn19ez19IENfe0QnfSJdLFsxLDAsIlxcbWF0aGNsYXB75pmu6YGN5bCE44Gu5a6a576p44Gu56K66KqNfSJdLFs0LDAsIlxcbWF0aGNsYXB76Zai5omLRuOBruWumue+qX0iXSxbOCwwLCJcXG1hdGhjbGFwe+maj+S8tOmWouS/guOBrueiuuiqjX0iXSxbNywxLCJcXG1hdGhiZntDfSJdLFs4LDEsIlxcbWF0aGJme0R9Il0sWzgsMiwiRCJdLFs5LDIsIkcoQ19EKSJdLFs5LDMsIkcoQykiXSxbNywyLCJGKEQpIl0sWzcsMywiQyJdLFs3LDQsIkYoRCkiXSxbNyw1LCJDIl0sWzksNCwiRyhDX0QpIl0sWzksNSwiRyhDKSJdLFs4LDQsIkQiXSxbMiwzLCJHKFxcPWYpIl0sWzEsMywiZiIsMl0sWzUsNiwiXFw9ZiIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxLDIsIlxcZXRhX0QiXSxbMSwzLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6LTQsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs5LDExLCJcXGV0YV9EIl0sWzEwLDEyLCJcXGV0YV97RCd9IiwyXSxbMTEsMTIsIkcoXFw9ZikiXSxbMTMsMTQsIkciLDAseyJvZmZzZXQiOi0yfV0sWzE0LDEzLCJGIiwwLHsib2Zmc2V0IjotMn1dLFsxNSwxNiwiRihmKSBcXG92ZXJzZXR7XFxtYXRocm17ZGVmfX17PX0gXFw9ZiIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs5LDEwLCJmIiwyXSxbOSwxMiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMjAsMjEsIkciLDAseyJvZmZzZXQiOi0zfV0sWzIxLDIwLCJGIiwwLHsib2Zmc2V0IjotM31dLFsyMiwyMywiXFxldGFfRCJdLFsyMywyNCwiRyhcXD1mKSJdLFsyMiwyNCwiXlxcZm9yYWxsIGYiLDJdLFsyNSwyNiwiXFw9ZiIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsyNCwyMiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJvZmZzZXQiOjQsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFswLDQsIkciXSxbMjcsMjgsIl5cXGZvcmFsbCBnIiwyXSxbMjksMzAsIkcoZykiXSxbMzEsMjksIlxcZXRhX0QiXSxbMzEsMzAsIl57XFxleGlzdHMhfSBHKGcpIFxcY2lyYyBcXGV0YV9EIiwyXSxbMzEsMzAsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsib2Zmc2V0IjotNCwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d

この$\Phi$, $\Psi$が同型射であることを確認する。

$$
\begin{aligned}
\Psi_{D, C}(\Phi_{D, C}(f)) &= \Psi_{D, C}(\=f) \\
&= G(\=f) \circ \eta_D \\
&= f
\end{aligned}
$$

$$
\begin{aligned}
\Phi_{D, C}(\Psi_{D, C}(g)) &= \Phi_{D, C}(G(g) \circ \eta_D) \\
&= \overline{G(g) \circ \eta_D} \\
&= g
\end{aligned}
$$

最後にこの自然同型が$C, D$について自然であることを確認する。
まず$C \in \mathbf{C}$については、以下の図式が可換となる。

![](https://storage.googleapis.com/zenn-user-upload/989648c481a5-20250225.png)

ここで$\hom_C(F(D), c)$は$c \circ -$である。つまり、ある$h : F(D) \to C$について、$c \circ h : F(D) \to C'$を得る。
また$\hom_D(D, G(c))$は$G(c) \circ -$である。つまり、ある$h : D \to G(C)$について、$G(c) \circ h$を得る。

![](https://storage.googleapis.com/zenn-user-upload/2b593d7e1f70-20250225.png)

次に$D \in \mathbf{D}$については、以下の図式が可換となる。

![](https://storage.googleapis.com/zenn-user-upload/1438652946c0-20250225.png)

ここで$\hom_C(F(d), C)$は$- \circ F(d)$である。つまり、ある$h : F(D') \to C$について、$h \circ F(d) : F(D) \to C$を得る。
また$\hom_D(d, G(C))$は$- \circ d$である。つまり、ある$h : D' \to G(C)$について、$h \circ d : D \to G(C)$を得る。

![](https://storage.googleapis.com/zenn-user-upload/5eee4fe06dec-20250225.png)

https://q.uiver.app/#q=WzAsMjMsWzQsMCwiXFxtYXRoYmZ7U2V0fSJdLFs0LDEsIlxcaG9tX0MoRihEKSwgQykiXSxbNSwxLCJcXGhvbV9DKEYoRCksIEMnKSJdLFsyLDAsIlxcbWF0aGJme0R9Il0sWzIsMSwiRCJdLFs0LDIsIlxcaG9tX0QoRCwgRyhDKSkiXSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFs1LDIsIlxcaG9tX0QoRCwgRyhDJykpIl0sWzAsMiwiRihEKSJdLFsyLDIsIkcoQykiXSxbMywyLCJHKEMnKSJdLFswLDMsIkMiXSxbMiwzLCJEIl0sWzMsMywiRCciXSxbNCwzLCJcXGhvbV9DKEYoRCksIEMpIl0sWzUsMywiXFxob21fQyhGKEQnKSwgQykiXSxbNCw0LCJcXGhvbV9EKEQsIEcoQykpIl0sWzUsNCwiXFxob21fRChEJywgRyhDKSkiXSxbMCw0LCJGKEQpIl0sWzEsNCwiRihEJykiXSxbMiw0LCJHKEMpIl0sWzEsMiwiXFxob21fQyhGKEQpLCBjKSJdLFs3LDgsImMiXSxbMSw1LCJcXFBoaV97RCwgQ30iLDJdLFs1LDksIlxcaG9tX0QoRCwgRyhjKSkiLDJdLFsyLDksIlxcUGhpX3tELCBDJ30iXSxbMTAsNywiXlxcZm9yYWxsIGgiXSxbMTAsOCwiXntcXGV4aXN0cyF9IGMgXFxjaXJjIGgiLDJdLFsxMCw4LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6LTQsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs0LDExLCJeXFxmb3JhbGwgaCIsMl0sWzQsMTIsIl57XFxleGlzdHMhfSBHKGMpIFxcY2lyYyBoIl0sWzExLDEyLCJHKGMpIiwyXSxbNCwxMiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJvZmZzZXQiOjQsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxLDksIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzE0LDE1LCJkIl0sWzE2LDE4LCJcXFBoaV97RCwgQ30iLDJdLFsxNywxOSwiXFxQaGlfe0QnLCBDfSJdLFsxNywxNiwiXFxob21fQyhGKGQpLCBDKSIsMl0sWzIwLDIxLCJGKGQpIiwyXSxbMTksMTgsIlxcaG9tX0QoZCwgRyhDKSkiXSxbMTQsMjIsIl57XFxleGlzdHMhfWggXFxjaXJjIGQiLDJdLFsxNSwyMiwiXlxcZm9yYWxsIGgiXSxbMjAsMTMsIl57XFxleGlzdHMhfSBoIFxcY2lyYyBGKGQpIl0sWzIxLDEzLCJeXFxmb3JhbGwgaCIsMl0sWzE2LDE5LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsyMSwxMywiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJvZmZzZXQiOi00LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTUsMjIsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsib2Zmc2V0Ijo0LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=

## 右随伴を得る

同様の議論で、普遍射から右随伴を得られる。

$G : \mathbf{C} \to \mathbf{D}$から圏$\mathbf{D}$の任意の対象への普遍射が存在するとき、ある関手$F: \mathbf{D} \to \mathbf{C}$が存在して、$G \dashv F$を満たす。すなわち$F$は$G$の右随伴である。
