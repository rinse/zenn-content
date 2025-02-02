---
title: "hom関手"
free: false
---

[局所的に小さな圏](largeness-of-categories "任意の2対象間の射の全体が集合である圏")$\mathbf C$とは、任意の対象$A, B \in \rm{ob}(C)$に対して射のあつまり$\hom_C(A, B)$が集合をなすものである。

つまり局所的に小さな圏の対象を選ぶ操作は、$\mathbf C$から$\mathbf{Set}$への関手と捉えることができる。

## 定義

局所的に小さな圏$\mathbf C$の対象$A$を固定して、共変関手$\hom_C(A, \_): \mathbf C \to \mathbf{Set}$を次のように定義する。

* 圏$\mathbf C$の任意の対象$X$を圏$\mathbf{Set}$の対象$\hom_C(A, X)$に写す
* 圏$\mathbf C$の任意の射$f: X \to Y$を圏$\mathbf {Set}$の射$\hom_C(A, f): \hom_C(A, X) \to \hom_C(A, Y)$に写す
    * ただし$\hom_C(A, f) \overset{\mathrm{def}}{=} g \mapsto f \circ g$
        * ここで引数$g$は$A \to X$

可換図式で表現すると次の通りだ。

[![hom_C(A, _)](https://storage.googleapis.com/zenn-user-upload/63a44bdf2889-20250202.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiQSJdLFswLDIsIlgiXSxbMSwyLCJZIl0sWzQsMCwiXFxtYXRoYmZ7U2V0fSJdLFs0LDEsIlxcaG9tX0MoQSwgQSkiXSxbNCwzLCJcXGhvbV9DKEEsIFgpIl0sWzYsMywiXFxob21fQyhBLCBZKSJdLFsxLDIsImciLDJdLFsyLDMsImYiLDJdLFsxLDMsImYgXFxjaXJjIGciXSxbNSw3LCJcXGhvbV9DKEEsIGYgXFxjaXJjIGcpID0gZSBcXG1hcHN0byBmIFxcY2lyYyBnIFxcY2lyYyBlIiwwLHsibGFiZWxfcG9zaXRpb24iOjEwMH1dLFs2LDcsIlxcaG9tX0MoQSwgZikgPSBnIFxcbWFwc3RvIGYgXFxjaXJjIGciLDJdLFs1LDYsIlxcaG9tX0MoQSwgZykgPSBlIFxcbWFwc3RvIGcgXFxjaXJjIGUiLDJdXQ==)

## 反変hom関手

同様にして、局所的に小さな圏$\mathbf C$の対象$B$を固定して、反変関手$\hom_C(\_, B): \mathbf C^{\mathrm{op}} \to \mathbf{Set}$を次のように定義する。

* 圏$\mathbf C$の対象$X$を圏$\mathbf{Set}$の対象$\hom_C(X, B)$に写す
* 圏$\mathbf C$の射$X \to Y$を$\hom_C(h, B): \hom_C(Y, B) \to \hom_C(X, B)$に写す
    * ただし$\hom_C(h, B)$は$g \mapsto g \circ h$で定義される
        * ここで引数$g$は$X \to B$

可換図式で表現すると次の通りだ。

[![hom_C(_, B)](https://storage.googleapis.com/zenn-user-upload/9c5105f17420-20250202.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiWCJdLFsxLDEsIlkiXSxbNCwwLCJcXG1hdGhiZntTZXR9Il0sWzQsMywiXFxob21fQyhCLCBCKSJdLFs0LDEsIlxcaG9tX0MoWCwgQikiXSxbNiwxLCJcXGhvbV9DKFksIEIpIl0sWzAsMiwiQiJdLFsyLDEsImgiLDJdLFsxLDcsImciLDJdLFs3LDIsImcgXFxjaXJjIGgiLDJdLFs1LDYsIlxcaG9tX0MoaCwgQik9ZyBcXG1hcHN0byBnIFxcY2lyYyBoIl0sWzQsNSwiXFxob21fQyhnLCBCKT1lIFxcbWFwc3RvIGUgXFxjaXJjIGciXSxbNCw2LCJcXGhvbV9DKGcgXFxjaXJjIGgsIEIpPWUgXFxtYXBzdG8gZSBcXGNpcmMgZyBcXGNpcmMgaCIsMix7ImxhYmVsX3Bvc2l0aW9uIjo5MH1dXQ==)

上の二つの可換図をぴったり重ね合わせると、次の可換図式が得られる。
$\hom_C(A, \_)$の可換図式の$X$, $Y$を$B$, $B'$に、$\hom_C(\_, B)$の可換図式の$X$, $Y$を$A$, $A'$に対応させる。$g$はそのままだ。

[![hom_C(_, _)](https://storage.googleapis.com/zenn-user-upload/cf017af934f2-20250202.png)](https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFs0LDAsIlxcbWF0aGJme1NldH0iXSxbNCwxLCJcXGhvbV9DKEEsIEIpIl0sWzQsMywiXFxob21fQyhBJywgQikiXSxbNiwxLCJcXGhvbV9DKEEsIEInKSJdLFs2LDMsIlxcaG9tX0MoQScsIEInKSJdLFswLDEsIkEiXSxbMSwxLCJBJyJdLFswLDIsIkIiXSxbMSwyLCJCJyJdLFsyLDMsIlxcaG9tX0MoaCwgQikgPSBnIFxcbWFwc3RvIGcgXFxjaXJjIGgiLDJdLFsyLDQsIlxcaG9tX0MoQSwgZikgPSBnIFxcbWFwc3RvIGYgXFxjaXJjIGciXSxbMyw1LCJcXGhvbV9DKEEnLCBmKT1naCBcXG1hcHN0byBmIFxcY2lyYyBnaCIsMl0sWzQsNSwiXFxob21fQyhoLCBCJyk9ZmcgXFxtYXBzdG8gZmcgXFxjaXJjIGgiXSxbOCw5LCJmIiwyXSxbNyw2LCJoIiwyXSxbNiw4LCJnIiwyXSxbNyw5LCJmIFxcY2lyYyBnIFxcY2lyYyBoIl1d)

上の可換図式は、双関手$\hom_C(\_, \_): \mathbf{C^{\rm{op}}} \times \mathbf C \to \mathbf{Set}$を表している。

なお圏$\mathbf{C^{\rm{op}}}$は圏$\mathbf C$のすべての射を反転させた双対圏であり、$\mathbf C$から$\mathbf{Set}$への反変関手は、$\mathbf{C^{\rm{op}}}$から$\mathbf{Set}$への共変関手とみなすことができる。

## 表記

* hom関手は、先頭を大文字にして$\rm{Hom}_C(A, B)$と書くこともある。
    * このノートではtexでの書きやすさを優先して、hom関手と書くことにする。
* hom関手によって写された射$f$の像$\hom_C(A, f)$を$f \circ -$と書くこともある。
    * また反変hom関手によって写された射$f$の像$\hom_C(f, A)$を$- \circ f$と書くこともある。
    * これらは$\hom_C(A, f)$と書くよりも短く、また計算する際も便利であるため、このノートでもしばしば用いる。
* $A$を固定した共変hom関手$\hom_C(A, \_)$を$H^A : \mathbf{C} \to \mathbf{Set}$と書くことがある。
    * このとき$A$を固定した反変hom関手$\hom_C(\_, A)$を$H_A : \mathbf{C}^{\mathrm{op}} \to \mathbf{Set}$と書く。
    * また$A$を固定する操作も動かすは場合$H^- : \mathbf{C} \to \mathbf{Set}^C$のように書く。
    * 同様に$H_- : \mathbf{C} \to \mathbf{Set}^{C^{\mathrm{op}}}$のように書く。
    * $H^-$, $H_-$はともに双関手$\hom_C(\_, \_)$の冪転置(exponential transpose)である。ゆえにこれらはすべて同型である。
        - 参考: デカルト閉圏(*Cartesian closed category*)
    * hom関手を得る関手$H^-$, $H_-$ は[米田埋め込み](yoneda-embedding)と呼ばれる。
