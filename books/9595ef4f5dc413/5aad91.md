---
title: "圏の例"
free: false
---

## Set

集合の圏$\mathbf{Set}$とは、すべての集合を対象に持ち、それらの間の写像を射として持つ圏である。
すべての集合を対象に持つため、その対象のあつまりは真クラスを成す。ゆえに$\mathbf{Set}$は大きい圏である。

$\mathbf{Set}$は大きいのでとても書ききれないが、ごく一部を取り出して図に書き出してみれば、このような感じだろう。

![Set_category](https://storage.googleapis.com/zenn-user-upload/8c61e5abbcd8-20231203.png)

https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZiB7U2V0fSJdLFswLDEsIlxcZW1wdHkiXSxbMSwxLCJcXFIiXSxbMSwyLCJbMCwgXFxpbmZ0eSkiXSxbMiwxLCJcXFoiXSxbMiwzLCJ8IC0gfCJdLFsxLDIsImYiXSxbMiw0LCJcXGxmbG9vciAtIFxccmZsb29yIl1d

## 1

自明な圏$\mathbf{1}$は、ただ一つの対象$\ast$とただ一つの射$\mathrm{id}_{\ast}$から成る圏だ。
$\mathbf{1}$のような、自明な射（単位射）しか持たないような圏を離散圏(*Discrete category*)と呼ぶ。

![1](https://storage.googleapis.com/zenn-user-upload/b693cb462694-20231203.png)

https://q.uiver.app/#q=WzAsMyxbMCwxLCJcXGFzdCJdLFswLDAsIlxcbWF0aGJmIDEiXSxbMSwxLCJcXGFzdCJdLFswLDIsImlkX1xcYXN0Il1d

## 2

離散圏$\mathbf{2}$とは、二つの対象$1$, $2$と二つの射$\mathrm{id}_{1}$, $\mathrm{id}_2$のみから成る圏である。

$\mathbf{2}$を見るのは、二つの対象の積を定義のために図式の形として用いる場合だろう。

以降、離散圏をそれが持つ対象の数に応じて$\mathbf{3}$, $\mathbf{4}$などと書く。

![2](https://storage.googleapis.com/zenn-user-upload/33b7705e7c51-20231203.png)

https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZiAyIl0sWzAsMSwiMSJdLFsxLDEsIjIiXV0=

## 0

空圏$\mathbf{0}$とは、対象を一つも持たず、それゆえ射も一つも持たない圏である。

## Hask

$\mathbf{Hask}$とは、プログラミング言語Haskellの型を対象に持ち、関数を射として持つ圏である。
恒等射に対して恒等関数`id :: a -> a`を、関数合成に対して`(.) :: (b -> c) -> (a -> b) -> a -> c`を割り当てる。Haskellでは多相的な関数を定義できるのに対して圏論の射は単相的であり、常にどの対象の恒等射であるかを下付き文字などで明示することに注意する。

![example_of_Hask](https://storage.googleapis.com/zenn-user-upload/97a518e3d661-20231112.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntIYXNrfSJdLFswLDEsIlxcdGV4dHtJbnR9Il0sWzIsMSwiXFx0ZXh0e1N0cmluZ30iXSxbMCwyLCJcXHRleHR7TWF5YmUgSW50fSJdLFsyLDIsIlxcdGV4dHtNYXliZSBTdHJpbmd9Il0sWzAsMywiXFx0ZXh0e0xpc3QgSW50fSJdLFsyLDMsIlxcdGV4dHtMaXN0IFN0cmluZ30iXSxbMSwyLCJcXHRleHR7c2hvd31fXFx0ZXh0e0ludH0iXSxbMSwzLCJcXHRleHR7cmV0dXJufV97XFx0ZXh0e01heWJlIEludH19IiwyXSxbMiw0LCJcXHRleHR7cmV0dXJufV9cXHRleHR7TWF5YmUgU3RyaW5nfSJdLFszLDQsIlxcdGV4dHtmbWFwfV9cXHRleHR7TWF5YmV9KFxcdGV4dHtzaG93fV9cXHRleHR7SW50fSkiLDJdLFs1LDYsIlxcdGV4dHtmbWFwfV9cXHRleHR7TGlzdH0oXFx0ZXh0e3Nob3d9X1xcdGV4dHtJbnR9KSIsMl0sWzMsNSwiXFx0ZXh0e21heWJlVG9MaXN0fV9cXHRleHR7SW50fSIsMl0sWzQsNiwiXFx0ZXh0e21heWJlVG9MaXN0fV9cXHRleHR7U3RyaW5nfSJdXQ==

一般的な圏$\mathbf{C}$の話ばかり聞いていても、なかなか脳は圏論的な議論に慣れてくれないので、自分が慣れ親しんだ具体的な圏で議論を解釈することは理解の役に立つ。

ただ、特に圏論に慣れないうちに具体的な圏を頼りにして議論を進めると、その圏が持つ特徴をいつの間にか圏一般の持つ性質のように勘違いしてしまうことがある。まずは一般的な圏についての議論を聞いて、ある程度理解できたと思ったら自分の知ってる圏に置き換えて、その議論が具体的な圏ではどういう意味を持つのかを吟味するというようなやり方をおすすめする。

特に$\mathbf{Hask}$を使う場合には、発散する関数や部分関数、`undefined :: a`、unsafeの扱いなどで、Haskellそのままではなくある程度恣意的な制限を仮定していることに気を付ける必要がある。
