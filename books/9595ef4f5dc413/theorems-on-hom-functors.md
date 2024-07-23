---
title: "対象と射は同一視できる"
free: false
---

## 定理

ある圏$\mathbf{C}$の任意の対象$X$, $Y$について$\hom_C(A, X) \simeq \hom_C(A, Y)$が成り立つとき、$X \simeq Y$が成り立つ。

### 証明

$X \simeq Y$とは、$f: X \to Y$, $g: Y \to X$が存在して、$g \circ f = \mathrm{id}_X$, $f \circ g = \mathrm{id}_Y$を満たすことをいうのであった。
また$\hom_C(A, f) \overset{\mathrm{def}}{=} g \mapsto f \circ g$であった。これを簡単のために$f \circ -$と書くことにする。

$\hom_C(A, X) \simeq \hom_C(A, Y)$であるとき、以下の条件を満たす2つの射$f \circ - : \hom_C(A, X) \to \hom_C(A, Y)$, $g \circ - \hom_C(A, Y) \to \hom_C(A, X)$が存在する。

$$
\begin{align}
(g \circ -) \circ (f \circ -) = \mathrm{id}_{\hom_C(A, X)} \\
(f \circ -) \circ (g \circ -) = \mathrm{id}_{\hom_C(A, Y)}
\end{align}
$$

ここで適当な射$h: A \to X$に条件1に適用すると、$(g \circ f) \circ h = h$が得られる。

$$
\begin{aligned}
((g \circ -) \circ (f \circ -))(h) &= \mathrm{id}_{\hom_C(A, X)}(h) \\
((g \circ -) \circ (f \circ -))(h) &= h \\
g \circ (f \circ h) &= h \\
(g \circ f) \circ h &= h
\end{aligned}
$$

これで$g \circ f = \mathrm{id}_X$が確認できた。

同様にして適当な射$k: A \to Y$に条件2に適用すると、$(f \circ g) \circ k = k$が得られる。

$$
\begin{aligned}
((f \circ -) \circ (g \circ -))(k) &= \mathrm{id}_{\hom_C(A, Y)}(k) \\
((f \circ -) \circ (g \circ -))(k) &= k \\
f \circ (g \circ k) &= k \\
(f \circ g) \circ k &= k
\end{aligned}
$$

これで$f \circ g = \mathrm{id}_Y$が確認できた。

これにより$X \simeq Y$が確認できたので、証明終了。
