---
title: "圏の例"
free: false
---

## Set

集合の圏 $\mathbf{Set}$ とは、すべての集合を対象に持ち、それらの間の写像を射として持つ圏である。
すべての集合を対象に持つため、その対象のあつまりは真クラスを成す。ゆえに $\mathbf{Set}$ は大きい圏である。

集合は現代の数学のあらゆる分野において重要なものだが、それは圏論にも当てはまる。
例えば圏の対象や射のあつまりが集合をなすかどうかはしばしば問題になるため、[圏の大きさ](./largeness-of-categories)として分類される。

また集合の圏 $\mathbf{Set}$ は様々な良い性質を持っているため、様々な圏の分析を集合の圏を介して行うことがある。

## Hask

$\mathbf{Hask}$ とは、プログラミング言語 Haskell の型を対象に持ち、関数を射として持つ圏である。
恒等射に対して恒等関数 `id :: a -> a` を、関数合成に対して `(.) :: (b -> c) -> (a -> b) -> a -> c` を割り当てる。Haskell では多相的な関数を定義できるのに対して圏論の射は単相的であり、常にどの対象の恒等射であるかを下付き文字などで明示することに注意する。

![example_of_Hask](https://storage.googleapis.com/zenn-user-upload/97a518e3d661-20231112.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntIYXNrfSJdLFswLDEsIlxcdGV4dHtJbnR9Il0sWzIsMSwiXFx0ZXh0e1N0cmluZ30iXSxbMCwyLCJcXHRleHR7TWF5YmUgSW50fSJdLFsyLDIsIlxcdGV4dHtNYXliZSBTdHJpbmd9Il0sWzAsMywiXFx0ZXh0e0xpc3QgSW50fSJdLFsyLDMsIlxcdGV4dHtMaXN0IFN0cmluZ30iXSxbMSwyLCJcXHRleHR7c2hvd31fXFx0ZXh0e0ludH0iXSxbMSwzLCJcXHRleHR7cmV0dXJufV97XFx0ZXh0e01heWJlIEludH19IiwyXSxbMiw0LCJcXHRleHR7cmV0dXJufV9cXHRleHR7TWF5YmUgU3RyaW5nfSJdLFszLDQsIlxcdGV4dHtmbWFwfV9cXHRleHR7TWF5YmV9KFxcdGV4dHtzaG93fV9cXHRleHR7SW50fSkiLDJdLFs1LDYsIlxcdGV4dHtmbWFwfV9cXHRleHR7TGlzdH0oXFx0ZXh0e3Nob3d9X1xcdGV4dHtJbnR9KSIsMl0sWzMsNSwiXFx0ZXh0e21heWJlVG9MaXN0fV9cXHRleHR7SW50fSIsMl0sWzQsNiwiXFx0ZXh0e21heWJlVG9MaXN0fV9cXHRleHR7U3RyaW5nfSJdXQ==

一般的な圏 $\mathbf{C}$ の話ばかり聞いていても、なかなか圏論的な議論に慣れるのは難しいので、自分が慣れ親しんだ（興味のある）具体的な圏で議論を解釈することは理解の役に立つ。

ただ、特に圏論に慣れないうちに具体的な圏を頼りにして議論を進めると、その圏が持つ特徴をいつの間にか圏一般の持つ性質のように勘違いしてしまうことがある。まずは一般的な圏についての議論を聞いて、ある程度理解できたと思ったら自分の知ってる圏に置き換えて、その議論が具体的な圏ではどういう意味を持つのかを吟味するというようなやり方をおすすめする。

特に $\mathbf{Hask}$ を使う場合には、発散する関数や部分関数、`undefined :: a`、unsafe の扱いなどで、Haskellそのままではなくある程度恣意的な制限を仮定していることに気を付ける必要がある。
