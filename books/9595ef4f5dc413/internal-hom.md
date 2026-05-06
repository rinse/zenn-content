---
title: "内部 hom 関手"
---

圏 $\mathbf{Set}$ において、hom 集合 $\hom_\mathbf{Set}(A, B)$ は、それ自体が $\mathbf{Set}$ の対象となる。
すなわち $A$ と $B$ の間の写像全体が集合である場合に、 $\hom_\mathbf{Set}(A, B) \in \mathrm{ob}(\mathbf{Set})$ が成り立つ。

これは便利な性質だが、当然ながら $\mathbf{Set}$ でしか成り立ちえない。内部 hom 関手は、そのような関手を一般化した概念である。

## 定義

内部 hom 関手 (*internal hom functor*) とは、hom 関手のようなふるまいを持つ関手 $[-, -] : \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf C$ のことをいう。

また内部 hom 関手を持つ圏を閉圏と呼ぶ。

## モノイダル閉圏の内部 hom 関手

[モノイダル圏](./monoidal-category.md) $\mathbf C$ において、モノイダル積の片側を任意の対象 $B$ で固定して得られる関手 $- \otimes B : \mathbf C \to \mathbf C$ が右随伴関手 $-^B : \mathbf C \to \mathbf C$ を持つとき、この圏をモノイダル閉圏 (*Closed monoidal category*) と呼ぶ。

この関手によって得られる指数対象は、モノイダル閉圏の内部 hom である。

またモノイダル閉圏には、カリー化として知られる以下の同型が存在する。

$$
\hom_\mathbf C(A, C^B) \simeq \hom_\mathbf C(A \otimes B, C)
$$
