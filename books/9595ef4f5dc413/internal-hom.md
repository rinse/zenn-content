---
title: "内部 hom 関手"
---

圏 $\mathbf{Set}$ において、hom 集合 $\hom_\mathbf{Set}(A, B)$ は、それ自体が $\mathbf{Set}$ の対象となる。
すなわち $A$ と $B$ の間の写像全体が集合である場合に、 $\hom_\mathbf{Set}(A, B) \in \mathrm{ob}(\mathbf{Set})$ が成り立つ。

これは便利な性質だが、当然ながら $\mathbf{Set}$ でしか成り立ちえない。内部 hom 関手は、そのような関手を一般化した概念である。

## 定義

内部 hom 関手 (*internal hom functor*) とは、双関手 $[-, -] : \mathbf C^\mathrm{op} \times \mathbf C \to \mathbf C$ であって、hom 関手のようにふるまう関手をいう。

また内部 hom 関手を持つ圏を閉圏 (*Closed category*) と呼ぶ。

特にカルテシアン閉圏やモノイダル閉圏では、積と内部 hom 関手との随伴 $- \otimes B \dashv [B, -]$ が成り立ち、この随伴を hom 集合で表した式 $\hom_\mathbf C(A \otimes B, C) \simeq \hom_\mathbf C(A, [B, C])$ は特にカリー化と呼ばれる。

## State モナド

一般に随伴関手からモナドが得られるが、この随伴 $- \otimes B \dashv [B, -]$ のモナドは State モナドとしてよく知られている。$F \dashv G$ のとき $G \circ F$ がモナドであったから、$[B, - \otimes B] : \mathbf C \to \mathbf C$ が State モナドである。

$[B, A \otimes B]$ は、$B$ を受け取って $A \otimes B$ を作る関数と解釈できる。
関数型プログラミング言語的には、ある状態 $B$ を受け取って、新しい値$A$と新しい状態 $B$ を返すような関数と解釈できる。

まずは随伴の unit と counit を見てみよう。

$$
\begin{aligned}
\eta &: \mathrm{Id} \Rightarrow [B, - \otimes B] \\
\epsilon &: [B, -] \otimes B \Rightarrow \mathrm{Id}
\end{aligned}
$$

それぞれの自然変換を State モナドの言葉で読み解いてみよう。

unit $\eta$ の成分は $\eta_A : A \to [B, A \otimes B]$ であり、値 $a$ を受け取って $b \mapsto a \otimes b$ なる関数を返す。すなわち、与えられた値をそのまま新しい値とし、状態 $b$ には手を触れずに返す計算である。これは関数型プログラミングでいう `return`（あるいは `pure`）にあたる。

counit $\epsilon$ の成分は $\epsilon_A : [B, A] \otimes B \to A$ であり、関数 $f$ と値 $b$ の組 $f \otimes b$ を受け取って $f(b)$ を返す。これは関数適用そのものである。とりわけ余域が値と状態の組 $A \otimes B$ である場合に限れば、これは「状態 $b$ を渡して計算 $f$ を走らせる」操作と読める。

そして乗法 $\mu$ は、[随伴はモナドを導く](./adjunctions-derive-monads) で見たように $\mu = G \ast \epsilon \ast F$ で与えられる。$G = [B, -]$, $F = - \otimes B$ を代入すると、その成分は次のようになる。

$$
\mu_A = [B, \epsilon_{A \otimes B}] : [B, [B, A \otimes B] \otimes B] \to [B, A \otimes B]
$$

始域 $[B, [B, A \otimes B] \otimes B]$ は $T^2(A) = T(T(A))$ に一致する。これは「状態 $b$ を受け取ると、別の計算 $g \in [B, A \otimes B]$ と新しい状態 $b'$ の組を返す」計算と読める。$\mu$ は内側の $\epsilon_{A \otimes B}$ によって、その $g$ を残った状態 $b'$ に対して走らせ、入れ子になった計算を一段ほどく。これは State モナドの `join` にほかならない。

このように、内部 hom 関手から定まる随伴 $- \otimes B \dashv [B, -]$ は、unit を `return`、乗法を入れ子の状態計算の平坦化とする State モナドを過不足なく与える。Haskell では `Writer` と `Reader` の随伴から同じモナドが得られる（[圏論の Haskell への応用](./haskell) を参照）。ただしそちらでは値と状態の組を `(s, a)` の順に取っているため、組の順序の規約だけがこのページと異なる。
