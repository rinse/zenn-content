---
title: "始対象と終対象"
free: false
---

ネタ元は[Wikipedia](https://ja.wikipedia.org/wiki/始対象と終対象)。

## 定義

ある圏$\mathbf{C}$の始対象(*Initial object*)とは、$\mathbf{C}$の対象$I$であって、$\mathbf{C}$の各対象$X$に対して射$I \to X$がちょうど一つ存在するものをいう。

終対象は始対象の双対である。
すなわちある圏$\mathbf{C}$の終対象(*Terminal object*)とは、$\mathbf{C}$の対象$T$であって、$\mathbf{C}$の各対象$X$に対して射$X \to T$がちょうど一つ存在するものをいう。

[![initial-terminal-objects](https://storage.googleapis.com/zenn-user-upload/e5b1dbafcf64-20240804.png)](https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhiZntDfSJdLFswLDIsIkkiXSxbMSwxLCJBIl0sWzEsMiwiQiJdLFsxLDMsIlxcdmRvdHMiXSxbMiwyLCJUIl0sWzEsMiwiZiJdLFsxLDMsImciLDJdLFsxLDRdLFsyLDUsImYnIl0sWzMsNSwiZyciLDJdLFs0LDVdXQ==)

始対象と終対象は存在するとは限らないが、存在すれば一意である。

始対象でも終対象でもあるような対象は零対象(*Zero object*)と呼び、零対象を持つ圏を**点付き圏**(*Pointed category*)と呼ぶ。

## 例

### Cat

小さい圏の圏$\mathbf{Cat}$の始対象は[空圏](discrete-categories#0) $\mathbf{0}$であり、終対象は[自明な圏](discrete-categories#1) $\mathbf{1}$である。

空圏$\mathbf{0}$は対象を一つも持たず、したがって射も一つも持たない圏である。この圏からは、任意の圏に対して対象を何も写さず、したがって射を何も写さない関手を考えることができる。
また自明な圏$\mathbf{1}$は唯一の対象$\ast$を持ち、唯一の射$\mathrm{id}_{\ast}$を持つ圏である。任意の圏からこの圏に対して、任意の対象を$\ast$に、任意の射を$\mathrm{id}_\ast$に写す定関手を考えることができる。

[![Cat](https://storage.googleapis.com/zenn-user-upload/14a8f5b4bd23-20240804.png)](https://q.uiver.app/#q=WzAsNixbMiwwLCJcXG1hdGhiZntDfSJdLFswLDAsIlxcbWF0aGJmezB9Il0sWzIsMSwiQSJdLFsyLDIsIkIiXSxbNCwwLCJcXG1hdGhiZnsxfSJdLFs0LDIsIlxcYXN0Il0sWzIsMywiZiJdLFsxLDAsIkYiXSxbMCw0LCJcXERlbHRhIl0sWzUsNSwiXFxtYXRocm17aWR9X1xcYXN0Il0sWzIsNSwiXFxEZWx0YShBKSIsMCx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1hcHMgdG8ifX19XSxbMyw1LCJcXERlbHRhKEIpIiwyLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibWFwcyB0byJ9fX1dXQ==)

### 普遍射

関手$F$から対象$A$への普遍射は[コンマ圏](comma-category)$F \downarrow A$における終対象である。

### 極限

図式$F$の[極限](limit)は錐の圏における終対象である。
