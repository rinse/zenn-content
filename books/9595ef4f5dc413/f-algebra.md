---
title: "F-代数"
free: false
---

## 定義

ある自己関手$F: \mathbf{C} \to \mathbf{C}$を考える。

このときある対象$A \in \mathbf{C}$と射$f: F(A) \to A$の組$(A, a)$をF-代数(*F-algebra*)という。

[![f-algebra](https://storage.googleapis.com/zenn-user-upload/76d561c0c15f-20240805.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMCwxLCJGKEEpIl0sWzIsMSwiYSJdXQ==)

## F-代数の準同型

ある自己関手$F$を考えるとき、F代数$(A, a)$から別のF代数$(B, b)$への準同型とは、射$f: A \to B$であって、$f \circ a = b \circ F(f)$を満たすものをいう。

すなわち下を可換にする射$f$のことである。

[![homomorphism-of-f-algebra](https://storage.googleapis.com/zenn-user-upload/16ee2ca77686-20240805.png)](https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMCwxLCJGKEEpIl0sWzAsMiwiRihCKSJdLFsxLDIsIkIiXSxbMiwxLCJhIl0sWzMsNCwiYiIsMl0sWzEsNCwiZiJdLFsyLDMsIkYoZikiLDJdXQ==)

## F-余代数の定義

F代数の双対を考える。

すなわち自己関手$F: \mathbf{C} \to \mathbf{C}$を考えたとき、ある対象$A \in \mathbf{C}$と射$f: A \to F(A)$の組$(A, f)$をF-余代数(*F-coalgebra*)という。

[![f-coalgebra](https://storage.googleapis.com/zenn-user-upload/cfe3ff9f0948-20240805.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJGKEEpIl0sWzEsMiwiYSJdXQ==)

## F-余代数の準同型

F-代数の準同型と同じ議論ができる。

すなわちF余代数$(A, a)$から別のF余代数$(B, b)$への準同型とは、射$f: A \to B$であって、$F(f) \circ a = b \circ f$を満たすものをいう。

すなわち下を可換にする射$f$のことである。

[![homomorphism-of-f-coalgebra](https://storage.googleapis.com/zenn-user-upload/8f1ec51ba257-20240805.png)](https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJGKEEpIl0sWzEsMiwiRihCKSJdLFswLDIsIkIiXSxbMSwyLCJmIl0sWzEsNCwiYSIsMl0sWzIsMywiRihhKSJdLFs0LDMsImciLDJdXQ==)

## F-代数の圏

ある関手$F$から構成されるF-代数の全体は、F-代数の準同型を射として圏を構成する。

[![falg](https://storage.googleapis.com/zenn-user-upload/190970a9886f-20240805.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkYoQSkiXSxbMSwxLCJBIl0sWzAsMiwiRihCKSJdLFsxLDIsIkIiXSxbMywwLCJcXG1hdGhiZntGYWxnfSJdLFszLDEsIihBLCBhKSJdLFszLDIsIihCLCBiKSJdLFsxLDIsImEiXSxbMyw0LCJiIiwyXSxbMSwzLCJGKGYpIiwyXSxbMiw0LCJmIl0sWzEsNCwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzYsNywiZiJdXQ==)

## F-代数の圏の始対象

F-代数の圏の[始対象](initial-object)$(I, i)$を考える。始対象とは任意の対象に対してただ一つの射を持つものである。

[![initial-object-of-category-of-f-algebra](https://storage.googleapis.com/zenn-user-upload/2c38d41706c0-20240805.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDIsIkYoQSkiXSxbMSwyLCJBIl0sWzMsMCwiXFxtYXRoYmZ7RmFsZ30iXSxbMywyLCIoQSwgYSkiXSxbMywxLCIoSSwgaSkiXSxbMCwxLCJGKEkpIl0sWzEsMSwiSSJdLFsxLDIsImEiXSxbNSw0LCJqX0EiXSxbNiw3LCJpIl0sWzYsMSwiRihqX0EpIiwyXSxbNywyLCJqX0EiXSxbNiwyLCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

F-代数の圏の始対象を始代数(*Initial algebra*)と呼ぶ。F-代数の終対象を終代数(*Terminal algebra*)と呼ぶ

## ランベックの定理

関手$F$が始代数$(I, i)$を持つとき、射$i$は同型射である。すなわち$F(I) \simeq I$を満たす。

これをもってFの始対象はFの最小不動点であるとも言う。

### 証明

関手$F$が始代数$(I, i)$を備えているとする。

F-代数$(F(I), F(i))$を考えると、$(I, i)$が始代数であるから、F代数の準同型$j: I \to F(I)$がただ一つ存在して、$j \circ i = F(i) \circ F(j)$を満たす。すなわち以下を可換にする。

[![lambeks-theorem](https://storage.googleapis.com/zenn-user-upload/70d3d1d722d1-20240805.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkYoSSkiXSxbMCwyLCJGKEYoSSkpIl0sWzEsMiwiRihJKSJdLFsxLDEsIkkiXSxbMywwLCJcXG1hdGhiZntGYWxnfSJdLFszLDEsIihJLCBpKSJdLFszLDIsIihGKEkpLCBGKGkpKSJdLFsxLDQsImkiXSxbNCwzLCJqIl0sWzIsMywiRihpKSIsMl0sWzEsMiwiRihqKSIsMl0sWzEsMywiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzYsNywiaiJdXQ==)

このとき$i \circ j: I \to I$という射を見つけることができるが、始代数の性質により$I$から$I$への準同型は唯一恒等射しか存在しない。すなわち$i \circ j = \mathrm{id}_I$である。
よって$i$は$j$を逆射とする同型射であり、$I \simeq F(I)$が成り立つ。

### 疑問

$I$から$I$への準同型は唯一恒等射しか存在しないからといって、即座に$i \circ j = \mathrm{id}_I$と言って良いのだろうか？
圏$\mathbf{C}$にF-代数を構成しない対象や射が含まれている場合に、$I \to I$の非自明な射が存在しないことをどうやって証明できるだろうか？
