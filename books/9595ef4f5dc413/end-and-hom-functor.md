---
title: "エンドと hom 関手の交換"
---

## 定理

エンドと hom 関手は、以下のようにして交換できる。

$$
\hom_{\mathbf D}(D, \int_{c \in \mathbf C} F(c, c)) \simeq
\int_{c \in \mathbf C} \hom_{\mathbf D}(D, F(c, c))
$$

すなわち圏 $\mathbf D$ の対象 $\int_{c \in \mathbf C} F(c, c)$ を hom 関手 $\hom_\mathbf D(D, -) : \mathbf D \to \mathbf{Set}$ で写した集合と、関手 $\hom_\mathbf D(D, F(-, -)) : \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf{Set}$ のエンドとの間には、全単射が存在する。

## 証明

hom 関手は連続なので、$\hom_{\mathbf D}(D, -) : \mathbf D \to \mathbf{Set}$ は極限を保存する。エンドは極限の一種であったから、$\hom_{\mathbf D}(D, -)$ はエンドをエンドに写す。したがってエンド $\int_{c \in \mathbf C} F(c, c)$ の像は、合成した関手 $\hom_{\mathbf D}(D, F(-, -)) : \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf{Set}$ のエンドに一致し、以下が成り立つ。

$$
\hom_{\mathbf D}(D, \int_{c \in \mathbf C} F(c, c)) \simeq
\int_{c \in \mathbf C} \hom_{\mathbf D}(D, F(c, c))
$$
