---
title: "スライス圏"
free: false
---

## 定義

圏$\mathbf{C}$を考える。

圏$\mathbf{C}$の対象$A$上のスライス圏$\mathbf{C}/A$とは、次の通り構成される。

1. 圏$\mathbf{C}$の射であって、コドメインが$A$であるものすべてを対象とする
2. 圏$\mathbf{C}$の射であって、$f = g \circ a$を満たす射$a$を$f$から$g$への射とする
3. コンマ圏$\mathbf{C}/A$の射の合成$b \circ a$は、圏$\mathbf{C}$での射の合成$b \circ a$で与えられる

可換図式を描くと次の通り。

![slice-category](https://storage.googleapis.com/zenn-user-upload/29c24a597d8d-20240715.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntDfS9BIl0sWzEsMCwiXFxtYXRoYmZ7Q30iXSxbMSwxLCJYIl0sWzIsMiwiQSJdLFsxLDIsIlkiXSxbMCwxLCJmIl0sWzAsMiwiZyJdLFsyLDMsImYiXSxbNCwzLCJnIiwyXSxbMiw0LCJhIiwyXSxbNSw2LCJhIl1d

## コンマ圏を使った構成

スライス圏$\mathbf{C}/A$は、コンマ圏$1_\mathbf{C} \downarrow \Delta_A$として表すことができる。

ただし$1_\mathbf{C}: \mathbf{C} \to \mathbf{C}$は恒等関手、$\Delta_A: \mathbf{1} \to \mathbf{C}$は$\ast \in \mathrm{Obj}(\mathbf{1})$を$A \in \mathrm{Obj}(\mathbf{C})$に写す定関手である。
