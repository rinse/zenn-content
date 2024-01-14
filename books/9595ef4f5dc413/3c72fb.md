---
title: "積圏"
free: false
---

積圏(*Product category*)とは、大雑把に言えば、圏と圏の積からなる圏のことをいう。

## 定義

ある圏$\mathbf C$, $\mathbf D$の積圏$\mathbf C \times \mathbf D$とは、以下の要素からなる圏である。

- 対象として$\mathbf C$の対象と$\mathbf D$の対象の組$\langle C, D \rangle$を持つ。
    - ここで$C$は圏$\mathbf C$の対象で、$D$は圏$\mathbf D$の対象である。
- $\langle C, D \rangle$から$\langle C', D' \rangle$への射として、$\langle f, g \rangle$を持つ。
    - ここで$f$は$\mathbf C$における$C$から$C'$への射であり、$g$は$\mathbf D$における$D$から$D'$への射である。
- 射$\langle f, g \rangle$と射$\langle f', g' \rangle$の合成$\langle f', g' \rangle \circ \langle f, g \rangle$を、$\langle f' \circ f, g' \circ g \rangle$と定義する。
- 対象$\langle C, D \rangle$における恒等射$\mathrm{id}_{\langle C, D \rangle}$を、$\langle \mathrm{id}_C, \mathrm{id}_D \rangle$と定義する。

![product_category](https://storage.googleapis.com/zenn-user-upload/c5fb87c38215-20231206.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzMsMCwiXFxtYXRoYmYgRCJdLFs2LDAsIlxcbWF0aGJmIEMgXFx0aW1lcyBcXG1hdGhiZiBEIl0sWzAsMSwiQyJdLFsxLDEsIkMnIl0sWzMsMSwiRCJdLFs0LDEsIkQnIl0sWzYsMSwiXFxsYW5nbGUgQywgRCBcXHJhbmdsZSJdLFs3LDEsIlxcbGFuZ2xlIEMnLCBEJyBcXHJhbmdsZSJdLFszLDQsImYiXSxbNSw2LCJnIl0sWzcsOCwiXFxsYW5nbGUgZiwgZyBcXHJhbmdsZSJdXQ==
