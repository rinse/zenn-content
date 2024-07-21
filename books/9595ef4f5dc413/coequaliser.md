---
title: "コイコライザ"
free: false
---

コイコライザは、[イコライザ](https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/7d35d8)の双対である。

## 定義

圏$\mathbf{C}$における射$f, g: A \to B$間のコイコライザ (*余等価子*, *Coequalizer*, *英: Coequaliser*) とは、対象$Q$と射$q: B \to Q$の組からなり、以下を満たす。

$$
q \circ f = q \circ g
$$

また以下の普遍性を満たす必要がある。

$$
^\forall z: B \to Z, \exists! u: Q \to Z, q = u \circ z
$$

すなわち任意の$z: B \to Z$に対して、射$u: Q \to Z$が一意に存在して、$z = u \circ q$を満たす。

![Coequaliser](https://storage.googleapis.com/zenn-user-upload/fd33d9151c14-20240104.png)
https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMSwiUSJdLFsyLDIsIloiXSxbMSwyLCJmIiwwLHsiY3VydmUiOi0xfV0sWzEsMiwiZyIsMix7ImN1cnZlIjoxfV0sWzIsMywicSJdLFszLDQsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiw0LCJ6IiwyXV0=

## 命題

$(Q, q)$がコイコライザであるとき、$q$は[エピ射](https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/82db73#%E3%82%A8%E3%83%94%E5%B0%84)である。

すなわち$y_1 \circ q = y_2 \circ q$であれば、$y_1 = y_2$であることが、普遍性の定義により分かる。

![coequaliser_is_epic](https://storage.googleapis.com/zenn-user-upload/86f61a921921-20240104.png)
https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMSwiUSJdLFsyLDIsIlkiXSxbMSwyLCJmIiwwLHsiY3VydmUiOi0xfV0sWzEsMiwiZyIsMix7ImN1cnZlIjoxfV0sWzIsMywicSJdLFszLDQsInlfMSA9IHlfMiA9IHUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiw0LCJ5XzEgXFxjaXJjIHEgPSB5XzIgXFxjaXJjIHEgPSB1IFxcY2lyYyBxIiwyLHsibGFiZWxfcG9zaXRpb24iOjB9XV0=


