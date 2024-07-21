---
title: "米田埋め込み"
free: false
---

[米田写像](yoneda-lemma)とは、局所的に小さな圏$\mathbf{C}$において対象$A$を固定したhom関手$\hom_{\mathbf{C}}(A, \_): \mathbf{C} \to \mathbf{Set}$から集合値関手$F: \mathbf{C} \to \mathbf{Set}$への自然変換全体の集合$\mathrm{Nat}_{\hom_{\mathbf{C}}(A, \_) \Rightarrow F}$と集合$F(A)$との間にある同型射のことであった。

ここで集合値関手$F$に圏$\mathbf{C}$の対象$B$を固定したhom関手$\hom_{\mathbf{C}}(B, \_)$をとることを考えると、米田の補題により米田写像$y: \mathrm{Nat}_{\hom_{\mathbf{C}}(A, \_) \Rightarrow \hom_{\mathbf{C}}(B, \_)} \simeq \hom_{\mathbf{C}}(B, A)$が得られる。

ここで$\hom_{\mathbf{C}}(B, A)$とは圏$\mathbf{C}$の対象$B$から対象$A$に伸びる射全体の集合である。

![yoneda](https://storage.googleapis.com/zenn-user-upload/d6e61b97baa5-20240721.png)

https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbNCwxLCJcXGhvbV9DKEEsIFgpIl0sWzUsMSwiXFxob21fQyhBLCBZKSJdLFs0LDAsIlxcbWF0aGJme1NldH0iXSxbMSwxLCJYIl0sWzAsMSwiQSJdLFsyLDEsIlkiXSxbNCwyLCJcXGhvbV9DKEIsIFgpIl0sWzUsMiwiXFxob21fQyhCLCBZKSJdLFswLDIsIkIiXSxbNiwxLCJcXG1hdGhybXtOYXR9X3tIXkEgXFxSaWdodGFycm93IEheQn0iXSxbNiwyLCJcXGhvbV9DKEIsIEEpIl0sWzgsMCwiXFxtYXRoYmZ7U2V0fV5cXG1hdGhiZntDfSJdLFs4LDEsIkheQSJdLFs4LDIsIkheQiJdLFs0LDYsImYiLDJdLFs1LDQsImEiXSxbMSwyLCJmIFxcY2lyYyAtIiwyXSxbNyw4LCJmIFxcY2lyYyAtIiwyXSxbOSw0LCJiIiwyXSxbMSw3LCJcXGV0YV9YIiwyXSxbMiw4LCJcXGV0YV9ZIl0sWzEwLDExLCJ5Il0sWzEzLDE0LCJcXGV0YSJdLFs5LDUsInciXV0=

米田写像により、自然変換$\hom_C(A, \_) \Rightarrow \hom_C(B, \_)$と圏$\mathbf{C}$の射$B \to A$が一対一対応することが確認できる。

## 定義

[表現](representable-functor)を割り当てる操作を考える。

すなわち局所的に小さな圏$\mathbf{C}$があるとき、対象$A \in \mathrm{ob}(\mathbf{C})$を固定してhom関手$\hom_C(A, \_): \mathbf C \to \mathbf{Set}$を得ることを考える。

このhom関手を$H^A$と書くと、この操作を反変関手$H^-: \mathbf{C} \to \mathbf{Set}^\mathbf{C}$と捉えることができる。すなわち：

- 圏$\mathbf{C}$の任意の対象$A$をhom関手$H^A = \hom_A(A, \_)$に写す
- 圏$\mathbf{C}$の任意の射$w: B \to A$を、米田写像によって自然変換$\eta: H^A \Rightarrow H^B$に写す

この関手$H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^\mathbf{C}$を米田埋め込みと呼ぶ。

![yoneda](https://storage.googleapis.com/zenn-user-upload/675c5acf4fd4-20240721.png)

https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKEEsIFgpIl0sWzQsMSwiXFxob21fQyhBLCBZKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMSwxLCJYIl0sWzAsMSwiQSJdLFsyLDEsIlkiXSxbMywyLCJcXGhvbV9DKEIsIFgpIl0sWzQsMiwiXFxob21fQyhCLCBZKSJdLFswLDIsIkIiXSxbNSwxLCJcXG1hdGhybXtOYXR9X3tIXkEgXFxSaWdodGFycm93IEheQn0iXSxbNSwyLCJcXGhvbV9DKEIsIEEpIl0sWzYsMCwiXFxtYXRoYmZ7U2V0fV5cXG1hdGhiZntDfSJdLFs2LDEsIlxcaG9tX0MoQSwgXFxfKSJdLFs2LDIsIlxcaG9tX0MoQiwgXFxfKSJdLFs0LDYsImYiXSxbNSw0LCJhIl0sWzEsMiwiZiBcXGNpcmMgLSJdLFs3LDgsImYgXFxjaXJjIC0iLDJdLFs5LDQsImIiLDJdLFsxLDcsIlxcZXRhX1giLDJdLFsyLDgsIlxcZXRhX1kiXSxbMTAsMTEsInkiXSxbMTMsMTQsIlxcZXRhIl0sWzksNSwidyJdXQ==

## 双対

反変hom関手として$\hom_C(\_, A): \mathbf{C} \to \mathbf{Set}$を取ることを考える。

このhom関手を$H_A$と書くと、この操作を関手$H_-: \mathbf{C} \to \mathbf{Set}^\mathbf{C^\mathrm{op}}$と捉えることができる。すなわち：

- 圏$\mathbf{C}$の任意の対象$A$をhom関手$H_A = \hom_A(\_, A)$に写す
- 圏$\mathbf{C}$の任意の射$v: A \to B$を、米田写像によって自然変換$\theta: H_A \Rightarrow H_B$に写す

この関手$H_-: \mathbf{C} \to \mathbf{Set}^\mathbf{C^\mathrm{op}}$も同様に米田埋め込みと呼ぶ。

![yoyoneda](https://storage.googleapis.com/zenn-user-upload/e937c481d8b7-20240721.png)

https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKFgsIEEpIl0sWzQsMSwiXFxob21fQyhZLCBBKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMCwxLCJBIl0sWzMsMiwiXFxob21fQyhYLCBCKSJdLFs0LDIsIlxcaG9tX0MoWSwgQikiXSxbMCwyLCJCIl0sWzUsMSwiXFxtYXRocm17TmF0fV97SF9BIFxcUmlnaHRhcnJvdyBIX0J9Il0sWzUsMiwiXFxob21fXFxtYXRoYmZ7Q30oQSwgQikiXSxbNiwwLCJcXG1hdGhiZntTZXR9XlxcbWF0aGJme0NeXFxtYXRocm17b3B9fSJdLFs2LDEsIlxcaG9tX0MoXFxfLCBBKSJdLFs2LDIsIlxcaG9tX0MoXFxfLCBCKSJdLFsyLDEsIlkiXSxbMSwxLCJYIl0sWzgsOSwieSJdLFsxMSwxMiwiXFx0aGV0YSJdLFsxLDIsIi0gXFxjaXJjIGYiXSxbNSw2LCItIFxcY2lyYyBmIiwyXSxbMTQsNCwiYSIsMl0sWzE0LDcsImIiXSxbMTMsMTQsImYiLDJdLFsxLDUsIlxcdGhldGFfWCIsMl0sWzIsNiwiXFx0aGV0YV9ZIl0sWzQsNywidiIsMl1d

## 表記

米田埋め込みは、$Y$や$よ$（ひらがな！）と書かれることがある。

https://ncatlab.org/nlab/show/Yoneda+embedding#ReferencesNotation
