---
title: "引き戻し"
free: false
---

引き戻し(*Pullback*)とは、共通の余域を持つ2つの射$f: X \to Z$, $g: Y \to Z$からなる図式の極限である。

二つの射の引き戻しは存在するとは限らないが、存在すれば一意に定まる。

## 定義

ある圏$\mathbf C$における射$f: X \to Z$, $g: Y \to Z$の引き戻しとは、対象$P$と2つの射$p_1: P \to X$, $p_2: P \to Y$の3つ組であって、条件$f \circ p1 = g \circ p2$を満たすものから成る：

[![](https://storage.googleapis.com/zenn-user-upload/379ff46f11eb-20251029.png)](https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiUCJdLFsxLDEsIlkiXSxbMCwyLCJYIl0sWzEsMiwiWiJdLFsxLDMsInBfMSIsMl0sWzMsNCwiZiIsMl0sWzIsNCwiZyJdLFsxLDQsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxLDIsInBfMiJdXQ==)

この3つ組$(P, p_1, p_2)$が引き戻しであるとき、以下の普遍性を満たす。
すなわち同じ条件を満たす別の任意の3つ組$(Q, q_1, q_2)$に対して、一意な仲介射$u: Q \to P$が存在して、$p_1 \circ u = q_1$, $p_2 \circ u = q_2$を満たす。

[![](https://storage.googleapis.com/zenn-user-upload/705f318bf421-20251029.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZiBDIl0sWzEsMiwiUCJdLFsyLDIsIlkiXSxbMSwzLCJYIl0sWzIsMywiWiJdLFswLDEsIlEiXSxbMSwyLCJwXzIiXSxbMSwzLCJwXzEiLDJdLFszLDQsImYiLDJdLFsyLDQsImciXSxbNSwxLCJ1IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzUsMywicV8xIiwyLHsib2Zmc2V0IjoxLCJjdXJ2ZSI6MX1dLFs1LDIsInFfMiIsMCx7ImN1cnZlIjotMX1dLFsxLDQsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

しばしば、対象$P$を$X \times_{Z} Y$と書く。

[![](https://storage.googleapis.com/zenn-user-upload/57e62061045b-20251029.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZiBDIl0sWzEsMiwiWCBcXHRpbWVzX1ogWSJdLFsyLDIsIlkiXSxbMSwzLCJYIl0sWzIsMywiWiJdLFswLDEsIlEiXSxbMSwyLCJwXzIiXSxbMSwzLCJwXzEiLDJdLFszLDQsImYiLDJdLFsyLDQsImciXSxbNSwxLCJ1IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzUsMywicV8xIiwyLHsib2Zmc2V0IjoxLCJjdXJ2ZSI6MX1dLFs1LDIsInFfMiIsMCx7ImN1cnZlIjotMX1dLFsxLDQsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

## 極限を用いた定義

添え字圏$\mathbf{J}$を、以下のような圏と定める:

- 対象として$0$, $1$, $2$を持つ
- 非自明な射として$f: 1 \to 0$, $g: 2 \to 0$を持つ

![index_category_j](https://storage.googleapis.com/zenn-user-upload/49b969211d22-20231210.png)

引き戻しとは、図式$D: \mathbf{J} \to \mathbf{C}$の極限$(L, \eta)$のことである。

[![](https://storage.googleapis.com/zenn-user-upload/0b94b83dd1b6-20251029.png)](https://q.uiver.app/#q=WzAsMTAsWzQsMCwiXFxtYXRoYmYgQyJdLFs1LDIsIkwiXSxbNiwzLCJEKDIpIl0sWzQsMywiRCgxKSJdLFs1LDQsIkQoMCkiXSxbNSwxLCJOIl0sWzAsMCwiXFxtYXRoYmZ7Sn0iXSxbMCwxLCIxIl0sWzIsMSwiMiJdLFsxLDIsIjAiXSxbMSwyLCJcXGV0YV8yIl0sWzEsMywiXFxldGFfMSIsMl0sWzMsNCwiRChmKSIsMl0sWzIsNCwiRChnKSJdLFs1LDEsInUiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNSwzLCJcXGVwc2lsb25fMSIsMix7Im9mZnNldCI6MSwiY3VydmUiOjF9XSxbNSwyLCJcXGVwc2lsb25fMiIsMCx7ImN1cnZlIjotMX1dLFs3LDksImYiLDJdLFs4LDksImciXSxbMSw0LCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

## 押し出し

押し出し (*Pushout*) とは、引き戻しの双対である。

[![](https://storage.googleapis.com/zenn-user-upload/fbcda4ecb0a2-20251029.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZiBDIl0sWzEsMiwiWCArX1ogWSJdLFsyLDIsIlkiXSxbMSwzLCJYIl0sWzIsMywiWiJdLFswLDEsIlEiXSxbMiwxLCJwXzIiLDJdLFszLDEsInBfMSJdLFs0LDMsImYiXSxbNCwyLCJnIiwyXSxbMSw1LCJ1IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzMsNSwicV8xIiwwLHsib2Zmc2V0IjotMSwiY3VydmUiOi0xfV0sWzIsNSwicV8yIiwyLHsiY3VydmUiOjF9XSxbMSw0LCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)
