---
title: "随伴関手3"
free: false
---

随伴関手を普遍射を用いて定義する。

## 普遍射の復習

圏$\mathbf D$の対象$A$から$F$への普遍射は、$\mathbf C$の対象$X$と$\mathbf D$の射$u: A \to F(X)$からなる対$(X, u)$で表され、以下の普遍性を満たす。

- $Y$が$\mathbf C$の対象で$f: A \to F(Y)$が$\mathbf D$の射であるような場合、常に$\mathbf C$の射$g: X \to Y$が一意に存在して、次の図を可換にする

![universal_morphism](https://storage.googleapis.com/zenn-user-upload/eab04eeb7094-20231023.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMSwiQSJdLFszLDEsIkYoWCkiXSxbMywyLCJGKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzQsMCwiQSJdLFs1LDAsIkYiXSxbMiwzLCJGKGcpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEsMywiZiIsMl0sWzUsNiwiZyIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxLDIsInUiXSxbNyw4LCLmma7pgY3lsIQiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=

## 定義

圏$\mathbf C$, $\mathbf D$, 関手$F: \mathbf D \to \mathbf C$, $G: \mathbf C \to \mathbf D$を考える。

圏$\mathbf D$の任意の対象$X$に対して、$X$から$G$への普遍射$(F(X), \eta_X)$が与えられたとする。このとき、$G$は$F$の右随伴関手である。

![definition](https://storage.googleapis.com/zenn-user-upload/ac241b1c5db0-20231210.png)

https://q.uiver.app/#q=WzAsOSxbMCwyLCJGKFkpIl0sWzAsMCwiWCJdLFsxLDAsIkciXSxbMiwyLCJZIl0sWzMsMiwiRyhGKFkpKSJdLFszLDMsIkcoRihZJykpIl0sWzAsMywiRihZJykiXSxbMCwxLCJcXG1hdGhiZiBDIl0sWzIsMSwiXFxtYXRoYmYgRCJdLFsxLDIsIuaZrumBjeWwhChGKFgpLCBcXGV0YV9YKSJdLFszLDQsIlxcZXRhX1kiXSxbMCw2LCJnIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzQsNSwiRyhnKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFszLDUsImQiLDJdXQ==

## 証明

圏$\mathbf D$の射$f: Y \to Y'$を考える。このとき$(F(Y), \eta_Y)$は普遍射であるから、射$\eta_{Y'} \circ f$を分解する一意な射$g: A \to B$を得る。
すなわち以下の図式が可換となる。

![f_Y2Y'](https://storage.googleapis.com/zenn-user-upload/6c36b9fb1f8f-20231210.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMSwiRihBKSJdLFs1LDAsIkEiXSxbNiwwLCJHIl0sWzIsMSwiQSJdLFszLDEsIkcoRihBKSkiXSxbMywyLCJHKEYoQikpIl0sWzAsMiwiRihCKSJdLFsyLDIsIkIiXSxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFsxLDIsIuaZrumBjeWwhChGKEEpLCBcXGV0YV9BKSJdLFszLDQsIlxcZXRhX0EiXSxbMCw2LCJnIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzQsNSwiRyhnKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs3LDUsIlxcZXRhX0IiLDJdLFszLDcsImYiLDJdXQ==

上で示された可換性より、以下が示唆される:

- $F$, $G$は関手なので、可換性より$g = F(f)$
- 可換性の示す自然性により、$\eta$は$1_D \Rightarrow G \circ F$であるような自然変換

可換図式を整理する。

![g_is_Ff](https://storage.googleapis.com/zenn-user-upload/5895263719e5-20231210.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMiwiRihZKSJdLFswLDAsIlgiXSxbMSwwLCJHIl0sWzIsMiwiWSJdLFszLDIsIkcoRihZKSkiXSxbMywzLCJHKEYoWScpKSJdLFswLDMsIkYoWScpIl0sWzIsMywiWSciXSxbMCwxLCJcXG1hdGhiZiBDIl0sWzIsMSwiXFxtYXRoYmYgRCJdLFsxLDIsIuaZrumBjeWwhChGKFgpLCBcXGV0YV9YKSJdLFszLDQsIlxcZXRhX1kiXSxbMCw2LCJGKGYpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzQsNSwiRyhGKGYpKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs3LDUsIlxcZXRhX3tZJ30iLDJdLFszLDcsImYiLDJdXQ==

次に、自然変換$\Phi: \hom_C(F(\_), \_) \Rightarrow \hom_D(\_, G(\_))$を考える。

圏$\mathbf{Set}$上の射$\Phi_{Y', X}: \hom_C(F(Y'), X) \to \hom_D(Y', G(X))$は、圏$\mathbf C$上の射$F(Y') \to X$を圏$\mathbf D$上の射$Y' \to G(X)$に写す写像である。
これを以下のように定義する。

$$
^\forall X \in \mathbf{C}, ^\forall Y' \in \mathbf{D},
\Phi_{Y', X} \overset{\mathrm{def}}{=} \phi \mapsto G(\phi) \circ \eta_{Y'}
$$

![Phi](https://storage.googleapis.com/zenn-user-upload/3be3627240a4-20231210.png)

https://q.uiver.app/#q=WzAsMTgsWzEsMiwiRihZKSJdLFsxLDAsIlgiXSxbMiwwLCJHIl0sWzMsMiwiWSJdLFs0LDIsIkcoRihZKSkiXSxbNCwzLCJHKEYoWScpKSJdLFsxLDMsIkYoWScpIl0sWzMsMywiWSciXSxbMCwxLCJcXG1hdGhiZiBDIl0sWzMsMSwiXFxtYXRoYmYgRCJdLFs0LDQsIkcoWCkiXSxbNiwyLCJcXGhvbV9DKEYoWScpLCBYKSJdLFs3LDIsIlxcaG9tX0MoRihZKSwgWCcpIl0sWzYsMSwiXFxtYXRoYmZ7U2V0fSJdLFs2LDMsIlxcaG9tX0QoWScsIEcoWCkpIl0sWzcsMywiXFxob21fRChZLCBHKFgnKSkiXSxbMCwyLCJYIl0sWzAsMywiWCciXSxbMSwyLCLmma7pgY3lsIQoRihYKSwgXFxldGFfWCkiXSxbMyw0LCJcXGV0YV9ZIl0sWzAsNiwiRihmKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs0LDUsIkcoRihmKSkiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNyw1LCJcXGV0YV97WSd9Il0sWzMsNywiZiIsMl0sWzUsMTAsIkcoXFxwaGkpIl0sWzcsMTAsIkcoXFxwaGkpIFxcY2lyYyBcXGV0YV97WSd9IiwyXSxbMTEsMTIsIlxcaG9tX0MoRihmKSwgeCkiXSxbMTQsMTUsIlxcaG9tX0QoZiwgRyh4KSkiXSxbMTEsMTQsIlxcUGhpX3tZJywgWH0iLDJdLFsxMiwxNSwiXFxQaGlfe1ksIFgnfSJdLFsxNiwxNywieCIsMl0sWzYsMTYsIlxccGhpIiwyXV0=

今度は逆に、自然変換$\Phi': \hom_D(\_, G(\_)) \Rightarrow \hom_C(F(\_), \_)$を考える。

圏$\mathbf{Set}$上の射$\Phi'_{Y', X}: \hom_D(Y', G(X)) \to \hom_C(F(Y'), X)$は、圏$\mathbf D$上の射$Y' \to G(X)$を圏$\mathbf C$上の射$F(Y') \to X$に写す写像である。
これを以下のように定義する。

圏$\mathbf D$の射$\phi: Y' \to G(X)$が与えられたとき、普遍射$(F(Y'), \eta_{Y'})$より得られる、与えられた射$\phi$を$\eta_{Y'}$を通って一意に分解する射$g: F(Y') \to X$に対応させる。

![Phi_inverse](https://storage.googleapis.com/zenn-user-upload/1866f9c0e59e-20231210.png)

https://q.uiver.app/#q=WzAsMTgsWzEsMiwiRihZKSJdLFsxLDAsIlgiXSxbMiwwLCJHIl0sWzMsMiwiWSJdLFs0LDIsIkcoRihZKSkiXSxbNCwzLCJHKEYoWScpKSJdLFsxLDMsIkYoWScpIl0sWzMsMywiWSciXSxbMSwxLCJcXG1hdGhiZiBDIl0sWzMsMSwiXFxtYXRoYmYgRCJdLFs0LDQsIkcoWCkiXSxbNiwyLCJcXGhvbV9DKEYoWScpLCBYKSJdLFs3LDIsIlxcaG9tX0MoRihZKSwgWCcpIl0sWzYsMSwiXFxtYXRoYmZ7U2V0fSJdLFs2LDMsIlxcaG9tX0QoWScsIEcoWCkpIl0sWzcsMywiXFxob21fRChZLCBHKFgnKSkiXSxbMCwyLCJYIl0sWzAsMywiWCciXSxbMSwyLCLmma7pgY3lsIQoRihYKSwgXFxldGFfWCkiXSxbMyw0LCJcXGV0YV9ZIl0sWzAsNiwiRihmKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs0LDUsIkcoRihmKSkiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNyw1LCJcXGV0YV97WSd9Il0sWzMsNywiZiIsMl0sWzUsMTAsIkcoXFxwaGkpIl0sWzcsMTAsIkcoXFxwaGkpIFxcY2lyYyBcXGV0YV97WSd9IiwyXSxbMTEsMTIsIlxcaG9tX0MoRihmKSwgYykiXSxbMTQsMTUsIlxcaG9tX0QoZiwgRyhjKSkiXSxbMTEsMTQsIlxcUGhpX3tZJywgWH0iLDJdLFsxMiwxNSwiXFxQaGlfe1ksIFgnfSJdLFsxNiwxNywiYyJdLFs2LDE2LCJcXHBoaSIsMl1d

ここで$\Phi'_{Y', X}(\Phi_{Y', X}(\phi))$を計算する。

普遍射$(F(Y'), \eta_{Y'})$より与えられる、$G(\phi) \circ \eta_{Y'}$を$\eta_{Y'}$を通って一意に分解する射は自明に$\phi$である。

$$
\begin{align}
\Phi'_{Y', X}(G(\phi) \circ \eta_{Y'}) = \phi
\end{align}
$$

よって以下が成り立つ。

$$
\begin{aligned}
\Phi'_{Y', X}(\Phi_{Y', X}(\phi)) &= \Phi'_{Y', X}(G(\phi) \circ \eta_{Y'}) \\
&= \phi
\end{aligned}
\\
\therefore
\Phi'_{Y', X} \circ \Phi_{Y', X} = \mathrm{id}_{\hom_C(F(Y'), X)}
$$

今度は$\Phi_{Y', X}(\Phi'_{Y', X}(\phi))$を計算する。

$(F(Y'), \eta_{Y'})$は普遍射であるから、以下を満たす圏$\mathbf C$上の射$g: F(Y') \to X$が一意に存在する。

$$
\begin{align}
\phi = G(g) \circ \eta_{Y'}
\end{align}
$$

よって以下が成り立つ。

$$
\begin{aligned}
\Phi_{Y', X}(\Phi'_{Y', X}(\phi)) &= G(\Phi'_{Y', X}(\phi)) \circ \eta_{Y'} \\
&= G(\Phi'_{Y', X}(G(g) \circ \eta_{Y'})) \circ \eta_{Y'} \\
&= G(g) \circ \eta_{Y'} \\
&= \phi
\end{aligned}
\\
\therefore
\Phi_{Y', X} \circ \Phi'_{Y', X} = \mathrm{id}_{\hom_D(Y', G(X))}
$$

以上により、$\Phi_{Y', X}$と$\Phi'{Y', X}$は互いに逆射であるような同型射であることが確認できた。

また下の可換図式により、$\Phi: \hom_C(F(\_), \_) \Rightarrow \hom_C(\_, G(\_))$が圏$\mathbf C$の任意の射$x: X \to X'$, 圏$\mathbf D$の任意の射$f: Y \to Y'$に対して自然であることを確認できる。

![Naturality](https://storage.googleapis.com/zenn-user-upload/0f4e6edf69fc-20231210.png)

https://q.uiver.app/#q=WzAsMTksWzEsMiwiRihZKSJdLFsxLDAsIlgiXSxbMiwwLCJHIl0sWzMsMiwiWSJdLFs0LDIsIkcoRihZKSkiXSxbNCwzLCJHKEYoWScpKSJdLFsxLDMsIkYoWScpIl0sWzMsMywiWSciXSxbMCwxLCJcXG1hdGhiZiBDIl0sWzMsMSwiXFxtYXRoYmYgRCJdLFs2LDIsIlxcaG9tX0MoRihZJyksIFgpIl0sWzgsMiwiXFxob21fQyhGKFkpLCBYJykiXSxbNiwxLCJcXG1hdGhiZntTZXR9Il0sWzYsMywiXFxob21fRChZJywgRyhYKSkiXSxbOCwzLCJcXGhvbV9EKFksIEcoWCcpKSJdLFswLDIsIlgiXSxbMCwzLCJYJyJdLFs0LDQsIkcoWCkiXSxbNCw1LCJHKFgnKSJdLFsxLDIsIuaZrumBjeWwhChGKFgpLCBcXGV0YV9YKSJdLFszLDQsIlxcZXRhX1kiXSxbNCw1LCJHKEYoZikpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzcsNSwiXFxldGFfe1knfSJdLFszLDcsImYiXSxbMTAsMTEsIlxcaG9tX0MoRihmKSwgeCkiXSxbMTMsMTQsIlxcaG9tX0QoZiwgRyh4KSkiXSxbMTAsMTMsIlxcUGhpX3tZJywgWH0iLDJdLFsxNSwxNiwieCJdLFs2LDE1LCJnIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzExLDE0LCJcXFBoaV97WSwgWCd9Il0sWzAsNiwiRihmKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFs1LDE3LCJHKGcpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzcsMTcsIlxccGhpID0gXFxQaGlfe1knLCBYfShnKSIsMV0sWzE3LDE4LCJHKHgpIl0sWzMsMTgsIlxcUGhpX3tZLCBYJ30oeCBcXGNpcmMgZyBcXGNpcmMgRihmKSkiLDIseyJsYWJlbF9wb3NpdGlvbiI6MzAsImN1cnZlIjo1fV1d

$$
\begin{aligned}
\Phi_{Y, X'}(x \circ g \circ F(f)) &= G(x) \circ G(g) \circ G(F(f)) \circ \eta_Y \\
&= G(x) \circ G(g) \circ \eta_{Y'} \circ f \\
&= G(x) \circ \Phi_{Y', X}(g) \circ f
\end{aligned}
$$

以上により、圏$\mathbf C$の任意の対象$X$から$G$への普遍射$(F(X), \eta_X)$が存在するとき、$G$が右随伴関手であることが確認できた。
