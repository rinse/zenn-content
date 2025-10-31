---
title: "自己関手"
free: false
---

自己関手 (*Endo functor*) とは、域と余域が同じである関手である。

$$
F : \mathbf{C} \to \mathbf{C}
$$

## 自己関手の合成

同じ圏を域・余域に持つ自己関手同士は合成できる。
すなわち圏$F : \mathbf C \to \mathbf C$, $G : \mathbf C \to \mathbf C$を考えると、新しい自己関手$G \circ F : \mathbf C \to \mathbf C$を得られる。

また恒等関手$1_\mathbf C$は合成の単位元となる。すなわち$1_\mathbf C \circ F = F \circ 1_\mathbf C = F$が成り立つ。

## 強モノイダル圏

自己関手の圏は、関手の合成をモノイダル積として強モノイダル圏を構成する。

1. 関手の合成をモノイダル積とする。すなわち$G \otimes F \overset{\text{def}}{=} G \circ F$
2. 単位対象として$1_\mathbf C$を定める。
3. 関手の合成は結合的な演算であり、$G \circ (F \circ H) = (G \circ F) \circ H$が成り立つ。すなわち自明な結合子が存在する。
    - $\alpha_{F, G, H} : F \otimes (G \otimes H) = (F \otimes G) \otimes H$
4. 関手の合成は恒等関手を単位元として持つ演算であるため、左単位律を保証する自明な自然同型が存在する。
    - $\lambda_F : 1_\mathbf C \otimes F = F$
5. 関手の合成は恒等関手を単位元として持つ演算であるため、右単位律を保証する自明な自然同型が存在する。
    - $\rho_F : F \otimes 1_\mathbf C = F$

自然同型$\alpha$, $\lambda$, $\rho$ がいずれも恒等射であるため、自己関手の圏は強モノイダル圏である。

コヒーレンス条件は関手の合成の結合律から自明である。

[![](https://storage.googleapis.com/zenn-user-upload/bbd52397eed4-20251031.png)](https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDXlxcbWF0aGJmIEMiXSxbMCwxLCIoKEYgXFxjaXJjIEcpIFxcY2lyYyBIKSBcXGNpcmMgSSJdLFsxLDEsIihGIFxcY2lyYyAoRyBcXGNpcmMgSCkpIFxcY2lyYyBJIl0sWzEsMiwiRiBcXGNpcmMgKChHIFxcY2lyYyBIKSBcXGNpcmMgSSkiXSxbMCwzLCIoRiBcXGNpcmMgRykgXFxjaXJjIChIIFxcY2lyYyBJKSJdLFsxLDMsIkYgXFxjaXJjIChHIFxcY2lyYyAoSCBcXGNpcmMgSSkpIl0sWzAsNCwiKEYgXFxjaXJjIDFfXFxtYXRoYmYgQykgXFxjaXJjIEciXSxbMSw0LCJGIFxcY2lyYyAoMV9cXG1hdGhiZiBDIFxcY2lyYyBHKSJdLFsxLDUsIkYgXFxjaXJjIEciXSxbMSwyXSxbMSw0XSxbMiwzXSxbMyw1XSxbNCw1XSxbNiw3XSxbNiw4XSxbNyw4XV0=)

### モノイド対象

自己関手の圏上の強モノイダル圏$\lang \mathbf C^\mathbf C, \circ, 1_\mathbf C \rang$のモノイド対象$\lang M : \mathbf C \to \mathbf C \in \mathrm{ob}(\mathbf C^\mathbf C), \mu : M^2 \to M, \eta : 1_\mathbf C \to M \rang$は[モナド](./monad)と呼ばれる。

## 表記

自分自身との合成を指数表記を使って表す。

$$
F^2 \overset{\mathrm{def}}{=} F \circ F
$$
