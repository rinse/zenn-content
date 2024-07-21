---
title: "可換図式"
free: false
---

## 可換図式(*Commutative diagram*)

圏は対象とそれらの間の射によって定義される。そして射の合成は、2つの射とその合成射からなる三角形を作る。

これを図にしたものは可換図式と呼ばれ、圏論の議論では分かりやすさのために多用される。Zennのマークダウンで作図をするのはつらいので、[quivar](https://q.uiver.app/)というサイトを使って図を示す。

以下が実際の可換図式である。
本来はこの三角形の中に可換であることを示す記号$\circlearrowright$を書くが、サイトの都合で省く。また恒等射も断りなく省く。

![Commutative_diagram](https://storage.googleapis.com/zenn-user-upload/f2b82f568b1c-20231203.png)

https://q.uiver.app/#q=WzAsMyxbMCwwLCJBIl0sWzEsMCwiQiJdLFsxLDEsIkMiXSxbMCwxLCJmIl0sWzEsMiwiZyJdLFswLDIsImcgXFxjaXJjIGYiLDJdXQ==

可換図式で書き表す、あるいは可換図式を示して「以下を可換にする」などと言った時には、図式にある射の可換性という条件を満たすことを意味している。
例えば以下を可換にすると言った場合には、$h = g \circ f$を満たすことを主張している。

![Commutative_diagram_example](https://storage.googleapis.com/zenn-user-upload/bf27f7726b17-20231203.png)

https://q.uiver.app/#q=WzAsNCxbMCwxLCJBIl0sWzEsMSwiQiJdLFsxLDIsIkMiXSxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiZiJdLFsxLDIsImciXSxbMCwyLCJoIiwyXV0=

