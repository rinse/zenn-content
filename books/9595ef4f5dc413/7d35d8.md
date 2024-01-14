---
title: "イコライザ"
free: false
---

## 定義

圏$\mathbf{C}$における射$f, g: A \to B$間のイコライザ (*等価子*, *Equalizer*, *英: Equaliser*) とは、対象$E$と射$e: E \to A$の組からなり、以下を満たす。

$$
f \circ e = g \circ e
$$

また以下の普遍性を満たす必要がある。

$$
^\forall z: Z \to A, ^{\exists!} u: Z \to E, z = e \circ u
$$

すなわち任意の$z: Z \to A$に対して、射$u: Z \to E$が一意に存在して、$z = e \circ u$を満たす。

![equaliser](https://storage.googleapis.com/zenn-user-upload/15668c058245-20240104.png)
https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMiwxLCJCIl0sWzAsMSwiRSJdLFswLDIsIloiXSxbMSwyLCJmIiwwLHsiY3VydmUiOi0xfV0sWzMsMSwiZSJdLFsxLDIsImciLDIseyJjdXJ2ZSI6MX1dLFs0LDMsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNCwxLCJ6IiwyXV0=

## 定理1. (E, e)がイコライザであるとき、eはモノ射である

$(E, e)$がイコライザであるとき、$e$は[モノ射](https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/82db73#%E3%83%A2%E3%83%8E%E5%B0%84)である。

### 証明

対象$E$と射$e: E \to A$を圏$\mathbf{C}$における射$f, g: A \to B$間のイコライザとする。任意に射$x_1, x_2: X \to E$をとって$e \circ x_1 = e \circ x_2$を満たすとしたとき、$x_1 = x_2$を満たすことを示す。

![equaliser_is_monic_assumption](https://storage.googleapis.com/zenn-user-upload/26241c4b6c1c-20240104.png)
https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMiwxLCJCIl0sWzAsMSwiRSJdLFswLDIsIlgiXSxbMSwyLCJmIiwwLHsiY3VydmUiOi0xfV0sWzMsMSwiZSJdLFsxLDIsImciLDIseyJjdXJ2ZSI6MX1dLFs0LDMsInhfMSwgeF8yIl0sWzQsMSwiZSBcXGNpcmMgeF8xID0gZSBcXGNpcmMgeF8yIiwyLHsibGFiZWxfcG9zaXRpb24iOjEwMH1dXQ==

仮定より$e \circ x_1 = e \circ x_2$であるから、これを$x$と置く。

![equalizer_is_monic1](https://storage.googleapis.com/zenn-user-upload/3f881e5e3881-20240104.png)
https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMiwxLCJCIl0sWzAsMSwiRSJdLFswLDIsIlgiXSxbMSwyLCJmIiwwLHsiY3VydmUiOi0xfV0sWzMsMSwiZSJdLFsxLDIsImciLDIseyJjdXJ2ZSI6MX1dLFs0LDEsInggXFxvdmVyc2V0e1xcbWF0aHJte2RlZn19ez19IGUgXFxjaXJjIHhfMSA9IGUgXFxjaXJjIHhfMiIsMix7ImxhYmVsX3Bvc2l0aW9uIjoxMDB9XV0=

$(E, e)$はイコライザであるから、$x: X \to A$に対して射$u: X \to E$が一意に存在して、$x = e \circ u$を満たす。

![equalizer_is_monic2](https://storage.googleapis.com/zenn-user-upload/f981ad59bb4f-20240104.png)
https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMiwxLCJCIl0sWzAsMSwiRSJdLFswLDIsIlgiXSxbMSwyLCJmIiwwLHsiY3VydmUiOi0xfV0sWzMsMSwiZSJdLFsxLDIsImciLDIseyJjdXJ2ZSI6MX1dLFs0LDEsInggPSBlIFxcY2lyYyB1IiwyLHsibGFiZWxfcG9zaXRpb24iOjgwfV0sWzQsMywidSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dXQ==

$x = e \circ x_1 = e \circ x_2 = e \circ u$と$u$の一意性より、$x_1 = x_2 = u$が示された。
以上より$(E, e)$がイコライザであるとき、$e$はモノ射である。

証明終わり。

## 定理2. 任意の二対象の積と任意の並行射のイコライザが存在するとき、引き戻しが存在する

圏$\mathbf{C}$を、任意の二対象の積と、任意の並行射に対するイコライザが存在する圏とする。対象$A$, $B$, $C$と射$f: A \to C$, $g: B \to C$と並行射$f \circ p_1, g \circ p_2: A \times B \to C$のイコライザ$(E, e)$を考えたとき、$(E, p_1 \circ e, p_2 \circ e)$は引き戻しである。

### 証明

$f \circ \pi_1 = g \circ \pi_2$を満たす、任意の3つ組$(Z, \pi_1, \pi_2)$を考える。

![triple](https://storage.googleapis.com/zenn-user-upload/c57dc429241f-20240107.png)

仮定より、圏$\mathbf{C}$には二対象$A$, $B$の積$(A \times B, p_1, p_2)$が存在して、一意な射$u: Z \to A \times B$は$\pi_1 = p_1 \circ u$, $\pi_2 = p_2 \circ u$を満たす。

![A_times_B](https://storage.googleapis.com/zenn-user-upload/3f5119e0c7ca-20240107.png)

仮定より、並行射$f \circ p_1, g \circ p_2: A \times B \to C$にはイコライザ$(E, e)$が存在して、$f \circ p_1 \circ e = g \circ p_2 \circ e$を満たす。また$u$に対して$u = e \circ v$を満たす一意な仲介射$v$が存在する。

![equaliser](https://storage.googleapis.com/zenn-user-upload/182bab16a7b2-20240107.png)

任意の$\pi_1: Z \to A$, $\pi_2: Z \to B$に対して、射$u: Z \to A \times B$が一意に存在して、$\pi_1 = p_1 \circ u$, $\pi_2 = p_2 \circ u$を満たし、なおかつ射$u: Z \to A \times B$には$v: Z \to E$が一意に存在して、$u = e \circ v$を満たす。
すなわち任意の$\pi_1: Z \to A$, $\pi_2: Z \to B$に対して、射$v: Z \to E$が一意に存在して、$\pi_1 = p_1 \circ e \circ v$, $\pi_2 = p_2 \circ e \circ v$を満たす。

以上より$(E, p_1 \circ e, p_2 \circ e)$は引き戻しである。

![pullback](https://storage.googleapis.com/zenn-user-upload/35148864a10e-20240107.png)

https://q.uiver.app/#q=WzAsMjAsWzAsMiwiQSJdLFsxLDEsIkIiXSxbMSwyLCJDIl0sWzAsMSwiWiJdLFswLDAsIlxcbWF0aGJme0N9Il0sWzMsMSwiWiJdLFs0LDMsIkEiXSxbNSwyLCJCIl0sWzUsMywiQyJdLFs0LDIsIkEgXFx0aW1lcyBCIl0sWzcsMSwiRSJdLFs4LDEsIkEgXFx0aW1lcyBCIl0sWzksMSwiQyJdLFsxMiwyLCJFIl0sWzEzLDMsIkEgXFx0aW1lcyBCIl0sWzE0LDQsIkMiXSxbMTQsMiwiQiJdLFsxMiw0LCJBIl0sWzcsMiwiWiJdLFsxMSwxLCJaIl0sWzMsMCwiXFxwaV8xIiwyXSxbMCwyLCJmIiwyXSxbMSwyLCJnIl0sWzMsMSwiXFxwaV8yIl0sWzYsOCwiZiIsMl0sWzcsOCwiZyJdLFs1LDksInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNSw2LCJcXHBpXzEiLDIseyJjdXJ2ZSI6MX1dLFs1LDcsIlxccGlfMiIsMCx7ImN1cnZlIjotMX1dLFs5LDYsInBfMSIsMl0sWzksNywicF8yIl0sWzExLDEyLCJmIFxcY2lyYyBwXzEiLDAseyJvZmZzZXQiOi0xfV0sWzExLDEyLCJnIFxcY2lyYyBwXzIiLDIseyJvZmZzZXQiOjF9XSxbMTAsMTEsImUiXSxbMTQsMTYsInBfMiJdLFsxNCwxNywicF8xIiwyXSxbMTcsMTUsImYiLDJdLFsxMywxNCwiZSIsMV0sWzE2LDE1LCJnIl0sWzE4LDExLCJ1IiwyXSxbMTgsMTAsInYiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTksMTMsInYiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTksMTQsInU9ZSBcXGNpcmMgdiIsMSx7ImN1cnZlIjotMiwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZG90dGVkIn19fV0sWzE5LDE3LCJcXHBpXzEgPSBwXzEgXFxjaXJjIHUiLDIseyJjdXJ2ZSI6MSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZG90dGVkIn19fV0sWzE5LDE2LCJcXHBpXzIgPSBwXzIgXFxjaXJjIHUiLDAseyJjdXJ2ZSI6LTIsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRvdHRlZCJ9fX1dXQ==

証明終わり。
