---
title: "引き戻し"
free: false
---

引き戻し(*Pullback*)とは、共通の余域を持つ2つの射$f: X \to Z$, $g: Y \to Z$からなる図式の極限である。

二つの射の引き戻しは存在するとは限らないが、存在すれば一意に定まる。

## 定義

ある圏$\mathbf C$における射$f: X \to Z$, $g: Y \to Z$の引き戻しとは、対象$P$と2つの射$p_1: P \to X$, $p_2: P \to Y$の3つ組であって、条件$f \circ p1 = g \circ p2$を満たすものから成る：

![pullback_element](https://storage.googleapis.com/zenn-user-upload/2bbd940d3a19-20231210.png)

この3つ組$(P, p_1, p_2)$が引き戻しであるとき、以下の普遍性を満たす。
すなわち同じ条件を満たす別の任意の3つ組$(Q, q_1, q_2)$に対して、一意な仲介射$u: Q \to P$が存在して、$p_1 \circ u = q_1$, $p_2 \circ u = q_2$を満たす。

![pullback](https://storage.googleapis.com/zenn-user-upload/7418c5ad2c64-20231210.png)

https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZiBDIl0sWzEsMiwiUCJdLFsyLDIsIlkiXSxbMSwzLCJYIl0sWzIsMywiWiJdLFswLDEsIlEiXSxbMSwyLCJwXzIiXSxbMSwzLCJwXzEiLDJdLFszLDQsImYiLDJdLFsyLDQsImciXSxbNSwxLCJ1IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzUsMywicV8xIiwyLHsib2Zmc2V0IjoxLCJjdXJ2ZSI6MX1dLFs1LDIsInFfMiIsMCx7ImN1cnZlIjotMX1dXQ==

しばしば、対象$P$を$X \times_{Z} Y$と書く。

## 極限を用いた定義

添え字圏$\mathbf{J}$を、以下のような圏と定める:

- 対象として$0$, $1$, $2$を持つ
- 非自明な射として$f: 1 \to 0$, $g: 2 \to 0$を持つ

![index_category_j](https://storage.googleapis.com/zenn-user-upload/49b969211d22-20231210.png)

引き戻しとは、図式$D: \mathbf{J} \to \mathbf{C}$の極限$(L, \eta)$のことである。

![limit_of_d](https://storage.googleapis.com/zenn-user-upload/6089470d69bf-20231210.png)

https://q.uiver.app/#q=WzAsMTAsWzQsMCwiXFxtYXRoYmYgQyJdLFs1LDIsIkwiXSxbNiwzLCJEKDIpIl0sWzQsMywiRCgxKSJdLFs1LDQsIkQoMCkiXSxbNSwxLCJOIl0sWzAsMCwiXFxtYXRoYmZ7Sn0iXSxbMCwxLCIxIl0sWzIsMSwiMiJdLFsxLDIsIjAiXSxbMSwyLCJcXGV0YV8yIl0sWzEsMywiXFxldGFfMSIsMl0sWzMsNCwiRChmKSIsMl0sWzIsNCwiRChnKSJdLFs1LDEsInUiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNSwzLCJcXGVwc2lsb25fMSIsMix7Im9mZnNldCI6MSwiY3VydmUiOjF9XSxbNSwyLCJcXGVwc2lsb25fMiIsMCx7ImN1cnZlIjotMX1dLFs3LDksImYiLDJdLFs4LDksImciXV0=