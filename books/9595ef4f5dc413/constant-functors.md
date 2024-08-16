---
title: "定関手"
free: false
---

関手$\Delta_A: \mathbf{J} \to \mathbf{C}$を考える。

この関手は、$\mathbf{J}$の任意の対象を圏$\mathbf{C}$のある要素$A$に対応づけ、$\mathbf{J}$の任意の射を圏$\mathbf{C}$の射$\mathrm{id}_A$に対応づけるものである。

このような関手を定関手(*Constant functor*)と呼ぶ。

[![constant-functor](https://storage.googleapis.com/zenn-user-upload/1ee4849f20f6-20240817.png)](https://q.uiver.app/#q=WzAsNSxbMCwxLCJqIl0sWzAsMCwiXFxtYXRoYmZ7Sn0iXSxbMSwwLCJcXG1hdGhiZntDfSJdLFsxLDEsIkEiXSxbMCwyLCJrIl0sWzEsMiwiXFxEZWx0YV9BIl0sWzAsMywiIiwwLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibWFwcyB0byJ9fX1dLFs0LDMsIiIsMix7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Im1hcHMgdG8ifX19XSxbMCw0LCJmIiwyXV0=)

定関手は[極限](limit)の定義に使われるため重要である。

## 自明な圏からの定関手

定関手の特殊なケースとして、自明な圏$\mathbf{1}$を域に持つ定関手$\Delta_A: \mathbf{1} \to \mathbf{C}$が存在する。

[![constant-functor](https://storage.googleapis.com/zenn-user-upload/486e694e5bde-20240817.png)](https://q.uiver.app/#q=WzAsNCxbMCwxLCJcXGFzdCJdLFswLDAsIlxcbWF0aGJmezF9Il0sWzEsMCwiXFxtYXRoYmZ7Q30iXSxbMSwxLCJBIl0sWzEsMiwiXFxEZWx0YV9BIl0sWzAsMywiIiwwLHsic3R5bGUiOnsidGFpbCI6eyJuYW1lIjoibWFwcyB0byJ9fX1dXQ==)

このような定関手は特に[コンマ圏の特殊な構成](variants-of-comma-category)に使われる。

## 定関手を得る関手

圏$\mathbf{C}$の対象$A$を固定して定関手$\Delta_A: \mathbf{J} \to \mathbf{C}$を得る関手$\Delta: \mathbf{C} \to \mathbf{C}^\mathbf{J}$を考えらえれる。
