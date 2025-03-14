---
title: "関手がKan拡張と交換するとは"
free: false
---

Kan拡張$\lang L, \eta \rang$が関手$H$と交換するとは、$\lang H \circ L, H \ast \eta \rang$がKan拡張であることをいう。

## 定義

$G : \mathbf{A} \to \mathbf{C}$の$F : \mathbf{A} \to \mathbf{B}$に沿った左Kan拡張$\lang L, \eta \rang$と、関手$H : \mathbf{C} \to \mathbf{D}$を仮定する。

![](https://storage.googleapis.com/zenn-user-upload/242d6d84b4d3-20250301.png)

関手$H$がKan拡張$\lang L, \eta \rang$と交換するとは、$\eta$と$H$を水平合成したときに$\lang H \circ L, H \ast \eta \rang$が$H \circ G$の$F$に沿った左Kan拡張になっていることをいう。

![](https://storage.googleapis.com/zenn-user-upload/cc2d0a4fd9b3-20250301.png)

右Kan拡張の場合でも同様の議論ができる。

![](https://storage.googleapis.com/zenn-user-upload/34c93ce6cd9b-20250301.png)

https://q.uiver.app/#q=WzAsMTUsWzAsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntDfSJdLFswLDIsIlxcbWF0aGJme0J9Il0sWzIsMiwiXFxtYXRoYmZ7RH0iXSxbMywyLCJcXG1hdGhiZntCfSJdLFszLDEsIlxcbWF0aGJme0F9Il0sWzUsMiwiXFxtYXRoYmZ7RH0iXSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMywiXFxtYXRoYmZ7QX0iXSxbMCw0LCJcXG1hdGhiZntCfSJdLFsxLDQsIlxcbWF0aGJme0N9Il0sWzIsNCwiXFxtYXRoYmZ7RH0iXSxbMywzLCJcXG1hdGhiZntBfSJdLFszLDQsIlxcbWF0aGJme0J9Il0sWzUsNCwiXFxtYXRoYmZ7RH0iXSxbMCwxLCJHIl0sWzAsMiwiRiIsMl0sWzIsMSwiTCIsMl0sWzEsMywiSCIsMl0sWzUsNiwiSCBcXGNpcmMgRyJdLFs0LDYsIkggXFxjaXJjIEwiLDJdLFs1LDQsIkYiLDJdLFsxMCwxMSwiSCIsMl0sWzgsOSwiRiIsMl0sWzksMTAsIkwiLDJdLFs4LDEwLCJHIl0sWzEyLDEzLCJGIiwyXSxbMTIsMTQsIkggXFxjaXJjIEciXSxbMTMsMTQsIkggXFxjaXJjIEwiLDJdLFsxNSwxNywiXFxldGEiLDIseyJvZmZzZXQiOjIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbMTksMjAsIkggXFxhc3QgXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV0sWzI0LDI1LCJcXGVwc2lsb24iLDAseyJvZmZzZXQiOi0yLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV0sWzI4LDI3LCJIIFxcYXN0IFxcZXBzaWxvbiIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=
