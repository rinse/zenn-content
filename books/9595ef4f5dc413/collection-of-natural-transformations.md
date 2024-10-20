---
title: "自然変換のあつまり"
free: false
---

## 復習：射のあつまりと関手のあつまり

$A$から$B$への射のあつまりは、$\hom_C(A, B)$のように表すのだった。

また$\mathbf{C}$から$\mathbf{D}$への関手全体の関手圏を$\mathrm{Func}(\mathbf{C}, \mathbf{D})$と表すのだった。

## 自然変換のあつまり

圏$\mathbf{C}$から$\mathbf{D}$への関手$F$, $G$を考えるとき、$F$から$G$への自然変換のあつまりを考えることができる。これを次のように書くことにする：

$$
\mathrm{Nat}(F, G)
$$

この$\mathrm{Nat}(F, G)$は、例えば$\eta: F \Rightarrow G$や$\epsilon: F \Rightarrow G$などのあつまりということだ。

各自然変換は圏$\mathbf{C}$の対象で添え字づけられた圏$\mathbf{D}$の射のあつまりなので、圏$\mathbf{D}$の射のあつまりのあつまりでもある。

[![collection-of-natural-transformations](https://storage.googleapis.com/zenn-user-upload/58a52f150ac4-20240819.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMCwiXFxtYXRoYmZ7RH0iXSxbMiwxLCJGKEEpIl0sWzMsMSwiRihCKSJdLFsyLDIsIkcoQSkiXSxbMywyLCJHKEIpIl0sWzQsNSwiRihmKSJdLFs2LDcsIkcoZikiLDJdLFs1LDcsIlxcZXRhX0IiLDIseyJvZmZzZXQiOjF9XSxbNCw2LCJcXGV0YV9BIiwyLHsib2Zmc2V0IjoxfV0sWzAsMywiRiIsMCx7Im9mZnNldCI6LTJ9XSxbMCwzLCJHIiwyLHsib2Zmc2V0IjoyfV0sWzEsMiwiZiJdLFs0LDYsIlxcZXBzaWxvbl9BIiwwLHsib2Zmc2V0IjotMX1dLFs1LDcsIlxcZXBzaWxvbl9CIiwwLHsib2Zmc2V0IjotMX1dXQ==)

## 記法

米田の補題では括弧が多く利用されるため、$\mathrm{Nat}(F, G)$では見づらい気がする。

$\mathrm{Nat}(F \Rightarrow G)$とかの方が分かりやすいだろうか？
