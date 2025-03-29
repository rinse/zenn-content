---
title: "極限はKan拡張である"
free: false
---

## 定理

$G : \mathbf{C} \to \mathbf{D}$ の $F : \mathbf{1} \to \mathbf{D}$ に沿った右Kan拡張が存在するとき、圏$\mathbf{D}$において$G$の極限$\lang \varprojlim_{c \in \mathbf{C}} G(C), \eta \rang$が存在する。

[![](https://storage.googleapis.com/zenn-user-upload/ecf0a4f8b1f5-20250303.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiXFxtYXRoYmZ7Q30iXSxbMSwyLCJcXG1hdGhiZntEfSJdLFswLDIsIlxcbWF0aGJmezF9Il0sWzEsMiwiRyJdLFsxLDMsIkYiLDJdLFszLDIsIlIiLDJdLFs2LDQsIlxcZXRhIiwwLHsib2Zmc2V0IjotMiwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfSwiZWRnZV9hbGlnbm1lbnQiOnsic291cmNlIjpmYWxzZSwidGFyZ2V0IjpmYWxzZX19XV0=)

[![](https://storage.googleapis.com/zenn-user-upload/57a9fb12aadc-20250329.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbNCwzLCJHKEIpIl0sWzIsMywiRyhBKSJdLFszLDIsIkwiXSxbMywxLCJYIl0sWzEsMiwiZiJdLFs1LDQsIkcoZikiLDJdLFs2LDUsIlxcZXRhX0EiLDJdLFs2LDQsIlxcZXRhX0IiXSxbNSw0LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6LTUsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs3LDYsIlxcdGF1X1xcYXN0IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzcsNSwiXFx0aGV0YV9BIiwyLHsiY3VydmUiOjF9XSxbNyw0LCJcXHRoZXRhX0IiLDAseyJjdXJ2ZSI6LTF9XV0=)

## 証明

圏$\mathbf{C}$が適当な構造を備えているとして、$\mathbf{C}$を関手$R \circ F$と$G$によって圏$\mathbf{D}$に写すと、次の可換図式を書ける。

[![](https://storage.googleapis.com/zenn-user-upload/549bc66e4ea9-20250329.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMiwxLCJSKEYoQSkpIl0sWzMsMSwiUihGKEIpKSJdLFszLDIsIkcoQikiXSxbMiwyLCJHKEEpIl0sWzEsMiwiZiJdLFs0LDUsIlIoRihmKSkiXSxbNSw2LCJcXGV0YV9CIl0sWzQsNywiXFxldGFfQSIsMl0sWzcsNiwiRyhmKSIsMl0sWzQsNiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

ここで$F$は$\mathbf{C} \to \mathbf{1}$への関手であり、離散圏$\mathbf{1}$は対象が$\ast$, 射が$\mathrm{id}_\ast : \ast \to \ast$しかない圏であるから、$R(F(A)) = R(F(B)) = R(\ast)$かつ$R(F(f)) = R(\mathrm{id}_\ast)$が成り立つ。

よって$R \circ F$は定関手である。$R \circ F : \mathbf{C} \to \mathbf{D}$が任意の対象$C$を移す先の対象を$L$としたとき、上図は下のように整理できる。

[![](https://storage.googleapis.com/zenn-user-upload/eb9d95e4ad00-20250329.png)](https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbNCwzLCJHKEIpIl0sWzIsMywiRyhBKSJdLFszLDIsIkwiXSxbMSwyLCJmIl0sWzUsNCwiRyhmKSIsMl0sWzYsNSwiXFxldGFfQSIsMl0sWzYsNCwiXFxldGFfQiJdLFs1LDQsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsib2Zmc2V0IjotNSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

Kan拡張の普遍性により、別の関手$S : \mathbf{1} \to \mathbf{D}$と自然変換$\theta : S \circ F \Rightarrow G$があったとき、自然変換$\tau : R \Rightarrow S$が一意に存在して、$\theta = \eta \circ (\tau \ast F)$ を満たすのであった。

![](https://storage.googleapis.com/zenn-user-upload/8ba1d0f87661-20250303.png)

これを先ほどの図式に圏$\mathbf{D}$の図式に書き加えると、次のようになる。

なお$X$は任意の対象$C \in \mathrm{ob}(\mathbf{C})$を$S \circ F$で移したものであり、$\tau_\ast$は$\tau_{F(C)}$に一致する。

[![](https://storage.googleapis.com/zenn-user-upload/dbbd464226d5-20250329.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbNCwzLCJHKEIpIl0sWzIsMywiRyhBKSJdLFszLDIsIkwiXSxbMywxLCJYIl0sWzEsMiwiZiJdLFs1LDQsIkcoZikiLDJdLFs2LDUsIlxcZXRhX0EiLDJdLFs2LDQsIlxcZXRhX0IiXSxbNSw0LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6LTUsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs3LDYsIlxcdGF1X1xcYXN0IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzcsNSwiXFx0aGV0YV9BIiwyLHsiY3VydmUiOjF9XSxbNyw0LCJcXHRoZXRhX0IiLDAseyJjdXJ2ZSI6LTF9XV0=)

これは極限の定義に一致するため、$\lang L, \eta \rang$は極限である。
このとき$L$は任意の$C \in \mathrm{ob}(\mathbf{C})$が移る先として仮に置いたものだったので、$\varprojlim_{c \in \mathbf{C}} G_C$と書いたほうがわかりやすいかもしれない。（[極限の記法](./limit#記法)を参照）
