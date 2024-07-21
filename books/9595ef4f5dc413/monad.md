---
title: "モナド"
free: false
---

## 定義

圏$\mathbf{C}$上のモナドは、関手$T: \mathbf{C} \to \mathbf{C}$と自然変換$\eta: 1_\mathbf{C} \to T$, $\mu: T^2 \to T$の3つ組$(T, \eta, \mu)$から成る。ただし$T^2 = T \circ T$である。
ここで自然変換$\eta$, $\mu$は以下の図式を可換にする。

![Coherence1](https://storage.googleapis.com/zenn-user-upload/8bfa4865f285-20231228.png)

https://q.uiver.app/#q=WzAsOSxbMCwxLCJUKFQoVChYKSkpIl0sWzEsMSwiVChUKFgpKSJdLFswLDIsIlQoVChYKSkiXSxbMSwyLCJUKFgpIl0sWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJUKFgpIl0sWzQsMSwiVChUKFgpKSJdLFszLDIsIlQoVChYKSkiXSxbNCwyLCJUKFgpIl0sWzEsMywiXFxtdV9YIl0sWzIsMywiXFxtdV9YIiwyXSxbMCwyLCJUKFxcbXVfWCkiLDJdLFswLDEsIlxcbXVfe1QoWCl9Il0sWzUsNiwiXFxldGFfe1QoWCl9Il0sWzUsNywiVChcXGV0YV9YKSIsMl0sWzYsOCwiXFxtdV9YIl0sWzcsOCwiXFxtdV9YIiwyXSxbNSw4LCJcXG1hdGhybXtpZH1fe1QoWCl9IiwxXV0=

## 自己関手の圏におけるモナド

[定義](#定義)で示した可換図式を、$\mathbf{C} \to \mathbf{C}$の関手を対象とする関手圏$\mathbf{C}^{\mathbf{C}}$の上に書き直すことができる。

![Coherence2](https://storage.googleapis.com/zenn-user-upload/fd02b315e178-20231228.png)

https://q.uiver.app/#q=WzAsOSxbMCwxLCJUXjMiXSxbMSwxLCJUXjIiXSxbMCwyLCJUXjIiXSxbMSwyLCJUIl0sWzAsMCwiXFxtYXRoYmZ7Q31ee1xcbWF0aGJme0N9fSJdLFszLDEsIlQiXSxbNCwxLCJUXjIiXSxbMywyLCJUXjIiXSxbNCwyLCJUIl0sWzEsMywiXFxtdSJdLFsyLDMsIlxcbXUiLDJdLFswLDIsIlQgXFxhc3QgXFxtdSIsMl0sWzAsMSwiXFxtdSBcXGFzdCBUIl0sWzUsNiwiXFxldGEgXFxhc3QgVCJdLFs1LDcsIlQgXFxhc3QgXFxldGEiLDJdLFs2LDgsIlxcbXUiXSxbNyw4LCJcXG11IiwyXSxbNSw4LCIxX1QiLDFdXQ==

この可換図式の主張するところは、以下の2点を示唆する:

1. $\mu \ast T = T \ast \mu$
    - 左辺は$T^2 \circ T \to T \circ T$であり、整理すると$T^3 \to T^2$となる
    - 右辺は$T \circ T^2 \to T \circ T$であり、整理すると$T^3 \to T^2$となる
3. $\eta \ast T = T \ast \eta$
    - 左辺は$1_C \circ T \to T \circ T$であり、整理すると$T \to T^2$となる
    - 右辺は$T \circ 1_C \to T \circ T$であり、整理すると$T \to T^2$となる

## モノイダル圏のモノイド対象としてのモナド

自己関手圏において、関手の合成をモノイダル積とする、強モノイダル圏$\mathbf{C}^\mathbf{C}$を構成できる。

1. 関手の合成$\circ: \mathbf{C}^\mathbf{C} \times \mathbf{C}^\mathbf{C} \to \mathbf{C}^\mathbf{C}$を、モノイダル積として定める。関数合成と紛らわしいので、以後$\otimes$と書く。
2. 自己関手の圏$\mathbf{C}^\mathbf{C}$には対象として恒等関手$1_C$が自明に存在する。これを単位対象に定める。
3. 関手の合成は結合的な演算であるから、モノイダル積の結合律を保証する自明な射$1$が存在する。
    - $G(F(A)) = (G \circ F)(A)$なので、$1$は（単なる自然同型ではなく）自明な射(各対象に対して恒等射となる)のはず。
    - 証明は[関手の合成](https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/91e65c#%E9%96%A2%E6%89%8B%E3%81%AE%E5%90%88%E6%88%90)を参照。
4. $1_C \circ T = T$であるから、左単位律を保証する自明な射$1_T$が存在する。
5. $T \circ 1_C = T$であるから、右単位律を保証する自明な射$1_T$が存在する。

![Monoidal_coherence](https://storage.googleapis.com/zenn-user-upload/4470dbbad7df-20231228.png)

https://q.uiver.app/#q=WzAsOSxbMCw0LCIoQSBcXG90aW1lcyAxX0MpIFxcb3RpbWVzIEIiXSxbMiw0LCJBIFxcb3RpbWVzICgxX0MgXFxvdGltZXMgQikiXSxbMSw1LCJBIFxcb3RpbWVzIEIiXSxbMCwwLCJcXG1hdGhiZntDfV5cXG1hdGhiZntDfSJdLFswLDEsIigoQSBcXG90aW1lcyBCKSBcXG90aW1lcyBDKSBcXG90aW1lcyBEIl0sWzIsMSwiKEEgXFxvdGltZXMgKEIgXFxvdGltZXMgQykpIFxcb3RpbWVzIEQiXSxbMCwzLCIoQSBcXG90aW1lcyBCKSBcXG90aW1lcyAoQyBcXG90aW1lcyBEKSJdLFsyLDIsIkEgXFxvdGltZXMgKChCIFxcb3RpbWVzIEMpIFxcb3RpbWVzIEQpIl0sWzIsMywiQSBcXG90aW1lcyAoQiBcXG90aW1lcyAoQyBcXG90aW1lcyBEKSkiXSxbMCwxLCIxX3tBIFxcb3RpbWVzIDFfQyBcXG90aW1lcyBCfSJdLFswLDIsIjFfQSBcXG90aW1lcyAxX0IiLDJdLFsxLDIsIjFfQSBcXG90aW1lcyAxX0IiXSxbNCw1LCIxX3soQSBcXG90aW1lcyBCIFxcb3RpbWVzIEMpfSBcXG90aW1lcyAxX0QiXSxbNCw2LCIxX3tBIFxcb3RpbWVzIEIgXFxvdGltZXMgQyBcXG90aW1lcyBEfSIsMl0sWzYsOCwiMV97QSBcXG90aW1lcyBCIFxcb3RpbWVzIEMgXFxvdGltZXMgRH0iLDJdLFs1LDcsIjFfe0EgXFxvdGltZXMgQiBcXG90aW1lcyBDIFxcb3RpbWVzIER9Il0sWzcsOCwiMV9BIFxcb3RpbWVzIDFfe0IgXFxvdGltZXMgQyBcXG90aW1lcyBEfSJdXQ==

ここで、構成したモノイダル圏($\mathbf{C}^\mathbf{C}$, $\circ$, $1_C$, $1$, $1$, $1$)のモノイド対象($M$, $\mu$, $\eta$)はモナドである。
すなわち以下を満たすような$\mathbf{C}^\mathbf{C}$の対象$M$, $\mu: M \otimes M \to M$, $\eta: I \to M$を考える。

![Coherence3](https://storage.googleapis.com/zenn-user-upload/8f7a348bee91-20231228.png)

三角形からは下の図式を描けるから、自己関手の合成をモノイダル積とする圏におけるモノイド対象はモナドである。

![Coherence4](https://storage.googleapis.com/zenn-user-upload/176517e81aca-20231228.png)

https://q.uiver.app/#q=WzAsMTQsWzAsMCwiXFxtYXRoYmZ7Q31eXFxtYXRoYmZ7Q30iXSxbMCwxLCIoTSBcXG90aW1lcyBNKSBcXG90aW1lcyBNIl0sWzIsMSwiTSBcXG90aW1lcyAoTSBcXG90aW1lcyBNKSJdLFswLDIsIk0gXFxvdGltZXMgTSJdLFsyLDIsIk0gXFxvdGltZXMgTSJdLFsxLDMsIk0iXSxbMCw0LCJNIFxcb3RpbWVzIDFfQyJdLFsxLDQsIk0gXFxvdGltZXMgTSJdLFsyLDQsIjFfQyBcXG90aW1lcyBNIl0sWzEsNSwiTSJdLFsxLDYsIk0gXFxvdGltZXMgTSJdLFswLDYsIk0iXSxbMCw3LCJNIFxcb3RpbWVzIE0iXSxbMSw3LCJNIl0sWzEsMiwiMV97TSBcXG90aW1lcyBNIFxcb3RpbWVzIE19Il0sWzEsMywiXFxtdSBcXG90aW1lcyAxX00iLDJdLFsyLDQsIjFfTSBcXG90aW1lcyBcXG11Il0sWzMsNSwiXFxtdSIsMl0sWzQsNSwiXFxtdSJdLFs2LDcsIjFfTSBcXG90aW1lcyBcXGV0YSJdLFs4LDcsIlxcZXRhIFxcb3RpbWVzIDFfTSIsMl0sWzYsOSwiXFxyaG8iLDJdLFs4LDksIlxcbGFtYmRhIl0sWzcsOSwiXFxtdSJdLFsxMSwxMywiMV9NIiwxXSxbMTEsMTIsIjFfTSBcXG90aW1lcyBcXGV0YSIsMl0sWzExLDEwLCJcXGV0YSBcXG90aW1lcyBNIl0sWzEwLDEzLCJcXG11Il0sWzEyLDEzLCJcXG11IiwyXV0=
