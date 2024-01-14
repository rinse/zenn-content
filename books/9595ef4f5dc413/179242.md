---
title: "添え字圏と図式"
free: false
---

## 定義

形(*Type*)が$\mathbf J$であるような図(*Diagram*)式とは、$\mathbf J$から$\mathbf C$への関手$D: \mathbf J \to \mathbf C$をいう。

形はしばしば添え字圏(*Index category*)とも呼ばれる。添え字圏や図式というのは単に呼び方の問題で、それら自体は単なる圏や関手である。

例えば、下に適当な圏$\mathbf C$を用意した。

![diagram_c](https://storage.googleapis.com/zenn-user-upload/a543cec830e9-20231028.png)

ここから対象$C_1$, $C_2$, $C_3$を"選択"することを考えよう。

対象を3つだけ持つ圏$\mathbf J$と、$\mathbf J$を$\mathbf C$に写す関手$D$を考えると、$\mathbf J$の対象を$\mathbf C$のどの対象に写すかという$D: \mathbf J \to \mathbf C$の定義によって、$\mathbf C$の対象と射とを選択することができる。

![select_123](https://storage.googleapis.com/zenn-user-upload/97092571b6a0-20231028.png)

ここで$D(1)=C_1$, $D(2)=C_2$, $D(3)=C_3$であることに注意する。そうなるように恣意的に関手$D$を定義したということだ。

対象$C_4$, $C_5$, $C_6$を選択したい場合は、$D$の定義を変えてやればよい。

![select_456](https://storage.googleapis.com/zenn-user-upload/4b1d3a1d30c2-20231028.png)

このように、圏$\mathbf J$の対象を添え字にして、関手$D$を使って圏$\mathbf C$を表すことができる。このような見方をするとき、圏$\mathbf J$を添え字圏、関手$D$を図式と呼ぶ。

https://q.uiver.app/#q=WzAsMTEsWzMsMCwiXFxtYXRoYmYgQyJdLFszLDEsIkQoMSkiXSxbNCwxLCJEKDIpIl0sWzMsMiwiRCgzKSJdLFs0LDIsIkQnKDEpIl0sWzUsMSwiRCcoMikiXSxbNSwyLCJEJygzKSJdLFswLDAsIlxcbWF0aGJmIEoiXSxbMCwxLCIxIl0sWzEsMSwiMiJdLFswLDIsIjMiXSxbMSwyLCJEKGYpIl0sWzMsMiwiYiIsMl0sWzgsOSwiZiJdLFs0LDUsIkQnKGYpIl1d

通常、添え字圏は小さかったり有限であったりする。離散圏を使うことも多い。

## 記法

添え字圏$\mathbf{J}$の対象を、小文字$i, j, k...$で表すことがある。このように書くときは、圏$\mathbf{C}$上の対象を図式$D$の像として表したいときである。括弧を使うのが煩わしいので、添え字圏の対象を小文字で表し、括弧を省略して$D$に添えて書く。
ただ、自然変換の添え字と紛らわしいので、個人的にはあまり多用はしないつもりでいる。

![index](https://storage.googleapis.com/zenn-user-upload/ba1b069e49c4-20240108.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntKfSJdLFswLDEsImkiXSxbMSwxLCJrIl0sWzAsMiwiaiJdLFszLDAsIlxcbWF0aGJme0N9Il0sWzMsMSwiRF9pIl0sWzMsMiwiRF9qIl0sWzQsMSwiRF9rIl0sWzEsMiwiZiJdLFs1LDcsIkRfZiJdXQ==
