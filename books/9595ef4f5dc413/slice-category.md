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

定義よりコンマ圏 $1_\mathbf{C} \downarrow \Delta_A$ は次のように構成される。

- 対象は3つ組 $\lang X, f, \ast \rang$
- 射は2つ組 $\lang a, \mathrm{id}_\ast \rang$

[![comma_cat](https://storage.googleapis.com/zenn-user-upload/dfdcf26582bd-20240812.png)](https://q.uiver.app/#q=WzAsMTAsWzAsMCwiMV9cXG1hdGhiZntDfSBcXGRvd25hcnJvdyBcXERlbHRhX0EiXSxbMywwLCJcXG1hdGhiZnsxfSJdLFszLDEsIlxcYXN0Il0sWzEsMCwiXFxtYXRoYmZ7Q30iXSxbMSwxLCIxX1xcbWF0aGJme0N9KFgpIl0sWzEsMiwiMV9cXG1hdGhiZntDfShZKSJdLFsyLDEsIlxcRGVsdGFfQShcXGFzdCkiXSxbMCwxLCJcXGxhbmcgWCwgZiwgXFxhc3QgXFxyYW5nIl0sWzAsMiwiXFxsYW5nIFksIGcsIFxcYXN0IFxccmFuZyJdLFsyLDIsIlxcRGVsdGFfQShcXGFzdCkiXSxbNCw2LCJmIl0sWzQsNSwiMV9cXG1hdGhiZntDfShhKSIsMl0sWzcsOCwiXFxsYW5nIGEsIFxcbWF0aHJte2lkfV9cXGFzdCBcXHJhbmciLDJdLFs1LDksImciLDJdLFs2LDksIlxcRGVsdGFfQShcXG1hdGhybXtpZH1fXFxhc3QpIl1d)

関手$F: \mathbf{C}/A \to 1_\mathbf{C} \downarrow \Delta_A$ を次の通り構成する。

- 対象を次の通り写す $f \mapsto \lang f, \mathrm{dom}(f), \ast \rang$
- 射を次の通り写す $a \mapsto \lang a, \mathrm{id}_\ast \rang$

関手$G: 1_\mathbf{C} \downarrow \Delta_A \to \mathbf{C}/A$を次の通り構成する。

- 対象を次の通り写す $\lang f, \mathrm{dom}(f), \ast \rang \mapsto f$
    - 常に $X = 1_\mathbf{C}(X) = \mathrm{dom}(f)$ が成り立つため、$X$を$\mathrm{dom}(f)$と置いている。
- 射を次の通り写す $\lang a, \mathrm{id}_\ast \rang \mapsto a$

これらの関手が定める対応関係は明らかに互いの逆であるから、コンマ圏$1_\mathbf{C} \downarrow \Delta_A$ と $\mathbf{C}/A$ は同じものを構成することが分かる。
