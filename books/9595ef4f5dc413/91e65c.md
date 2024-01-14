---
title: "関手"
free: false
---

## 定義

圏の対象と射とをそれぞれ別の圏に写すものを関手(*Functor*)と呼ぶ。
圏$\mathbf{C}$の対象と射を圏$\mathbf{D}$に写す関手を、$F: \mathbf{C} \to \mathbf{D}$のように書く。

共変関手(*Covariant functor*)$F: \mathbf C \to \mathbf D$は、$\mathbf C$の任意の対象$X$を、$\mathbf D$の対象$F(X)$に写す。
また$F$は$\mathbf C$の任意の射$f: X \to Y$を$\mathbf D$の射$F(f): F(X) \to F(Y)$に写し、以下を満たす:
- $\mathbf C$の任意の対象$X$について、$\mathbf D$において恒等射を保つ。すなわち$F(\mathrm{id}_X) = \mathrm{id}_{F(X)}$
- $\mathbf C$の任意の射$f: X \to Y$, $g: Y \to Z$について、$\mathbf D$において射の合成を保つ。すなわち$F(g \circ f) = F(g) \circ F(f)$

可換図式にすると次の通りだ。

![Covariant](https://storage.googleapis.com/zenn-user-upload/4a0b5faaf96f-20231203.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMSwiQSJdLFswLDAsIlxcbWF0aGJmIEMiXSxbNCwwLCJcXG1hdGhiZiBEIl0sWzQsMSwiRihBKSJdLFs0LDIsIkYoQSkiXSxbMCwyLCJBIl0sWzEsMSwiQiJdLFsyLDEsIkMiXSxbNSwxLCJGKEIpIl0sWzYsMSwiRihDKSJdLFswLDUsImlkX0EiLDJdLFswLDYsImYiXSxbNiw3LCJnIl0sWzMsNCwiRihpZF9BKSA9IGlkX3tGKEEpfSIsMl0sWzMsOCwiRihmKSJdLFs4LDksIkYoZykiXSxbNCw5LCJGKGcgXFxjaXJjIGYpID0gRihnKSBcXGNpcmMgRihmKSIsMix7ImxhYmVsX3Bvc2l0aW9uIjoxMDB9XSxbNSw3LCJnIFxcY2lyYyBmIiwyXV0=

反変関手(*Contravariant functor*)$F: \mathbf C \to \mathbf D$は、対象については共変関手と同様に任意の対象$X \in \mathrm{ob}(C)$を対象$F(X) \in \mathrm{ob}(D)$に写す。
しかし射については、$\mathbf C$の任意の射$f: X \to Y$を$\mathbf D$の射$F(f): F(Y) \to F(X)$に写す。
なお$\mathbf C$の全ての射の向きを逆転した双対圏(*Opposite category*)$\mathbf{C^{\mathrm{op}}}$を考えると、反変関手$F: \mathbf C \to \mathbf D$を共変関手$F': \mathbf{C^{\mathrm{op}}} \to \mathbf D$として捉えなおすことができる。

![Contravariant](https://storage.googleapis.com/zenn-user-upload/c8fe05bc2ec7-20231203.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMSwiQSJdLFswLDAsIlxcbWF0aGJmIEMiXSxbNCwwLCJcXG1hdGhiZiBEIl0sWzQsMSwiRihBKSJdLFs0LDIsIkYoQSkiXSxbMCwyLCJBIl0sWzEsMSwiQiJdLFsyLDEsIkMiXSxbNSwxLCJGKEIpIl0sWzYsMSwiRihDKSJdLFswLDUsImlkX0EiLDJdLFswLDYsImYiXSxbNiw3LCJnIl0sWzQsMywiRihpZF9BKSA9IGlkX3tGKEEpfSJdLFs4LDMsIkYoZikiLDJdLFs5LDgsIkYoZykiLDJdLFs5LDQsIkYoZyBcXGNpcmMgZikgPSBGKGcpIFxcY2lyYyBGKGYpIiwwLHsibGFiZWxfcG9zaXRpb24iOjB9XSxbNSw3LCJnIFxcY2lyYyBmIiwyXV0=

## 関手の合成

関手$F: \mathbf C \to \mathbf D$と関手$G: \mathbf D \to \mathbf E$があったとき、それら関手の合成$G \circ F: \mathbf C \to \mathbf E$は関手である。

![Composition of functors](https://storage.googleapis.com/zenn-user-upload/011e0ef08af7-20231013.png)

https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZiBDIl0sWzEsMCwiXFxtYXRoYmYgRCJdLFsxLDEsIlxcbWF0aGJmIEUiXSxbMCwxLCJGIl0sWzEsMiwiRyJdLFswLDIsIkcgXFxjaXJjIEYiLDJdXQ==

また任意の圏$\mathbf C$には恒等関手$1_C: \mathbf C \to \mathbf C$が存在して、任意の関手$F: \mathbf A \to \mathbf B$に対して$1_B \circ F = F \circ 1_A = F$を満たす。

### 証明

圏$\mathbf C$, $\mathbf D$, $\mathbf E$と関手$F: \mathbf C \to \mathbf D$, $G: \mathbf D \to \mathbf E$が与えられたとする。

このとき、これら関手の合成$G \circ F: \mathbf C \to \mathbf E$は、圏$\mathbf C$の任意の対象$X$を圏$\mathbf E$の対象$G(F(X))$に写し、また圏$\mathbf C$の任意の射$f: X \to Y$を圏$\mathbf E$の射$G(F(f)): G(F(X)) \to G(F(Y))$に写す。

ここで$F$は関手であるため、$\mathbf C$の任意の対象$X$について$\mathbf D$上で$F(\mathrm{id}_X) = \mathrm{id}_{F(X)}$が成り立つ。同様に$G$は関手であるため、$\mathbf D$の対象$F(X)$について$\mathbf E$上で$G(\mathrm{id}_{F(X)}) = \mathrm{id}_{G(F(X))}$が成り立つ。よって$\mathbf C$の任意の対象$X$について$\mathbf E$上で$G(F(\mathrm{id}_X)) = \mathrm{id}_{G(F(X))}$が成り立つため、$G \circ F$は恒等射を保存する。

また$F$は関手であるため、$\mathbf C$の任意の射$f: X \to Y$, $g: Y \to Z$について$F(g \circ f) = F(g) \circ F(f)$が成り立つ。同様に$G$は関手であるため、$\mathbf D$の射$F(f): F(X) \to F(Y)$, $F(g): F(Y) \to F(Z)$について$G(F(g) \circ F(f)) = G(F(g)) \circ G(F(f))$が成り立つ。よって$G(F(g \circ f)) = G(F(g)) \circ G(F(f))$が成り立つため、$G \circ F$は射の合成を保存する。

以上より$G \circ F: \mathbf C \to \mathbf E$は関手であると確認できた。

証明終わり。

## 関手の性質

1. 関手は可換性を保つ
2. 関手は同型射を保つ

## 関手の合成の記法

関手の合成の記法については、今回取り扱ったように$G \circ F$のように丁寧に書くものと、省略して$GF$のように書くものがある。
また$F; G$や$F \ggg G$のように図式順で書く場合がある。図式順の演算子は、特にString diagramを書く場合に便利だ。

恒等関手の記号については、今回使った$1_C$を使うほか$\mathrm{Id}_C$のように書く場合がある。このノートでは$1_C$で統一する。
また、恒等関手を小さな圏の圏の恒等射と見做すときには、$\mathrm{id}_C$のように書く。

## 圏の圏

すべての小さな圏のあつまりは圏$\mathbf{Cat}$をなす。この圏の対象はすべての小さな圏であり、射はすべての関手である。
なお、この圏自体は小さくない。
