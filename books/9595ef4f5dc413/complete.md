---
title: "完備"
free: false
---

## 定理

圏$\mathbf{C}$において、任意の対象の有限積と任意の平行射のイコライザが存在するならば、またその時に限って極限が存在する。
そのような圏を完備(*Complete*)であるという。

双対性より、また任意の対象の有限和とコイコライザが存在するならば、またその時に限って余極限が存在する。そのような圏を余完備(*Cocomplete*)であるという。

### 引き戻しの拡張

まずは引き戻しを任意の有限個の要素に拡張する。引き戻しは普遍性を満たす可換な四角形からなる。これを$A \times_C B$と書くのだった。

![pullback_2objs](https://storage.googleapis.com/zenn-user-upload/1e2497157095-20240109.png)

仮に、引き戻しを3つの射からなるように拡張する。射$f: A \to D$, $g: B \to D$, $h: C \to D$と、$f \circ q_1 = g \circ q_2 = h \circ q_3$を満たす組$(Q, q_1, q_2, q_3)$を考える。
この$Q$は普遍性を満たすものとする。すなわち同じ条件を満たす任意の組$(X, x_1, x_2, x_3)$に対して、仲介射$u: X \to Q$が一意に存在して、$x_1 = q_1 \circ u$, $x_2 = q_2 \circ u$, $x_3 = q_3 \circ u$を満たす。
このとき$Q$は引き戻しである。これを$A \times_D B \times_D C$と書くことにする。

![pullback_3objs](https://storage.googleapis.com/zenn-user-upload/88ac0e4710ee-20240109.png)

なお、$A \times_D B \times_D C$が存在するとき、常に3つの引き戻し$A \times_D B$, $A \times_D C$, $B \times_D C$が存在する。例えば$A \times_D B$に注目すれば、以下の可換図式が描ける。

![pullback](https://storage.googleapis.com/zenn-user-upload/d83e796b4257-20240109.png)

ここから任意の有限の数の射(対象)を取る引き戻しを考えることができる。
直感的には次のようなものだ（$\prod$の右下に$Z$の添え字を付けたかったが、tex力が足りなくてできなかった）。

![extended_pullback](https://storage.googleapis.com/zenn-user-upload/737934962a4a-20240109.png)

https://q.uiver.app/#q=WzAsMjEsWzEsMywiQSJdLFsyLDIsIkIiXSxbMiwzLCJDIl0sWzEsMiwiUCJdLFs1LDIsIlEiXSxbNywyLCJDIl0sWzYsMywiQiJdLFs1LDQsIkEiXSxbNyw0LCJEIl0sWzQsMSwiWCJdLFswLDEsIlgiXSxbMCwwLCJcXG1hdGhiZntDfSJdLFs5LDEsIlxcbWF0aGNsYXB7QSBcXHRpbWVzX0QgQiBcXHRpbWVzX0QgQ30iXSxbMTAsMywiQSJdLFsxMSwyLCJCIl0sWzExLDMsIkQiXSxbMTAsMiwiQSBcXHRpbWVzX0QgQiJdLFsxMywyLCJcXHByb2Rfe1xcbGFtYmRhIFxcaW4gXFxMYW1iZGF9IEFfe1xcbGFtYmRhfSJdLFsxNCwzLCJaIl0sWzEzLDMsIkEiXSxbMTIsMSwiWCJdLFswLDIsImYiLDJdLFsxLDIsImciXSxbMywxLCJwXzIiXSxbMywwLCJwXzEiLDJdLFs0LDcsInFfMSIsMl0sWzQsNiwicV8yIiwxXSxbNCw1LCJxXzMiXSxbNiw4LCJnIiwxXSxbNSw4LCJoIl0sWzcsOCwiZiIsMl0sWzksNCwidSIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs5LDcsInhfMSIsMix7ImN1cnZlIjoxfV0sWzksNSwieF8zIiwwLHsiY3VydmUiOi0xfV0sWzksNiwieF8yIiwwLHsib2Zmc2V0IjotMSwiY3VydmUiOi0xfV0sWzEwLDMsInUiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTAsMCwieF8xIiwyLHsiY3VydmUiOjF9XSxbMTAsMSwieF8yIiwwLHsiY3VydmUiOi0xfV0sWzEzLDE1LCJmIiwyXSxbMTQsMTUsImciXSxbMTYsMTMsInBfMSIsMl0sWzE2LDE0LCJwXzIiXSxbMTIsMTQsInFfMiIsMSx7ImxhYmVsX3Bvc2l0aW9uIjo2MCwiY3VydmUiOi0xLCJzaG9ydGVuIjp7InNvdXJjZSI6MzB9fV0sWzEyLDEzLCJxXzEiLDEseyJjdXJ2ZSI6MX1dLFsxMiwxNiwidSIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxNywxOSwicF9pIiwyXSxbMTksMTgsImZfaSIsMl0sWzIwLDE3LCJ1IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIwLDE5LCJ4X2kiLDIseyJjdXJ2ZSI6MX1dXQ==

$\Lambda$をきちんと定式化するために、引き戻しが[極限](limit)であることを思い出す。
$\mathbf{J}$を小さな圏とする。以下の図式$D: \mathbf{J} \to \mathbf{C}$の極限$(L, p)$が任意の有限の数の射(対象)を取る引き戻しである。ここで$j$は圏$\mathbf{J}$のそれぞれの対象である。
なお錐の性質により$\forall i, j \in \mathrm{ob}(\mathbf{J}), f_i \circ p_i = f_j \circ p_j$が保証されている。

![limit](https://storage.googleapis.com/zenn-user-upload/bda78e86f4c5-20240109.png)
https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmZ7Sn0iXSxbMCwxLCIxIl0sWzIsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJMIl0sWzMsMiwiRChqKSJdLFs0LDIsIkQoMCkiXSxbMiwxLCJYIl0sWzEsMiwiMCJdLFswLDMsIm4iXSxbMCwyLCJcXHZkb3RzIl0sWzMsNCwicF9qIl0sWzQsNSwiRChmX2opIiwyXSxbNiwzLCJ1IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzYsNCwieF9qIiwyXSxbMSw3LCJmXzEiXSxbOCw3LCJmX24iLDJdXQ==

### 証明

引き戻しを任意の数の射を取るように拡張できれば、自明に証明だと思うので、省略する。

[任意の二対象の積と任意の並行射のイコライザが存在するとき、引き戻しが存在する](equaliser#定理2-任意の二対象の積と任意の並行射のイコライザが存在するとき引き戻しが存在する)
