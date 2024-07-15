---
title: "コンマ圏"
free: false
---

Awodey本には載っていない気がする。元ネタはこちら：

https://alg-d.com/math/kan_extension/comma.pdf

## 定義

圏$\mathbf{C}$, $\mathbf{D}$, $\mathbf{E}$と、圏$\mathbf{C}$をコドメインとする関手$F: \mathbf{D} \to \mathbf{C}$, $\mathbf{E} \to \mathbf{C}$を考える。

このとき以下の通り構成される圏をコンマ圏 *(Comma category)* と呼び$F \downarrow G$と書く。

1. 圏$\mathbf{C}$の射$f: F(D) \to G(E)$, 圏$\mathbf{D}$の対象$D$, 圏$\mathbf{E}$の対象$E$の3つ組$\lang f, D, E \rang$を対象とする
2. 圏$\mathbf{D}$の射$d: D \to D'$, 圏$\mathbf{E}$の射$e: E \to E'$の組$\lang d, e \rang$を射とする
    - ただし$d$, $e$は$G(e) \circ f = f' \circ F(d)$を満たす
3. 射の合成は$\lang d', e' \rang \circ \lang d, e \rang = \lang d' \circ d, e' \circ e \rang$で与える

可換図式は次の通り。

![D-C-E](https://storage.googleapis.com/zenn-user-upload/0276acfda30d-20240715.png)

上図の要素を用いて、コンマ圏を下のように構成する。

![Comma-category](https://storage.googleapis.com/zenn-user-upload/096464c98a7b-20240715.png)

https://q.uiver.app/#q=WzAsMTQsWzAsMCwiRiBcXGRvd25hcnJvdyBHIl0sWzAsMSwiXFxsYW5nIGYsIEQsIEUgXFxyYW5nIl0sWzQsMCwiXFxtYXRoYmZ7Q30iXSxbNSwxLCJHKEUpIl0sWzMsMSwiRihEKSJdLFs2LDAsIlxcbWF0aGJme0V9Il0sWzYsMSwiRSJdLFs2LDIsIkUnIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMiwxLCJEIl0sWzIsMiwiRCciXSxbMywyLCJGKEQnKSJdLFs1LDIsIkcoRScpIl0sWzAsMiwiXFxsYW5nIGYnLCBEJywgRScgXFxyYW5nIl0sWzQsMywiZiJdLFs2LDcsImUiXSxbOSwxMCwiZCJdLFszLDEyLCJHKGUpIl0sWzQsMTEsIkYoZCkiLDJdLFsxMSwxMiwiZiciLDJdLFsxLDEzLCJcXGxhbmcgZCwgZSBcXHJhbmciXSxbOCwyLCJGIl0sWzUsMiwiRyIsMl1d
