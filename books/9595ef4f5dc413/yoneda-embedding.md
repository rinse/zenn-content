---
title: "米田埋め込み"
free: false
---

[米田写像](yoneda-lemma)とは、局所的に小さな圏$\mathbf{C}$において対象$A$を固定したhom関手$\hom_{\mathbf{C}}(A, \_): \mathbf{C} \to \mathbf{Set}$から集合値関手$F: \mathbf{C} \to \mathbf{Set}$への自然変換全体の集合$\mathrm{Nat}(\hom_{\mathbf{C}}(A, \_) \Rightarrow F)$と集合$F(A)$との間にある同型射のことであった。

ここで集合値関手$F$に圏$\mathbf{C}$の対象$B$を固定したhom関手$\hom_{\mathbf{C}}(B, \_)$をとることを考えると、米田の補題により米田写像$y: \mathrm{Nat}(\hom_{\mathbf{C}}(A, \_) \Rightarrow \hom_{\mathbf{C}}(B, \_)) \simeq \hom_{\mathbf{C}}(B, A)$が得られる。

ここで$\hom_{\mathbf{C}}(B, A)$とは圏$\mathbf{C}$の対象$B$から対象$A$に伸びる射全体の集合である。

[![yoneda](https://storage.googleapis.com/zenn-user-upload/d6e61b97baa5-20240721.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbNCwxLCJcXGhvbV9DKEEsIFgpIl0sWzUsMSwiXFxob21fQyhBLCBZKSJdLFs0LDAsIlxcbWF0aGJme1NldH0iXSxbMSwxLCJYIl0sWzAsMSwiQSJdLFsyLDEsIlkiXSxbNCwyLCJcXGhvbV9DKEIsIFgpIl0sWzUsMiwiXFxob21fQyhCLCBZKSJdLFswLDIsIkIiXSxbNiwxLCJcXG1hdGhybXtOYXR9X3tIXkEgXFxSaWdodGFycm93IEheQn0iXSxbNiwyLCJcXGhvbV9DKEIsIEEpIl0sWzgsMCwiXFxtYXRoYmZ7U2V0fV5cXG1hdGhiZntDfSJdLFs4LDEsIkheQSJdLFs4LDIsIkheQiJdLFs0LDYsImYiLDJdLFs1LDQsImEiXSxbMSwyLCJmIFxcY2lyYyAtIiwyXSxbNyw4LCJmIFxcY2lyYyAtIiwyXSxbOSw0LCJiIiwyXSxbMSw3LCJcXGV0YV9YIiwyXSxbMiw4LCJcXGV0YV9ZIl0sWzEwLDExLCJ5Il0sWzEzLDE0LCJcXGV0YSJdLFs5LDUsInciXV0=)

上図式において$w \in \hom_C(A, B)$, $\eta \in \mathrm{Nat}_{H^A \Rightarrow H^B}$であり、
米田写像$y$により自然変換$\hom_C(A, \_) \Rightarrow \hom_C(B, \_)$と圏$\mathbf{C}$の射$B \to A$が一対一対応することが確認できる。

## 定義

[表現](representable-functor)を割り当てる操作を考える。

すなわち局所的に小さな圏$\mathbf{C}$があるとき、対象$A \in \mathrm{ob}(\mathbf{C})$を固定してhom関手$\hom_C(A, \_): \mathbf C \to \mathbf{Set}$を得ることを考える。

このhom関手を$H^A$と書くと、この操作を反変関手$H^-: \mathbf{C} \to \mathbf{Set}^\mathbf{C}$と捉えることができる。すなわち：

- 圏$\mathbf{C}$の任意の対象$A$をhom関手$H^A = \hom_A(A, \_)$に写す
- 圏$\mathbf{C}$の任意の射$w: B \to A$を、米田写像によって自然変換$\eta: H^A \Rightarrow H^B$に写す

この関手$H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^\mathbf{C}$を米田埋め込みと呼ぶ。

[![yoneda](https://storage.googleapis.com/zenn-user-upload/8be696975151-20240820.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKEEsIFgpIl0sWzQsMSwiXFxob21fQyhBLCBZKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMSwxLCJYIl0sWzAsMSwiQSJdLFsyLDEsIlkiXSxbMywyLCJcXGhvbV9DKEIsIFgpIl0sWzQsMiwiXFxob21fQyhCLCBZKSJdLFswLDIsIkIiXSxbNSwxLCJcXG1hdGhybXtOYXR9KEheQSBcXFJpZ2h0YXJyb3cgSF5CKSJdLFs1LDIsIlxcaG9tX0MoQiwgQSkiXSxbNiwwLCJcXG1hdGhiZntTZXR9XlxcbWF0aGJme0N9Il0sWzYsMSwiSF5BIl0sWzYsMiwiSF5CIl0sWzQsNiwiZiIsMl0sWzUsNCwiYSJdLFsxLDIsImYgXFxjaXJjIC0iLDJdLFs3LDgsImYgXFxjaXJjIC0iLDJdLFs5LDQsImIiLDJdLFsxLDcsIlxcZXRhX1giLDJdLFsyLDgsIlxcZXRhX1kiXSxbMTAsMTEsInkiXSxbMTMsMTQsIlxcZXRhIl0sWzksNSwidyJdXQ==)

## 双対

反変hom関手として$\hom_C(\_, A): \mathbf{C} \to \mathbf{Set}$を取ることを考える。

このhom関手を$H_A$と書くと、この操作を関手$H_-: \mathbf{C} \to \mathbf{Set}^\mathbf{C^\mathrm{op}}$と捉えることができる。すなわち：

- 圏$\mathbf{C}$の任意の対象$A$をhom関手$H_A = \hom_A(\_, A)$に写す
- 圏$\mathbf{C}$の任意の射$v: A \to B$を、米田写像によって自然変換$\theta: H_A \Rightarrow H_B$に写す

この関手$H_-: \mathbf{C} \to \mathbf{Set}^\mathbf{C^\mathrm{op}}$も同様に米田埋め込みと呼ぶ。

[![coyoneda](https://storage.googleapis.com/zenn-user-upload/8b6c61ca3c66-20240820.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKFgsIEEpIl0sWzQsMSwiXFxob21fQyhZLCBBKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMCwxLCJBIl0sWzMsMiwiXFxob21fQyhYLCBCKSJdLFs0LDIsIlxcaG9tX0MoWSwgQikiXSxbMCwyLCJCIl0sWzUsMSwiXFxtYXRocm17TmF0fShIX0EgXFxSaWdodGFycm93IEhfQikiXSxbNSwyLCJcXGhvbV9cXG1hdGhiZntDfShBLCBCKSJdLFs2LDAsIlxcbWF0aGJme1NldH1eXFxtYXRoYmZ7Q15cXG1hdGhybXtvcH19Il0sWzYsMSwiSF9BIl0sWzYsMiwiSF9CIl0sWzIsMSwiWSJdLFsxLDEsIlgiXSxbOCw5LCJ5Il0sWzExLDEyLCJcXHRoZXRhIl0sWzEsMiwiLSBcXGNpcmMgZiJdLFs1LDYsIi0gXFxjaXJjIGYiLDJdLFsxNCw0LCJhIiwyXSxbMTQsNywiYiJdLFsxMywxNCwiZiIsMl0sWzEsNSwiXFx0aGV0YV9YIiwyXSxbMiw2LCJcXHRoZXRhX1kiXSxbNCw3LCJ2IiwyXV0=)

## 米田埋め込みは忠実充満

米田埋め込み$H^-$および$H_-$は[忠実充満関手](full-and-faithful-functors)である。

関手$F: \mathbf{C} \to \mathbf{D}$が忠実充満であるとは、局所的に小さな圏$\mathbf{C}$の任意の二対象$X$, $Y$について集合の圏上の射$\hom_\mathbf{C}(X, Y) \to \hom_\mathbf{D}(F(X), F(Y))$が単射かつ全射であることをいうのだった。

これを米田埋め込み$H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^\mathbf{C}$に当てはめると、局所的に小さな圏$\mathbf{C^{\mathrm{op}}}$の任意の二対象$X$, $Y$について集合の圏上の射$\hom_{\mathbf{C}^\mathrm{op}}(X, Y) \to \hom_{\mathbf{Set}^{\mathbf{C}}}(H^X, H^Y)$が単射かつ全射になればよい。

ところで、自然変換$\hom_C(A, \_) \Rightarrow \hom_C(B, \_)$と圏$\mathbf{C}$の射$B \to A$（あるいは同じことだが圏$\mathbf{C}^{\mathrm{op}}$の射$A \to B$）の間には米田写像があるのだった。米田写像は同型写像であるから、米田埋め込みは忠実充満関手である。

[![yoneda-embedding-is-full-and-faithful](https://storage.googleapis.com/zenn-user-upload/9001591d34cd-20240820.png)](https://q.uiver.app/#q=WzAsMTEsWzAsMCwiXFxtYXRoYmZ7Q31ee1xcbWF0aHJte29wfX0iXSxbNCwwLCJcXG1hdGhiZntTZXR9Il0sWzEsMSwiWCJdLFswLDEsIkEiXSxbMiwxLCJZIl0sWzAsMiwiQiJdLFszLDAsIlxcbWF0aGJme1NldH1eXFxtYXRoYmZ7Q30iXSxbMywxLCJIXkEiXSxbMywyLCJIXkIiXSxbNCwxLCJcXGhvbV97XFxtYXRoYmZ7Q31ee1xcbWF0aHJte29wfX19KEEsIEIpIl0sWzQsMiwiXFxob21fe1xcbWF0aGJme1NldH1eXFxtYXRoYmZ7Q319KEheQSwgSF5CKSJdLFs0LDIsImYiLDJdLFsyLDMsImEiLDJdLFsyLDUsImIiXSxbNyw4LCJcXGV0YSJdLFszLDUsInciLDJdLFs5LDEwLCJ5Il1d)

## 表記

米田埋め込みは、$Y$や$よ$（ひらがな！）と書かれることがある。

https://ncatlab.org/nlab/show/Yoneda+embedding#ReferencesNotation
