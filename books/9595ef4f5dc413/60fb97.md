---
title: "随伴関手2"
free: false
---

[随伴関手1](https://zenn.dev/esnir/books/9595ef4f5dc413/viewer/16aece)では、自然変換である単位$\eta: 1_{\mathbf D} \Rightarrow G \circ F$と余単位$\epsilon: F \circ G \Rightarrow 1_{\mathbf C}$をを用いて定義した。
ここでは同等の随伴関手を、hom集合を用いて定義する。

## 定義

局所的に小さな圏$\mathbf C$と$\mathbf D$の間の随伴とは、二つの関手$F: \mathbf D \to \mathbf C$, $G: \mathbf C \to \mathbf D$の対であって、任意の対象$X \in \mathrm{ob}(C)$, $Y \in \mathrm{ob}(D)$に対して集合の全単射$\hom_C(F(Y), X) \simeq \hom_D(Y, G(X))$が存在して、これが$X$と$Y$について自然となるものをいう。

このとき、関手$F$を左随伴関手, $G$を右随伴関手と呼び、$F$は$G$の左随伴であることを以下のように書く。

$$
F \dashv G
$$

これだけではわかりづらいので、図を書こう。まずは圏$\mathbf C$と圏$\mathbf D$、二つの関手$F: \mathbf D \to \mathbf C$, $G: \mathbf C \to \mathbf D$がある。

![Functors](https://storage.googleapis.com/zenn-user-upload/227caa452a94-20231020.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwxLCJYIl0sWzEsMSwiWCciXSxbMywxLCJZIl0sWzQsMSwiWSciXSxbMCwyLCJGKFkpIl0sWzEsMiwiRihZJykiXSxbMywyLCJHKFgpIl0sWzQsMiwiRyhYJykiXSxbMiwzLCJhIl0sWzgsOSwiRyhhKSIsMl0sWzUsNCwiYiIsMl0sWzcsNiwiRihiKSJdXQ==

圏$\mathbf C$と圏$\mathbf D$はそれぞれ局所的に小さいため、圏$\mathbf C$では$F(Y) \to X$の射の集合$\hom_C(F(Y), X)$、圏$\mathbf D$では$Y \to G(X)$の射の集合$\hom_D(Y, G(X))$を見つけることができる。
以下の図における$f$, $g$をそれぞれ$\hom_C(F(Y), X)$と$\hom_D(Y, G(X))$の要素に見立てている。

![Hom-set](https://storage.googleapis.com/zenn-user-upload/78ee289b4c8a-20231206.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwxLCJYIl0sWzEsMSwiWCciXSxbMywxLCJZIl0sWzQsMSwiWSciXSxbMCwyLCJGKFkpIl0sWzEsMiwiRihZJykiXSxbMywyLCJHKFgpIl0sWzQsMiwiRyhYJykiXSxbMiwzLCJhIl0sWzgsOSwiRyhhKSIsMl0sWzUsNCwiYiIsMl0sWzcsNiwiRihiKSJdLFs0LDgsImciLDJdLFs2LDIsImYiXV0=

この射の集合を見つける操作はhom関手と捉えられる。

そこで、この二つの関手を$\hom_C(F(\_), \_): \mathbf D^{op} \times \mathbf C \to \mathbf{Set}$, $\hom_D(\_, G(\_)): \mathbf D^{\mathrm{op}} \times \mathbf C \to \mathbf{Set}$と書くことにして、それらの自然変換$\Phi: \hom_C(F(\_), \_) \Rightarrow \hom_D(\_, G(\_))$を考える。

![Natural isomorphism](https://storage.googleapis.com/zenn-user-upload/fae9d9ee2f5b-20231020.png)

https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIEQiXSxbMCwxLCJYIl0sWzEsMSwiWCciXSxbMywxLCJZIl0sWzQsMSwiWSciXSxbMCwyLCJGKFkpIl0sWzEsMiwiRihZJykiXSxbMywyLCJHKFgpIl0sWzQsMiwiRyhYJykiXSxbNiwwLCJcXG1hdGhiZntTZXR9Il0sWzYsMSwiSG9tX0MoRihZKSwgWCkiXSxbOCwxLCJIb21fQyhGKFknKSwgWCcpIl0sWzYsMiwiSG9tX0QoWSwgRyhYKSkiXSxbOCwyLCJIb21fRChZJywgRyhYJykpIl0sWzIsMywiYSJdLFs4LDksIkcoYSkiLDJdLFsxMSwxMiwiSG9tX0MoRihiKSwgYSkiXSxbMTMsMTQsIkhvbV9EKGIsIEcoYSkpIiwyXSxbMTEsMTMsIlxcUGhpX3tZLCBYfSIsMl0sWzEyLDE0LCJcXFBoaV97WScsIFgnfSJdLFs1LDQsImIiLDJdLFs3LDYsIkYoYikiXSxbNCw4LCJIb20oWSwgRyhYKSkiLDIseyJsZXZlbCI6Mn1dLFs2LDIsIkhvbShGKFkpLCBYKSIsMCx7ImxldmVsIjoyfV1d

この自然変換$\Phi$が自然同型である場合、すなわち圏$\mathbf C$の任意の$X$, 圏$\mathbf D$の任意の$Y$に対して$\Phi_{Y, X} \in \hom_{Set}$が同型射である場合、関手$F$を$G$の左随伴と呼ぶことができる。

具体的には、圏$\mathbf C$の射$f \in \hom_C(F(Y), X)$をひとつ取ってきて、それに$\Phi_{Y, X}$を適用することで$\Phi_{Y, X}(f): Y \to G(X) \in \hom_D$を得ることができる。
$\Phi_{Y, X}$は同型射であるから、逆射$\Phi^{-1}_{Y, X}: \hom_D(Y, G(X)) \to \hom_C(F(Y), X)$が存在する。同様に$\mathbf D$の射$g \in \hom_D(Y, G(X))$をひとつ取ってきて、それに$\Phi^{-1}_{Y, X}$を適用することで$\Phi^{-1}_{Y, X}(g): F(Y) \to G$を得ることができる。

直感的には$f$から$g$を、$g$から$f$を得られるようなイメージであり、$F \dashv G$がある種の双対的な概念であることを示唆している。
