---
title: "表現可能関手"
free: false
---

局所的に小さな圏$\mathbf C$について、ある対象$A \in \rm{ob}(C)$を固定したhom関手$\hom_C(A, \_): \mathbf C \to \mathbf{Set}$を、しばしば表現(*Representation*)と呼ぶ。

より一般的に、hom関手と自然同型であるような関手を表現可能関手(*Representable functor*)と呼び、$\hom_C(A, \_)$は$F$によって表現可能である、などという。

関手$F: \mathbf C \to \mathbf{Set}$が表現可能関手である場合、局所的に小さな圏$\mathbf C$の任意の対象$X$に対して$\mathbf{Set}$の同型射$\epsilon_X$が存在する。
$\epsilon_X$は同型射であるので、$\epsilon_X$の逆射$\epsilon^{-1}_X$が存在して、$\epsilon_X \circ \epsilon^{-1}_X = \rm{id}_{F(X)}$, $\epsilon^{-1}_X \circ \epsilon_X = \rm{id}_{\hom_C(A, X)}$を満たす。　

![representable_functor](https://storage.googleapis.com/zenn-user-upload/082ca0da7d80-20231206.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiQSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMywxLCJIb21fQyhBLCBYKSJdLFs1LDEsIkhvbV9DKEEsIFgnKSJdLFswLDIsIlgiXSxbMSwyLCJYJyJdLFszLDIsIkYoWCkiXSxbNSwyLCJGKFgnKSJdLFszLDQsIkhvbV9DKEEsIGYpIl0sWzUsNiwiZiJdLFs3LDgsIkYoZikiXSxbMyw3LCJcXGVwc2lsb25fWCIsMCx7ImN1cnZlIjotMX1dLFs0LDgsIlxcZXBzaWxvbl97WCd9IiwwLHsiY3VydmUiOi0xfV0sWzcsMywiXFxlcHNpbG9uXnstMX1fWCIsMCx7ImN1cnZlIjotMX1dLFs4LDQsIlxcZXBzaWxvbl57LTF9X3tYJ30iLDAseyJjdXJ2ZSI6LTF9XSxbMSw1LCJhIl1d