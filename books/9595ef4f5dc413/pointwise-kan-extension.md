---
title: "各点Kan拡張"
free: false
---

## 定義

$G$の$F$に沿った左Kan拡張$\lang \mathrm{Lan}_F G, \eta \rang$を考える。

[![](https://storage.googleapis.com/zenn-user-upload/2a173fad0cec-20250329.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiXFxtYXRoYmZ7QX0iXSxbMCwyLCJcXG1hdGhiZntCfSJdLFsxLDIsIlxcbWF0aGJme0N9Il0sWzEsMiwiRiIsMl0sWzIsMywiXFxtYXRocm17TGFufV9GIEciLDJdLFsxLDMsIkciXSxbNiw1LCJcXGV0YSIsMix7Im9mZnNldCI6Miwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==)

余域の圏$\mathbf{C}$が余極限を持つ場合、圏$\mathbf{B}$の各対象（点）ごとにKan拡張を構成できる。

すなわち圏$\mathbf{B}$の各対象$B$について、これを[格上げ](./elevation)した関手$\tilde B$と関手$F$とのコンマ圏$F \downarrow \tilde B$を考える。
このとき関手$(\mathrm{Lan}_F G) \circ \tilde B : \mathbf{1} \to \mathbf{C}$は$G \circ P_0$ の $P_1$ に沿った左Kan拡張$\mathrm{Lan}_{P_1} (G \circ P_0)$である。

なお自然変換$\phi : F \circ P_0 \Rightarrow \tilde B \circ P_1$は[コンマ圏の普遍性](./comma-category-meets-ump)で導入されるもので、 $\phi_{\lang A, \ast, f \rang} \mapsto f: F(A) \to B$ である。

[![](https://storage.googleapis.com/zenn-user-upload/433d5e7ea239-20250330.png)](https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzEsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntCfSJdLFsyLDIsIlxcbWF0aGJme0N9Il0sWzAsMSwiRiBcXGRvd25hcnJvdyBcXHRpbGRlIEIiXSxbMCwyLCJcXG1hdGhiZnsxfSJdLFszLDEsIkYgXFxkb3duYXJyb3cgXFx0aWxkZSBCIl0sWzUsMiwiXFxtYXRoYmZ7Q30iXSxbMywyLCJcXG1hdGhiZnsxfSJdLFsxLDIsIkYiLDJdLFsyLDMsIlxcbWF0aHJte0xhbn1fRiBHIiwyXSxbMSwzLCJHIl0sWzQsNSwiUF8xIiwyXSxbNCwxLCJQXzAiXSxbNSwyLCJcXHRpbGRlIEIiLDJdLFsxLDUsIlxccGhpIiwyLHsibGV2ZWwiOjJ9XSxbOCw3LCJcXG1hdGhybXtMYW59X3tQXzF9IChHIFxcY2lyYyBQXzApIiwyXSxbNiw3LCJHIFxcY2lyYyBQXzAiXSxbNiw4LCJQXzEiLDJdLFsxMSwxMCwiXFxldGEiLDIseyJvZmZzZXQiOjIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbMTcsMTYsIlxcZXRhJyIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InNvdXJjZSI6ZmFsc2UsInRhcmdldCI6ZmFsc2V9fV1d)

このようにして構成されるKan拡張を備えているKan拡張は、各点Kan拡張 (*Pointwise kan extension*) と呼ばれる。

## 定理1

$\mathrm{Lan}_F G$が各点Kan拡張であるとき、任意の対象$B \in \mathrm{ob}(\mathbf{B})$について$(\mathrm{Lan}_F G)(B)$は圏$\mathbf{C}$における余極限である。

### 証明

仮定より、$\mathrm{Lan}_F G$が各点Kan拡張であるから、各対象$B \in \mathrm{ob}(\mathbf{B})$について、左Kan拡張$\mathrm{Lan}_{P_1} (G \circ P_0)$が存在する。
このとき、[極限はKan拡張である](./kan-extension-limit)から、余極限 $\varinjlim (G \circ P_0)$ が存在する。

この余極限は、次の可換図式を$P_1(A) = P_1(B) = \ast$によって括って三角形にして得られる。

[![](https://storage.googleapis.com/zenn-user-upload/497fcaa77b81-20250330.png)](https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFswLDEsIkYgXFxkb3duYXJyb3cgXFx0aWxkZSBCIl0sWzAsMiwiXFxtYXRoYmZ7MX0iXSxbMSwyLCJcXG1hdGhiZntEfSJdLFsyLDAsIlxcbWF0aGJme0R9Il0sWzUsMSwiXFxtYXRocm17TGFufV97UF8xfSAoRyBcXGNpcmMgUF8wKShcXGFzdCkiXSxbNCwyLCIoRyBcXGNpcmMgUF8wKShBKSJdLFs2LDIsIihHIFxcY2lyYyBQXzApKEIpIl0sWzUsMCwiUyhcXGFzdCkiXSxbMiwxLCJcXG1hdGhybXtMYW59X3tQXzF9KEcgXFxjaXJjIFBfMCkoUF8xKEEpKSJdLFszLDEsIlxcbWF0aHJte0xhbn1fe1BfMX0oRyBcXGNpcmMgUF8wKShQXzEoQikpIl0sWzIsMiwiKEcgXFxjaXJjIFBfMCkoQSkiXSxbMywyLCIoRyBcXGNpcmMgUF8wKShCKSJdLFsxLDIsIlBfMSIsMl0sWzIsMywiXFxtYXRocm17TGFufV97UF8wfSAoRyBcXGNpcmMgUF8wKSIsMl0sWzEsMywiRyBcXGNpcmMgUF8wIl0sWzYsNywiKEcgXFxjaXJjIFBfMCkoZikiLDJdLFs2LDUsIlxcZXRhX0EiXSxbNyw1LCJcXGV0YV9CIiwyXSxbNiw3LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6LTUsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs1LDgsImgiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNiw4LCJcXGVwc2lsb25fQSIsMCx7ImN1cnZlIjotMX1dLFs3LDgsIlxcZXBzaWxvbl9CIiwyLHsiY3VydmUiOjF9XSxbMTEsMTIsIihHIFxcY2lyYyBQXzApKGYpIiwyXSxbMTIsMTAsIlxcZXRhX0IiLDJdLFs5LDEwLCJcXG1hdGhybXtMYW59X3tQXzF9KEcgXFxjaXJjIFBfMCkoUF8xKGYpKSIsMCx7Im9mZnNldCI6LTJ9XSxbMTEsMTAsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzExLDksIlxcZXRhX0EiXSxbMTUsMTQsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dXQ==)

普遍性の条件も足して、次のような形の余極限になる。

[![](https://storage.googleapis.com/zenn-user-upload/cfcaf726279a-20250330.png)](https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFswLDEsIkYgXFxkb3duYXJyb3cgXFx0aWxkZSBCIl0sWzAsMiwiXFxtYXRoYmZ7MX0iXSxbMSwyLCJcXG1hdGhiZntEfSJdLFsyLDAsIlxcbWF0aGJme0R9Il0sWzUsMSwiXFxtYXRocm17TGFufV97UF8xfSAoRyBcXGNpcmMgUF8wKShcXGFzdCkiXSxbNCwyLCIoRyBcXGNpcmMgUF8wKShBKSJdLFs2LDIsIihHIFxcY2lyYyBQXzApKEIpIl0sWzUsMCwiUyhcXGFzdCkiXSxbMiwxLCJcXG1hdGhybXtMYW59X3tQXzF9KEcgXFxjaXJjIFBfMCkoUF8xKEEpKSJdLFszLDEsIlxcbWF0aHJte0xhbn1fe1BfMX0oRyBcXGNpcmMgUF8wKShQXzEoQikpIl0sWzIsMiwiKEcgXFxjaXJjIFBfMCkoQSkiXSxbMywyLCIoRyBcXGNpcmMgUF8wKShCKSJdLFsxLDIsIlBfMSIsMl0sWzIsMywiXFxtYXRocm17TGFufV97UF8wfSAoRyBcXGNpcmMgUF8wKSIsMl0sWzEsMywiRyBcXGNpcmMgUF8wIl0sWzYsNywiKEcgXFxjaXJjIFBfMCkoZikiLDJdLFs2LDUsIlxcZXRhX0EiXSxbNyw1LCJcXGV0YV9CIiwyXSxbNiw3LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6LTUsInN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs1LDgsImgiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNiw4LCJcXGVwc2lsb25fQSIsMCx7ImN1cnZlIjotMX1dLFs3LDgsIlxcZXBzaWxvbl9CIiwyLHsiY3VydmUiOjF9XSxbMTEsMTIsIihHIFxcY2lyYyBQXzApKGYpIiwyXSxbMTIsMTAsIlxcZXRhX0IiLDJdLFs5LDEwLCJcXG1hdGhybXtMYW59X3tQXzF9KEcgXFxjaXJjIFBfMCkoUF8xKGYpKSIsMCx7Im9mZnNldCI6LTJ9XSxbMTEsMTAsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzExLDksIlxcZXRhX0EiXSxbMTUsMTQsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dXQ==)

よって$\mathrm{Lan}_{P_1}(G \circ P_0)(\ast)$は余極限$\varinjlim(G \circ P_0)$である。

ここで$\mathrm{Lan}_{P_1}(G \circ P_0) \simeq (\mathrm{Lan}_F G) \circ \tilde B$であるから、以下が成り立つ。

$$
\begin{aligned}
\mathrm{Lan}_{P_1}(G \circ P_0)(\ast) & \simeq (\mathrm{Lan}_F G) (\tilde B(\ast)) \\
 & \simeq (\mathrm{Lan}_F G)(B)
\end{aligned}
$$

よって$(\mathrm{Lan}_F G) (B)$は余極限$\varinjlim(G \circ P_0)$である。

## 定理2

$\mathbf{A}$が小さい圏であって$\mathbf{C}$が有限完備ならば、圏$\mathbf{C}$は局所小圏であって、関手$G : \mathbf{A} \to \mathbf{C}$の各点右Kan拡張$\mathrm{Ran}_F G : \mathbf{B} \to \mathbf{C}$が存在する。また$B \in \mathrm{ob}(\mathbf{B})$における$\mathrm{Ran}_F G$の値 $(\mathrm{Ran}_F G)(B)$ の値は、次の極限で与えられる。

$$
(\mathrm{Ran}_F G)(B) \simeq \varprojlim (G \circ P_0)
$$

[![](https://storage.googleapis.com/zenn-user-upload/9ba0c7d8b0af-20250330.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzEsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntCfSJdLFsyLDIsIlxcbWF0aGJme0N9Il0sWzAsMSwiRiBcXGRvd25hcnJvdyBcXHRpbGRlIEIiXSxbMCwyLCJcXG1hdGhiZnsxfSJdLFsxLDIsIkYiLDJdLFsyLDMsIlxcbWF0aHJte1Jhbn1fRiBHIiwyXSxbMSwzLCJHIl0sWzQsMSwiUF8wIl0sWzQsNSwiUF8xIiwyXSxbNSwyLCJcXHRpbGRlIEIiLDJdLFsxLDUsIlxccGhpIiwyLHsibGV2ZWwiOjJ9XSxbNyw4LCJcXGV0YSIsMCx7Im9mZnNldCI6LTIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=)

## 定理3

任意の$B \in \mathrm{ob}(\mathbf{B})$に対して$\varinjlim_{j \in F \downarrow \tilde B}(G \circ P_0)$が存在するとき、$\mathrm{Lan}_F G$が存在して、$(\mathrm{Lan}_F G)(B) \simeq \varinjlim_{j \in F \downarrow \tilde B}(G \circ P_0)$を満たす。

[![](https://storage.googleapis.com/zenn-user-upload/2f8d2e1d1e2c-20250330.png)](https://q.uiver.app/#q=WzAsNixbMSwxLCJcXG1hdGhiZntBfSJdLFsxLDIsIlxcbWF0aGJme0J9Il0sWzIsMiwiXFxtYXRoYmZ7Q30iXSxbMCwxLCJGIFxcZG93bmFycm93IFxcdGlsZGUgQiJdLFswLDIsIlxcbWF0aGJmezF9Il0sWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFswLDEsIkYiLDJdLFswLDIsIkciXSxbMyw0LCJQXzEiLDJdLFs0LDEsIlxcdGlsZGUgQiIsMl0sWzMsMCwiUF8wIl0sWzAsNCwiXFxwaGkiLDIseyJsZXZlbCI6Mn1dXQ==)

## 定理4

$F$に沿った$G$の各点左Kan拡張$\mathrm{Lan}_F G$が存在するとき、$B \in \mathrm{ob}(\mathbf{B})$, $C \in \mathrm{ob}(\mathbf{C})$ について自然に以下の等式が成り立つ。

$$
\hom_C((\mathrm{Lan}_F G)(B), C) \simeq \hom_{\mathbf{Set}^{\mathbf{A}^\mathrm{op}}}(\hom_B(F(\_), B), \hom_C(G(\_), C))
$$

すなわち以下の図式で$\lang \mathrm{Lan}_F G, \eta \rang$が$F$に沿った$G$の各点左Kan拡張だとする。

[![](https://storage.googleapis.com/zenn-user-upload/2a173fad0cec-20250329.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiXFxtYXRoYmZ7QX0iXSxbMCwyLCJcXG1hdGhiZntCfSJdLFsxLDIsIlxcbWF0aGJme0N9Il0sWzEsMiwiRiIsMl0sWzIsMywiXFxtYXRocm17TGFufV9GIEciLDJdLFsxLDMsIkciXSxbNiw1LCJcXGV0YSIsMix7Im9mZnNldCI6Miwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==)

すると、圏$C$における射と、圏$\mathbf{C}^\mathrm{op}$から圏$\mathbf{Set}$への反変関手$\hom_D(F(\_), D)$から$\hom_U(E(\_), U)$への自然変換との間に、一対一対応が存在する。

[![](https://storage.googleapis.com/zenn-user-upload/f33efa2c5fcd-20250330.png)](https://q.uiver.app/#q=WzAsMTMsWzAsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntDfSJdLFswLDIsIlxcbWF0aGJme0J9Il0sWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFs0LDAsIlxcbWF0aGJme1NldH0iXSxbNCwxLCJcXGhvbV9DKChcXG1hdGhybXtMYW59X0YgRykoQiksIEMpIl0sWzIsMCwiXFxtYXRoYmZ7Q30iXSxbMiwxLCIoXFxtYXRocm17TGFufV9GIEcpKEIpIl0sWzIsMiwiQyJdLFs0LDIsIlxcaG9tX3tcXG1hdGhiZntTZXR9XntcXG1hdGhiZntDfV5cXG1hdGhybXtvcH19fShcXGhvbV9CKEYoXFxfKSwgQiksIFxcaG9tX0MoRyhcXF8pLCBDKSkiXSxbMywwLCJcXG1hdGhiZntTZXR9XntcXG1hdGhiZntDfV5cXG1hdGhybXtvcH19Il0sWzMsMSwiXFxob21fQihGKFxcXyksIEIpIl0sWzMsMiwiXFxob21fQyhHKFxcXyksICBDKSJdLFswLDEsIkciXSxbMCwyLCJGIiwyXSxbMiwxLCJcXG1hdGhybXtMYW59X0YgRyIsMl0sWzcsOCwiYyJdLFsxMSwxMiwiXFx0aGV0YSJdLFs1LDksIlxcc2ltZXEiXSxbMTMsMTUsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJ0YXJnZXQiOmZhbHNlfX1dXQ==)
