---
title: "hom関手"
free: false
---

局所的に小さな圏$\mathbf C$とは、任意の対象$A, B \in \rm{ob}(C)$に対して射のあつまり$\hom_C(A, B)$が集合をなすものである。

つまり局所的に小さな圏の対象を選ぶ操作は、$\mathbf C$から$\mathbf{Set}$への関手と捉えることができる。

## 定義

局所的に小さな圏$\mathbf C$の対象$A$を固定して、共変関手$\hom_C(A, \_): \mathbf C \to \mathbf{Set}$を次のように定義する。

* 圏$\mathbf C$の任意の対象$X$を圏$\mathbf{Set}$の対象$\hom_C(A, X)$に写す
* 圏$\mathbf C$の任意の射$f: X \to Y$を圏$\mathbf {Set}$の射$\hom_C(A, f): \hom_C(A, X) \to \hom_C(A, Y)$に写す
    * ただし$\hom_C(A, f) \overset{\mathrm{def}}{=} g \mapsto f \circ g$
        * ここで引数$g$は$A \to X$

可換図式で表現すると次の通りだ。

![Hom_C(A, _)](https://storage.googleapis.com/zenn-user-upload/987e0d5ebbbb-20231205.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiQSJdLFswLDIsIlgiXSxbMSwyLCJZIl0sWzQsMCwiXFxtYXRoYmZ7U2V0fSJdLFs0LDEsIkhvbV9DKEEsIEEpIl0sWzQsMywiSG9tX0MoQSwgWCkiXSxbNiwzLCJIb21fQyhBLCBZKSJdLFsxLDIsImciLDJdLFsyLDMsImYiLDJdLFsxLDMsImYgXFxjaXJjIGciXSxbNSw3LCJIb21fQyhBLCBmIFxcY2lyYyBnKSA9IGUgXFxtYXBzdG8gZiBcXGNpcmMgZyBcXGNpcmMgZSIsMCx7ImxhYmVsX3Bvc2l0aW9uIjoxMDB9XSxbNiw3LCJIb21fQyhBLCBmKSA9IGcgXFxtYXBzdG8gZiBcXGNpcmMgZyIsMl0sWzUsNiwiSG9tX0MoQSwgZykgPSBlIFxcbWFwc3RvIGcgXFxjaXJjIGUiLDJdXQ==

同様にして、双対を考える。局所的に小さな圏$\mathbf C$の対象$B$を固定して、反変関手$\hom_C(\_, B): \mathbf C \to \mathbf{Set}$を次のように定義する。

* 圏$\mathbf C$の対象$X$を圏$\mathbf{Set}$の対象$\hom_C(X, B)$に写す
* 圏$\mathbf C$の射$X \to Y$を$\hom_C(h, B): \hom_C(Y, B) \to \hom_C(X, B)$に写す
    * ただし$\hom_C(h, B)$は$g \mapsto g \circ h$で定義される
        * ここで引数$g$は$X \to B$

可換図式で表現すると次の通りだ。

![Hom_C(_, B)](https://storage.googleapis.com/zenn-user-upload/4d69d9135eec-20231205.png)

https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiWCJdLFsxLDEsIlkiXSxbNCwwLCJcXG1hdGhiZntTZXR9Il0sWzQsMywiSG9tX0MoQiwgQikiXSxbNCwxLCJIb21fQyhYLCBCKSJdLFs2LDEsIkhvbV9DKFksIEIpIl0sWzAsMiwiQiJdLFsyLDEsImgiLDJdLFsxLDcsImciLDJdLFs3LDIsImcgXFxjaXJjIGgiLDJdLFs1LDYsIkhvbV9DKGgsIEIpPWcgXFxtYXBzdG8gZyBcXGNpcmMgaCJdLFs0LDUsIkhvbV9DKGcsIEIpPWUgXFxtYXBzdG8gZSBcXGNpcmMgZyJdLFs0LDYsIkhvbV9DKGcgXFxjaXJjIGgsIEIpPWUgXFxtYXBzdG8gZSBcXGNpcmMgZyBcXGNpcmMgaCIsMix7ImxhYmVsX3Bvc2l0aW9uIjo5MH1dXQ==

上の二つの可換図をぴったり重ね合わせると、次の可換図式が得られる。
$\hom_C(A, \_)$の可換図式の$X$, $Y$を$B$, $B'$に、$\hom_C(\_, B)$の可換図式の$X$, $Y$を$A$, $A'$に対応させる。$g$はそのままだ。

![Hom_C(\_, \_)](https://storage.googleapis.com/zenn-user-upload/138608967f70-20231205.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmYgQyJdLFs0LDAsIlxcbWF0aGJme1NldH0iXSxbNCwxLCJIb21fQyhBLCBCKSJdLFs0LDMsIkhvbV9DKEEnLCBCKSJdLFs2LDEsIkhvbV9DKEEsIEInKSJdLFs2LDMsIkhvbV9DKEEnLCBCJykiXSxbMCwxLCJBIl0sWzEsMSwiQSciXSxbMCwyLCJCIl0sWzEsMiwiQiciXSxbMiwzLCJIb21fQyhoLCBCKSA9IGcgXFxtYXBzdG8gZyBcXGNpcmMgaCIsMl0sWzIsNCwiSG9tX0MoQSwgZikgPSBnIFxcbWFwc3RvIGYgXFxjaXJjIGciXSxbMyw1LCJIb21fQyhBJywgZik9Z2ggXFxtYXBzdG8gZiBcXGNpcmMgZ2giLDJdLFs0LDUsIkhvbV9DKGgsIEInKT1mZyBcXG1hcHN0byBmZyBcXGNpcmMgaCJdLFs4LDksImYiLDJdLFs3LDYsImgiLDJdLFs2LDgsImciLDJdLFs3LDksImYgXFxjaXJjIGcgXFxjaXJjIGgiXV0=

上の可換図式は、双関手$\hom_C(\_, \_): \mathbf{C^{\rm{op}}} \times \mathbf C \to \mathbf{Set}$を表している。

なお圏$\mathbf{C^{\rm{op}}}$は圏$\mathbf C$のすべての射を反転させた双対圏であり、$\mathbf C$から$\mathbf{Set}$への反変関手は、$\mathbf{C^{\rm{op}}}$から$\mathbf{Set}$への共変関手とみなすことができる。

## 表記

* hom関手は、先頭を大文字にして$\rm{Hom}_C(A, B)$と書くこともある。
    * このノートではtexでの書きやすさを優先して、hom関手と書くことにする。
* hom関手によって写された射$f$の像$\hom_C(A, f)$を$f \circ -$と書くこともある。
    * また反変hom関手によって写された射$f$の像$\hom_C(f, A)$を$- \circ f$と書くこともある。
    * これらは$\hom_C(A, f)$と書くよりも短く、また計算する際も便利であるため、このノートでもしばしば用いる。
