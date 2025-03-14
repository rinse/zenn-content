---
title: "随伴はモナドを導く"
free: false
---

## 定理

関手$F : \mathbf{D} \to \mathbf{C}$, $G : \mathbf{C} \to \mathbf{D}$を考える。

これらが随伴$F \dashv G$であるとき、すなわち$\hom_C(F(\_), \_) \simeq hom_D(\_, G(\_))$であるとき、自然変換$\epsilon: 1_C \Rightarrow F \circ G$と$\eta: 1_D \Rightarrow G \circ F$が存在するのだった。

このとき、3つ組$(G \circ F, \eta, G \ast \epsilon \ast F)$は圏$\mathbf{D}$上の[モナド](./monad)を構成する。（なお一般に圏$\mathbf{C}$上のモナドとは、関手$T: \mathbf{C} \to \mathbf{C}$と自然変換$\eta: 1_\mathbf{C} \to T$, $\mu: T^2 \to T$から成る3つ組$(T, \eta, \mu)$である）

[![](https://storage.googleapis.com/zenn-user-upload/128044d55b13-20250218.png)](https://q.uiver.app/#q=WzAsMTgsWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDIsIkMiXSxbMSwyLCJDJyJdLFsyLDEsIkQiXSxbMywxLCJEJyJdLFswLDEsIkYoRyhDKSkiXSxbMSwxLCJGKEcoQycpKSJdLFsyLDIsIkcoRihEKSkiXSxbMywyLCJHKEYoRCcpKSJdLFsyLDMsIkcoRihHKEYoRCkpKSkiXSxbMiw0LCJHKEYoRCkpIl0sWzMsMywiRyhGKEcoRihEJykpKSkiXSxbMCwzLCJGKEcoRihEKSkpIl0sWzEsMywiRihHKEYoRCcpKSJdLFswLDQsIkYoRCkiXSxbMSw0LCJGKEQnKSJdLFszLDQsIkcoRihEJykpIl0sWzIsMywiYyIsMl0sWzYsMiwiXFxlcHNpbG9uX2MiLDJdLFs3LDMsIlxcZXBzaWxvbl97Yyd9Il0sWzYsNywiRihHKGMpKSJdLFs4LDksIkcoRihkKSkiLDJdLFs0LDgsIlxcZXRhX0QiLDJdLFs0LDksIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzYsMywiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTAsMTEsIkcoXFxlcHNpbG9uX3tGKEQpfSkiLDJdLFs5LDEyLCJcXGV0YV97RyhGKEQnKSl9Il0sWzEzLDE0LCJGKEcoRihkKSkpIl0sWzEzLDE1LCJcXGVwc2lsb25fe0YoRCl9IiwyXSxbMTQsMTYsIlxcZXBzaWxvbl97RihEJyl9Il0sWzE1LDE2LCJGKGQpIiwyXSxbMTMsMTYsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzEwLDEyXSxbMTEsMTcsIkcoRihkKSkiLDJdLFsxMiwxNywiRyhcXGVwc2lsb25fe0YoRCcpfSkiXSxbOCwxMiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTAsMTcsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzgsMTAsIlxcZXRhX3tHKEYoRCkpfSIsMl0sWzUsOSwiXFxldGFfe0QnfSJdLFs0LDUsImQiXSxbMCwxLCJGIiwyLHsib2Zmc2V0IjoyfV0sWzEsMCwiRyIsMix7Im9mZnNldCI6Mn1dLFs0MSw0MiwiIiwyLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJhZGp1bmN0aW9uIn19XV0=)

同様に、3つ組$(F \circ G, \epsilon, F \ast \eta \ast G)$は圏$\mathbf{C}$上のコモナドである。

[![](https://storage.googleapis.com/zenn-user-upload/d8159d13084b-20250218.png)](https://q.uiver.app/#q=WzAsMTgsWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDQsIkMiXSxbMSw0LCJDJyJdLFsyLDEsIkQiXSxbMywxLCJEJyJdLFswLDMsIkYoRyhDKSkiXSxbMSwzLCJGKEcoQycpKSJdLFsyLDIsIkcoRihEKSkiXSxbMywyLCJHKEYoRCcpKSJdLFswLDIsIkYoRyhGKEcoQykpKSkiXSxbMCwxLCJGKEcoQykpIl0sWzEsMSwiRihHKEMnKSkiXSxbMSwyLCJGKEcoRihHKEMnKSkpKSJdLFsyLDMsIkcoQykiXSxbMiw0LCJHKEYoRyhDKSkpIl0sWzMsMywiRyhDJykiXSxbMyw0LCJHKEYoRyhDJykpKSJdLFsyLDMsImMiLDJdLFs2LDIsIlxcZXBzaWxvbl9jIiwyXSxbNywzLCJcXGVwc2lsb25fe2MnfSJdLFs2LDcsIkYoRyhjKSkiXSxbOCw5LCJHKEYoZCkpIiwyXSxbNCw4LCJcXGV0YV9EIiwyXSxbNCw5LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs2LDMsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzUsOSwiXFxldGFfe0QnfSJdLFs0LDUsImQiXSxbMCwxLCJGIiwyLHsib2Zmc2V0IjoyfV0sWzEsMCwiRyIsMix7Im9mZnNldCI6Mn1dLFsxMCw2LCJcXGVwc2lsb25fe0YoRyhjKSl9IiwyXSxbMTMsNywiXFxlcHNpbG9uX3tGKEcoYycpKX0iXSxbMTAsMTNdLFsxMSwxMCwiRihcXGV0YV97RyhDKX0pIiwyXSxbMTIsMTMsIkYoXFxldGFfe0coQycpfSkiXSxbMTEsMTIsIkYoRyhjKSkiXSxbMTYsMTcsIlxcZXRhX3tHKEMnKX0iXSxbMTQsMTUsIlxcZXRhX3tHKEMpfSIsMl0sWzE0LDE2LCJHKGMpIl0sWzE1LDE3XSxbMTQsMTcsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzExLDEzLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxMCw3LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsyOCwyOSwiIiwyLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJhZGp1bmN0aW9uIn19XV0=)

## 証明

3つ組$(G \circ F, \eta, G \ast \epsilon \ast F)$が圏$\mathbf{D}$上のモナドであることを示す。

圏$\mathbf{C}$上のモナドとは、関手$T: \mathbf{C} \to \mathbf{C}$と自然変換$\eta: 1_\mathbf{C} \to T$, $\mu: T^2 \to T$から成る3つ組$(T, \eta, \mu)$であって、$\mu \circ (\mu \ast T) = \mu \circ (T \ast \mu)$かつ$\mu \circ (\eta \ast T) = \mu \circ (T \ast \eta) = 1_T$を満たすものをいうのであった。

[![](https://storage.googleapis.com/zenn-user-upload/28e00b789c02-20250218.png)](https://q.uiver.app/#q=WzAsOSxbMCwxLCJUXjMiXSxbMSwxLCJUXjIiXSxbMCwyLCJUXjIiXSxbMSwyLCJUIl0sWzAsMCwiXFxtYXRoYmZ7Q31ee1xcbWF0aGJme0N9fSJdLFsyLDEsIlQiXSxbMywxLCJUXjIiXSxbMiwyLCJUXjIiXSxbMywyLCJUIl0sWzEsMywiXFxtdSJdLFsyLDMsIlxcbXUiLDJdLFswLDIsIlQgXFxhc3QgXFxtdSIsMl0sWzAsMSwiXFxtdSBcXGFzdCBUIl0sWzUsNiwiXFxldGEgXFxhc3QgVCJdLFs1LDcsIlQgXFxhc3QgXFxldGEiLDJdLFs2LDgsIlxcbXUiXSxbNSw4LCIxX1QiLDFdLFs3LDgsIlxcbXUiLDJdLFswLDMsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

まずは左側の図の可換性を示そう。式で書くと次の通りとなるが、これは$\epsilon$をどの順序で合成しても結果が変わらないことを要求している。

$$
(G \ast \epsilon \ast F) \circ ((G \ast \epsilon \ast F) \ast (G \circ F)) = (G \ast \epsilon \ast F) \circ ((G \circ F) \ast (G \ast \epsilon \ast F))
$$

これは任意の対象$D$について以下の図式が可換になるのと同値である。

![](https://storage.googleapis.com/zenn-user-upload/0257d48398ce-20250220.png)

簡単のために$G$を外して、$F(D)$を$C \in \mathrm{ob}(\mathbf{C})$で置き換えよう。（関手の定義より、関手を外しても可換性は保たれる）

そうすれば、圏$\mathbf{C}$上で次の可換図式を示せればよいことになる。

![](https://storage.googleapis.com/zenn-user-upload/cd43ceef34eb-20250220.png)

関手の定義より、圏$\mathbf{C}$の任意の射$f : F(G(C)) \to C$について以下の可換図式が成り立つ。

![](https://storage.googleapis.com/zenn-user-upload/0147fe3d884e-20250220.png)

自然変換の定義より、圏$\mathbf{C}$の任意の射$f : F(G(C)) \to C$について以下の可換図式が成り立つ。

![](https://storage.googleapis.com/zenn-user-upload/0aff46c739c2-20250220.png)

すなわち圏$\mathbf{C}$の任意の射$f : F(G(C)) \to C$に対して、$\epsilon_C \circ F(G(f)) = f \circ F(G(\epsilon_C))$かつ$\epsilon_C \circ F(G(f)) = f \circ \epsilon_{F(G(C))}$であるから、$f \circ F(G(\epsilon_C)) = f \circ \epsilon_{F(G(C))}$が成り立つ。

そしてこれは$f$が$\epsilon_C : F(G(C)) \to C$の場合にも成り立つから、これで左側の図式の可換性を示すことができた。

https://q.uiver.app/#q=WzAsMjksWzAsMSwiKEcgXFxjaXJjIEYpXjMiXSxbMSwxLCIoRyBcXGNpcmMgRileMiJdLFswLDIsIihHIFxcY2lyYyBGKV4yIl0sWzEsMiwiKEcgXFxjaXJjIEYpIl0sWzAsMCwiXFxtYXRoYmZ7RH1eXFxtYXRoYmZ7RH0iXSxbMCwzLCJGIl0sWzEsMywiRiJdLFswLDQsIkciXSxbMSw0LCJHIl0sWzMsMCwiXFxtYXRoYmZ7RH0iXSxbMywxLCJHKEYoRyhGKEcoRihEKSkpKSkpIl0sWzMsMiwiRyhGKEcoRihEKSkpKSJdLFs0LDIsIkcoRihEKSkiXSxbNSwwLCJcXG1hdGhiZntDfSJdLFs1LDEsIkYoRyhGKEcoQykpKSkiXSxbNSwyLCJGKEcoQykpIl0sWzYsMiwiQyJdLFs4LDEsIkYoRyhDKSkiXSxbOCwyLCJDIl0sWzcsMSwiRihHKEYoRyhDKSkpKSJdLFs3LDIsIkYoRyhDKSkiXSxbNCwxLCJHKEYoRyhGKEQpKSkpIl0sWzYsMSwiRihHKEMpKSJdLFs3LDQsIkYoRyhGKEcoQykpKSkiXSxbNyw1LCJGKEcoQykpIl0sWzcsMCwi6Zai5omL44Gu5a6a576p44KI44KKIl0sWzgsNCwiRihHKEMpKSJdLFs4LDUsIkMiXSxbNywzLCLoh6rnhLblpInmj5vjga7lrprnvqnjgojjgooiXSxbMSwzLCJHIFxcYXN0IFxcZXBzaWxvbiBcXGFzdCBGIl0sWzAsMiwiKEcgXFxjaXJjIEYpIFxcYXN0IChHIFxcYXN0IFxcZXBzaWxvbiBcXGFzdCBGKSIsMl0sWzAsMSwiKEcgXFxhc3QgXFxlcHNpbG9uIFxcYXN0IEYpIFxcYXN0IChHIFxcY2lyYyBGKSJdLFsyLDMsIkcgXFxhc3QgXFxlcHNpbG9uIFxcYXN0IEYiLDJdLFs3LDgsIihHIFxcYXN0IFxcZXBzaWxvbikgXFxjaXJjIChcXGV0YSBcXGFzdCBHKSA9IDFfRyJdLFs1LDYsIihcXGVwc2lsb24gXFxhc3QgRikgXFxjaXJjIChGIFxcYXN0IFxcZXRhKSA9IDFfRiJdLFsxMCwxMSwiRyhGKEcoXFxlcHNpbG9uX3tGKEQpfSkpKSIsMl0sWzExLDEyLCJHKFxcZXBzaWxvbl97RihEKX0pIiwyXSxbMTUsMTYsIlxcZXBzaWxvbl9DIiwyXSxbMTQsMTUsIkYoRyhcXGVwc2lsb25fe0N9KSkiLDJdLFsxNywxOCwiXFxlcHNpbG9uX0MiXSxbMTksMjAsIkYoRyhcXGVwc2lsb25fQykpIiwyXSxbMTksMTcsIkYoRyhmKSkiXSxbMjAsMTgsImYiLDJdLFsyMSwxMiwiRyhcXGVwc2lsb25fe0YoRCl9KSJdLFsxMCwyMSwiRyhcXGVwc2lsb25fe0YoRyhGKEQpKSl9KSJdLFsyMiwxNiwiXFxlcHNpbG9uX0MiXSxbMTQsMjIsIlxcZXBzaWxvbl97RihHKEMpKX0iXSxbMjMsMjQsIlxcZXBzaWxvbl97RihHKEMpKX0iLDJdLFsyMywyNiwiRihHKGYpKSJdLFsyNCwyNywiZiIsMl0sWzI2LDI3LCJcXGVwc2lsb25fQyJdLFsxOSwxOCwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMjMsMjcsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d

次に右側の図の等式を示す。

こちらは式で書くと次のようになる。2つの合成が両辺が$1_{G \circ F}$に等しいことを示そう。

$$
(G \ast \epsilon \ast F) \circ (\eta \ast (G \circ F)) = (G \ast \epsilon \ast F) \circ ((G \circ F) \ast \eta) = 1_{G \circ F}
$$

$(G \ast \epsilon \ast F) \circ (\eta \ast (G \circ F))$について、成分$D$に注目して図に書き起こすと、unit-counit恒等式$(G \ast \epsilon) \circ (\eta \ast G) = 1_G$の特別な場合であることが分かる。つまり$G(\epsilon_{F(D)}) \circ \eta_{G(F(D))} = \mathrm{id}_D$であるから、$(G \ast \epsilon \ast F) \circ (\eta \ast (G \circ F)) = 1_{G \circ F}$であることを確かめられた。

[![](https://storage.googleapis.com/zenn-user-upload/b04ba3d3527d-20250218.png)](https://q.uiver.app/#q=WzAsNyxbMCwxLCJHKEYoRCkpIl0sWzAsMiwiRyhGKEcoRihEKSkpKSJdLFswLDMsIkcoRihEKSkiXSxbMSwxLCJHKEEpIl0sWzEsMiwiRyhGKEcoQSkpKSJdLFsxLDMsIkcoQSkiXSxbMCwwLCJcXG1hdGhiZntEfSJdLFswLDEsIlxcZXRhX3tHKEYoRCkpfSIsMl0sWzEsMiwiRyhcXGVwc2lsb25fe0YoRCl9KSIsMl0sWzMsNCwiXFxldGFfe0coQSl9Il0sWzQsNSwiRyhcXGVwc2lsb25fQSkiXV0=)

次に$(G \ast \epsilon \ast F) \circ ((G \circ F) \ast \eta)$について、成分$D$に注目すると、$G(\epsilon_{F(D)}) \circ G(F(\eta_D))$という射が得られる。unit-counit恒等式によって$\epsilon_{F(D)} \circ F(\eta_D) = 1_F$であるから、これを$G$で送ったこの式は$G(\epsilon_{F(D)}) \circ G(F(\eta_D)) = 1_{G \circ F}$であることが分かる。

[![](https://storage.googleapis.com/zenn-user-upload/c6eb1c293832-20250218.png)](https://q.uiver.app/#q=WzAsOCxbMSwxLCJHKEYoRCkpIl0sWzEsMiwiRyhGKEcoRihEKSkpKSJdLFsxLDMsIkcoRihEKSkiXSxbMSwwLCJcXG1hdGhiZntEfSJdLFswLDAsIlxcbWF0aGJme0N9Il0sWzAsMSwiRihEKSJdLFswLDIsIkYoRyhGKEQpKSkiXSxbMCwzLCJGKEQpIl0sWzAsMSwiRyhGKFxcZXRhX0QpKSJdLFsxLDIsIkcoXFxlcHNpbG9uX3tGKEQpfSkiXSxbNSw2LCJGKFxcZXRhX0QpIiwyXSxbNiw3LCJcXGVwc2lsb25fe0YoRCl9IiwyXV0=)

これで右の図式も可換であることを示すことができた。

証明終わり。
