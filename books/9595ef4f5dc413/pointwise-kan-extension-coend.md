---
title: "コエンドによる各点左Kan拡張"
---

[各点左Kan拡張](./pointwise-kan-extension) では、余極限を用いて$\mathrm{Lan}_F G(D)$の値を計算した。
ここでは[コエンド](./end)と[コパワー](./power)を使って各点左Kan拡張の値を計算できることを確認する。

## 定理

各点右Kan拡張はエンドを使って計算できる。

$$
(\mathrm{Ran}_F G)(D) \simeq \int_{C \in \mathbf C} \hom_\mathbf D(D, F(C)) \pitchfork G(C)
$$

## 双対

各点左Kan拡張はコエンドを使って計算できる。

$$
(\mathrm{Lan}_F G)(D) \simeq \int^{C \in \mathbf C} \hom_\mathbf D(F(C), D) \odot G(C)
$$
