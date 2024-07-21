---
title: "格上げ"
free: false
---

## 格上げ

離散圏$\mathbf 1$からある圏$\mathbf C$への関手を考える。

![1toC](https://storage.googleapis.com/zenn-user-upload/3ae17ee1d249-20231112.png)

https://q.uiver.app/#q=WzAsNSxbMCwxLCJcXGFzdCJdLFsyLDEsIkEiXSxbMywxLCJCIl0sWzAsMCwiXFxtYXRoYmYgMSJdLFsyLDAsIlxcbWF0aGJmIEMiXSxbMSwyLCJmIl1d

関手$F_A: \mathbf 1 \to \mathbf C$を$\mathbf 1$の対象$\ast$を$\mathbf C$の対象$A$に、関手$F_B: \mathbf 1 \to \mathbf C$を$\mathbf 1$の対象$\ast$を$\mathbf C$の対象$B$に写すものとすると、上図を下のように書き換えることができる。自然変換を強調するために、$\mathbf 1$に自明な射を書き足している。

![F_X](https://storage.googleapis.com/zenn-user-upload/625aca3e2471-20231206.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiAxIl0sWzAsMSwiXFxhc3QiXSxbMSwxLCJcXGFzdCJdLFszLDAsIlxcbWF0aGJmIEMiXSxbMywxLCJGX0EoXFxhc3QpIl0sWzQsMSwiRl9BKFxcYXN0KSJdLFszLDIsIkZfQihcXGFzdCkiXSxbNCwyLCJGX0IoXFxhc3QpIl0sWzEsMiwiaWRfXFxhc3QiXSxbNCw1LCJGX0EoaWRfXFxhc3QpID0gaWRfQSJdLFs2LDcsIkZfQihcXGFzdCkgPSBpZF9CIiwyXSxbNCw2LCJcXGV0YV9cXGFzdCA9IGYiLDJdLFs1LDcsIlxcZXRhX1xcYXN0ID0gZiJdXQ==

ここで$F_A(\ast) = A$, $F_B(\ast) = B$, $\eta_\ast = f$である。

一般に、$\mathbf C$の対象$X$を関手$F_X: \mathbf 1 \to \mathbf C$に、射$f: X \to Y$を自然変換$\eta: F_X \Rightarrow F_Y$に対応させることができる。
この対象を関手に、射を自然変換に対応させることを、格上げ(*Elevation*)と呼ぶ。

しばしば、格上げした対象をチルダを使って表すことがある。

- 圏$\mathbf C$の対象$A$から関手$F_A$への格上げ: $\tilde{A}: \mathbf 1 \to \mathbf C \overset{\mathrm{def}}{=} F_A$
- 圏$\mathbf C$の射$f: A \to B$から自然変換$\eta$への格上げ: $\tilde{f}: \tilde{A} \Rightarrow \tilde{B} \overset{\mathrm{def}}{=} \eta$

あるいは、まったく同一視してしまって、チルダを省略することもあるようだ。

チルダを使った記法で描くと、次のように関手圏$\mathbf C^{\mathbf 1}$の図を描ける。これは関手である対象と自然変換である射から構成される圏だ。

![C1](https://storage.googleapis.com/zenn-user-upload/ddc5f0d64ad1-20231206.png)

https://q.uiver.app/#q=WzAsMyxbMCwxLCJcXHRpbGRlIEEiXSxbMSwxLCJcXHRpbGRlIEIiXSxbMCwwLCJcXG1hdGhiZiBDIF4ge1xcbWF0aGJmIDF9Il0sWzAsMSwiXFx0aWxkZSBmIl1d
