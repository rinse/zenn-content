---
title: "余米田の補題"
---

## 定理

余米田の補題とは以下の同型である。

$$
F(A) \simeq \int^{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C}(A, C) \times F(C)
$$

## 余米田の補題とは？

米田の補題は右Kan拡張で表せる。
$F : \mathbf C^\mathrm{op} \to \mathbf{Set}$に沿った恒等関手$1_{\mathbf C^\mathrm{op}}$の右Kan拡張を考える。

この右Kan拡張$\mathrm{Ran}_1 F$のある点$A \in \mathbf C$を[エンド](./end)で計算すると、以下のように米田の補題が得られる。

$$
\begin{align}
F(A) &\simeq (\mathrm{Ran}_1 F)(A) \notag \\
&\simeq \int_{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C^\mathrm{op}}(A, 1(C)) \pitchfork F(C) \\
&\simeq \int_{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C}(C, A) \pitchfork F(C) \\
&\simeq \int_{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf{Set}}(\hom_{\mathbf C}(C, A), F(C)) \\
&\simeq \hom_{\mathbf{Set}^{\mathbf C^\mathrm{op}}}(\hom_{\mathbf C}(-, A), F) \\
\end{align}
$$

$(1)$は各点右Kan拡張のエンドでの計算である。
$(2)$では恒等関手と$\mathrm{op}$を外している。
$(3)$では[パワー](./power#setにおけるパワー)の$\mathbf{Set}$における定義を展開している。
$(4)$は[エンドと自然変換全体の集合の同型](./end-nat)によって与えられる。

ある右Kan拡張をエンドで計算して得られるものが米田の補題であれば、ある左Kan拡張をコエンドで計算して得られるものが余米田の補題であるという、というのがここでの余米田の補題の定義である。

そのため、上と同じ議論を各点左Kan拡張に対して行う。

$$
\begin{align}
F(A) &\simeq (\mathrm{Lan}_1 F)(A) \notag \\
&\simeq \int^{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C^\mathrm{op}}(1(C), A) \odot F(C) \\
&\simeq \int^{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C}(A, C) \odot F(C) \\
&\simeq \int^{C \in \mathbf C^\mathrm{op}} \hom_{\mathbf C}(A, C) \times F(C) \\
\end{align}
$$

$(5)$は各点左Kan拡張のコエンドでの計算である。
$(6)$では恒等関手と$\mathrm{op}$を外している。
$(7)$では[コパワー](./power#setにおけるコパワー)の$\mathbf{Set}$における定義を展開している。

このように計算すると、最終的に上で紹介した式が得られる。
