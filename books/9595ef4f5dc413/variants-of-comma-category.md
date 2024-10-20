---
title: "コンマ圏の特殊な例"
free: false
---

コンマ圏の特殊な事例には、スライス圏を含む有用な構成が存在する。

これらの亜種を指して単にコンマ圏と呼ぶこともあるので、単にコンマ圏というときにはその構成に注意を払わなければならない。

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

### コンマ圏を使った表現

$F \downarrow C$は、コンマ圏$F \downarrow \Delta_C$と表すことができる。

ただし$\Delta_C: \mathbf{1} \to \mathbf{C}$は$\ast \in \mathrm{ob}(\mathbf{1})$を$C \in \mathrm{ob}(\mathbf{C})$に写す定関手である。

[![F-downarrow-A](https://storage.googleapis.com/zenn-user-upload/5aa5f8b8b3a4-20240816.png)](https://q.uiver.app/#q=WzAsMTYsWzMsMCwiXFxtYXRoYmZ7Q30iXSxbNCwxLCJcXERlbHRhX0MoXFxhc3QpIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMywxLCJGKEQpIl0sWzMsMiwiRihEJykiXSxbMiwxLCJEIl0sWzIsMiwiRCciXSxbMSwwLCJGIFxcZG93bmFycm93IEMiXSxbMSwxLCJcXGxhbmcgZiwgRCBcXHJhbmciXSxbMSwyLCJcXGxhbmcgZicsIEQnIFxccmFuZyJdLFswLDAsIkYgXFxkb3duYXJyb3cgXFxEZWx0YV9DIl0sWzUsMCwiXFxtYXRoYmZ7MX0iXSxbNSwxLCJcXGFzdCJdLFswLDEsIlxcbGFuZyBmLCBELCBcXGFzdCBcXHJhbmciXSxbMCwyLCJcXGxhbmcgZicsIEQnLCBcXGFzdCBcXHJhbmciXSxbNCwyLCJcXERlbHRhX0MoKikiXSxbOCw5LCJkIiwyXSxbMyw0LCJGKGQpIiwyXSxbMywxLCJmIl0sWzIsMCwiRiJdLFs1LDYsImQiLDJdLFsxMywxNCwiXFxsYW5nIGQsIFxcbWF0aHJte2lkfV9cXGFzdCBcXHJhbmciLDJdLFsxMSwwLCJcXERlbHRhX0MiLDJdLFs0LDE1LCJmJyIsMl0sWzEsMTUsIlxcRGVsdGFfQyhcXG1hdGhybXtpZH1fXFxhc3QpIl1d)

## 関手の下方の対象から成る圏

圏$\mathbf{C}$, $\mathbf{E}$, 関手$G: \mathbf{C} \to \mathbf{E}$を考える。
対象CのG-下方の対象から成る圏(*Category of objects G-under C*) $C \downarrow G$ は、以下の通り構成される圏である。

1. 対象: 圏$\mathbf{C}$の対象$C$を固定して、これを域とする$C$から$G$の像への射$g: C \to G(E)$と、余域の像の元となった圏$\mathbf{E}$の対象$E$との組$\lang g, E \rang$
2. 射: 圏$\mathbf{E}$の射$e: E \to E'$であって、$g' = G(e) \circ g$を満たすもの

[![category-of-objects-g-under-c](https://storage.googleapis.com/zenn-user-upload/0d3b9e4bbb5a-20240806.png)](https://q.uiver.app/#q=WzAsMTgsWzYsMCwiXFxtYXRoYmZ7YyBcXGRvd25hcnJvdyBHfSJdLFszLDAsIlxcbWF0aGJme0N9Il0sWzMsMSwiQyJdLFs0LDEsIkcoRSkiXSxbNiwxLCJcXGxhbmcgZywgRSBcXHJhbmciXSxbMSwwLCJcXG1hdGhiZntEfSJdLFs1LDEsIkUiXSxbNCwyLCJHKEUnKSJdLFs1LDIsIkUnIl0sWzYsMiwiXFxsYW5nIGcnLCBFJyBcXHJhbmciXSxbMiwxLCJGKEQpIl0sWzIsMiwiRihEJykiXSxbMSwxLCJEIl0sWzEsMiwiRCciXSxbMCwwLCJcXG1hdGhiZntGIFxcZG93bmFycm93IGN9Il0sWzAsMSwiXFxsYW5nIGYsIEQgXFxyYW5nIl0sWzAsMiwiXFxsYW5nIGYnLCBEJyBcXHJhbmciXSxbNSwwLCJcXG1hdGhiZntFfSJdLFsyLDMsImciXSxbMiw3LCJnJyIsMl0sWzMsNywiRyhlKSJdLFs0LDksImUiXSxbMTUsMTYsImQiLDJdLFsxMCwxMSwiRihkKSIsMl0sWzEwLDIsImYiXSxbMTEsMiwiZiciLDJdLFs1LDEsIkYiXSxbMTIsMTMsImQiLDJdLFsxLDE3LCJHIl0sWzYsOCwiZSJdXQ=)

### コンマ圏を使った表現

$C \downarrow G$は$\Delta_C \downarrow G$で表すことができる。

[![C-downarrow-G](https://storage.googleapis.com/zenn-user-upload/d1b225cbbe9c-20240817.png)](https://q.uiver.app/#q=WzAsMTYsWzEsMCwiQyBcXGRvd25hcnJvdyBHIl0sWzMsMCwiXFxtYXRoYmZ7Q30iXSxbMiwwLCJcXG1hdGhiZnsxfSJdLFs1LDAsIlxcbWF0aGJme0V9Il0sWzIsMSwiXFxhc3QiXSxbMywxLCJcXERlbHRhX0MoXFxhc3QpIl0sWzMsMiwiXFxEZWx0YV9DKFxcYXN0KSJdLFs0LDEsIkcoRSkiXSxbNSwxLCJFIl0sWzUsMiwiRSciXSxbNCwyLCJHKEUnKSJdLFswLDAsIlxcRGVsdGFfQyBcXGRvd25hcnJvdyBHIl0sWzEsMSwiXFxsYW5nIGcsIEUgXFxyYW5nIl0sWzEsMiwiXFxsYW5nIGcnLCBFJyBcXHJhbmciXSxbMCwxLCJcXGxhbmcgZywgXFxhc3QsIEUgXFxyYW5nIl0sWzAsMiwiXFxsYW5nIGcnLCBcXGFzdCwgRScgXFxyYW5nIl0sWzMsMSwiRyIsMl0sWzIsMSwiRiJdLFs1LDYsIlxcRGVsdGFfQyhcXG1hdGhybXtpZH1fXFxhc3QpIiwyXSxbOCw5LCJlIl0sWzcsMTAsIkcoZSkiXSxbNSw3LCJnIl0sWzYsMTAsImcnIiwyXSxbMTIsMTMsImUiLDJdLFsxNCwxNSwiXFxsYW5nIFxcbWF0aHJte2lkfV9cXGFzdCwgZSBcXHJhbmciLDJdXQ==)

## 上方の対象から成る圏

圏$\mathbf{C}$を考える。圏$\mathbf{C}$の上方の対象から成る圏$\mathbf{C} \downarrow A$ は、以下の通り構成される圏である。

1. 圏$\mathbf{C}$の射であって、余域が$A$であるものすべてを対象とする
2. 圏$\mathbf{C}$の射であって、$f = f' \circ c$を満たす射$c$を$f$から$f'$への射とする

[![C-downarrow-c](https://storage.googleapis.com/zenn-user-upload/c9ef2c8970d0-20240817.png)](https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntDfSBcXGRvd25hcnJvdyBBIl0sWzEsMCwiXFxtYXRoYmZ7Q30iXSxbMSwxLCJDIl0sWzEsMiwiQyciXSxbMiwxLCJBIl0sWzAsMSwiZiJdLFswLDIsImYnIl0sWzIsMywiYyIsMl0sWzIsNCwiZiJdLFszLDQsImYnIiwyXSxbNSw2LCJjIiwyXSxbMyw0LCJcXGNpcmNsZWFycm93cmlnaHQiXV0=)

### スライス圏

この構成はスライス圏とも呼ばれ、$\mathbf{C} / A$とも書かれる。

[スライス圏](slice-category)も参照。

### コンマ圏を使った表現

$\mathbf{C} \downarrow A$は$1_\mathbf{C} \downarrow \Delta_A$で表すことができる。

[![1c-downarrow-DeltaA](https://storage.googleapis.com/zenn-user-upload/b0bf636803c1-20240817.png)](https://q.uiver.app/#q=WzAsMTYsWzMsMCwiXFxtYXRoYmZ7Q30iXSxbMSwwLCJcXG1hdGhiZntDfSBcXGRvd25hcnJvdyBBIl0sWzQsMSwiXFxEZWx0YV9BKFxcYXN0KSJdLFsyLDAsIlxcbWF0aGJme0N9Il0sWzUsMCwiXFxtYXRoYmZ7MX0iXSxbNSwxLCJcXGFzdCJdLFs0LDIsIlxcRGVsdGFfQShcXGFzdCkiXSxbMywxLCJDIl0sWzMsMiwiQyciXSxbMiwxLCJDIl0sWzIsMiwiQyciXSxbMSwxLCJmIl0sWzEsMiwiZyJdLFswLDAsIjFfXFxtYXRoYmZ7Q30gXFxkb3duYXJyb3cgXFxEZWx0YV9BIl0sWzAsMSwiXFxsYW5nIGYsIEMsIFxcYXN0IFxccmFuZyJdLFswLDIsIlxcbGFuZyBmJywgQycsIFxcYXN0IFxccmFuZyJdLFszLDAsIjFfXFxtYXRoYmZ7Q30iXSxbNCwwLCJcXERlbHRhX0EiLDJdLFsyLDYsIlxcRGVsdGFfQShcXG1hdGhybXtpZH1fXFxhc3QpIl0sWzcsOCwiYyIsMl0sWzcsMiwiZiJdLFs4LDYsImYnIiwyXSxbOSwxMCwiYyIsMl0sWzExLDEyLCJjIiwyXSxbMTQsMTUsIlxcbGFuZyBjLCBcXG1hdGhybXtpZH1fXFxhc3QgXFxyYW5nIiwyXV0=)

## 下方の対象から成る圏

圏$\mathbf{C}$を考える。圏$\mathbf{C}$の下方の対象から成る圏$A \downarrow \mathbf{C}$ は、以下の通り構成される圏である。

1. 圏$\mathbf{C}$の射であって、域が$A$であるものすべてを対象とする
2. 圏$\mathbf{C}$の射であって、$f' = c \circ f$を満たす射$c$を$f$から$f'$への射とする

[![category-of-objects-over-a](https://storage.googleapis.com/zenn-user-upload/97ef568892c0-20240817.png)](https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDIsIkMnIl0sWzAsMSwiQSJdLFsxLDEsIkMiXSxbMiwwLCJBIFxcZG93bmFycm93IFxcbWF0aGJme0N9Il0sWzIsMSwiZiJdLFsyLDIsImYnIl0sWzIsMywiZiJdLFsyLDEsImYnIiwyXSxbMywxLCJjIl0sWzIsMSwiXFxjaXJjbGVhcnJvd3JpZ2h0Il0sWzUsNiwiYyJdXQ==)

### コスライス圏

この構成はコスライス圏とも呼ばれ、$A / \mathbf{C}$とも書かれる。

### コンマ圏を使った表現

$A \downarrow \mathbf{C}$は$\Delta_A \downarrow 1_\mathbf{C}$で表すことができる。

[![DeltaA-downarrow-1c](https://storage.googleapis.com/zenn-user-upload/4d5450aedbe0-20240817.png)](https://q.uiver.app/#q=WzAsMTYsWzMsMCwiXFxtYXRoYmZ7Q30iXSxbNCwyLCJDJyJdLFs0LDEsIkMiXSxbMSwwLCJBIFxcZG93bmFycm93IFxcbWF0aGJme0N9Il0sWzEsMSwiZiJdLFsxLDIsImYnIl0sWzIsMCwiXFxtYXRoYmZ7MX0iXSxbMywxLCJcXERlbHRhX0EoXFxhc3QpIl0sWzMsMiwiXFxEZWx0YV9DKFxcYXN0KSJdLFsyLDEsIlxcYXN0Il0sWzUsMCwiXFxtYXRoYmZ7Q30iXSxbNSwxLCJDIl0sWzUsMiwiQyciXSxbMCwwLCJcXERlbHRhX0EgXFxkb3duYXJyb3cgMV9cXG1hdGhiZntDfSJdLFswLDEsIlxcbGFuZyBmLCBcXGFzdCwgQyBcXHJhbmciXSxbMCwyLCJcXGxhbmcgZicsIFxcYXN0LCBDJyBcXHJhbmciXSxbMiwxLCJjIl0sWzQsNSwiYyJdLFs3LDgsIlxcRGVsdGFfQShcXG1hdGhybXtpZH1fXFxhc3QpIiwyXSxbNywyLCJmIl0sWzgsMSwiZiciLDJdLFs2LDAsIlxcRGVsdGFfQSJdLFsxMCwwLCIxX1xcbWF0aGJme0N9IiwyXSxbMTEsMTIsImMiXSxbMTQsMTUsImMiXV0=)
