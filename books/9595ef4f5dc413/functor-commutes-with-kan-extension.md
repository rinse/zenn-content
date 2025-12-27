---
title: "関手がKan拡張と交換するとは"
free: false
---

Kan拡張$\lang L, \eta \rang$が関手$H$と交換するとは、$\lang H \circ L, H \ast \eta \rang$がKan拡張であることをいう。

すなわち以下が成り立つことをいう。

$$
H \circ (\mathrm{Lan}_F G) = \mathrm{Lan}_F (H \circ G)
$$

## 定義

$G : \mathbf{A} \to \mathbf{C}$の$F : \mathbf{A} \to \mathbf{B}$に沿った左Kan拡張$\lang L, \eta \rang$と、関手$H : \mathbf{C} \to \mathbf{D}$を考える。

[![diagram](/images/book/9595ef4f5dc413/functor-commutes-with-kan-extension/diagram-2144b6bf.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntBfSJdLFsxLDEsIlxcbWF0aGJme0N9Il0sWzAsMSwiXFxtYXRoYmZ7Qn0iXSxbMiwxLCJcXG1hdGhiZntEfSJdLFswLDEsIkciXSxbMCwyLCJGIiwyXSxbMiwxLCJMIiwyXSxbMSwzLCJIIiwyXSxbNCw2LCJcXGV0YSIsMix7Im9mZnNldCI6Miwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==)

関手$H$がKan拡張$\lang L, \eta \rang$と交換するとは、$\eta$と$H$を水平合成したときに$\lang H \circ L, H \ast \eta \rang$が$H \circ G$の$F$に沿った左Kan拡張になっていることをいう。

[![diagram](/images/book/9595ef4f5dc413/functor-commutes-with-kan-extension/diagram-ea767469.png)](https://q.uiver.app/#q=WzAsMyxbMiwxLCJcXG1hdGhiZntEfSJdLFswLDEsIlxcbWF0aGJme0J9Il0sWzAsMCwiXFxtYXRoYmZ7QX0iXSxbMiwwLCJIIFxcY2lyYyBHIl0sWzEsMCwiSCBcXGNpcmMgTCIsMl0sWzIsMSwiRiIsMl0sWzMsNCwiSCBcXGFzdCBcXGV0YSIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=)

右Kan拡張の場合でも同様の議論ができる。

[![diagram](/images/book/9595ef4f5dc413/functor-commutes-with-kan-extension/diagram-88adb606.png)](https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntBfSJdLFswLDEsIlxcbWF0aGJme0J9Il0sWzEsMSwiXFxtYXRoYmZ7Q30iXSxbMiwxLCJcXG1hdGhiZntEfSJdLFszLDEsIlxcbWF0aGJme0J9Il0sWzMsMCwiXFxtYXRoYmZ7QX0iXSxbNSwxLCJcXG1hdGhiZntEfSJdLFswLDEsIkYiLDJdLFswLDIsIkciXSxbMSwyLCJMIiwyXSxbMiwzLCJIIiwyXSxbNSw0LCJGIiwyXSxbNSw2LCJIIFxcY2lyYyBHIl0sWzQsNiwiSCBcXGNpcmMgTCIsMl0sWzksOCwiXFxlcHNpbG9uIiwwLHsib2Zmc2V0IjotMiwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dLFsxMywxMiwiSCBcXGFzdCBcXGVwc2lsb24iLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV1d)
