---
title: "恒等な自然変換"
free: false
---

## 命題

圏$\mathbf{C}$, $\mathbf{D}$があったとき、任意の関手$F: \mathbf{C} \Rightarrow \mathbf{D}$に対して恒等な自然変換$1_F: F \Rightarrow F$が常に存在して、任意の自然変換$\eta: F \Rightarrow G$に対して以下を満たす。
 
$$
1_G \circ \eta = \eta \circ 1_F = \eta
$$

（ただし$\circ$は自然変換の[垂直合成](fa185d)）

### 証明

圏$\mathbf{C}$上の任意の射$f: X \to Y$における関手$F$の像$F(f): F(X) \to F(Y)$を考える。
圏$\mathbf{D}$には恒等射$\mathrm{id}_{F(X)}$, $\mathrm{id}_{F(Y)}$が常に存在して、自明に$\mathrm{id}_{F(Y)} \circ F(f) = F(f) \circ \mathrm{id}_{F(X)}$を満たす。

![identity_natural_formation](https://storage.googleapis.com/zenn-user-upload/75b869c8d059-20240401.png)

以上より、圏$\mathbf{C}$上の任意の対象$X$に対して圏$\mathbf{D}$上の射$\mathrm{id}_{F(X)}$を与える自然変換$1_F$が存在する。

また関手$F, G: \mathbf{C} \to \mathbf{D}$の間の任意の自然変換$\eta: F \Rightarrow G$を考えると、圏$\mathbf{C}$上の任意の対象$X$に対して圏$\mathbf{D}$上の射$\eta_X, \mathrm{id}_{G(X)} \circ \eta_X$, $\eta_X \circ \mathrm{id}_{F(X)}: F(X) \to G(X)$はそれぞれ自明に等しい。

![identity_law](https://storage.googleapis.com/zenn-user-upload/04ed88188038-20240401.png)

証明終わり。

https://q.uiver.app/#q=WzAsMTYsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMCwxLCJYIl0sWzMsMCwiXFxtYXRoYmZ7RH0iXSxbMywxLCJGKFgpIl0sWzEsMSwiWSJdLFs0LDEsIkYoWSkiXSxbMywyLCJGKFgpIl0sWzQsMiwiRihZKSJdLFs2LDIsIkYoWCkiXSxbNywyLCJGKFkpIl0sWzYsMywiRyhYKSJdLFs3LDMsIkcoWSkiXSxbNiw0LCJHKFgpIl0sWzcsNCwiRyhZKSJdLFs2LDEsIkYoWCkiXSxbNywxLCJGKFkpIl0sWzEsNCwiZiJdLFszLDUsIkYoZikiXSxbNiw3LCJGKGYpIiwyXSxbMyw2LCJcXG1hdGhybXtpZH1fe0YoWCl9IiwyXSxbNSw3LCJcXG1hdGhybXtpZH1fe0YoWSl9Il0sWzgsOSwiRihmKSJdLFsxMCwxMSwiRyhmKSIsMl0sWzgsMTAsIlxcZXRhX1giLDJdLFs5LDExLCJcXGV0YV9ZIl0sWzEyLDEzLCJHKGYpIiwyXSxbMTAsMTIsIlxcbWF0aHJte2lkfV97RyhYKX0iLDJdLFsxMSwxMywiXFxtYXRocm17aWR9X3tHKFkpfSJdLFsxNCw4LCJcXG1hdGhybXtpZH1fe0YoWCl9IiwyXSxbMTUsOSwiXFxtYXRocm17aWR9X3tGKFkpfSIsMl0sWzE0LDE1LCJGKGYpIl1d

## 恒等な自然変換の一意性

恒等な自然変換は常に単位射のあつまりである。
よってある関手の恒等な自然変換は一意である。

## 恒等な自然変換と水平合成

ある自然変換と恒等な自然変換との[水平合成](0f4e84)を考えると、これは単に自然変換と関手の水平合成である。

圏$\mathbf{C}$, $\mathbf{D}$, $\mathbf{E}$, 関手$F, F': \mathbf{C} \to \mathbf{D}$とその間の自然変換$\eta: F \Rightarrow F'$, 関手$G: \mathbf{D} \to \mathbf{E}$があるとき、$1_G \ast \eta = G \ast \eta: G \circ F \Rightarrow G \circ F'$である。

![horizontal_composition_1](https://storage.googleapis.com/zenn-user-upload/9cd7a3ffc9de-20240401.png)

https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywwLCJcXG1hdGhiZntEfSJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFszLDEsIkYoQykiXSxbNCwxLCJGKEMnKSJdLFszLDIsIkYnKEMpIl0sWzQsMiwiRicoQycpIl0sWzYsMCwiRSJdLFs2LDEsIkcoRihDKSkiXSxbNiwyLCJHKEYnKEMpKSJdLFs3LDEsIkcoRihDKSkiXSxbNywyLCJHKEYnKEMpKSJdLFsyLDMsImYiXSxbNCw1LCJGKGYpIl0sWzYsNywiRicoZikiLDJdLFs0LDYsIlxcZXRhX0MiLDJdLFs1LDcsIlxcZXRhX3tDJ30iXSxbOSwxMCwiRyhcXGV0YV9DKSIsMl0sWzksMTEsIlxcbWF0aHJte2lkfV97RyhGKEMpKX0iXSxbMTEsMTIsIkcoXFxldGFfQykiXSxbMTAsMTIsIlxcbWF0aHJte2lkfV97RyhGKEMpKX0iLDJdLFs5LDEyLCIxX0cgXFxhc3QgXFxldGEiLDFdXQ==


同様にして、圏$\mathbf{C}$, $\mathbf{D}$, $\mathbf{E}$, 関手$F: \mathbf{C} \to \mathbf{D}$, 関手$G, G': \mathbf{D} \to \mathbf{E}$とその間の自然変換$\epsilon: G \Rightarrow G'$があるとき、$\eta \ast 1_F = \eta \ast F: G \circ F \Rightarrow G' \circ F$である。

![horizontal_composition_2](https://storage.googleapis.com/zenn-user-upload/45ab3bcee8ec-20240401.png)

https://q.uiver.app/#q=WzAsMTMsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywwLCJcXG1hdGhiZntEfSJdLFswLDEsIkMiXSxbMSwxLCJDJyJdLFszLDEsIkYoQykiXSxbNCwxLCJGKEMnKSJdLFszLDIsIkYoQykiXSxbNCwyLCJGKEMnKSJdLFs2LDAsIkUiXSxbNiwxLCJHKEYoQykpIl0sWzYsMiwiRyhGKEMpKSJdLFs3LDEsIkcnKEYoQykpIl0sWzcsMiwiRycoRihDKSkiXSxbMiwzLCJmIl0sWzQsNSwiRihmKSJdLFs2LDcsIkYnKGYpIiwyXSxbNCw2LCJcXG1hdGhybXtpZH1fe0YoQycpfSIsMl0sWzUsNywiXFxtYXRocm17aWR9X3tGKEMnKX0iXSxbOSwxMCwiRyhcXG1hdGhybXtpZH1fe0YoQyl9KSIsMl0sWzksMTEsIlxcZXBzaWxvbl97RihDKX0iXSxbMTEsMTIsIkcoXFxtYXRocm17aWR9X3tGKEMpfSkiXSxbMTAsMTIsIlxcZXBzaWxvbl97RihDKX0iLDJdLFs5LDEyLCJcXGV0YSBcXGFzdCAxX0YiLDFdXQ==
