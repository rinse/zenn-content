---
title: "カン拡張"
free: false
---

*すべての概念はカン拡張である。(Mac Lane)*

上の名言だけは前々から知っていたので、定義自体は簡単であることに少し驚いた。

Awodey先生の教科書にはあまりカン拡張についての記述がないように思えるので、alg-d先生の[PDF](https://alg-d.com/math/kan_extension/kan_extension.pdf)を参照する。

## 定義

圏$\mathbf{A}$, $\mathbf{B}$, $\mathbf{C}$および二つの関手$F: A \to B$, $G: A \to C$を考える。
$F$に沿った$G$の右カン拡張(*Right Kan extension of $G$ along $F$*)とは、関手$R: B \to C$と自然変換$\eta: R \circ F \Rightarrow G$からなる普遍射$(R, \eta)$である。

この普遍射は、関手$- \circ F: \mathbf{C}^\mathbf{B} \to \mathbf{C}^\mathbf{A}$から$G: A \to C$への普遍射である。

![right_kan_extension](https://storage.googleapis.com/zenn-user-upload/61ef21142a6e-20240115.png)

$F$に沿った$G$の左カン拡張(*Left Kan extension of $G$ along $F$*)とは、関手$L: B \to C$と自然変換$\epsilon: G \Rightarrow L \circ F$からなる普遍射$(L, \epsilon)$である。

この普遍射は、$G: A \to C$から関手$- \circ F: \mathbf{C}^\mathbf{B} \to \mathbf{C}^\mathbf{A}$への普遍射である。

![left_kan_extension](https://storage.googleapis.com/zenn-user-upload/6df7d561186e-20240116.png)

https://q.uiver.app/#q=WzAsMjIsWzAsMSwiQSJdLFswLDMsIkIiXSxbMiwzLCJDIl0sWzMsMywiWCJdLFszLDIsIlIiXSxbNSwzLCJYIFxcY2lyYyBGIl0sWzQsMiwiRyJdLFs1LDIsIlIgXFxjaXJjIEYiXSxbMywxLCJcXG1hdGhiZntDfV57XFxtYXRoYmZ7Qn19Il0sWzQsMSwiXFxtYXRoYmZ7Q31eXFxtYXRoYmZ7QX0iXSxbMyw1LCJMIl0sWzMsNiwiWCJdLFs0LDUsIkciXSxbNSw1LCJMIFxcY2lyYyBGIl0sWzAsNSwiQSJdLFswLDcsIkIiXSxbMiw3LCJDIl0sWzUsNiwiWCBcXGNpcmMgRiJdLFsxLDAsIlxcbWF0aGNsYXB7XFx0ZXh0e1JpZ2h0IEthbiBleHRlbnNpb259fSJdLFsxLDQsIlxcbWF0aGNsYXB7XFx0ZXh0e0xlZnQgS2FuIGV4dGVuc2lvbn19Il0sWzQsMCwiXFxtYXRoY2xhcHstIFxcY2lyYyBGIFxcdGV4dHvjgYvjgol9IEcgXFx0ZXh0e+OBuOOBruaZrumBjeWwhH0gKFIsIFxcZXRhKX0iXSxbNCw0LCJcXG1hdGhjbGFwe0cgXFx0ZXh0e+OBi+OCiX0gLSBcXGNpcmMgRiBcXHRleHR744G444Gu5pmu6YGN5bCEfSAoTCwgXFxlcHNpbG9uKX0iXSxbMCwyLCJHIl0sWzAsMSwiRiIsMl0sWzEsMiwiUiIsMl0sWzUsNywiXFxnYW1tYSBcXGFzdCBGIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzcsNiwiXFxldGEiLDJdLFs1LDYsIlxccGhpIl0sWzMsNCwiXFxnYW1tYSIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMCwxMSwiXFxkZWx0YSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxNCwxNSwiRiIsMl0sWzE0LDE2LCJHIl0sWzEzLDE3LCJcXGRlbHRhIFxcYXN0IEYiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTIsMTMsIlxcZXBzaWxvbiJdLFsxMiwxNywiXFxwc2kiLDJdLFsxNSwxNiwiTCIsMl0sWzEsMjIsIlxcZXRhIiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFszMSwxNSwiXFxlcHNpbG9uIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwfX1dXQ==

## 記法

右カン拡張の関手$R$と左カン拡張の関手$L$とを、$G$の$F$に沿ったカン拡張であることを強調して書く書き方がいくつかある。

- 右カン拡張 $\mathrm{Ran}_F G$, 左カン拡張 $\mathrm{Lan}_F G$
- 右カン拡張 $F^\ddag G$, 左カン拡張 $F^\dag G$

## 説明

カン拡張とは圏論的な拡張のことである。
ここでの拡張とは、写像の定義域をより大きな集合に拡張することであり、その操作の一般化といえる。

つまり$F$に沿った$G$のカン拡張を得るとは、関手$G: \mathbf{A} \to \mathbf{C}$の域を$\mathbf A$から$\mathbf B$に拡張した関手$R: \mathbf{B} \to \mathbf{C}$を得るイメージとなる。
ただ単に定義域が拡張されるだけではなく、関手$G$の性質と整合性の取れた良い感じの拡張がされていてほしいため、それが普遍性によって担保されている。
