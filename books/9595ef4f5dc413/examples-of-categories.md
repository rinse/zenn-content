---
title: "圏の例"
free: false
---

## Set

集合の圏$\mathbf{Set}$とは、すべての集合を対象に持ち、それらの間の写像を射として持つ圏である。

すべての集合を対象に持つため、その対象のあつまりは真クラスを成す。ゆえに$\mathbf{Set}$は大きい圏である。

## ひらがなの圏

[圏](category)の定義を満たしていれば、あらゆるものは圏である。例えば射は必ずしも関数っぽいものである必要はないし、圏自体が数学的に有意義なものである必要はない。

ここでは対象が文字で射が文字列であるようなひらがなの圏を考えてみよう。

- 対象: すべてのひらがな
- 射: ひらがなから成る文字列。ただし先頭の文字が始域で、末尾の文字が終域
- 射の合成は次の通り定義する：
    - $ひらがな: ひ \to な$
    - $なしごれん: な \to ん$
    - $なしごれん \circ ひらがな = ひらがなしごれん: ひ \to ん$
- 単位射は1文字の文字列(E.g. $あ: あ \to あ$)

![category_of_characters](https://storage.googleapis.com/zenn-user-upload/8e3281df86f9-20240724.png)

このようにすると、このひらがなの圏は圏の定義をきちんと満たすことが分かる。

## Hask

$\mathbf{Hask}$とは、プログラミング言語Haskellの型を対象に持ち、関数を射として持つ圏である。
恒等射に対して恒等関数`id :: a -> a`を、関数合成に対して`(.) :: (b -> c) -> (a -> b) -> a -> c`を割り当てる。Haskellでは多相的な関数を定義できるのに対して圏論の射は単相的であり、常にどの対象の恒等射であるかを下付き文字などで明示することに注意する。

![example_of_Hask](https://storage.googleapis.com/zenn-user-upload/97a518e3d661-20231112.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZntIYXNrfSJdLFswLDEsIlxcdGV4dHtJbnR9Il0sWzIsMSwiXFx0ZXh0e1N0cmluZ30iXSxbMCwyLCJcXHRleHR7TWF5YmUgSW50fSJdLFsyLDIsIlxcdGV4dHtNYXliZSBTdHJpbmd9Il0sWzAsMywiXFx0ZXh0e0xpc3QgSW50fSJdLFsyLDMsIlxcdGV4dHtMaXN0IFN0cmluZ30iXSxbMSwyLCJcXHRleHR7c2hvd31fXFx0ZXh0e0ludH0iXSxbMSwzLCJcXHRleHR7cmV0dXJufV97XFx0ZXh0e01heWJlIEludH19IiwyXSxbMiw0LCJcXHRleHR7cmV0dXJufV9cXHRleHR7TWF5YmUgU3RyaW5nfSJdLFszLDQsIlxcdGV4dHtmbWFwfV9cXHRleHR7TWF5YmV9KFxcdGV4dHtzaG93fV9cXHRleHR7SW50fSkiLDJdLFs1LDYsIlxcdGV4dHtmbWFwfV9cXHRleHR7TGlzdH0oXFx0ZXh0e3Nob3d9X1xcdGV4dHtJbnR9KSIsMl0sWzMsNSwiXFx0ZXh0e21heWJlVG9MaXN0fV9cXHRleHR7SW50fSIsMl0sWzQsNiwiXFx0ZXh0e21heWJlVG9MaXN0fV9cXHRleHR7U3RyaW5nfSJdXQ==

一般的な圏$\mathbf{C}$の話ばかり聞いていても、なかなか圏論的な議論に慣れるのは難しいので、自分が慣れ親しんだ（興味のある）具体的な圏で議論を解釈することは理解の役に立つ。

ただ、特に圏論に慣れないうちに具体的な圏を頼りにして議論を進めると、その圏が持つ特徴をいつの間にか圏一般の持つ性質のように勘違いしてしまうことがある。まずは一般的な圏についての議論を聞いて、ある程度理解できたと思ったら自分の知ってる圏に置き換えて、その議論が具体的な圏ではどういう意味を持つのかを吟味するというようなやり方をおすすめする。

特に$\mathbf{Hask}$を使う場合には、発散する関数や部分関数、`undefined :: a`、unsafeの扱いなどで、Haskellそのままではなくある程度恣意的な制限を仮定していることに気を付ける必要がある。
