---
title: "各点Kan拡張"
free: false
---

## アイデア

$G$の$F$に沿った左Kan拡張$\lang L, \eta \rang$を考える。

[![](https://storage.googleapis.com/zenn-user-upload/c61ea4cc1504-20250305.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiXFxtYXRoYmZ7QX0iXSxbMCwyLCJcXG1hdGhiZntCfSJdLFsxLDIsIlxcbWF0aGJme0N9Il0sWzEsMiwiRiIsMl0sWzIsMywiTCIsMl0sWzEsMywiRyJdLFs2LDUsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9fV1d)

このとき、関手$L$とは実際のところ、どういう関手なのだろうか？
特に、$\mathbf{B}$の対象$B$を写した$L(B)$は、圏$\mathbf{C}$ではどのような性質を持つ対象なのだろうか。

圏$\mathbf{B}$のある対象$B$に注目するために、$\tilde B(\ast) = B$であるような関手$\tilde B : \mathbf{1} \to \mathbf{B}$を考える。
（これは対象の関手への[格上げ](./elevation)である）

そうすると、[関手の上方から成る圏](./variants-of-comma-category.md#関手の上方の対象から成る圏) $F \downarrow B$ （あるいは同じことだがコンマ圏 $F \downarrow \tilde B$）、忘却関手$U : F \downarrow B \to \mathbf{A}$、小さい圏の圏の終対象$\mathbf{1}$への射である関手$T$が存在するから、下のように図に書き加えられる。

[![](https://storage.googleapis.com/zenn-user-upload/26a2052481c7-20250305.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzEsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntCfSJdLFsyLDIsIlxcbWF0aGJme0N9Il0sWzAsMSwiRiBcXGRvd25hcnJvdyBCIl0sWzAsMiwiXFxtYXRoYmZ7MX0iXSxbMSwyLCJGIiwyXSxbMiwzLCJMIiwyXSxbMSwzLCJHIl0sWzQsNSwiVCIsMl0sWzQsMSwiVSJdLFs1LDIsIlxcdGlsZGUgQiIsMl0sWzgsNywiXFxldGEiLDIseyJvZmZzZXQiOjIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=)

（ちなみにコンマ圏$F \downarrow B$は次のような圏である）

[![](https://storage.googleapis.com/zenn-user-upload/d6acf406a6e6-20250305.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFsxLDEsIlxcbWF0aGJme0F9Il0sWzIsMSwiXFxtYXRoYmZ7Qn0iXSxbMCwxLCJGIFxcZG93bmFycm93IEIiXSxbNCwxLCJcXG1hdGhiZnsxfSJdLFswLDIsIlxcbGFuZyBBLCBmIFxccmFuZyJdLFswLDMsIlxcbGFuZyBBJywgZicgXFxyYW5nIl0sWzEsMiwiQSJdLFsxLDMsIkEnIl0sWzIsMiwiRihBKSJdLFszLDIsIlxcdGlsZGUgQihcXGFzdCkiXSxbMywzLCJcXHRpbGRlIEIoXFxhc3QpIl0sWzIsMywiRihBJykiXSxbNCwyLCJcXGFzdCJdLFs0LDMsIlxcYXN0Il0sWzEsMiwiRiJdLFszLDEsIlUiXSxbNCwyLCJcXHRpbGRlIEIiLDJdLFs1LDYsImEiLDJdLFs3LDgsImEiLDJdLFs5LDEwLCJmIl0sWzEwLDExLCJcXHRpbGRlIEIoXFxtYXRocm17aWR9X1xcYXN0KSJdLFs5LDEyLCJGKGEpIiwyXSxbMTIsMTEsImYnIiwyXSxbMTMsMTQsIlxcbWF0aHJte2lkfV9cXGFzdCJdLFs5LDExLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

そうすると、もう少し大きな三角形が見えるようになる。
もしこの三角形について、$T$に沿った$G \circ U$の左Kan拡張$\lang L \circ \tilde B, \sigma \rang$が存在した場合、$L(\tilde B(\ast))$は圏$\mathbf{C}$における余極限に一致する。（[極限はKan拡張である](./kan-extension-limit)）

[格上げ](./elevation)の定義より$\tilde B(\ast) = B$であるため、つまるところ$L(B)$とは、（この三角形が左Kan拡張である場合）$\mathbf{C}$において余極限であることになる。

[![](https://storage.googleapis.com/zenn-user-upload/c7dfd9fd7ece-20250305.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzEsMiwiXFxtYXRoYmZ7Q30iXSxbMCwxLCJGIFxcZG93bmFycm93IEIiXSxbMCwyLCJcXG1hdGhiZnsxfSJdLFsyLDMsIlQiLDJdLFsyLDEsIkcgXFxjaXJjIFUiXSxbMywxLCJMIFxcY2lyYyBcXHRpbGRlIEIiLDJdLFs1LDYsIlxcc2lnbWEiLDIseyJvZmZzZXQiOjIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=)

## 定理

任意の$B \in \mathrm{ob}(\mathbf{B})$について余極限$\varinjlim G \circ U$が存在する場合、
左Kan拡張$\lang L, \eta \rang$が存在して、$L(B) \simeq \varinjlim G \circ U$となる。

また$\mathbf{C}$が[余完備](./complete)であれば、$\lang L, \eta \rang$は存在する。（正確には$\mathbf{A}$が小圏で$\mathbf{B}$が局所的に小さい圏でなければならないらしい）

[![](https://storage.googleapis.com/zenn-user-upload/26a2052481c7-20250305.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzEsMSwiXFxtYXRoYmZ7QX0iXSxbMSwyLCJcXG1hdGhiZntCfSJdLFsyLDIsIlxcbWF0aGJme0N9Il0sWzAsMSwiRiBcXGRvd25hcnJvdyBCIl0sWzAsMiwiXFxtYXRoYmZ7MX0iXSxbMSwyLCJGIiwyXSxbMiwzLCJMIiwyXSxbMSwzLCJHIl0sWzQsNSwiVCIsMl0sWzQsMSwiVSJdLFs1LDIsIlxcdGlsZGUgQiIsMl0sWzgsNywiXFxldGEiLDIseyJvZmZzZXQiOjIsInNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XV0=)

### 証明

TODO

## 定理2

$\lang T, \eta \rang$が$F$に沿った$E$の各点左Kan拡張であると仮定する。
このとき、$D \in \mathrm{ob}(\mathbf{D})$, $U \in \mathrm{ob}(\mathbf{U})$ について自然に以下の等式が成り立つ。

$$
\hom_U(T(D), U) \simeq \hom_{\mathbf{Set}^{\mathbf{C}^\mathrm{op}}}(\hom_D(F(\_), D), \hom_U(E(\_), U))
$$

すなわち以下の図式で$\lang T, \eta \rang$が$F$に沿った$E$の各点左Kan拡張だとする。

![](https://storage.googleapis.com/zenn-user-upload/1480812b022a-20250314.png)

すると、圏$U$における射と、圏$\mathbf{C}^\mathrm{op}$から圏$\mathbf{Set}$への反変関手$\hom_D(F(\_), D)$から$\hom_U(E(\_), U)$への自然変換との間に、一対一対応が存在する。

![](https://storage.googleapis.com/zenn-user-upload/d084fcf00837-20250314.png)

https://q.uiver.app/#q=WzAsMTIsWzAsMSwiXFxtYXRoYmZ7Q30iXSxbMSwyLCJcXG1hdGhiZntVfSJdLFswLDIsIlxcbWF0aGJme0R9Il0sWzAsMCwiXFxtYXRoYmZ7Q2F0fSJdLFs0LDAsIlxcbWF0aGJme1NldH0iXSxbNCwxLCJcXGhvbV9VKFQoRCksIFUpIl0sWzIsMCwiXFxtYXRoYmZ7VX0iXSxbMiwxLCJUKEQpIl0sWzMsMSwiVSJdLFs1LDEsIlxcaG9tX3tcXG1hdGhiZntTZXR9XntcXG1hdGhiZntDfV5cXG1hdGhybXtvcH19fShcXGhvbV9EKEYoXFxfKSwgRCksIFxcaG9tX1UoRShcXF8pLCBVKSkiXSxbNCwyLCJ1Il0sWzUsMiwiXFxnYW1tYSJdLFswLDEsIkUiXSxbMCwyLCJGIiwyXSxbMiwxLCJUIiwyXSxbNyw4LCJ1Il0sWzExLDksIlxcaW4iLDMseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbNSw5LCJcXHNpbWVxIiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzEwLDExLCLkuIDlr77kuIDlr77lv5wiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJtYXBzIHRvIn19fV0sWzEwLDUsIlxcaW4iLDMseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTIsMTQsIlxcZXRhIiwyLHsib2Zmc2V0IjoyLCJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJ0YXJnZXQiOmZhbHNlfX1dXQ==

$\mathbf{C}$の各要素について自然変換を書き下すと次の通りだ。

[![](https://storage.googleapis.com/zenn-user-upload/60d2f3d60c1e-20250315.png)](https://q.uiver.app/#q=WzAsMTcsWzMsMCwiXFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fSJdLFszLDEsIlxcaG9tX0QoRihcXF8pLCBEKSJdLFszLDIsIlxcaG9tX1UoRShcXF8pLCBVKSJdLFswLDEsIlxcbWF0aGJme0R9Il0sWzEsMSwiRihDKSJdLFsyLDEsIkQiXSxbMSwyLCJFKEMpIl0sWzIsMiwiVSJdLFswLDIsIlxcbWF0aGJme1V9Il0sWzAsMywiXFxtYXRoYmZ7Q30iXSxbMSwzLCJDIl0sWzIsMywiQyciXSxbNCwwLCJcXG1hdGhiZntTZXR9Il0sWzQsMSwiXFxob21fRChGKEMpLCBEKSJdLFs0LDIsIlxcaG9tX1UoRShDKSwgVSkiXSxbNSwxLCJcXGhvbV9EKEYoQycpLCBEKSJdLFs1LDIsIlxcaG9tX1UoRShDJyksIFUpIl0sWzQsNV0sWzEsMiwiXFxnYW1tYSJdLFsxNSwxMywiXFxob21fRChGKGMpLCBEKSIsMl0sWzE2LDE0LCJcXGhvbV9VKEUoYyksIFUpIl0sWzEzLDE2LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxMywxNCwiXFxnYW1tYV9DIiwyXSxbMTUsMTYsIlxcZ2FtbWFfe0MnfSJdLFsxMCwxMSwiYyJdLFs2LDddXQ==)

## 元ネタ

元ネタはalg-dさんの動画です。

https://www.youtube.com/watch?v=kgoaLnlYr1Y&t=582s
