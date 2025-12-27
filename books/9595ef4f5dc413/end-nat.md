---
title: "エンドと自然変換全体の集合との同型"
---

## 定理

関手$F, G : \mathbf C \to \mathbf D$を考える。
これらから作る双関手$\hom_{\mathbf D}(F(-), G(-)): \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf{Set}$の[エンド](./end)は、$F, G$の間の自然変換全体の集合と同型になる。

すなわち以下が成り立つ。

$$
\int_{C \in \mathbf C}\hom_{\mathbf D}(F(C), G(C)) \simeq \hom_{\mathbf D^\mathbf C}(F, G)
$$
