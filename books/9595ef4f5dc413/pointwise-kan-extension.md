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

## 証明

TODO

## 元ネタ

例によって元ネタはalg-dさんの動画だ。

https://www.youtube.com/watch?v=kgoaLnlYr1Y&t=582s
