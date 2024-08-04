---
title: "極限"
free: false
---

極限とは、普遍性の特殊な場合である。積などの幅広い概念が極限に一般化される。

単に極限と言ったときには、圏$\mathbf{J}$を形とする図式$D: \mathbf{J} \to \mathbf{C}$の極限(*Limit*)を指す。
図式については[添え字圏と図式](diagram-and-index-category)を参照。

## 定義

$D: \mathbf J \to \mathbf C$をCにおける図式とすると、$D$への錐とは、$\mathbf J$の対象をすべて$\mathbf C$の対象$N$に写し、$\mathbf J$の射をすべて$\mathrm{id}_N$に写す定関手$\Delta_N: \mathbf J \to \mathbf C$から図式$D$への自然変換$\epsilon: \Delta_N \Rightarrow D$としてあらわされる。

![redundant_cone](https://storage.googleapis.com/zenn-user-upload/cc9af460dccd-20231028.png)

https://q.uiver.app/#q=WzAsOCxbNCwwLCJcXG1hdGhiZiBDIl0sWzMsMSwiXFxEZWx0YV9OKEEpIl0sWzMsMiwiRChBKSJdLFs1LDIsIkQoQikiXSxbMCwwLCJcXG1hdGhiZiBKIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbNSwxLCJcXERlbHRhX04oQikiXSxbMiwzLCJEKGYpIl0sWzEsMiwiXFxlcHNpbG9uX0EiLDJdLFs1LDYsImYiXSxbNywzLCJcXGVwc2lsb25fQiJdLFsxLDcsIlxcRGVsdGFfTihmKT1pZF9OIl1d

ここで、$\Delta_N(A)$, $\Delta_N(B)$は共に対象$N$のことなので、次のように可換図式を整理できる。

![cone](https://storage.googleapis.com/zenn-user-upload/bf2703d59166-20231028.png)

https://q.uiver.app/#q=WzAsNyxbNCwwLCJcXG1hdGhiZiBDIl0sWzQsMSwiTiJdLFszLDIsIkQoQSkiXSxbNSwyLCJEKEIpIl0sWzAsMCwiXFxtYXRoYmYgSiJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMywiRChmKSJdLFsxLDIsIlxcZXBzaWxvbl9BIiwyXSxbNSw2LCJmIl0sWzEsMywiXFxlcHNpbG9uX0IiXV0=

この三角形を構成する組$(N, \epsilon)$を錐(*Cone*)と呼ぶ。

極限とは、$D$への錐$(L, \eta)$であって、任意の錐の対象$N$に対して一意な仲介射(*Mediating morphism*)$u: N \to L$が存在して、$\mathbf J$の任意の対象$X$に対して$\epsilon_X = \eta_X \circ u$を満たすものである。

![limit](https://storage.googleapis.com/zenn-user-upload/590e1fc45b5e-20231028.png)

https://q.uiver.app/#q=WzAsOCxbNCwwLCJcXG1hdGhiZiBDIl0sWzMsMywiRChBKSJdLFs1LDMsIkQoQikiXSxbMCwwLCJcXG1hdGhiZiBKIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbNCwyLCJMIl0sWzQsMSwiTiJdLFsxLDIsIkQoZikiXSxbNCw1LCJmIl0sWzYsMiwiXFxldGFfQiJdLFs2LDEsIlxcZXRhX0EiLDJdLFs3LDEsIlxcZXBzaWxvbl9BIiwyLHsiY3VydmUiOjF9XSxbNywyLCJcXGVwc2lsb25fQiIsMCx7ImN1cnZlIjotMX1dLFs3LDYsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=

## 記法

図式$F$の極限$(L, \eta)$を$\varprojlim{F}$と書くことがある。

## 普遍性を用いた定義

関手$F: \mathbf C \to \mathbf D$から圏$\mathbf D$の対象Aへの普遍射とは、以下の可換図式上の組$(X, u)$のことだった。

![opposite_universal_morphism](https://storage.googleapis.com/zenn-user-upload/d909538b8a99-20231023.png)

https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMSwiQSJdLFszLDEsIkYoWCkiXSxbMywyLCJGKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzQsMCwiQSJdLFs1LDAsIkYiXSxbMywyLCJGKGcpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzMsMSwiZiJdLFs2LDUsImciLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiwxLCJ1IiwyXSxbOCw3LCLmma7pgY3lsIQiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=

極限は関手$\Delta: \mathbf C \to \mathbf C^{\mathbf J}$から圏$\mathbf C^{\mathbf J}$の対象$D$への普遍射$(L, \eta)$として表すことができる。

![limit_universal_morphism](https://storage.googleapis.com/zenn-user-upload/38e1a8b616a0-20231028.png)

https://q.uiver.app/#q=WzAsMTIsWzMsMSwiXFxtYXRoYmYgQyJdLFs1LDIsIkQiXSxbNiwyLCJcXERlbHRhKEwpIl0sWzYsMywiXFxEZWx0YShOKSJdLFs1LDEsIlxcbWF0aGJmIENee1xcbWF0aGJmIEp9Il0sWzMsMiwiTCJdLFszLDMsIk4iXSxbMiwwLCJEIl0sWzMsMCwiXFxEZWx0YSJdLFswLDEsIlxcbWF0aGJmIEoiXSxbMCwyLCJBIl0sWzEsMiwiQiJdLFszLDIsIlxcRGVsdGEodSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGVwc2lsb24iXSxbNiw1LCJ1IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIsMSwiXFxldGEiLDJdLFsxMCwxMSwiZiJdLFs4LDcsIuaZrumBjeWwhCIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dXQ==

ここで圏$\mathbf C^{\mathbf J}$とは、$\mathbf J$から$\mathbf C$への関手を対象として持ち、それらの間の自然変換を射として持つ関手圏である。ゆえに対象$D$は$\mathbf J \to \mathbf C$の関手である。

また関手$\Delta: \mathbf C \to \mathbf C^{\mathbf J}$は、圏$\mathbf C$の対象$X$を定関手$\Delta_X$に写し、射$f: X \to Y$を$\Delta(f): \Delta_X \Rightarrow \Delta_Y$に写す関手である。すなわち$\Delta(X)=\Delta_X: \mathbf J \to \mathbf C$であり、圏$\mathbf C$上では任意の$J \in \mathbf J$に対して$\Delta(f)_J=f: X \to Y$である。
なお$\Delta$は積の例に登場した対角関手$\mathbf C \to \mathbf C \times \mathbf C$の一般化である。（添え字圏$\mathbf J$に離散圏$\mathbf 2$を使うことで$\mathbf C \to \mathbf C^{\mathbf 2}$を得られる。自明に$\mathbf C^{\mathbf 2} \simeq \mathbf C \times \mathbf C$である）

さて、積の時と同様に、上の普遍射の可換図式が極限のそれと一致することを確認していこう。

まずは$\mathbf C^{\mathbf J}$を圏$\mathbf C$上に書き下してみよう。

![redundant_cone_limit](https://storage.googleapis.com/zenn-user-upload/447eb327fff0-20231028.png)

https://q.uiver.app/#q=WzAsMTksWzMsMSwiXFxtYXRoYmYgQyJdLFs1LDIsIkQiXSxbNiwyLCJcXERlbHRhKEwpIl0sWzYsMywiXFxEZWx0YShOKSJdLFs1LDEsIlxcbWF0aGJmIENee1xcbWF0aGJmIEp9Il0sWzMsMiwiTCJdLFszLDMsIk4iXSxbMiwwLCJEIl0sWzMsMCwiXFxEZWx0YSJdLFswLDEsIlxcbWF0aGJmIEoiXSxbMCwyLCJBIl0sWzEsMiwiQiJdLFs4LDEsIlxcbWF0aGJmIEMiXSxbOSwyLCJcXERlbHRhX04oQSkiXSxbMTAsMiwiXFxEZWx0YV9OKEIpIl0sWzksMywiXFxEZWx0YV9MKEEpIl0sWzEwLDMsIlxcRGVsdGFfTChCKSJdLFs4LDQsIkQoQSkiXSxbMTEsNCwiRChCKSJdLFszLDIsIlxcRGVsdGEodSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGVwc2lsb24iXSxbNiw1LCJ1IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIsMSwiXFxldGEiLDJdLFsxMCwxMSwiZiJdLFs4LDcsIuaZrumBjeWwhCIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMywxNCwiXFxEZWx0YV9OKGYpIl0sWzE1LDE2LCJcXERlbHRhX0woZikiXSxbMTcsMTgsIkQoZikiXSxbMTUsMTcsIlxcZXRhX0EiLDJdLFsxNiwxOCwiXFxldGFfQiJdLFsxMywxNywiXFxlcHNpbG9uX0EiLDIseyJjdXJ2ZSI6MX1dLFsxNCwxOCwiXFxlcHNpbG9uX0IiLDAseyJjdXJ2ZSI6LTF9XSxbMTQsMTYsIlxcRGVsdGEodSlfe0J9IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEzLDE1LCJcXERlbHRhKHUpX3tBfSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dXQ==

ここで、定関手$\Delta_X$は$\mathbf J$の対象をすべて$\mathbf C$の対象$X$に写すから、$\Delta_L(A) = \Delta_L(B) = L$、かつ$\Delta_N(A) = \Delta_N(B) = N$だ。また$\Delta(u)$は任意の$J \in \mathbf J$に対して$\Delta(u)_J = u$であるから、$\Delta(u)_A = \Delta(u)_B = u$だ。

これらから上の可換図式を整理すると、次の可換図式を得られる。これはまさに、錐から作った極限の図式と同じだ。

![cone_limit](https://storage.googleapis.com/zenn-user-upload/fef90f52a69b-20231028.png)

https://q.uiver.app/#q=WzAsMTcsWzMsMSwiXFxtYXRoYmYgQyJdLFs1LDIsIkQiXSxbNiwyLCJcXERlbHRhKEwpIl0sWzYsMywiXFxEZWx0YShOKSJdLFs1LDEsIlxcbWF0aGJmIENee1xcbWF0aGJmIEp9Il0sWzMsMiwiTCJdLFszLDMsIk4iXSxbMiwwLCJEIl0sWzMsMCwiXFxEZWx0YSJdLFswLDEsIlxcbWF0aGJmIEoiXSxbMCwyLCJBIl0sWzEsMiwiQiJdLFs4LDEsIlxcbWF0aGJmIEMiXSxbOSwyLCJOIl0sWzksMywiTCJdLFs4LDQsIkQoQSkiXSxbMTAsNCwiRChCKSJdLFszLDIsIlxcRGVsdGEodSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGVwc2lsb24iXSxbNiw1LCJ1IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIsMSwiXFxldGEiLDJdLFsxMCwxMSwiZiJdLFs4LDcsIuaZrumBjeWwhCIsMl0sWzE1LDE2LCJEKGYpIl0sWzE0LDE1LCJcXGV0YV9BIiwyXSxbMTMsMTUsIlxcZXBzaWxvbl9BIiwyLHsiY3VydmUiOjF9XSxbMTMsMTQsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTQsMTYsIlxcZXRhX0IiXSxbMTMsMTYsIlxcZXBzaWxvbl9CIiwwLHsiY3VydmUiOi0xfV1d

余談だが、積とは、極限の添え字圏$\mathbf J$に離散圏を使ったもののことだった。
対象が2つしかない離散圏$\mathbf 2$を使えば、次の可換図式を得られる。

![cone_product](https://storage.googleapis.com/zenn-user-upload/05ec6dfa2168-20231028.png)

https://q.uiver.app/#q=WzAsMTcsWzMsMSwiXFxtYXRoYmYgQyJdLFs1LDIsIkQiXSxbNiwyLCJcXERlbHRhKEwpIl0sWzYsMywiXFxEZWx0YShOKSJdLFs1LDEsIlxcbWF0aGJmIENee1xcbWF0aGJmIDJ9Il0sWzMsMiwiTCJdLFszLDMsIk4iXSxbMiwwLCJEIl0sWzMsMCwiXFxEZWx0YSJdLFswLDEsIlxcbWF0aGJmIDIiXSxbMCwyLCIxIl0sWzEsMiwiMiJdLFs4LDEsIlxcbWF0aGJmIEMiXSxbOSwyLCJOIl0sWzksMywiTCJdLFs4LDQsIkQoMSkiXSxbMTAsNCwiRCgyKSJdLFszLDIsIlxcRGVsdGEodSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGVwc2lsb24iXSxbNiw1LCJ1IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIsMSwiXFxldGEiLDJdLFs4LDcsIuaZrumBjeWwhCIsMl0sWzE0LDE1LCJcXGV0YV8xIiwyXSxbMTMsMTUsIlxcZXBzaWxvbl8xIiwyLHsiY3VydmUiOjF9XSxbMTMsMTQsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTQsMTYsIlxcZXRhXzIiXSxbMTMsMTYsIlxcZXBzaWxvbl8yIiwwLHsiY3VydmUiOi0xfV1d

離散圏の対象であることを強調するために、$A$を$1$に、$B$を$2$に置き換えている。また離散圏には自明でない射が存在しないので、極限の可換図式から$f$が消えている。

図式$D: \mathbf 2 \to \mathbf C$は、圏$\mathbf C$の中から2つ対象を選ぶ関手であると捉えられるから、この図はまさに積を表しているといえる。
