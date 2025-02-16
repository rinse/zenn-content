---
title: "双自然変換"
free: false
---

双自然変換(*dinatural transformation*)とは、自然変換のある種の一般化である。

## 定義

圏$\mathbf{C}$, $\mathbf{D}$, 関手$F, G : \mathbf{C}^\mathrm{op} \times \mathbf{C} \to D$を考える。
このとき双自然変換$\eta : F \.\to G$とは、圏$\mathbf{C}$の対象で添え字づけられた圏$\mathbf{D}$の射の族$\{\eta_c : F(c, c) \to G(c, c)\}_{c \in \mathbf{C}}$であって、以下を満たすものである：

$$
G(\mathrm{id}_A, f) \circ \eta_A \circ F(f, \mathrm{id}_A) = G(f, \mathrm{id}_B) \circ \eta_B \circ F(\mathrm{id}_B, f)
$$

すなわち以下の図式を可換にする。（$F(B, A)$から$G(A, B)$へ、左回りでいっても右回りでいってもよいということ）

[![](https://storage.googleapis.com/zenn-user-upload/d41f34a7039e-20250216.png)](https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMCwxLCJBIl0sWzEsMSwiQiJdLFsyLDAsIlxcbWF0aGJme0R9Il0sWzMsMSwiRihCLCBBKSJdLFsyLDEsIkYoQSwgQSkiXSxbNCwxLCJGKEIsIEIpIl0sWzQsMiwiRyhCLCBCKSJdLFsyLDIsIkcoQSwgQSkiXSxbMywyLCJHKEEsIEIpIl0sWzEsMiwiZiJdLFs0LDUsIkYoZiwgXFxtYXRocm17aWR9X0EpIiwyXSxbNCw2LCJGKFxcbWF0aHJte2lkfV9CLCBmKSJdLFs2LDcsIlxcZXRhX0IiXSxbNSw4LCJcXGV0YV9BIiwyXSxbOCw5LCJHKFxcbWF0aHJte2lkfV9BLCBmKSIsMl0sWzcsOSwiRyhmLCBcXG1hdGhybXtpZH1fQikiXSxbNCw5LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

## 記法

双自然変換の書き方には、矢印の上に点をいくつ打つかのバリエーションがあるようだ。

- $\eta : F \dot\to G$
- $\eta : F \"\to G$

