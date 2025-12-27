---
title: "パワーとコパワー"
---

## 定義

集合 $X \in \mathbf{Set}$と対象$C \in \mathbf C$の power とは、$A \in \mathbf C$について自然に

$$
\hom_\mathbf C(A, X \pitchfork C) \simeq \hom_\mathbf{Set}(X, \hom_\mathbf C(A, C))
$$

が成り立つ対象$X \pitchfork C \in \mathbf C$のことをいう。

## 双対

集合 $X \in \mathbf{Set}$と対象$C \in \mathbf C$の copower とは、$A \in \mathbf C$について自然に

$$
\hom_\mathbf C(X \odot C, A) \simeq \hom_\mathbf{Set}(X, \hom_\mathbf C(C, A))
$$

が成り立つ対象$x \odot C \in \mathbf C$のことをいう。

## Setにおけるパワー

圏$\mathbf{Set}$においては、パワーはHomセットに一致する。

$$
X \pitchfork A \simeq \hom_\mathbf{Set}(X, A)
$$

これは定義に照らせば簡単に確認できる。

$$
\begin{aligned}
\hom_\mathbf{Set}(X, \hom_\mathbf{Set}(A, C))
&\simeq \hom_\mathbf{Set}(A, X \pitchfork C) \\
&\simeq \hom_\mathbf{Set}(A, \hom_{\mathbf{Set}}(X, C)) \\
\end{aligned}
$$

集合の圏においては、ホムセット$\hom_\mathbf{Set}(A, B)$が集合の圏における指数対象$B^A$に一致するから、冪 (power) という命名に得心が行く。

### Setにおけるコパワー

圏$\mathbf{Set}$においては、コパワーは直積に一致する。

$$
X \odot A \simeq X \times A
$$

これも定義に照らせば簡単に確認できる。

$$
\begin{aligned}
\hom_\mathbf{Set}(X, \hom_\mathbf{Set}(C, A)) &\simeq \hom_\mathbf{Set}(X \times C, A)
\end{aligned}
$$

## 疑問

パワーとコパワーは、カルテシアン閉とはどのような関係があるのだろう？
