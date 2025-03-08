---
title: "可換図式"
free: false
---

## 可換図式(*Commutative diagram*)

圏は対象とそれらの間の射によって定義される。射の合成は、2つの射とそれらの合成射からなる三角形を作る。

![diagram](https://storage.googleapis.com/zenn-user-upload/f2b82f568b1c-20231203.png)

この三角形が可換である(*Commutes*)とは、その2つの射とそれらの合成射が"等しい"ことを意味し、記号$\circlearrowright$で表す。
つまり下図は、右回りに$f$, $g$と行くのと、左回りに$g \circ f$を一息に行くことが"等しい"ことを表している。（下図が可換であることは、圏の定義より自明に成り立つ）

![commutative_diagram](https://storage.googleapis.com/zenn-user-upload/76d7cf8092d7-20250309.png)

この図は可換図式(*Commutative diagram*)と呼ばれ、圏論の議論では分かりやすさのために多用される。Zennのマークダウンで作図をするのはつらいので、[quivar](https://q.uiver.app/)というサイトを使って図を作成している。

## 可換図式のバリエーション

可換図式は必ずしも三角形ではなく、様々な形で射が"等しい"ことを表す。

例えば以下の可換図式は、$f' \circ f = g' \circ g$であることを意味している。

![](https://storage.googleapis.com/zenn-user-upload/c4dc64492b0d-20250309.png)
