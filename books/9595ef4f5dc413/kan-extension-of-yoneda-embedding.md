---
title: "米田埋め込みのKan拡張"
free: false
---

## 定理

$F$に沿った米田埋め込み$H_- : \mathbf{C} \to \mathbf{Set}^{\mathbf{C}^\mathrm{op}}$の左Kan拡張$\mathrm{Lan}_F H_- : \mathbf{D} \to \mathbf{Set}^{\mathbf{C}^\mathrm{op}}$を考える。

[![](https://storage.googleapis.com/zenn-user-upload/b230596ad830-20250315.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIlxcbWF0aGJme0R9Il0sWzEsMSwiXFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fSJdLFsxLDIsIlxcbWF0aHJte0xhbn1fRiBIXy0iLDJdLFswLDIsIkhfLSJdLFswLDEsIkYiLDJdLFs0LDMsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dXQ==)

このとき、任意の$D \in \mathrm{ob}(\mathbf{D})$に対して、以下が成り立つ。

$$
(\mathrm{Lan}_F H_-)(D) \simeq \hom_D(F(\_), D)
$$

### 証明

$\mathbf{Set}^{\mathbf{C}^\mathrm{op}}$は余完備なので、$\mathrm{Lan}_F H_-$は[各点左Kan拡張](./pointwise-kan-extension)である。

ここで各点左Kan拡張の[定理](./pointwise-kan-extension#定理2)を考えると、$D \in \mathrm{ob}(\mathbf{D})$, $P \in \mathrm{ob}(\mathbf{Set}^{\mathbf{C}^\mathrm{op}})$ について自然に以下の等式が成り立つ。

$$
\hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}((\mathrm{Lan}_F H_-)(D), P) \simeq \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(\hom_D(F(\_), D), \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(H_-(\_), P))
$$

右辺が分かりにくいが、以下のような図式で書き下した自然変換$\alpha$の集まりだ。

![](https://storage.googleapis.com/zenn-user-upload/3ef194d16e46-20250315.png)

自然変換$\alpha \in \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(\hom_D(F(\_), D), \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(H_-(\_), P))$を圏$\mathbf{C}$の要素で書き下すと、次のようになる。

![](https://storage.googleapis.com/zenn-user-upload/07c224ab8cd1-20250315.png)

https://q.uiver.app/#q=WzAsMTYsWzEsMCwiXFxtYXRoYmZ7RH0iXSxbMSwyLCJEIl0sWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMCwxLCJDIl0sWzEsMSwiRihDKSJdLFsyLDAsIlxcbWF0aGJme1NldH1ee1xcbWF0aGJme0NeXFxtYXRocm17b3B9fX0iXSxbNCwxLCJcXGhvbV9EKEYoXFxfKSwgRCkiXSxbMywyLCJQIl0sWzQsMiwiXFxob21fe1xcbWF0aGJme1NldH1ee1xcbWF0aGJme0N9XlxcbWF0aHJte29wfX19KEhfLShcXF8pLCBQKSkiXSxbMiwyLCJIX0MgPSBcXGhvbV9DKFxcXywgQykiXSxbNSwwLCJcXG1hdGhiZntTZXR9Il0sWzAsMiwiQyciXSxbNSwxLCJcXGhvbV9EKEYoQyksIEQpIl0sWzUsMiwiXFxob21fe1xcbWF0aGJme1NldH1ee1xcbWF0aGJme0N9XlxcbWF0aHJte29wfX19KEhfQywgUCkiXSxbNiwxLCJcXGhvbV9EKEYoQycpLCBEKSJdLFs2LDIsIlxcaG9tX3tcXG1hdGhiZntTZXR9XntcXG1hdGhiZntDfV5cXG1hdGhybXtvcH19fShIX3tDJ30sIFApIl0sWzQsMSwiZCIsMl0sWzksN10sWzYsOCwiXFxhbHBoYSJdLFszLDExLCJjIiwyXSxbMTIsMTMsIlxcYWxwaGFfQyIsMl0sWzE0LDE1LCJcXGFscGhhX3tDJ30iXSxbMTQsMTIsIlxcaG9tX0QoRihjKSwgRCkiLDJdLFsxNSwxMywiXFxob21fe1xcbWF0aGJme1NldH1ee1xcbWF0aGJme0N9XlxcbWF0aHJte29wfX19KEhfLShjKSwgUCkiXSxbMTIsMTUsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d

いま、右辺に対して、[米田の補題](./yoneda-lemma)を適用することを考える。米田の補題によって、任意の$A \in \mathrm{ob}(\mathbf{C})$ について、以下の自然な同型が成り立つ。

$$
\hom_{\mathrm{Set}^{C^\mathrm{op}}}(H_A, F) \simeq F(A)
$$

よって$\hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(H_-(\_), P) \simeq P(\_)$であるから、最初の式を以下のように書き換えられる。

$$
\hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(\mathrm{Lan}_F H_-(D), P) \simeq \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(\hom_D(F(\_), D), P)
$$

[Hom関手の性質](./theorems-on-hom-functors)により、$\hom_C(X, C) \simeq \hom_C(Y, C)$が成り立つとき$X \simeq Y$が成り立つから、以下が得られる。

$$
(\mathrm{Lan}_F H_-)(D) \simeq \hom_D(F(\_), D)
$$

証明おわり。

## 定理1

米田埋め込みに沿った米田埋め込みのKan拡張は恒等関手である。

$$
\mathrm{Lan}_{H_-} H_- = \mathrm{Id}_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}
$$

[![](https://storage.googleapis.com/zenn-user-upload/37d75d16bbc6-20250315.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIlxcbWF0aGJme1NldH1ee1xcbWF0aGJme0N9XlxcbWF0aHJte29wfX0iXSxbMCwxLCJcXG1hdGhiZntTZXR9XntcXG1hdGhiZntDfV5cXG1hdGhybXtvcH19Il0sWzAsMSwiSF8tIl0sWzAsMiwiSF8tIiwyXSxbMiwxLCJcXG1hdGhybXtMYW59X3tIXy19IEhfLSA9IFxcbWF0aHJte0lkfV97XFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fX0iLDJdLFszLDUsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dXQ==)

一般に$\mathrm{Lan}_F F$は恒等関手にはならないが、米田埋め込みに沿った米田埋め込みのKan拡張は恒等関手である。
