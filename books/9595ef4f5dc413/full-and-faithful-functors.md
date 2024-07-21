---
title: "充満関手と忠実関手"
free: false
---

## 定義

局所的に小さな圏$\mathbf{C}$, $\mathbf{D}$と関手$F: \mathbf{C} \to \mathbf{D}$を考える。

- 圏$\mathbf{C}$の任意の対象$A$, $B$について、集合の圏上の射$\hom_C(A, B) \to \hom_D(F(A), F(B))$が単射であるとき、$F$は忠実(*failthful*)であるという。
- 圏$\mathbf{C}$の任意の対象$A$, $B$について、集合の圏上の射$\hom_C(A, B) \to \hom_D(F(A), F(B))$が全射であるとき、$F$は充満(*full*)であるという。
- $F$が充満かつ忠実であるとき、$F$は充満忠実(*full and failthful*)であるという。

![full-and-failthful](https://storage.googleapis.com/zenn-user-upload/820201ca9047-20240721.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMCwyLCJCIl0sWzEsMCwiXFxtYXRoYmZ7RH0iXSxbMSwxLCJGKEEpIl0sWzEsMiwiRihCKSJdLFsyLDAsIlxcbWF0aGJme1NldH0iXSxbMiwxLCJcXGhvbV9DKEEsIEIpIl0sWzMsMSwiXFxob21fRChGKEEpLCBGKEIpKSJdLFsxLDIsImYiXSxbNCw1LCJGKGYpIl0sWzcsOCwiYSJdXQ==

## 単斜・全射との違い

元ネタはalg-dさんの動画[^1]です。

関手$F$が充満・忠実であることは、$F$が（直感的に）単射・全射であることを意味しない。

例えば次のような対象が4つ、射が2つしかない圏$\mathbf{C}$と$F(A)=F(C)$, $F(B)=F(D)$, $F(f)=F(g)$であるような関手$F$のケースを考える。

![fa=fc](https://storage.googleapis.com/zenn-user-upload/597a8a7df9ed-20240721.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMCwyLCJCIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMiwxLCJGKEEpPUYoQykiXSxbMiwyLCJGKEIpPUYoRCkiXSxbMSwyLCJEIl0sWzEsMSwiQyJdLFsxLDIsImYiXSxbNCw1LCJGKGYpPUYoZykiXSxbNyw2LCJnIl1d

このとき$F(A)=F(C)$にもかかわらず$A \neq C$であったり、また$F(f)=F(g)$にもかかわらず$f \neq g$であるため、$F$は対象・射について単射ではないように見える。

しかしながら二対象に注目して忠実かどうかを検証すると、例えば$A$, $B$については$\hom_C(A, B) \hookrightarrow \hom_C(F(A), F(B))$であることが分かる。同様にして任意の二対象$X$, $Y$について$\hom_C(X, Y) \hookrightarrow \hom_C(F(X), F(Y))$であることを確かめられるため、この関手$F$は忠実である。

一方で、次のように並行射を1つの射につぶすような関手$F$は忠実ではない。

![Ff=Fg](https://storage.googleapis.com/zenn-user-upload/8dcfd904a0ad-20240721.png)

[^1]: https://www.youtube.com/watch?v=UHDwnPHnyf8
