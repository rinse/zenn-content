---
title: "米田埋め込み"
free: false
---

[米田写像](yoneda-lemma)とは、局所的に小さな圏$\mathbf{C}$において対象$A$を固定したhom関手$\hom_{\mathbf{C}}(A, \_): \mathbf{C} \to \mathbf{Set}$から集合値関手$F: \mathbf{C} \to \mathbf{Set}$への自然変換全体の集合$\hom_{\mathrm{Set}^C}(\hom_C(A, \_), F)$と集合$F(A)$との間にある同型射のことであった。

ここで集合値関手$F$に圏$\mathbf{C}$の対象$B$を固定したhom関手$\hom_{\mathbf{C}}(B, \_)$をとることを考えると、米田の補題により米田写像$y: \hom_{\mathrm{Set}^C}(\hom_{\mathbf{C}}(A, \_), \hom_{\mathbf{C}}(B, \_)) \simeq \hom_{\mathbf{C}}(B, A)$が得られる。

ここで$\hom_{\mathbf{C}}(B, A)$とは圏$\mathbf{C}$の対象$B$から対象$A$に伸びる射全体の集合である。

[![yoneda-lemma-with-hom-functor](https://storage.googleapis.com/zenn-user-upload/1bf6093b791f-20250202.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKEEsIFgpIl0sWzQsMSwiXFxob21fQyhBLCBZKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMSwxLCJYIl0sWzAsMSwiQSJdLFsyLDEsIlkiXSxbMywyLCJcXGhvbV9DKEIsIFgpIl0sWzQsMiwiXFxob21fQyhCLCBZKSJdLFswLDIsIkIiXSxbNSwxLCJcXGhvbV97XFxtYXRocm17U2V0fV5DfShcXGhvbV9DKEEsIFxcXyksIFxcaG9tX0MoQiwgXFxfKSkiXSxbNSwyLCJcXGhvbV9DKEIsIEEpIl0sWzYsMCwiXFxtYXRoYmZ7U2V0fV5cXG1hdGhiZntDfSJdLFs2LDEsIlxcaG9tX0MoQSwgXFxfKSJdLFs2LDIsIlxcaG9tX0MoQiwgXFxfKSJdLFs0LDYsImYiXSxbNSw0LCJhIl0sWzEsMiwiXFxob21fQyhBLCBmKSJdLFs3LDgsIlxcaG9tX0MoQiwgZikiLDJdLFs5LDQsImIiLDJdLFsxLDcsIlxcZXRhX1giLDJdLFsyLDgsIlxcZXRhX1kiXSxbMTAsMTEsInkiXSxbOSw1LCJ3Il0sWzEzLDE0LCJcXGV0YSJdXQ==)


上図式において$w \in \hom_C(A, B)$, $\eta \in \hom_{\mathrm{Set}^C}(\hom_C(A, \_), \hom_C(B, \_))$であり、
米田写像$y$により自然変換$\hom_C(A, \_) \Rightarrow \hom_C(B, \_)$と圏$\mathbf{C}$の射$B \to A$が一対一対応することが確認できる。

## 定義

局所的に小さな圏$\mathbf{C}$の対象$A \in \mathrm{ob}(\mathbf{C})$を固定した[hom関手](hom-functor)$\hom_C(A, \_): \mathbf C \to \mathbf{Set}$を考える。

このhom関手を$H^A$と書くと、この操作を反変関手$H^-: \mathbf{C} \to \mathbf{Set}^\mathbf{C}$と捉えることができる。すなわち：

- 圏$\mathbf{C}$の任意の対象$A$をhom関手$H^A = \hom_C(A, \_)$に写す
- 圏$\mathbf{C}$の任意の射$w: B \to A$を、米田写像によって自然変換$\eta: H^A \Rightarrow H^B$に写す

この関手$H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^\mathbf{C}$を米田埋め込み(*Yoneda embedding*)と呼ぶ。

[![yoneda](https://storage.googleapis.com/zenn-user-upload/e8e80c9dc8b5-20250202.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKEEsIFgpIl0sWzQsMSwiXFxob21fQyhBLCBZKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMSwxLCJYIl0sWzAsMSwiQSJdLFsyLDEsIlkiXSxbMywyLCJcXGhvbV9DKEIsIFgpIl0sWzQsMiwiXFxob21fQyhCLCBZKSJdLFswLDIsIkIiXSxbNSwxLCJcXGhvbV97XFxtYXRocm17U2V0fV5DfShIXkEsIEheQikiXSxbNSwyLCJcXGhvbV9DKEIsIEEpIl0sWzYsMCwiXFxtYXRoYmZ7U2V0fV5cXG1hdGhiZntDfSJdLFs2LDEsIkheQSJdLFs2LDIsIkheQiJdLFs0LDYsImYiXSxbNSw0LCJhIl0sWzEsMiwiXFxob21fQyhBLCBmKSJdLFs3LDgsIlxcaG9tX0MoQiwgZikiLDJdLFs5LDQsImIiLDJdLFsxLDcsIlxcZXRhX1giLDJdLFsyLDgsIlxcZXRhX1kiXSxbMTAsMTEsInkiXSxbMTMsMTQsIlxcZXRhIl0sWzksNSwidyJdLFsxLDgsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

## 反変hom関手による構成

反変hom関手として$\hom_C(\_, A): \mathbf{C^{\mathrm{op}}} \to \mathbf{Set}$を取ることを考える。

このhom関手を$H_A$と書くと、この操作を関手$H_-: \mathbf{C} \to \mathbf{Set}^\mathbf{C^\mathrm{op}}$と捉えることができる。すなわち：

- 圏$\mathbf{C}$の任意の対象$A$をhom関手$H_A = \hom_C(\_, A)$に写す
- 圏$\mathbf{C}$の任意の射$v: A \to B$を、米田写像によって自然変換$\theta: H_A \Rightarrow H_B$に写す

$H^- \simeq H_-$であるため、この関手$H_-: \mathbf{C} \to \mathbf{Set}^\mathbf{C^\mathrm{op}}$も米田埋め込みと呼ぶ。

[![contravariant-yoneda](https://storage.googleapis.com/zenn-user-upload/ee1235385b7e-20250202.png)](https://q.uiver.app/#q=WzAsMTUsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMywxLCJcXGhvbV9DKFgsIEEpIl0sWzQsMSwiXFxob21fQyhZLCBBKSJdLFszLDAsIlxcbWF0aGJme1NldH0iXSxbMCwxLCJBIl0sWzMsMiwiXFxob21fQyhYLCBCKSJdLFs0LDIsIlxcaG9tX0MoWSwgQikiXSxbMCwyLCJCIl0sWzUsMSwiXFxob21fe1xcbWF0aHJte1NldH1ee0Nee1xcbWF0aHJte29wfX19fShIX0EsIEhfQikiXSxbNSwyLCJcXGhvbV9cXG1hdGhiZntDfShBLCBCKSJdLFs2LDAsIlxcbWF0aGJme1NldH1eXFxtYXRoYmZ7Q15cXG1hdGhybXtvcH19Il0sWzYsMSwiSF9BIl0sWzYsMiwiSF9CIl0sWzIsMSwiWSJdLFsxLDEsIlgiXSxbOCw5LCJ5Il0sWzExLDEyLCJcXHRoZXRhIl0sWzEsMiwiXFxob21fQyhmLCBBKSJdLFs1LDYsIlxcaG9tX0MoZiwgQikiLDJdLFsxNCw0LCJhIiwyXSxbMTQsNywiYiJdLFsxMywxNCwiZiIsMl0sWzEsNSwiXFx0aGV0YV9YIiwyXSxbMiw2LCJcXHRoZXRhX1kiXSxbNCw3LCJ2IiwyXSxbMSw2LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

## 米田埋め込みは忠実充満

米田埋め込み$H^-$および$H_-$は[忠実充満関手](full-and-faithful-functors)である。

関手$F: \mathbf{C} \to \mathbf{D}$が忠実充満であるとは、局所的に小さな圏$\mathbf{C}$の任意の二対象$X$, $Y$について集合の圏上の射$\hom_\mathbf{C}(X, Y) \to \hom_\mathbf{D}(F(X), F(Y))$が単射かつ全射であることをいうのだった。

これを米田埋め込み$H^-: \mathbf{C}^\mathrm{op} \to \mathbf{Set}^\mathbf{C}$に当てはめると、局所的に小さな圏$\mathbf{C^{\mathrm{op}}}$の任意の二対象$X$, $Y$について集合の圏上の射$\hom_{\mathbf{C}^\mathrm{op}}(X, Y) \to \hom_{\mathbf{Set}^{\mathbf{C}}}(H^X, H^Y)$が単射かつ全射になればよい。

ところで、自然変換$\hom_C(A, \_) \Rightarrow \hom_C(B, \_)$と圏$\mathbf{C}$の射$B \to A$（あるいは同じことだが圏$\mathbf{C}^{\mathrm{op}}$の射$A \to B$）の間には米田写像があるのだった。米田写像は同型写像であるから、米田埋め込みは忠実充満関手である。

[![yoneda-embedding-is-full-and-faithful](https://storage.googleapis.com/zenn-user-upload/9001591d34cd-20240820.png)](https://q.uiver.app/#q=WzAsMTEsWzAsMCwiXFxtYXRoYmZ7Q31ee1xcbWF0aHJte29wfX0iXSxbNCwwLCJcXG1hdGhiZntTZXR9Il0sWzEsMSwiWCJdLFswLDEsIkEiXSxbMiwxLCJZIl0sWzAsMiwiQiJdLFszLDAsIlxcbWF0aGJme1NldH1eXFxtYXRoYmZ7Q30iXSxbMywxLCJIXkEiXSxbMywyLCJIXkIiXSxbNCwxLCJcXGhvbV97XFxtYXRoYmZ7Q31ee1xcbWF0aHJte29wfX19KEEsIEIpIl0sWzQsMiwiXFxob21fe1xcbWF0aGJme1NldH1eXFxtYXRoYmZ7Q319KEheQSwgSF5CKSJdLFs0LDIsImYiLDJdLFsyLDMsImEiLDJdLFsyLDUsImIiXSxbNyw4LCJcXGV0YSJdLFszLDUsInciLDJdLFs5LDEwLCJ5Il1d)

## 表記

米田埋め込みは、$Y$や$よ$（ひらがな！）と書かれることがある。

https://ncatlab.org/nlab/show/Yoneda+embedding#ReferencesNotation
