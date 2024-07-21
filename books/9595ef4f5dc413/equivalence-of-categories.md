---
title: "圏同型と圏同値"
free: false
---

## 圏同型

圏同型とは、読んで字のごとく圏どうしの同型のこと。

### 復習: 同型射

圏$\mathbf C$のある対象$A$と$B$が同型であるとは、射$f: A \to B$, $g: B \to A$が存在して、$g \circ f = \mathrm{id}_A$かつ$f \circ g = \mathrm{id}_B$であることを言うのであった。

![isomorphism](https://storage.googleapis.com/zenn-user-upload/bbbef8a70e04-20231125.png)

### 定義

圏$\mathbf C$, $\mathbf D$が圏同型であるとは、関手$F: D \to C$, $G: C \to D$が存在して、$F \circ G = 1_C$かつ$G \circ F = 1_D$が成り立つことをいう。

![isomorhphic_categories](https://storage.googleapis.com/zenn-user-upload/50f457ad8c4f-20231125.png)

可換図式にすると以下の通りだ。

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwxLCJDIl0sWzEsMSwiQyciXSxbMywxLCJEIl0sWzQsMSwiRCciXSxbMCwyLCJGKEcoQykpIl0sWzEsMiwiRihHKEMnKSkiXSxbMywyLCJHKEYoRCkpIl0sWzQsMiwiRyhGKEQnKSkiXSxbMiwzLCJmIl0sWzQsNSwiZyJdLFs2LDcsImYiXSxbOCw5LCJHKEYoZykpIiwyXSxbNCw4LCJpZF9EIiwyXSxbNSw5LCJpZF97RCd9Il0sWzIsNiwiaWRfQyIsMl0sWzMsNywiaWRfe0MnfSJdXQ==

圏同型が成り立つとき、それぞれの圏の対象と射には一対一対応が存在している。

## 圏同値

### ほぼ圏同型

たいていの場合、圏論で「ほぼ同じ」というときは同型であることをいうが、圏どうしの場合、同型は制限が強すぎることが多い。

例えば下図の圏$\mathbf C$, $\mathbf D$は、いかにも「ほぼ同じ」だが、圏同型ではない。なぜなら、$F: \mathbf D \to \mathbf C$は対象$D_2$を$C_2$に写すか$C_3$に写すか選ばなければならないからだ。

![nearly_isomorphic_categories](https://storage.googleapis.com/zenn-user-upload/3a617318cea3-20231125.png)

同型な対象については対応関係がなくても問題にしない、圏同型よりもゆるい同値関係があれば、より便利に使えそうだ。
圏同値(*Equivalence of categories*)は、まさにこのような関係をいう。

### 定義

圏$\mathbf C$, $\mathbf D$が圏同値であるとは、関手$F: D \to C$, $G: C \to D$と自然変換$\epsilon: 1_C \Rightarrow F \circ G$と$\eta: 1_D \Rightarrow G \circ F$が存在して、$\epsilon$, $\eta$がそれぞれ自然同型であることをいう。

可換図式にすると以下の通りだ。

![equivalent_categories](https://storage.googleapis.com/zenn-user-upload/cfc4f56bfa1f-20231125.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwxLCJDIl0sWzEsMSwiQyciXSxbMywxLCJEIl0sWzQsMSwiRCciXSxbMCwyLCJGKEcoQykpIl0sWzEsMiwiRihHKEMnKSkiXSxbMywyLCJHKEYoRCkpIl0sWzQsMiwiRyhGKEQnKSkiXSxbMiwzLCJmIl0sWzQsNSwiZyJdLFs2LDcsIkYoRyhmKSkiLDJdLFs4LDksIkcoRihnKSkiLDJdLFsyLDYsIlxcZXBzaWxvbl9DIiwyXSxbMyw3LCJcXGVwc2lsb25fe0MnfSJdLFs0LDgsIlxcZXRhX0QiLDJdLFs1LDksIlxcZXRhX3tEJ30iXV0=

ここで$\epsilon$, $\eta$は自然同型であるので、圏$\mathbf C$の任意の対象$X$における$\epsilon_X: X \to F(G(X))$が同型射であり、圏$\mathbf D$の任意の対象$Y$における$\eta_Y: Y \to G(F(Y))$もまた同型射であることに注意する。

すなわち上図で$C$と$F(G(C))$, $D$と$G(F(D))$はそれぞれ同型であるということだ。もちろん、$C'$, $D'$についても同様だ。

### ほぼ圏同型（再掲）

先ほどの「ほぼ圏同型」な例は、圏同値と呼ぶことができる。

関手$F: \mathbf D \to \mathbf C$が$C_2$, $C_3$を潰すような関手だとしよう。すなわち$F(G(C_2)) = F(G(C_3))$である場合、次のような可換図式で圏同値を表現することができる。

![nearly_isomorphic_categories](https://storage.googleapis.com/zenn-user-upload/2d913b31c18f-20231125.png)

