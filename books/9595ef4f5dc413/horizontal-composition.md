---
title: "自然変換の水平合成"
free: false
---

## 自然変換と関手の水平合成

圏$\mathbf C$, $\mathbf D$, $\mathbf E$, 関手$F, F': \mathbf C \to \mathbf D$とそれら間の自然変換$\sigma: F \Rightarrow F'$, 関手$G: \mathbf D \to \mathbf E$があったとき、圏$\mathbf C$の任意の対象$X$における射$\sigma_X$を関手$\mathbf G$で$\mathbf E$に写した射$G(\sigma_X)$の族を、自然変換$\sigma$と関手$G$の水平合成(*horizontal composition*)と呼び、$G \ast \sigma : G \circ F \Rightarrow G \circ F'$と表す。

$$
(G \ast \sigma)_X \overset{\mathrm{def}}{=} G(\sigma_X)
$$

このとき以下を可換にする。

![horizontal_compose1](https://storage.googleapis.com/zenn-user-upload/a721aaffa2ef-20231203.png)

https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMywxLCJGKEMpIl0sWzQsMSwiRihDJykiXSxbMywyLCJGJyhDKSJdLFs0LDIsIkYnKEMnKSJdLFs2LDAsIlxcbWF0aGJmIEUiXSxbNiwxLCJHKEYoQykpIl0sWzcsMSwiRyhGKEMnKSkiXSxbNiwyLCJHKEYnKEMpKSJdLFs3LDIsIkcoRicoQycpKSJdLFsxLDIsImYiXSxbNCw1LCJGKGYpIl0sWzYsNywiRicoZikiLDJdLFs0LDYsIlxcc2lnbWFfe0N9IiwyXSxbNSw3LCJcXHNpZ21he0MnfSJdLFs5LDEwLCJHKEYoZikpIl0sWzExLDEyLCJHKEYnKGYpKSIsMl0sWzksMTEsIkcoXFxzaWdtYV9DKSIsMl0sWzEwLDEyLCJHKFxcc2lnbWFfe0MnfSkiXV0=

直感的な図を書くと次の通りだ。関手と自然変換が合成されて、新たな自然変換が生まれている。

![horizontal_compose1_2](https://storage.googleapis.com/zenn-user-upload/1bedb1d8e00b-20231204.png)

このとき、自然変換$G \ast \sigma: G \circ F \Rightarrow G \circ F'$は以下の図式を可換にする。

![horizontal_compose_commutative](https://storage.googleapis.com/zenn-user-upload/2e76e5f7ba49-20231204.png)

## 関手と自然同型の水平合成

圏$\mathbf C$, $\mathbf D$, $\mathbf E$, 関手$F: \mathbf C \to \mathbf D$, 関手$G, G': \mathbf D \to \mathbf E$とそれら間の自然変換$\tau: G \Rightarrow G'$があったとき、圏$\mathbf C$の任意の対象$X$に対して、圏$\mathbf D$の$F(X)$における射$\tau_{F(X)}$の族を$\tau \ast F : G\circ F \Rightarrow G'\circ F$と表す。

$$
(\tau \ast F)_X \overset{\mathrm{def}}{=} \tau_{F(X)}
$$

このとき以下の右端の図を可換にする。

![horizontal_compose2](https://storage.googleapis.com/zenn-user-upload/f8a901a9345e-20231203.png)

https://q.uiver.app/#q=WzAsMTEsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMywxLCJGKEMpIl0sWzQsMSwiRihDJykiXSxbNiwwLCJcXG1hdGhiZiBFIl0sWzYsMSwiRyhGKEMpKSJdLFs3LDEsIkcoRihDJykpIl0sWzYsMiwiRycoRihDKSkiXSxbNywyLCJHJyhGKEMnKSkiXSxbMSwyLCJmIl0sWzQsNSwiRihmKSJdLFs3LDgsIkcoRihmKSkiXSxbOSwxMCwiRycoRihmKSkiLDJdLFs3LDksIlxcdGF1X3tGKEMpfSIsMl0sWzgsMTAsIlxcdGF1X3tGKEMnKX0iXV0=

直感的な図を書くと次の通りだ。関手と自然変換が合成されて、新たな自然変換が生まれている。

![horizontal_compose2_2](https://storage.googleapis.com/zenn-user-upload/2cf11c31c14b-20231204.png)

このとき、自然変換$\tau \ast F: G \circ F \Rightarrow G' \circ F$は以下の図式を可換にする。

![horizontal_compose_commutative2](https://storage.googleapis.com/zenn-user-upload/f475e6236049-20231204.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMSwiXFxtYXRoYmYgQyJdLFsxLDEsIlxcbWF0aGJmIEQiXSxbMywxLCJcXG1hdGhiZiBFIl0sWzAsMywiXFxtYXRoYmYgQyJdLFszLDMsIlxcbWF0aGJmIEUiXSxbNSwwLCJcXG1hdGhiZiBFIl0sWzUsMSwiRyhGKEMpKSJdLFs2LDEsIkcoRihDJykpIl0sWzUsMiwiRycoRihDKSkiXSxbNiwyLCJHJyhGKEMnKSkiXSxbMCwxLCJGIl0sWzEsMiwiRyIsMCx7ImN1cnZlIjotMn1dLFsxLDIsIkcnIiwyLHsiY3VydmUiOjJ9XSxbMyw0LCJHIFxcY2lyYyBGIiwwLHsiY3VydmUiOi0yfV0sWzMsNCwiRycgXFxjaXJjIEYiLDIseyJjdXJ2ZSI6Mn1dLFs2LDcsIkcoRihmKSkiXSxbNiw4LCIoXFx0YXUgXFxhc3QgRilfQyIsMl0sWzgsOSwiRycoRihmKSkiLDJdLFs3LDksIihcXHRhdSBcXGFzdCBGKV97Qyd9Il0sWzExLDEyLCJcXHRhdSIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbMTMsMTQsIlxcdGF1IFxcYXN0IEYiLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV1d

## 自然変換と自然変換の水平合成

関手と自然変換の水平合成ができると、自然変換と自然変換を水平合成することができるようになる。

圏$\mathbf C$, $\mathbf D$, $\mathbf E$, 関手$F, F': \mathbf C \to \mathbf D$とそれらの間の自然変換$\sigma: F \Rightarrow F'$, 関手$G, G': \mathbf D \to \mathbf E$とそれらの間の自然変換$\tau: G \Rightarrow G'$があったとき、$\sigma$と$\tau$の間の水平合成$\tau \ast \sigma: G\circ F \Rightarrow G' \circ F'$を考えることができる。

このとき以下の右端の図を可換にする。

![horizontal_compose3](https://storage.googleapis.com/zenn-user-upload/86ec42c63826-20231203.png)

https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMywxLCJGKEMpIl0sWzQsMSwiRihDJykiXSxbMywyLCJGJyhDKSJdLFs0LDIsIkYnKEMnKSJdLFs2LDAsIlxcbWF0aGJmIEUiXSxbNiwxLCJHKEYoQykpIl0sWzYsMiwiRyhGJyhDKSkiXSxbNywyLCJHJyhGJyhDKSkiXSxbNywxLCJHJyhGKEMpKSJdLFsxLDIsImYiXSxbNCw1LCJGKGYpIl0sWzUsNywiXFxzaWdtYV97Qyd9Il0sWzQsNiwiXFxzaWdtYV9DIl0sWzYsNywiRicoZikiLDJdLFs5LDEwLCJHKFxcc2lnbWFfQykiLDJdLFsxMCwxMSwiXFx0YXVfe0YnKEMpfSIsMl0sWzksMTEsIlxcdGF1IFxcYXN0IFxcc2lnbWEiLDFdLFs5LDEyLCJcXHRhdV97RihDKX0iXSxbMTIsMTEsIkcnKFxcc2lnbWFfQykiXV0=

直感的な図を描くと次の通りだ。

![horizontal_compose3_2](https://storage.googleapis.com/zenn-user-upload/9126a834201a-20231204.png)

## 相互交換法則 (*interchange law*)

自然変換$\theta$, $\eta$, $\tau$, $\sigma$に対して、それらの間の垂直合成と水平合成との間には、相互交換法則と呼ばれる次の等式が成り立つ。

$$
(\theta \circ \eta) \ast (\tau \circ \sigma) = (\theta \ast \tau) \circ (\eta \ast \sigma)
$$

この主張は、直感的な図で描けば自明なことのように思われるだろう。

一番上が登場人物を全て書き下したものだ。
二番目の図が$(\theta \circ \eta) \ast (\tau \circ \sigma)$を表している。
三番目の図が$(\theta \ast \tau) \circ (\eta \ast \sigma)$を表している。

![interchange_law](https://storage.googleapis.com/zenn-user-upload/c6bcaa1246a1-20231204.png)

### 証明

圏$\mathbf C$, $\mathbf D$, $\mathbf E$, 関手$F, F', F'': \mathbf C \to \mathbf D$と$G, G', G'': \mathbf D \to \mathbf E$, および自然変換$\sigma: F \Rightarrow F'$, $\tau: F' \Rightarrow F''$, $\eta: G \Rightarrow G'$, $\theta: G' \Rightarrow G''$を考える。

![Two_vertical_compositions](https://storage.googleapis.com/zenn-user-upload/78a1934f666b-20231203.png)

https://q.uiver.app/#q=WzAsMTcsWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMywxLCJGKEMpIl0sWzQsMSwiRihDJykiXSxbMywyLCJGJyhDKSJdLFs0LDIsIkYnKEMnKSJdLFszLDMsIkYnJyhDKSJdLFs0LDMsIkYnJyhDJykiXSxbNiwwLCJcXG1hdGhiZiBFIl0sWzYsMSwiRyhEKSJdLFs3LDEsIkcoRCcpIl0sWzYsMiwiRycoRCkiXSxbNywyLCJHJyhEJykiXSxbNiwzLCJHJycoRCkiXSxbNywzLCJHJycoRCcpIl0sWzEsMiwiZiJdLFs0LDUsIkYoZikiXSxbNiw3LCJGJyhmKSJdLFs4LDksIkYnJyhmKSIsMl0sWzYsOCwiXFx0YXVfQyIsMl0sWzUsNywiXFxzaWdtYV97Qyd9Il0sWzcsOSwiXFx0YXVfe0MnfSJdLFsxMSwxMiwiRyhnKSJdLFsxMywxNCwiRycoZykiXSxbMTUsMTYsIkcnJyhnKSIsMl0sWzExLDEzLCJcXGV0YV9EIiwyXSxbMTMsMTUsIlxcdGhldGFfRCIsMl0sWzQsNiwiXFxzaWdtYV9DIiwyXSxbMTIsMTQsIlxcZXRhX3tEJ30iXSxbMTQsMTYsIlxcdGhldGFfe0QnfSJdXQ==

このとき、自然変換$\tau \circ \sigma: F \Rightarrow F''$と$\theta \circ \eta: G \Rightarrow G''$の水平合成$(\theta\circ\eta)\ast(\tau\circ\sigma): G \circ F \to G'' \circ F''$を見つけることができる。

![(theta . eta) * (tau . sigma)](https://storage.googleapis.com/zenn-user-upload/201f64f856a3-20231203.png)

https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZiBFIl0sWzAsMSwiRyhGKEMpKSJdLFswLDIsIkcnJyhGKEMpKSJdLFsyLDIsIkcnJyhGJycoQykpIl0sWzIsMSwiRyhGJycoQykpIl0sWzEsNCwiRygoXFx0YXUgXFxjaXJjIFxcc2lnbWEpX0MpIl0sWzIsMywiRycnKChcXHRhdSBcXGNpcmMgXFxzaWdtYSlfQykiLDJdLFsxLDIsIihcXHRoZXRhIFxcY2lyYyBcXGV0YSlfe0YoQyl9IiwyXSxbNCwzLCIoXFx0aGV0YSBcXGNpcmMgXFxldGEpX3tGJycoQyl9Il0sWzEsMywiKFxcdGhldGEgXFxjaXJjIFxcZXRhKSBcXGFzdCAoXFx0YXUgXFxjaXJjIFxcc2lnbWEpIiwxXV0=

また上とは別のしかたで、$\eta\ast\sigma : G \circ F \Rightarrow G' \circ F'$と$\theta\ast\tau : G' \circ F' \Rightarrow G'' \circ F''$の垂直合成$(\theta\ast\tau)\circ(\eta\ast\sigma): F \circ G \to F'' \circ G''$を見つけることができる。
ちょうど可換図式を斜めに横断する射だ。

![(theta * tau) . (eta * sigma)](https://storage.googleapis.com/zenn-user-upload/7feb4a3adaf5-20231203.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBFIl0sWzAsMSwiRyhGKEMpKSJdLFswLDIsIkcnKEYoQykpIl0sWzEsMSwiRyhGJyhDKSkiXSxbMSwyLCJHJyhGJyhDKSkiXSxbMiwyLCJHJyhGJycoQykpIl0sWzEsMywiRycnKEYnKEMpKSJdLFsyLDMsIkcnJyhGJycoQykpIl0sWzEsMywiRyhcXHNpZ21hX0MpIl0sWzEsMiwiXFxldGFfe0YoQyl9IiwyXSxbMiw0LCJHJyhcXHNpZ21hX0MpIiwyXSxbMyw0LCJcXGV0YV97RicoQyl9Il0sWzQsNSwiRycoXFx0YXVfe0N9KSJdLFs0LDYsIlxcdGhldGFfe0YnKEMpfSIsMl0sWzUsNywiXFx0aGV0YV97RicnKEMpfSJdLFs2LDcsIkcnJyhcXHRhdV9DKSIsMl0sWzEsNCwiXFxldGEgXFxhc3QgXFxzaWdtYSIsMV0sWzQsNywiXFx0aGV0YSBcXGFzdCBcXHRhdSIsMV1d

これら二つの合成は、以下のように可換図式にまとめることができる。よって自然変換の自然性により、これら二つの合成は等しいことが証明できた。

![interchange_law](https://storage.googleapis.com/zenn-user-upload/aaeb85a4b337-20231203.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgRSJdLFswLDEsIkcoRihDKSkiXSxbMCwyLCJHJyhGKEMpKSJdLFsxLDEsIkcoRicoQykpIl0sWzEsMiwiRycoRicoQykpIl0sWzIsMiwiRycoRicnKEMpKSJdLFsxLDMsIkcnJyhGJyhDKSkiXSxbMiwzLCJHJycoRicnKEMpKSJdLFswLDMsIkcnJyhGKEMpKSJdLFsyLDEsIkcoRicnKEMpKSJdLFsxLDMsIkcoXFxzaWdtYV9DKSJdLFsxLDIsIlxcZXRhX3tGKEMpfSIsMl0sWzIsNCwiRycoXFxzaWdtYV9DKSIsMl0sWzMsNCwiXFxldGFfe0YnKEMpfSJdLFs0LDUsIkcnKFxcdGF1X3tDfSkiXSxbNCw2LCJcXHRoZXRhX3tGJyhDKX0iLDJdLFs1LDcsIlxcdGhldGFfe0YnJyhDKX0iXSxbNiw3LCJHJycoXFx0YXVfQykiLDJdLFsxLDQsIlxcZXRhIFxcYXN0IFxcc2lnbWEiLDFdLFs0LDcsIlxcdGhldGEgXFxhc3QgXFx0YXUiLDFdLFsyLDgsIlxcdGhldGFfe0YoQyl9IiwyXSxbOCw2LCJHJycoXFxzaWdtYV9DKSIsMl0sWzMsOSwiRyhcXHRhdV9DKSJdLFs5LDUsIlxcZXRhX3tGJycoQyl9Il1d

## 恒等な自然変換

関手$F: \mathbf C \to \mathbf D$に対する恒等な自然変換とは、圏$\mathbf C$の任意の対象$X$に対する自然変換$\iota_X$が$F(X)$の恒等射$id_{F(X)}$に等しいような自然変換のことであり、$1_F$と書く。

![identity_transformation](https://storage.googleapis.com/zenn-user-upload/af0e92ef58b2-20231022.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbMywwLCJEIl0sWzMsMSwiRihBKSJdLFs0LDEsIkYoQikiXSxbMywyLCJGKEEpIl0sWzQsMiwiRihCKSJdLFsxLDIsImYiXSxbNCw1LCJGKGYpIl0sWzYsNywiRihmKSIsMl0sWzQsNiwiXFxpb3RhX0EgPSBpZF97RihBKX0iLDJdLFs1LDcsIlxcaW90YV9CID0gaWRfe0YoQil9Il1d

## 自然変換のひし形合成

典型的な自然変換の合成として、ひし形の合成がある。
（これは私がそう呼んでいるだけなので、より一般的な名前があったらそちらを採用したい）

次の登場人物を用意する。

- 圏 $\mathbf A$, $\mathbf B$, $\mathbf C$, $\mathbf D$
- 関手
    - $F: \mathbf A \to \mathbf B$
    - $G: \mathbf B \to \mathbf C$
    - $H: \mathbf A \to \mathbf C$
    - $K: \mathbf C \to \mathbf K$
    - $L: \mathbf B \to \mathbf D$
- 自然変換
    - $\epsilon: H \Rightarrow G \circ F$
    - $\eta: K \circ G \Rightarrow L$

文字で書いても分かりづらいので、図で書くと次の通りだ。

![diamond_nats](https://storage.googleapis.com/zenn-user-upload/375cca73ca84-20231204.png)

このとき$\epsilon: H \Rightarrow G \circ F$と$\eta: K \circ G \Rightarrow L$を次のように合成することができる。

$$
(\eta \ast F) \circ (K \ast \epsilon):K \circ H \Rightarrow L \circ F
$$

![diamond_composition](https://storage.googleapis.com/zenn-user-upload/38013cf80c29-20231205.png)

https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZiBBIl0sWzEsMSwiXFxtYXRoYmYgQiJdLFsyLDAsIlxcbWF0aGJmIEMiXSxbMywxLCJcXG1hdGhiZiBEIl0sWzAsMiwiQSJdLFszLDMsIkQiXSxbMCwxLCJGIiwyXSxbMSwyLCJHIiwyXSxbMCwyLCJIIl0sWzIsMywiSyJdLFsxLDMsIkwiLDJdLFs0LDUsIksgXFxjaXJjIEgiLDAseyJjdXJ2ZSI6LTN9XSxbNCw1LCJMIFxcY2lyYyBGIiwyLHsiY3VydmUiOjN9XSxbOCwxLCJcXGVwc2lsb24iLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV0sWzIsMTAsIlxcZXRhIiwwLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFsxMSwxMiwiKFxcZXRhIFxcYXN0IEYpIFxcY2lyYyBLIFxcYXN0IFxcZXBzaWxvbiIsMCx7ImxhYmVsX3Bvc2l0aW9uIjozMCwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==

このとき、以下を可換にする。

![diamond_composition_commutative](https://storage.googleapis.com/zenn-user-upload/474c50eedcea-20231205.png)

https://q.uiver.app/#q=WzAsMTMsWzAsMSwiXFxtYXRoYmYgQSJdLFsxLDIsIlxcbWF0aGJmIEIiXSxbMiwxLCJcXG1hdGhiZiBDIl0sWzMsMiwiXFxtYXRoYmYgRCJdLFswLDMsIkEiXSxbMyw0LCJEIl0sWzUsMCwiXFxtYXRoYmYgQSJdLFs1LDEsIkEiXSxbNiwxLCJBJyJdLFs4LDAsIlxcbWF0aGJmIEQiXSxbOCwxLCJLKEgoQSkpIl0sWzksMiwiTChGKEEpKSJdLFs4LDIsIksoRyhGKEEpKSkiXSxbMCwxLCJGIiwyXSxbMSwyLCJHIiwyXSxbMCwyLCJIIl0sWzIsMywiSyJdLFsxLDMsIkwiLDJdLFs0LDUsIksgXFxjaXJjIEgiLDAseyJjdXJ2ZSI6LTN9XSxbNCw1LCJMIFxcY2lyYyBGIiwyLHsiY3VydmUiOjN9XSxbNyw4LCJmIl0sWzEwLDEyLCJLKFxcZXBzaWxvbl9BKSIsMl0sWzEyLDExLCJcXGV0YV97RihBKX0iLDJdLFsxMCwxMSwiKChcXGV0YSBcXGFzdCBGKSBcXGNpcmMgKEsgXFxhc3QgXFxlcHNpbG9uKSlfQSIsMCx7ImxhYmVsX3Bvc2l0aW9uIjoxMDB9XSxbMTUsMSwiXFxlcHNpbG9uIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwfX1dLFsyLDE3LCJcXGV0YSIsMCx7InNob3J0ZW4iOnsidGFyZ2V0IjoyMH19XSxbMTgsMTksIlxcZXRhIFxcY2lyYyBcXGVwc2lsb24iLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV1d

直感的な図を描くと、次のような感じだ。

![diamond_composition_diagram](https://storage.googleapis.com/zenn-user-upload/a7cb3fc270b8-20231205.png)

自然変換の向きを逆転しても、同様に合成することができる。

すなわち（圏や関手は上のものと同じものを使って）以下の自然変換を考える。

- $\epsilon: G \circ F \Rightarrow H$
- $\eta: L \Rightarrow K \circ G$

![reversed_diamond_nats](https://storage.googleapis.com/zenn-user-upload/311beb693b51-20231205.png)

ここから合成$(K \ast \epsilon) \circ (\eta \ast F): L \circ F \Rightarrow K \circ H$を得られる。

![reversed_diamond_composition](https://storage.googleapis.com/zenn-user-upload/885bfdc576b3-20231205.png)

https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZiBBIl0sWzEsMSwiXFxtYXRoYmYgQiJdLFsyLDAsIlxcbWF0aGJmIEMiXSxbMywxLCJcXG1hdGhiZiBEIl0sWzAsMiwiQSJdLFszLDMsIkQiXSxbMCwxLCJGIiwyXSxbMSwyLCJHIiwyXSxbMCwyLCJIIl0sWzIsMywiSyJdLFsxLDMsIkwiLDJdLFs0LDUsIksgXFxjaXJjIEgiLDAseyJjdXJ2ZSI6LTN9XSxbNCw1LCJMIFxcY2lyYyBGIiwyLHsiY3VydmUiOjN9XSxbMTAsMiwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV0sWzEsOCwiXFxlcHNpbG9uIiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFsxMiwxMSwiXFxldGEgXFxhc3QgXFxlcHNpbG9uIiwyLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==

このとき、以下を可換にする。

![diamond_composition_commutative2](https://storage.googleapis.com/zenn-user-upload/36803ea7041d-20231205.png)

https://q.uiver.app/#q=WzAsMTMsWzAsMSwiXFxtYXRoYmYgQSJdLFsxLDIsIlxcbWF0aGJmIEIiXSxbMiwxLCJcXG1hdGhiZiBDIl0sWzMsMiwiXFxtYXRoYmYgRCJdLFswLDMsIkEiXSxbMyw0LCJEIl0sWzUsMCwiXFxtYXRoYmYgQSJdLFs1LDEsIkEiXSxbNiwxLCJBJyJdLFs4LDAsIlxcbWF0aGJmIEQiXSxbOCwxLCJLKEgoQSkpIl0sWzgsMiwiSyhHKEYoQSkpKSJdLFs5LDIsIkwoRihBKSkiXSxbMCwxLCJGIiwyXSxbMSwyLCJHIiwyXSxbMCwyLCJIIl0sWzIsMywiSyJdLFsxLDMsIkwiLDJdLFs0LDUsIksgXFxjaXJjIEgiLDAseyJjdXJ2ZSI6LTN9XSxbNCw1LCJMIFxcY2lyYyBGIiwyLHsiY3VydmUiOjN9XSxbNyw4LCJmIl0sWzExLDEwLCJLKFxcZXBzaWxvbl9BKSJdLFsxMiwxMSwiXFxldGFfe0YoQSl9Il0sWzEyLDEwLCIoKEsgXFxhc3QgXFxlcHNpbG9uKSBcXGNpcmMgKFxcZXRhIFxcYXN0IEYpKV9BIiwyLHsibGFiZWxfcG9zaXRpb24iOjB9XSxbMTcsMiwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV0sWzEsMTUsIlxcZXBzaWxvbiIsMix7InNob3J0ZW4iOnsidGFyZ2V0IjoyMH19XSxbMTksMTgsIihLIFxcYXN0IFxcZXBzaWxvbikgXFxjaXJjIChcXGV0YSBcXGFzdCBGKSIsMix7ImxhYmVsX3Bvc2l0aW9uIjo3MCwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==

直感的な図を描くと、次のような感じだ。

![diamond_composition_diagram2](https://storage.googleapis.com/zenn-user-upload/cdb2e49f89ea-20231205.png)
