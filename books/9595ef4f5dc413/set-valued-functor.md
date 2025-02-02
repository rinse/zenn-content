---
title: "集合値関手"
free: false
---

## 定義

終域が集合の圏$\mathbf{Set}$であるような関手について、このことを特に強調して集合値関手(*Set valued functor*)と呼ぶ。

すなわち一般の圏$\mathbf{C}$と集合の圏$\mathbf{Set}$との間の関手$F : \mathbf{C} \to \mathbf{Set}$は集合値関手である。

## 有用な集合値関手

- [hom関手](hom-functor)は集合値関手である
    - $\hom_C(A, \_) : \mathbf{C} \to \mathbf{Set}$
    - $\hom_C(\_, A) : \mathbf{C}^{\mathrm{op}} \to \mathbf{Set}$

## 集合値関手の圏

集合値関手の圏とは、対象に集合値関手を持つ[関手圏](category-of-functors)である。

## 集合値関手の圏の大きさ

* $\mathbf{C}$が小さいとき、$\mathbf{Set}^C$, $\mathbf{Set}^{C^{\mathrm{op}}}$は常に局所的に小さい。
* $\mathbf{C}$が局所的に小さいとき、$\mathbf{Set}^C$, $\mathbf{Set}^{C^{\mathrm{op}}}$は必ずしも局所小ではない。
    * ただし[米田の補題](yoneda-lemma)によって$\hom_{\mathrm{Set}^C}(\hom(A, \_), F)$および$\hom_{\mathrm{Set}^{C^{\mathrm{op}}}}(\hom(\_, A), F)$は常に集合である。
* $\mathbf{C}$が局所小ではないとき、[米田埋め込み](yoneda-embedding)は定義されず、米田の補題も適用されない。

参考: [圏の大きさ](largeness-of-categories)
