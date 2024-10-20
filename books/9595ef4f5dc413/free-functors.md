---
title: "自由関手"
free: false
---

元ネタはnLabの[Free object](https://ncatlab.org/nlab/show/free+object)。

## 定義

$U: \mathbf{C} \to \mathbf{D}$を[忘却関手](forgetful-functors)とする。

$F \dashv U$を満たすとき、$U$の左随伴関手$F$を自由関手と呼ぶ。

## 自由対象

$F$が$U$の左随伴関手であるとき、圏$\mathbf D$の任意の対象$X$に対して$X$から$D$への普遍射$(F(X), \eta_X)$が存在するのだった。^[[随伴関手](adjunction-hom-functor)]

これに対して、圏$\mathbf D$のある対象$X$に対して$X$から$D$への普遍射$(F(X), \eta_X)$が存在するとき、$F(X)$を自由対象(*Free object*)、より厳密には$U$に対する$X$上の自由C-対象(Free C-object on $X$ with respect to $U$)と呼ぶ。

それぞれの自由対象は必ずしも$F$と$U$の随伴関係を要求しない。
しかしながら圏$\mathbf{D}$の任意の対象$X$が自由対象であるとき$F \dashv U$が成り立つ。

![free-objects](https://storage.googleapis.com/zenn-user-upload/bc3cc6bcd886-20240731.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntDfSJdLFsyLDAsIlxcbWF0aGJme0R9Il0sWzAsMSwiRihYKSJdLFswLDIsIkYoWCcpIl0sWzIsMSwiWCJdLFszLDEsIlUoRihYKSkiXSxbMywyLCJVKEYoWCcpKSJdLFsyLDMsIkYoZykiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNCw1LCJcXGV0YV9YIl0sWzUsNiwiVShGKGcpKSJdLFs0LDYsImYiLDJdLFswLDEsIlUiLDAseyJvZmZzZXQiOi0yfV0sWzEsMCwiRiIsMCx7Im9mZnNldCI6LTJ9XSxbMTIsMTEsIiIsMCx7ImxldmVsIjoxLCJzdHlsZSI6eyJuYW1lIjoiYWRqdW5jdGlvbiJ9fV1d
