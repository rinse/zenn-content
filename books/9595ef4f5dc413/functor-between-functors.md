---
title: "関手間の関手"
---

関手を合成する操作は、それ自体が関手になる。
すなわち、関手$F$を適用してから関手を適用する操作$- \circ F$と、関手を適用してから$F$を適用する操作$F \circ -$は、それぞれ関手となる。

また左Kan拡張$\mathrm{Lan}_F$とは$- \circ F$の左随伴関手のことであり、右Kan拡張$\mathrm{Ran}_F$とは$- \circ F$の右随伴関手のことである。すなわち以下が成り立つ：

$$
\mathrm{Lan}_F \dashv - \circ F \dashv \mathrm{Ran}_F
$$

## 関手間の関手

関手$F : \mathbf A \to \mathbf B$を考える。

$- \circ F : \mathbf C^B \to \mathbf C^A$は、対象$G : \mathbf B \to \mathbf C$を$G \circ F : \mathbf A \to \mathbf C$に、射$\theta : G \Rightarrow H$を水平合成$\theta \ast F : F \circ G \Rightarrow F \circ H$に写す。

[![diagram](/images/book/9595ef4f5dc413/functor-between-functors/diagram-f89c8ea9.png)](https://q.uiver.app/#q=WzAsMTAsWzMsMCwiXFxtYXRoYmYgQ15cXG1hdGhiZiBCIl0sWzQsMCwiXFxtYXRoYmYgQ15cXG1hdGhiZiBBIl0sWzMsMSwiRyJdLFszLDIsIkgiXSxbNCwxLCJHIFxcY2lyYyBGIl0sWzQsMiwiSCBcXGNpcmMgRiJdLFsxLDEsIlxcbWF0aGJmIEIiXSxbMiwxLCJcXG1hdGhiZiBDIl0sWzAsMSwiXFxtYXRoYmYgQSJdLFswLDAsIlxcbWF0aGJmIHtDYXR9Il0sWzAsMSwiLSBcXGNpcmMgRiJdLFsyLDMsIlxcdGhldGEiXSxbNCw1LCJcXHRoZXRhIFxcYXN0IEYiXSxbNiw3LCJHIiwwLHsiY3VydmUiOi0xfV0sWzYsNywiSCIsMix7ImN1cnZlIjoxfV0sWzgsNiwiRiJdLFsxMywxNCwiXFx0aGV0YSIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=)

同様に関手$H : \mathbf B \to \mathbf C$を考える。
関手$H \circ -: \mathbf B^\mathbf A \to \mathbf C ^\mathbf A$は、対象$F : \mathbf A \to \mathbf B$を$H \circ F : \mathbf A \to \mathbf C$に、射$\theta : F \Rightarrow G$を水平変換$\theta : H \ast \theta : H \circ F \Rightarrow H \circ G$ に写す。

[![diagram](/images/book/9595ef4f5dc413/functor-between-functors/diagram-fbbfe42b.png)](https://q.uiver.app/#q=WzAsMTAsWzMsMCwiXFxtYXRoYmYgQl5cXG1hdGhiZiBBIl0sWzQsMCwiXFxtYXRoYmYgQ15cXG1hdGhiZiBBIl0sWzMsMSwiRiJdLFszLDIsIkciXSxbNCwxLCJIIFxcY2lyYyBGIl0sWzQsMiwiSCBcXGNpcmMgRyJdLFsxLDEsIlxcbWF0aGJmIEIiXSxbMiwxLCJcXG1hdGhiZiBDIl0sWzAsMSwiXFxtYXRoYmYgQSJdLFswLDAsIlxcbWF0aGJmIHtDYXR9Il0sWzAsMSwiSCBcXGNpcmMgLSJdLFsyLDMsIlxcdGhldGEiXSxbNCw1LCJIIFxcYXN0IFxcdGhldGEiXSxbNiw3LCJIIiwyXSxbOCw2LCJGIiwwLHsiY3VydmUiOi0xfV0sWzgsNiwiRyIsMix7ImN1cnZlIjoxfV0sWzE0LDE1LCJcXHRoZXRhIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==)

## 左Kan拡張

$F$に沿った関手の左Kan拡張は$- \circ F$の左随伴である。すなわち以下が成り立つ。

$$
\mathrm{Lan}_F \dashv - \circ F
$$

$\mathrm{Lan}_F$の定義は、[随伴関手の普遍性による定義](./adjunction-ump)によって得られるものである。

すなわち$\mathrm{Lan}_F$は、対象$G \in \mathbf C^\mathbf B$を$\mathrm{Lan}_F G$に写す。
また射$\mathrm{Lan}_F(\xi) : \mathrm{Lan}_F G \to \mathrm{Lan}_F G'$は普遍性により定める。すなわち、$\xi : G \to G'$が与えられたとき、ある$h : \mathrm{Lan}_F G \to \mathrm{Lan}_F G'$が一意に存在して、$\lambda' \circ \xi = (h \ast F) \circ \lambda$を満たす。この$h$を$\mathrm{Lan}_F(\xi)$と定義する。なお$\lambda$, $\lambda'$の存在は、任意の$G \in \mathbf C^\mathbf A$から$- \circ F$への普遍射$\lang \mathrm{Lan}_F G, \lambda \rang$が与えられていることから保証されている。

[![diagram](/images/book/9595ef4f5dc413/functor-between-functors/diagram-3972f108.png)](https://q.uiver.app/#q=WzAsOCxbMCwxLCJcXG1hdGhybXtMYW59X0YgRyJdLFswLDIsIlxcbWF0aHJte0xhbn1fRiBHJyJdLFsxLDEsIkciXSxbMSwyLCJHJyJdLFsyLDEsIihcXG1hdGhybXtMYW59X0YgRykgXFxjaXJjIEYiXSxbMiwyLCIoXFxtYXRocm17TGFufV9GIEcnKSBcXGNpcmMgRiJdLFswLDAsIlxcbWF0aGJmIENeXFxtYXRoYmYgQiJdLFsxLDAsIlxcbWF0aGJmIENeXFxtYXRoYmYgQSJdLFswLDEsImgiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiwzLCJcXHhpIiwyXSxbMiw0LCJcXGxhbWJkYSJdLFs0LDUsImggXFxhc3QgRiJdLFszLDUsIlxcbGFtYmRhJyIsMl0sWzIsNSwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)


## 右Kan拡張

$F$に沿った右Kan拡張は$- \circ F$の右随伴である。すなわち以下が成り立つ。

$$
- \circ F \dashv \mathrm{Ran}_F
$$
