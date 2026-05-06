---
title: "内部 hom 関手"
---

圏 $\mathbf{Set}$ において、hom 集合 $\hom_\mathbf{Set}(A, B)$ は、それ自体が $\mathbf{Set}$ の対象となる。
すなわち $A$ と $B$ の間の写像全体が集合である場合に、 $\hom_\mathbf{Set}(A, B) \in \mathrm{ob}(\mathbf{Set})$ が成り立つ。

これは便利な性質だが、当然ながら $\mathbf{Set}$ でしか成り立ちえない。内部 hom 関手は、そのような関手を一般化した概念である。

## 定義

内部 hom 関手 (*internal hom functor*) とは、双関手 $[-, -] : \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf C$ であって、hom 関手のようなふるまう関手をいう。

また内部 hom 関手を持つ圏を閉圏 (*Closed category*) と呼ぶ。

特にカルテシアン閉圏やモノイダル閉圏では、積と内部 hom 関手との随伴 $- \otimes B \dashv [B, -]$ が成り立ち、この随伴を hom 集合で表した式 $\hom_\mathbf C(A \otimes B, C) \simeq \hom_\mathbf C(A, [B, C])$ は特にカリー化と呼ばれる。
