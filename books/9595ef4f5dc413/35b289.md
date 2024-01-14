---
title: "普遍性"
free: false
---

## 定義

圏$\mathbf C$, $\mathbf D$, 関手$F: \mathbf C \to \mathbf D$を考える。
この時、関手$F: \mathbf C \to \mathbf D$から圏$\mathbf D$の対象Aへの普遍射(*Universal morphism*)は、圏$\mathbf C$の対象$X$と圏$D$の射$u: F(X) \to A$の組$(X, u)$で表され、以下の普遍性(*Universal property*)を満たす。

- $Y$が$\mathbf C$の対象で$f: F(Y) \to A$が$\mathbf D$の射であるような場合、常に$\mathbf C$の射$g: Y \to X$が一意に存在して、次の図を可換にする

![opposite_universal_morphism](https://storage.googleapis.com/zenn-user-upload/d909538b8a99-20231023.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMSwiQSJdLFszLDEsIkYoWCkiXSxbMywyLCJGKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzQsMCwiQSJdLFs1LDAsIkYiXSxbMywyLCJGKGcpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzMsMSwiZiJdLFs2LDUsImciLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiwxLCJ1IiwyXSxbOCw3LCLmma7pgY3lsIQiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=

普遍射は、射とは言うが、ある関手$F$から対象$A$への矢印のことである。またその実体は圏$\mathbf C$の対象$X$と圏$\mathbf D$の射$u: F(X) \to A$の組$(X, u)$である。

### 双対

先の普遍射の定義には、双対を考えることができる。すなわち圏$\mathbf D$の対象$A$から$F$への普遍射（あるいは余普遍射）は、$\mathbf C$の対象$X$と$\mathbf D$の射$u: A \to F(X)$からなる対$(X, u)$で表され、以下の普遍性を満たす。

- $Y$が$\mathbf C$の対象で$f: A \to F(Y)$が$\mathbf D$の射であるような場合、常に$\mathbf C$の射$g: X \to Y$が一意に存在して、次の図を可換にする

![universal_morphism](https://storage.googleapis.com/zenn-user-upload/eab04eeb7094-20231023.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMSwiQSJdLFszLDEsIkYoWCkiXSxbMywyLCJGKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzQsMCwiQSJdLFs1LDAsIkYiXSxbMiwzLCJGKGcpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEsMywiZiIsMl0sWzUsNiwiZyIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxLDIsInUiXSxbNyw4LCLmma7pgY3lsIQiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=

普遍射には双対を含めて二つあるが、一般にどちらを普遍射と呼びどちらを余普遍射と呼ぶような決まりはないらしい。文脈に応じて判断する必要がある。

このノートでは、積-余積あるいは極限-余極限を意識して順序を構成した。

## 解釈

ウィキペディアでは、普遍性は次のように説明される。

> 普遍性（英語: universality、または universal property）とは、ある特定の状況下において一意に射（あるいは準同型、構造を保つ写像）を定めるような抽象的性質で、それが特定の構成（例えば直積や直和、加群のテンソル積、距離空間の完備化など）を特徴づけるようなものをいう。

普遍性は一意に射を定めるような性質であるが、たいていの場合、その主張するところは特定の構造が同型を除いて一意であることである。

## 積の例

積の普遍性を用いた定義を参照。

https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/3e053e#%E6%99%AE%E9%81%8D%E6%80%A7%E3%82%92%E7%94%A8%E3%81%84%E3%81%9F%E5%AE%9A%E7%BE%A9

## 極限の例

極限の普遍性を用いた定義を参照。

https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/954f1b
