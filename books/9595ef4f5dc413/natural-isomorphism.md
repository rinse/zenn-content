---
title: "自然同型"
free: false
---

## 自然同型

自然変換$\iota$が自然同型であるとは、関手$F: \mathbf C \to \mathbf D$, $G: \mathbf C \to \mathbf D$とその間の自然変換$\iota: F \Rightarrow G$があったとき、圏$\mathbf C$の任意の対象$X$に対して圏$\mathbf D$の射$\iota_X: F(X) \to G(X)$が同型射であることをいう。すなわち逆射$\iota^{-1}_X: G(X) \to F(X)$が存在して、$\iota_X \circ \iota^{-1}_X = \mathrm{id}_{G(X)}$と$\iota^{-1}_X \circ \iota_X = \mathrm{id}_{F(X)}$を満たす。

自然同型の存在する関手$F$, $G$を$F \simeq G$のように書く。

![natural_isomorphism](https://storage.googleapis.com/zenn-user-upload/3c357c766309-20231022.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbMywwLCJcXG1hdGhiZiBEIl0sWzMsMSwiRihBKSJdLFs1LDEsIkYoQikiXSxbMywyLCJHKEEpIl0sWzUsMiwiRyhCKSJdLFsxLDIsImYiXSxbNCw1LCJGKGYpIl0sWzYsNywiRyhmKSIsMl0sWzQsNiwiXFxpb3RhX0EiLDAseyJjdXJ2ZSI6LTF9XSxbNSw3LCJcXGlvdGFfQiIsMCx7ImN1cnZlIjotMX1dLFs2LDQsIlxcaW90YV57LTF9X3tBfSIsMCx7ImN1cnZlIjotMX1dLFs3LDUsIlxcaW90YV57LTF9X0IiLDAseyJjdXJ2ZSI6LTF9XV0=

