---
title: "随伴関手3"
free: false
---

随伴関手は普遍射を用いても同等の定義を得ることができる。

## 右随伴

圏$\mathbf{C}$, 圏$\mathbf{D}$とそれらの間の関手$G: \mathbf{C} \to \mathbf{D}$を考える。

圏$\mathbf{D}$の任意の対象$X$から$G$への普遍射が存在するとき、ある関手$F: \mathbf{D} \to \mathbf{C}$が存在して、$F \dashv G$を満たす。
すなわち$G$は$F$の右随伴である。

$A$から$G$への普遍射とは、組$(X, u)$であって、圏$\mathbf{D}$の任意の射$f: A \to G(Y)$を分解する圏$\mathbf{C}$の射$g: X \to Y$が一意に存在するものをいうのであった。

![right-universal-arrow](https://storage.googleapis.com/zenn-user-upload/b2467bcad800-20240801.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMSwiQSJdLFszLDEsIkcoWCkiXSxbMywyLCJHKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzIsMywiRyhnKSJdLFsxLDMsImYiLDJdLFs1LDYsImciLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMSwyLCJ1Il1d

いま、2つの普遍射を考える。すなわち$A_1$から$G$への普遍射$(X_1, u_1)$と$A_2$から$G$への普遍射$(X_2, u_2)$である。

![two-right-universal-arrows](https://storage.googleapis.com/zenn-user-upload/3694e55ccc9a-20240801.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMSwiQSJdLFszLDEsIkcoWCkiXSxbMywyLCJHKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzIsMywiRyhnKSJdLFsxLDMsImYiLDJdLFs1LDYsImciLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMSwyLCJ1Il1d

このとき普遍性により任意の$h: A_1 \to A_2$に対して$u_2 \circ h = G(g) \circ u_1$を満たす$g: X_1 \to X_2$が一意に存在する。
すなわち圏$\mathbf{D}$の射$h$に対して圏$\mathbf{C}$の射$g$を対応させることができる。また圏$\mathbf{D}$の対象$A_i$を圏$\mathbf{C}$の対象$X_i$に対応させることを考えれば、これらの対応は$\mathbf{D}$から$\mathbf{C}$への関手を成す。

すなわち関手$F: \mathbf{D} \to \mathbf{C}$を次のように定義できる。

- $F(A_i) \overset{\mathrm{def}}{=} X_i$
- $F(h) \overset{\mathrm{def}}{=} g$

このようにしたとき$F$は$G$の左随伴関手である。（同じことだが$G$は$F$の右随伴である。）

## 左随伴から右随伴を得る

同じようにして、$F: \mathbf{D} \to \mathbf{C}$から圏$\mathbf{C}$の任意の対象$X$への普遍射が存在するとき、ある関手$G: \mathbf{C} \to \mathbf {D}$が存在して、$F \dashv G$を満たす。

## 疑問

右随伴関手から左随伴関手を得たとき、 圏$\mathbf{C}$の要素を$F$を使って次のように書ける。

![GF](https://storage.googleapis.com/zenn-user-upload/39487c951ba5-20240801.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFsyLDAsIlxcbWF0aGJme0R9Il0sWzAsMSwiRihBXzEpIl0sWzAsMiwiRihBXzIpIl0sWzIsMSwiQV8xIl0sWzMsMSwiRyhGKEFfMSkpIl0sWzMsMiwiRyhGKEFfMikpIl0sWzIsMiwiQV8yIl0sWzIsMywiRihoKSJdLFs0LDUsInVfMSJdLFs1LDYsIkcoRihoKSkiXSxbMCwxLCJHIiwwLHsib2Zmc2V0IjotMn1dLFs0LDcsImgiLDJdLFs3LDYsInVfMiIsMl0sWzEsMCwiRiIsMCx7Im9mZnNldCI6LTJ9XV0=

このとき普遍性により$G(F(h)) \circ u_1 = u_2 \circ h$を満たすから、$u_i: A_i \to G(F(A_i))$を自然変換$1_{\mathbf{D}} \Rightarrow G \circ F$と捉えることができる。
この$u_i$は明らかに[unit](adjoint-functors1#定義)である。

$F \dashv G$が成り立つのであれば、ここから[counit](adjoint-functors1#定義)も得ることができるはずだが、それはどうすれば得られるのだろうか？

同じ議論だが、左随伴関手から右随伴関手を得るときにはcounitを得られるが、ここからunitをどう得るのだろうか？

