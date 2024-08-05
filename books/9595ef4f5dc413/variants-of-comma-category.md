---
title: "コンマ圏の亜種"
free: false
---

コンマ圏にはスライス圏を含む亜種がいくつか存在する。それらは非常に重要な性質を持つので紹介する。

これらの亜種はまとめてコンマ圏と呼ばれることもあるので、単にコンマ圏というときにはその構成要素に注意を払わなければならない。

## 関手の上方の対象から成る圏

圏$\mathbf{C}$, $\mathbf{D}$, 関手$F: \mathbf{D} \to \mathbf{C}$を考える。
対象CのF-上方の対象から成る圏(*Category of objects F-over C*) $F \downarrow C$ は、以下の通り構成される圏である。

1. 対象: 圏$\mathbf{C}$の対象$C$を固定して、これを余域とする$F$の像から$C$への射$f: F(D) \to C$と、域の像の元となった圏$\mathbf{D}$の対象$D$との組$\lang f, D \rang$
2. 射: 圏$\mathbf{D}$の射$d: D \to D'$であって、$f = f' \circ F(d)$を満たすもの


[![category-of-objects-f-over-c](https://storage.googleapis.com/zenn-user-upload/8a86b27a2689-20240806.png)](https://q.uiver.app/#q=WzAsMTAsWzIsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJDIl0sWzEsMCwiXFxtYXRoYmZ7RH0iXSxbMiwxLCJGKEQpIl0sWzIsMiwiRihEJykiXSxbMSwxLCJEIl0sWzEsMiwiRCciXSxbMCwwLCJGIFxcZG93bmFycm93IEMiXSxbMCwxLCJcXGxhbmcgZiwgRCBcXHJhbmciXSxbMCwyLCJcXGxhbmcgZicsIEQnIFxccmFuZyJdLFs4LDksImQiLDJdLFszLDQsIkYoZCkiLDJdLFszLDEsImYiXSxbNCwxLCJmJyIsMl0sWzIsMCwiRiJdLFs1LDYsImQiLDJdLFs0LDEsIlxcY2lyY2xlYXJyb3dyaWdodCJdXQ==)

### 終対象は普遍射と一致する

$F \downarrow A$における終対象は、関手$F$から$A$への[普遍射](universal-mapping-property)である。

#### 証明

関手$F$から$A$への普遍射とは、$\mathbf{C}$の対象$X$と$\mathbf{D}$の射$u: F(X) \to A$の組$\lang X, u \rang$であって、任意の射$F(Y) \to A$についてこれを分解する圏$\mathbf{C}$の射$g: Y \to X$が一意に定まるものをいうのであった。

![ump](https://storage.googleapis.com/zenn-user-upload/d2c995257fe0-20240806.png)

$F \downarrow A$の終対象は、対象$\lang t, T \rang$であって、$F \downarrow A$の任意の対象から射がただ一つ存在するものである。
終対象の性質から、任意の$D \in \mathrm{ob}(\mathbf{D})$に対して射$\tau_D: D \to T$がただ一つ対応することが分かるので、$F \downarrow A$の終対象が$F$から$A$への普遍射に一致することが分かる。

![terminal-object-of-f-down-a](https://storage.googleapis.com/zenn-user-upload/6af7ab470a44-20240806.png)

## 関手の下方の対象から成る圏

圏$\mathbf{C}$, $\mathbf{E}$, 関手$G: \mathbf{C} \to \mathbf{E}$を考える。
対象CのG-下方の対象から成る圏(*Category of objects G-under C*) $C \downarrow G$ は、以下の通り構成される圏である。

1. 対象: 圏$\mathbf{C}$の対象$C$を固定して、これを域とする$C$から$G$の像への射$g: C \to G(E)$と、余域の像の元となった圏$\mathbf{E}$の対象$E$との組$\lang g, E \rang$
2. 射: 圏$\mathbf{E}$の射$e: E \to E'$であって、$g' = G(e) \circ g$を満たすもの

[![category-of-objects-g-under-c](https://storage.googleapis.com/zenn-user-upload/0d3b9e4bbb5a-20240806.png)](https://q.uiver.app/#q=WzAsMTgsWzYsMCwiXFxtYXRoYmZ7YyBcXGRvd25hcnJvdyBHfSJdLFszLDAsIlxcbWF0aGJme0N9Il0sWzMsMSwiQyJdLFs0LDEsIkcoRSkiXSxbNiwxLCJcXGxhbmcgZywgRSBcXHJhbmciXSxbMSwwLCJcXG1hdGhiZntEfSJdLFs1LDEsIkUiXSxbNCwyLCJHKEUnKSJdLFs1LDIsIkUnIl0sWzYsMiwiXFxsYW5nIGcnLCBFJyBcXHJhbmciXSxbMiwxLCJGKEQpIl0sWzIsMiwiRihEJykiXSxbMSwxLCJEIl0sWzEsMiwiRCciXSxbMCwwLCJcXG1hdGhiZntGIFxcZG93bmFycm93IGN9Il0sWzAsMSwiXFxsYW5nIGYsIEQgXFxyYW5nIl0sWzAsMiwiXFxsYW5nIGYnLCBEJyBcXHJhbmciXSxbNSwwLCJcXG1hdGhiZntFfSJdLFsyLDMsImciXSxbMiw3LCJnJyIsMl0sWzMsNywiRyhlKSJdLFs0LDksImUiXSxbMTUsMTYsImQiLDJdLFsxMCwxMSwiRihkKSIsMl0sWzEwLDIsImYiXSxbMTEsMiwiZiciLDJdLFs1LDEsIkYiXSxbMTIsMTMsImQiLDJdLFsxLDE3LCJHIl0sWzYsOCwiZSJdXQ=)


## 上方の対象から成る圏

[スライス圏](slice-category)を参照。
スライス圏$\mathbf{C}/A$はコンマ圏の記法を使って$\mathbf{C} \downarrow A$と書かれることもある。

## 下方の対象から成る圏

コスライス圏$A / \mathbf{C}$とも呼ばれる。

圏$\mathbf{C}$を考える。圏$\mathbf{C}$の下方の対象から成る圏$A \downarrow \mathbf{C}$ は、以下の通り構成される圏である。

1. 圏$\mathbf{C}$の射であって、域が$A$であるものすべてを対象とする
2. 圏$\mathbf{C}$の射であって、$g = a \circ f$を満たす射$a$を$f$から$g$への射とする

[![category-of-objects-over-a](https://storage.googleapis.com/zenn-user-upload/5998a640f08a-20240806.png)](https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDIsIkMiXSxbMCwxLCJBIl0sWzEsMSwiQiJdLFsyLDAsIkEgXFxkb3duYXJyb3cgXFxtYXRoYmZ7Q30iXSxbMiwxLCJmIl0sWzIsMiwiZyJdLFsyLDMsImYiXSxbMiwxLCJnIiwyXSxbMywxLCJhIl0sWzIsMSwiXFxjaXJjbGVhcnJvd3JpZ2h0Il0sWzUsNiwiYSJdXQ==)
