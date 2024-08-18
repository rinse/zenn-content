---
title: "同型"
free: false
---

圏論の議論の中心は、ある概念が別のある概念と「ほぼ同じ」ことを示すことにある。そのため「ほぼ同じ」を意味する同型(*Isomorphic*)は重要な概念だ。

## 定義

圏$\mathbf C$において、ある対象$A$と$B$とが同型であるとは、ある対象$A$, $B$に対してある射$f: A \to B$, $g: B \to A$が存在して$g \circ f = \mathrm{id}_A$, $f \circ g = \mathrm{id}_B$を満たすことをいい、以下のように書き表す。

$$
A \simeq B
$$

[![isomorphism](https://storage.googleapis.com/zenn-user-upload/50c54c9bdf2e-20240818.png)](https://q.uiver.app/#q=WzAsNSxbMCwxLCJBIl0sWzAsMiwiQSJdLFsxLDEsIkIiXSxbMCwwLCJcXG1hdGhiZntDfSJdLFsxLDIsIkIiXSxbMCwyLCJmIl0sWzIsMSwiZyIsMV0sWzAsMSwiXFxtYXRocm17aWR9X0EiLDJdLFsyLDQsIlxcbWF0aHJte2lkfV9CIl0sWzEsNCwiZiIsMl0sWzIsMSwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzIsMSwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

同型の定義は、上の可換図式でいうと、左上の$A$から$f$, $g$を通って左下の$A$に行く操作が$\mathbf{id}_A$に等しいことと、右上の$B$から$g$, $f$を通って右下の$B$に行く操作が$\mathbf{id}_B$に等しいことが同時に成り立つことを要求している。

このとき$A$と$B$とが「ほぼ同じ」、つまり同型であり、圏論の議論では同一のものと見なして問題ない。

## 記法

同型は合同(Congruent)の記号を使って以下のように書き表すこともある。

$$
A \cong B
$$

## 同型射と逆射

ある射$f: A \to B$に対して射$g: B \to A$が存在して$g \circ f = \mathrm{id}_A$かつ$f \circ g = \mathrm{id}_B$を満たすとき、そのような射$f$を同型射(*Isomorphism*)と呼ぶ。
またこのときの同型射$f$に対して、射$g$を逆射または単に逆(*Inverse*)と呼び、任意の$f$の逆射をしばしば$f^{-1}$と書く。

