---
title: "随伴関手1"
free: false
---

## 復習: 圏同値

圏$\mathbf C$, $\mathbf D$が圏同値であるとは、関手$F: \mathbf D \to \mathbf C$, $G: \mathbf C \to \mathbf D$と自然変換$\epsilon: 1_C \Rightarrow F \circ G$と$\eta: 1_D \Rightarrow G \circ F$が存在して、かつ$\epsilon$, $\eta$がそれぞれ自然同型であることをいうのだった。

![equivalent_categories](https://storage.googleapis.com/zenn-user-upload/cfc4f56bfa1f-20231125.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwxLCJDIl0sWzEsMSwiQyciXSxbMywxLCJEIl0sWzQsMSwiRCciXSxbMCwyLCJGKEcoQykpIl0sWzEsMiwiRihHKEMnKSkiXSxbMywyLCJHKEYoRCkpIl0sWzQsMiwiRyhGKEQnKSkiXSxbMiwzLCJmIl0sWzQsNSwiZyJdLFs2LDcsIkYoRyhmKSkiLDJdLFs4LDksIkcoRihnKSkiLDJdLFsyLDYsIlxcZXBzaWxvbl9DIiwyXSxbMyw3LCJcXGVwc2lsb25fe0MnfSJdLFs0LDgsIlxcZXRhX0QiLDJdLFs1LDksIlxcZXRhX3tEJ30iXV0=

## 導入

随伴関手(*Adjoint functors*)とは、圏同値よりも緩い同値関係を作る関手対のことだ。

圏同値を構成するのは、関手$F: \mathbf D \to \mathbf C$, $G: \mathbf C \to \mathbf D$と自然変換$\epsilon: 1_C \Rightarrow F \circ G$と$\eta: 1_D \Rightarrow G \circ F$であった。
随伴関手も構成要素は同様だが、自然変換に対する条件が緩くなっている。

## 定義

圏$\mathbf C$, $\mathbf D$の間の随伴(*Adjunction*)とは、関手$F: \mathbf D \to \mathbf C$と関手$G: \mathbf C \to \mathbf D$と自然変換$\epsilon: F \circ G \Rightarrow 1_C$と$\eta: 1_D \Rightarrow G \circ F$がが存在して、かつ$1_F = (\epsilon \ast F) \circ (F \ast \eta)$と$1_G = (G \ast \epsilon) \circ (\eta \ast G)$（counit-unit 恒等式）がそれぞれ成り立つことをいう。

このとき$F$, $G$を随伴関手と呼び、$F \dashv G$と書く。また$F$を$G$の左随伴、同じことだが、$G$を$F$の右随伴と呼ぶ。
また自然変換$\epsilon: F \circ G \Rightarrow 1_C$を余単位(*counit*)、$\eta: 1_D \Rightarrow G \circ F$を単位(*unit*)と呼ぶ。

下図では上半分が構成要素たる関手と自然変換の提示を、下半分が満たすべき条件を表している。圏同値とは違い、随伴では自然変換が満たすべき条件が複雑なので、このように分けて書くことにした。
下半分で、圏$\mathbf D$の任意の対象$Y$に対して$\epsilon_{F(Y)} \circ F(\eta_Y) = \mathrm{id}_{F(Y)}$であり、圏$\mathbf C$の任意の対象$X$に対して$G(\epsilon_X) \circ \eta_{G(X)} = \mathrm{id}_{G(X)}$であれば、unit-counit恒等式が満たされているといえる。

![adjunction](https://storage.googleapis.com/zenn-user-upload/220762674f37-20231125.png)

https://q.uiver.app/#q=WzAsMjIsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwyLCJDIl0sWzEsMiwiQyciXSxbMywxLCJEIl0sWzQsMSwiRCciXSxbMCwxLCJGKEcoQykpIl0sWzEsMSwiRihHKEMnKSkiXSxbMywyLCJHKEYoRCkpIl0sWzQsMiwiRyhGKEQnKSkiXSxbMCw0LCJGKEQpIl0sWzEsNCwiRihEJykiXSxbMCw1LCJGKEcoRihEKSkpIl0sWzEsNSwiRihHKEYoRCcpKSkiXSxbMCw2LCJGKEQpIl0sWzEsNiwiRihEJykiXSxbMyw1LCJHKEYoRyhDKSkpIl0sWzQsNSwiRyhGKEcoQycpKSkiXSxbMyw0LCJHKEMpIl0sWzQsNCwiRyhDJykiXSxbMyw2LCIgRyhDKSJdLFs0LDYsIkcoQycpIl0sWzIsMywiZiIsMl0sWzQsNSwiZyJdLFs2LDcsIkYoRyhmKSkiXSxbOCw5LCJHKEYoZykpIiwyXSxbNiwyLCJcXGVwc2lsb25fQyIsMl0sWzcsMywiXFxlcHNpbG9uX3tDJ30iXSxbNCw4LCJcXGV0YV9EIiwyXSxbNSw5LCJcXGV0YV97RCd9Il0sWzEwLDExLCJGKGcpIl0sWzEyLDEzLCJGKEcoRihnKSkpIl0sWzEwLDEyLCJGKFxcZXRhX0QpIiwyXSxbMTEsMTMsIkYoXFxldGFfe0QnfSkiXSxbMTQsMTUsIkYoZykiLDJdLFsxMiwxNCwiXFxlcHNpbG9uX3tGKEQpfSIsMl0sWzEzLDE1LCJcXGVwc2lsb25fe0YoRCcpfSJdLFsxNiwxNywiRyhGKEcoZikpKSJdLFsxOCwxOSwiRyhmKSJdLFsxOCwxNiwiXFxldGFfe0coQyl9IiwyXSxbMTksMTcsIlxcZXRhX3tHKEMnKX0iXSxbMjAsMjEsIkcoZikiLDJdLFsxNiwyMCwiRyhcXGVwc2lsb25fQykiLDJdLFsxNywyMSwiRyhcXGVwc2lsb25fe0MnfSkiXV0=

## 圏同値との比較

### 構成要素は共通か？

先に、圏同値と随伴とでは構成要素が共通していると言ったが、よく見比べてみると少し違うことに気がつく。

再掲するが、これが圏同値で使った図だ。

![equivalent_categories](https://storage.googleapis.com/zenn-user-upload/cfc4f56bfa1f-20231125.png)

これが随伴で使った図だ。

![adjunction](https://storage.googleapis.com/zenn-user-upload/07bec241519b-20231125.png)

圏$\mathbf C$における自然変換$\epsilon$の方向がそれぞれ違ってしまっている。
しかしながら、圏同値であれば自然変換$\epsilon$は自然同型であるので、圏$\mathbf C$の各対象$X$について$\epsilon_X: X \to F(G(X))$には必ず逆射$\epsilon_X^{-1}: F(G(X)) \to X$が存在するので、構成要素は同じといって差し支えないだろう。

## ひし形合成との比較

随伴関手を構成する自然変換に求められる性質（counit-unit 恒等式）は、自然変換のひし形合成でより分かりやすく可視化できる。

以下の二つのひし形の合成が、それぞれ$1_G$, $1_F$に等しくなると主張しているのだ。

![diamond_GFG](https://storage.googleapis.com/zenn-user-upload/b27e82c1fe8b-20231206.png)

![diamond_FGF](https://storage.googleapis.com/zenn-user-upload/55f1defe310e-20231206.png)

ひし形合成にまだ慣れていない場合は、下の水平合成まで行った計算途中の図を補助輪のように使うといいだろう。

![GFG](https://storage.googleapis.com/zenn-user-upload/1ffecb8d0648-20231206.png)

![FGF](https://storage.googleapis.com/zenn-user-upload/9f58bbe40256-20231206.png)

https://q.uiver.app/#q=WzAsMTYsWzAsMSwiXFxtYXRoYmYgQyJdLFsxLDAsIlxcbWF0aGJmIEQiXSxbMiwxLCJcXG1hdGhiZiBDIl0sWzMsMCwiXFxtYXRoYmYgRCJdLFswLDIsIlxcbWF0aGJmIEQiXSxbMiwyLCJcXG1hdGhiZiBEIl0sWzEsMywiXFxtYXRoYmYgQyJdLFszLDMsIlxcbWF0aGJmIEMiXSxbNCwxLCJcXG1hdGhiZiBDIl0sWzYsMCwiXFxtYXRoYmYgRCJdLFs0LDIsIlxcbWF0aGJmIEQiXSxbNiwzLCJcXG1hdGhiZiBDIl0sWzgsMCwiQyJdLFsxMCwwLCJEIl0sWzgsMywiRCJdLFsxMCwzLCJDIl0sWzAsMSwiRyJdLFswLDIsIjFfe1xcbWF0aGJmIEN9IiwyXSxbMiwzLCJHIiwyXSxbMSwzLCIxX3tcXG1hdGhiZiBEfSJdLFsxLDIsIkYiLDFdLFs0LDUsIjFfe1xcbWF0aGJmIER9Il0sWzQsNiwiRiIsMl0sWzUsNywiRiJdLFs2LDUsIkciLDFdLFs4LDksIkciLDAseyJsYWJlbF9wb3NpdGlvbiI6NDAsImN1cnZlIjotMn1dLFs4LDksIkciLDIseyJjdXJ2ZSI6Mn1dLFs2LDcsIjFfe1xcbWF0aGJmIEN9IiwyXSxbMTAsMTEsIkYiLDAseyJjdXJ2ZSI6LTJ9XSxbMTAsMTEsIkYiLDIseyJjdXJ2ZSI6Mn1dLFsxMiwxMywiRyIsMCx7ImN1cnZlIjotM31dLFsxMiwxMywiRyIsMix7ImN1cnZlIjozfV0sWzEyLDEzLCJHRkciLDFdLFsxNCwxNSwiRiIsMCx7ImN1cnZlIjotM31dLFsxNCwxNSwiRiIsMix7ImN1cnZlIjozfV0sWzE0LDE1LCJGR0YiLDFdLFsxLDE3LCJcXGVwc2lsb24iLDAseyJzaG9ydGVuIjp7InRhcmdldCI6MjB9fV0sWzE5LDIsIlxcZXRhIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwfX1dLFsyMSw2LCJcXGV0YSIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMH19XSxbNSwyNywiXFxlcHNpbG9uIiwwLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFszMCwzMiwiXFxldGEgXFxhc3QgRyIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbMzIsMzEsIkcgXFxhc3QgXFxlcHNpbG9uIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dLFszNSwzNCwiXFxlcHNpbG9uIFxcYXN0IEYiLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV0sWzMzLDM1LCJGIFxcYXN0IFxcZXRhIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dLFsyOCwyOSwiKFxcZXBzaWxvbiBcXGFzdCBGKSBcXGNpcmMgKEYgXFxhc3QgXFxldGEpID0gMV9GIiwwLHsibGFiZWxfcG9zaXRpb24iOjAsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbMjUsMjYsIihHIFxcYXN0IFxcZXBzaWxvbikgXFxjaXJjIChcXGV0YSBcXGFzdCBHKSA9IDFfRyIsMCx7ImxhYmVsX3Bvc2l0aW9uIjoxMDAsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=

## 随伴関手の左と右

随伴では、その定義から、圏同値とは異なり、それを構成する関手対の間に立場上の違いが存在して、それぞれ左右という言い方で区別される。

この立場の違いを作り出しているのは、自然変換の非対称性だ。すなわち、二つの自然変換$\epsilon: F \circ G \Rightarrow 1_C$, $\eta: 1_D \Rightarrow G \circ F$の始域と余域の非対称性が左右の違いを生む。
