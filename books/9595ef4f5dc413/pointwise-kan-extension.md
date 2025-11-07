---
title: "各点Kan拡張"
free: false
---

Kan拡張は、関手の定義域を自然に拡張するものと捉えられる。

関手$G : \mathbf A \to \mathbf C$の定義域を$F : \mathbf A \to \mathbf B$に沿って拡張した関手を$\mathrm{Lan}_F G : \mathbf B \to \mathbf C$とすると、$A \in \mathrm{ob}(\mathbf A)$については$G(A) = \mathrm{Lan}_F G(F(A))$となることが期待される。（実際にはこれは真ではなく、例えば一般には$\mathrm{Ran}_F F \simeq \mathrm{Id}$は成り立たない）

[![](https://storage.googleapis.com/zenn-user-upload/a003d2aeffae-20250926.png)](https://q.uiver.app/#q=WzAsNCxbMCwxLCJcXG1hdGhiZiBBIl0sWzAsMiwiXFxtYXRoYmYgQiJdLFsxLDIsIlxcbWF0aGJmIEMiXSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiRiIsMl0sWzEsMiwiXFxtYXRocm17TGFufV9GIEciLDJdLFswLDIsIkciXSxbNiw1LCJcXGV0YSIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InRhcmdldCI6ZmFsc2V9fV1d)

より気になる点は、$F$で写されないような$\mathbf B$の点が$\mathbf C$のどこに写るかである。なぜなら、これらがまさにKan拡張によって拡張される部分だからである。

これは一般には考えることができないが、$\mathbf C$が余極限を持つ場合には各点Kan拡張 (*Pointwise kan extension*) を考えることである程度計算できる。

## 定義

$G$の$F$に沿った左Kan拡張$\lang \mathrm{Lan}_F G, \eta \rang$を考える。

[![](https://storage.googleapis.com/zenn-user-upload/a003d2aeffae-20250926.png)](https://q.uiver.app/#q=WzAsNCxbMCwxLCJcXG1hdGhiZiBBIl0sWzAsMiwiXFxtYXRoYmYgQiJdLFsxLDIsIlxcbWF0aGJmIEMiXSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiRiIsMl0sWzEsMiwiXFxtYXRocm17TGFufV9GIEciLDJdLFswLDIsIkciXSxbNiw1LCJcXGV0YSIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InRhcmdldCI6ZmFsc2V9fV1d)

圏$\mathbf{B}$のある対象$B$に注目して、これを[格上げ](./elevation)した関手$\tilde B : \mathbf 1 \to \mathbf B$と関手$F$との[コンマ圏](./comma-category.md)$F \downarrow \tilde B$を考える。
するとコンマ圏の関手と自然変換とを用いて、大きな三角形を構成できる。

[![](https://storage.googleapis.com/zenn-user-upload/37c6400b29a5-20250926.png)](https://q.uiver.app/#q=WzAsMTcsWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFsxLDEsIlxcbWF0aGJme0F9Il0sWzEsMiwiXFxtYXRoYmZ7Qn0iXSxbMiwyLCJcXG1hdGhiZntDfSJdLFswLDEsIkYgXFxkb3duYXJyb3cgXFx0aWxkZSBCIl0sWzAsMiwiXFxtYXRoYmZ7MX0iXSxbNSwyLCJcXG1hdGhiZntDfSJdLFszLDIsIlxcbWF0aGJmezF9Il0sWzMsMSwiRiBcXGRvd25hcnJvdyBcXHRpbGRlIEIiXSxbMCw0LCJGIFxcZG93bmFycm93IFxcdGlsZGUgQiJdLFsyLDQsIlxcbWF0aGJmIEIiXSxbMyw0LCJcXG1hdGhiZiBDIl0sWzAsMywiRiBcXGRvd25hcnJvdyBcXHRpbGRlIEIiXSxbMSwzLCJcXG1hdGhiZiBBIl0sWzMsMywiXFxtYXRoYmYgQyJdLFs0LDQsIkYgXFxkb3duYXJyb3cgXFx0aWxkZSBCIl0sWzcsNCwiXFxtYXRoYmYgQyJdLFsxLDIsIkYiLDJdLFsyLDMsIlxcbWF0aHJte0xhbn1fRiBHIiwyXSxbMSwzLCJHIl0sWzQsNSwiUF8xIiwyXSxbNCwxLCJQXzAiXSxbNSwyLCJcXHRpbGRlIEIiLDJdLFs3LDYsIihcXG1hdGhybXtMYW59X0YgRykgXFxjaXJjIFxcdGlsZGUgQiIsMl0sWzgsNiwiRyBcXGNpcmMgUF8wIl0sWzgsNywiUF8xIiwyXSxbMSw1LCJcXHBoaSIsMix7ImxldmVsIjoyfV0sWzEwLDExLCJcXG1hdGhybXtMYW59X0YgRyIsMl0sWzksMTAsIkYgXFxjaXJjIFBfMCIsMCx7ImN1cnZlIjotMX1dLFs5LDEwLCJcXHRpbGRlIEIgXFxjaXJjIFBfMSIsMix7ImN1cnZlIjoxfV0sWzEyLDEzLCJQXzAiXSxbMTMsMTQsIkciLDAseyJjdXJ2ZSI6LTF9XSxbMTMsMTQsIihcXG1hdGhybXtMYW59X0YgRykgXFxjaXJjIEYiLDIseyJjdXJ2ZSI6MX1dLFsxNSwxNiwiRyBcXGNpcmMgUF8wIiwwLHsib2Zmc2V0IjotMSwiY3VydmUiOi0zfV0sWzE1LDE2LCIoXFxtYXRocm17TGFufV9GIEcpIFxcY2lyYyAgXFx0aWxkZSBCIFxcY2lyYyBQXzEiLDIseyJvZmZzZXQiOjEsImN1cnZlIjozfV0sWzE1LDE2LCIoXFxtYXRocm17TGFufV9GKSBHIFxcY2lyYyBGIFxcY2lyYyBQXzAiLDFdLFsxOSwxOCwiXFxldGEiLDIseyJvZmZzZXQiOjIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InNvdXJjZSI6ZmFsc2V9fV0sWzI4LDI5LCJcXHBoaSIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbMzEsMzIsIlxcZXRhIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dLFsyNCwyMywiKChcXG1hdGhybXtMYW59X0YgRykgXFxhc3QgXFxwaGkpIFxcY2lyYyAgKFxcZXRhIFxcYXN0IFBfMCkiLDAseyJvZmZzZXQiOjUsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InNvdXJjZSI6ZmFsc2UsInRhcmdldCI6ZmFsc2V9fV0sWzMzLDM1LCJcXGV0YSBcXGFzdCBQXzAiLDAseyJvZmZzZXQiOjUsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InNvdXJjZSI6ZmFsc2UsInRhcmdldCI6ZmFsc2V9fV0sWzM1LDM0LCIoXFxtYXRocm17TGFufV9GIEcpIFxcYXN0IFxccGhpIiwwLHsib2Zmc2V0Ijo1LCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dXQ==)

一般的にはこの$(\mathrm{Lan}_F G) \circ \tilde B$が$G \circ P_0$の$P_1$に沿った左Kan拡張になっているとは限らないが、このようにして構成されるKan拡張を$\mathbf B$の各点$B$について備えているKan拡張を各点Kan拡張 (*Pointwise kan extension*) と呼ばれる。

なおKan拡張の一意性から、各点Kan拡張については$(\mathrm{Lan}_F G) \circ \tilde B \simeq \mathrm{Lan}_{P_1} (G \circ P_0)$が常に成り立つ。

## 各点右Kan拡張

各点左Kan拡張と同じようにして、各点右Kan拡張を考えることができる。

[![](https://storage.googleapis.com/zenn-user-upload/20584f6e3e5f-20251101.png)](https://q.uiver.app/#q=WzAsNixbMSwxLCJcXG1hdGhiZiBBIl0sWzEsMiwiXFxtYXRoYmYgQiJdLFsyLDIsIlxcbWF0aGJmIEMiXSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiXFx0aWxkZSBCIFxcZG93bmFycm93IEYiXSxbMCwyLCJcXG1hdGhiZiAxIl0sWzAsMSwiRiIsMl0sWzEsMiwiXFxtYXRocm17UmFufV9GIEciLDJdLFswLDIsIkciXSxbNCwwLCJQXzEiXSxbNSwxLCJcXHRpbGRlIEIiLDJdLFs0LDUsIlBfMCIsMl0sWzUsMCwiXFxwaGkiLDEseyJsZXZlbCI6Mn1dLFs3LDgsIlxcZXRhIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfSwiZWRnZV9hbGlnbm1lbnQiOnsidGFyZ2V0IjpmYWxzZX19XV0=)

コンマ圏の取り方を逆にする必要がある点に注意する。

## 定理1

$\mathrm{Lan}_F G$が各点Kan拡張であるとき、任意の対象$B \in \mathrm{ob}(\mathbf{B})$について$\mathrm{Lan}_F G(B)$は圏$\mathbf{C}$における余極限$\varinjlim_{j \in F \downarrow \tilde B} (G \circ P_0)_j$である。

またこの主張は逆も成り立つ。すなわち任意の対象$B \in \mathrm{ob}(\mathbf{B})$について余極限$\varinjlim_{j \in F \downarrow \tilde B} (G \circ P_0)_j$が存在するとき、各点Kan拡張$\mathrm{Lan}_F G$が存在する。

### 証明

[極限がKan拡張である](./kan-extension-limit)ことを思い出すと、$P_1$に沿った$G \circ P_0$の左Kan拡張$\mathrm{Lan}_{P_1} (G \circ P_0) : \mathbf 1 \to \mathbf C$は$G \circ P_0$の余極限$\varinjlim_{j \in F \downarrow \tilde B} (G \circ P_0)_j$に一致する。
Kan拡張の一意性により$\mathrm{Lan}_{P_1} (G \circ P_0) \simeq (\mathrm{Lan}_F G) \circ \tilde B$が成り立つ。また自明に$(\mathrm{Lan}_F G) \circ \tilde B \simeq (\mathrm{Lan}_F G)(B)$である。

上の議論は$\mathbf B$の各点$B$について成り立つから、任意の$B \in \mathrm{ob}(\mathbf B)$について$(\mathrm{Lan}_F G)(B) \simeq \varinjlim_{j \in F \downarrow \tilde B} (G \circ P_0)_j$が成り立つ。

[![](https://storage.googleapis.com/zenn-user-upload/db95cbd6782a-20251107.png)](https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzEsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntCfSJdLFsyLDIsIlxcbWF0aGJme0N9Il0sWzAsMSwiRiBcXGRvd25hcnJvdyBcXHRpbGRlIEIiXSxbMCwyLCJcXG1hdGhiZnsxfSJdLFs1LDIsIlxcbWF0aGJme0N9Il0sWzMsMiwiXFxtYXRoYmZ7MX0iXSxbMywxLCJGIFxcZG93bmFycm93IFxcdGlsZGUgQiJdLFsxLDIsIkYiLDJdLFsxLDMsIkciXSxbNCw1LCJQXzEiLDJdLFs0LDEsIlBfMCJdLFs1LDIsIlxcdGlsZGUgQiIsMl0sWzcsNiwiKFxcbWF0aHJte0xhbn1fRiBHKSBcXGNpcmMgXFx0aWxkZSBCIFxcc2ltZXEgXFxtYXRocm17TGFufV97UF8xfShHIFxcY2lyYyBQXzApIFxcc2ltZXEgXFx2YXJpbmpsaW0oRyBcXGNpcmMgUF8wKSIsMl0sWzgsNiwiRyBcXGNpcmMgUF8wIl0sWzgsNywiUF8xIiwyXSxbMSw1LCJcXHBoaSIsMix7ImxldmVsIjoyfV0sWzIsMywiXFxtYXRocm17TGFufV9GIEciLDJdLFsxNSwxNCwiKChcXG1hdGhybXtMYW59X0YgRykgXFxhc3QgXFxwaGkpIFxcY2lyYyAgKFxcZXRhIFxcYXN0IFBfMCkiLDAseyJvZmZzZXQiOjUsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH0sImVkZ2VfYWxpZ25tZW50Ijp7InNvdXJjZSI6ZmFsc2UsInRhcmdldCI6ZmFsc2V9fV0sWzEwLDE4LCJcXGV0YSIsMix7Im9mZnNldCI6Miwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfSwiZWRnZV9hbGlnbm1lbnQiOnsic291cmNlIjpmYWxzZX19XV0=)
