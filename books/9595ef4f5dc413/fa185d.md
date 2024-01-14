---
title: "自然変換の垂直合成"
free: false
---

## 自然変換の垂直合成 (*Vertical composition*)

圏$\mathbf C$, $\mathbf D$, 関手$F, G, H: \mathbf C \to \mathbf D$とそれらの間の自然変換$\eta: F \Rightarrow G$, $\theta: G \Rightarrow H$があった時、$\eta$と$\theta$の垂直合成$\theta \circ \eta: F \Rightarrow H$を考えることができる。

$\eta$と$\theta$の垂直合成$\theta \circ \eta$は、$\mathbf C$の任意の$X$に対して$\theta_X \circ \eta_X$であるような自然変換であり、下図を可換にする。

![vertical_composition](https://storage.googleapis.com/zenn-user-upload/f00ad108670c-20231203.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMSwiQSJdLFszLDEsIkYoQSkiXSxbMSwxLCJCIl0sWzQsMSwiRihCKSJdLFszLDIsIkcoQSkiXSxbNCwyLCJHKEIpIl0sWzMsMywiSChBKSJdLFs0LDMsIkgoQikiXSxbMCwwLCJcXG1hdGhiZiBDIl0sWzMsMCwiXFxtYXRoYmYgRCJdLFswLDIsImYiXSxbMSwzLCJGKGYpIl0sWzQsNSwiRyhmKSJdLFsxLDQsIlxcZXRhX0EiXSxbMyw1LCJcXGV0YV9CIl0sWzYsNywiSChmKSJdLFs0LDYsIlxcdGhldGFfQSJdLFs1LDcsIlxcdGhldGFfQiJdLFszLDcsIihcXHRoZXRhIFxcY2lyYyBcXGV0YSlfQiA9IFxcdGhldGFfQiBcXGNpcmMgXFxldGFfQiIsMCx7ImN1cnZlIjotM31dLFsxLDYsIihcXHRoZXRhIFxcY2lyYyBcXGV0YSlfQSA9IFxcdGhldGFfQSBcXGNpcmMgXFxldGFfQSIsMix7ImN1cnZlIjozfV1d

垂直合成$\theta \circ \eta$とその成分$\eta$, $\theta$は、圏$\mathbf C$の対象で添え字づけられた圏$\mathbf D$の射の族である。

自然変換$\eta$と$\theta$の垂直合成$\theta \circ \eta$が自然変換であることの証明は、自明であるため省略する。