---
title: "普遍随伴"
free: false
---

[普遍随伴](#用語)とは、圏論で最も重要な定理のひとつである。

## 定理

[各点左Kan拡張](./pointwise-kan-extension)であるような$F$の[米田拡張](./yoneda-extension)を考える。（すなわち$\mathbf{U}$は余完備）

[![](https://storage.googleapis.com/zenn-user-upload/c0c7c7bcc266-20250315.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIlxcbWF0aGJme1V9Il0sWzAsMSwiXFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fSJdLFswLDEsIkYiXSxbMCwyLCJIXy0iLDJdLFsyLDEsIlxcbWF0aHJte0xhbn1fe0hfLX0gRiIsMl0sWzMsNSwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dXQ==)

このとき、$\mathrm{Lan}_{H_-} F : \mathbf{Set}^{\mathbf{C}^\mathrm{op}} \to \mathbf{U}$とは逆向きの、$F$に沿った[米田埋め込み](./yoneda-embedding)の各点左Kan拡張$\mathrm{Lan}_F H_- : \mathbf{U} \to \mathbf{Set}^{\mathbf{C}^\mathrm{op}}$が存在する。（$\mathbf{Set}^{\mathbf{C}^\mathrm{op}}$は余完備）

[![](https://storage.googleapis.com/zenn-user-upload/af7e137b05a5-20250315.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIlxcbWF0aGJme1V9Il0sWzEsMSwiXFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fSJdLFswLDEsIkYiLDJdLFswLDIsIkhfLSJdLFsxLDIsIlxcbWF0aHJte0xhbn1fRiBIXy0iLDJdLFs0LDUsIlxcZXBzaWxvbiIsMix7Im9mZnNldCI6Miwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfSwiZWRnZV9hbGlnbm1lbnQiOnsic291cmNlIjpmYWxzZSwidGFyZ2V0IjpmYWxzZX19XV0=)

この二つは随伴関手であり、すなわち以下が成り立つ。

$$
\mathrm{Lan}_{H_-} F \dashv \mathrm{Lan}_F H_-
$$

ひとつの三角形にまとめると、次のような図になる。

[![](https://storage.googleapis.com/zenn-user-upload/dbcd31c0b38e-20250315.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFsyLDIsIlxcbWF0aGJme1V9Il0sWzAsMiwiXFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fSJdLFswLDEsIkYiXSxbMCwyLCJIXy0iLDJdLFsxLDIsIlxcbWF0aHJte0xhbn1fRiBIXy0iLDIseyJjdXJ2ZSI6MX1dLFsyLDEsIlxcbWF0aHJte0xhbn1fe0hfLX0gRiIsMix7ImN1cnZlIjoxfV0sWzYsNSwiIiwyLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJhZGp1bmN0aW9uIn19XV0=)

### 証明

$\mathrm{Lan}_{H_-}$は各点左Kan拡張であるから、[定理](./pointwise-kan-extension#定理2)より$P \in \mathrm{ob}(\mathbf{Set}^{\mathbf{C}^\mathrm{op}})$, $U \in \mathrm{ob}(\mathbf{U})$について自然に以下が成り立つ。

$$
\hom_U(\mathrm{Lan}_{H_-} F(P), U) \simeq \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(\hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(H_-(\_), P), \hom_U(F(\_), U))
$$

米田の補題より $\hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(H_-(\_), P) \simeq P$、[米田埋め込みのKan拡張の定理](./kan-extension-of-yoneda-embedding#定理)により$\hom_U(F(\_), U) \simeq \mathrm{Lan}_F H_-(U)$が成り立つから、以下のように式を変形できる。

$$
\hom_U(\mathrm{Lan}_{H_-} F(P), U) \simeq \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(P, \mathrm{Lan}_F H_-(U))
$$

上の式より、$\mathrm{Lan}_{H_-} F$が$\mathrm{Lan}_F H_-$の左随伴であることが証明できた。

## 定理2

普遍随伴は逆も成り立つ。

すなわち随伴$L \dashv R : \mathbf{Set}^{\mathbf{C}^\mathrm{op}} \to \mathbf{U}$が成り立つとき、関手$E : \mathbf{C} \to \mathbf{U}$が存在して、$\mathrm{Lan}_{H_-} E \simeq L, \mathrm{Lan}_E H_- \simeq R$ が成り立つ。

### 証明

TODO

左随伴関手は左Kan拡張と交換する。

$L \circ (\mathrm{Lan}_F G) \simeq \mathrm{Lan}_F (L \circ G)$

## 用語

普遍随伴の用語は、alg-dさんの動画から拝借したもの。
動画でも触れられている通り、nlabでは [nerve and realization](https://ncatlab.org/nlab/show/nerve+and+realization) という題になっている。

https://www.youtube.com/watch?v=AVFoFxn3rjg
