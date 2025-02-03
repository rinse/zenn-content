---
title: "自然変換のあつまり"
free: false
---

## 復習：射のあつまりと関手のあつまり

$A$から$B$への射のあつまりは、$\hom_C(A, B)$のように表すのだった。

また$\mathbf{C}$から$\mathbf{D}$への関手全体の関手圏を$\mathrm{Func}(\mathbf{C}, \mathbf{D})$と表すのだった。

## 自然変換のあつまり

圏$\mathbf{C}$から$\mathbf{D}$への関手$F$, $G$を考えるとき、$F$から$G$への自然変換のあつまりを考えることができる。これを関手圏$\mathbf{D}^C$の射のあつまりと考えることにして、次のように書くことにする：

$$
\hom_{D^C}(F, G)
$$

[![hom_fg](https://storage.googleapis.com/zenn-user-upload/105c68cc7b86-20250203.png)](https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMiwwLCJcXG1hdGhiZntEfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMSwiRihBKSJdLFszLDEsIkYoQikiXSxbMiwyLCJHKEEpIl0sWzMsMiwiRyhCKSJdLFs0LDAsIlxcbWF0aGJme0R9XkMiXSxbNCwxLCJGIl0sWzQsMiwiRyJdLFs1LDAsIlxcbWF0aGJme0NMQVNTfSJdLFs1LDEsIlxcaG9tX3tEXkN9KEYsIEcpIl0sWzIsMywiZiJdLFs0LDUsIkYoZikiXSxbNiw3XSxbNCw2LCJcXGV0YV9BIiwyXSxbNSw3LCJcXGV0YV9CIl0sWzksMTAsIlxcZXRhIl1d)

上図において$\eta$は$\hom_{D^C}(F, G)$の適当な要素である。

## 性質

- 一般に$\hom_{D^C}(F, C)$は集合になるとは限らない
- $\mathbf{D}$が集合の圏$\mathbf{Set}$である場合、$\mathbf{C}$が局所的に小さいに場合に限って、$\hom_{\mathrm{Set}^C}(F, G)$は集合になる（米田の補題）
