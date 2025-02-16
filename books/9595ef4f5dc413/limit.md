---
title: "極限"
free: false
---

極限とは、普遍性の特殊な場合である。積などの幅広い概念が極限に一般化される。

単に極限と言ったときには、圏$\mathbf{J}$を形とする[図式](diagram-and-index-category)$D: \mathbf{J} \to \mathbf{C}$の極限(*Limit*)を指す。

## 定義

$D: \mathbf J \to \mathbf C$をCにおける図式とすると、$D$への錐とは、$\mathbf J$の対象をすべて$\mathbf C$の対象$N$に写し、$\mathbf J$の射をすべて$\mathrm{id}_N$に写す定関手$\Delta_N: \mathbf J \to \mathbf C$から図式$D$への自然変換$\epsilon: \Delta_N \Rightarrow D$としてあらわされる。

[![redundant_cone](https://storage.googleapis.com/zenn-user-upload/aad39b1ad3a4-20250216.png)](https://q.uiver.app/#q=WzAsOCxbMywwLCJcXG1hdGhiZiBDIl0sWzIsMSwiXFxEZWx0YV9OKEEpIl0sWzIsMiwiRChBKSJdLFs0LDIsIkQoQikiXSxbMCwwLCJcXG1hdGhiZiBKIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbNCwxLCJcXERlbHRhX04oQikiXSxbMiwzLCJEKGYpIiwyXSxbMSwyLCJcXGVwc2lsb25fQSIsMl0sWzUsNiwiZiJdLFs3LDMsIlxcZXBzaWxvbl9CIl0sWzEsNywiXFxEZWx0YV9OKGYpPWlkX04iXSxbMSwzLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

ここで、$\Delta_N(A)$, $\Delta_N(B)$は共に対象$N$のことなので、次のように可換図式を整理できる。

[![cone](https://storage.googleapis.com/zenn-user-upload/39e58f538ec7-20250216.png)](https://q.uiver.app/#q=WzAsNyxbMywwLCJcXG1hdGhiZiBDIl0sWzMsMSwiTiJdLFsyLDIsIkQoQSkiXSxbNCwyLCJEKEIpIl0sWzAsMCwiXFxtYXRoYmYgSiJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMywiRChmKSIsMl0sWzEsMiwiXFxlcHNpbG9uX0EiLDJdLFs1LDYsImYiXSxbMSwzLCJcXGVwc2lsb25fQiJdLFsyLDMsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsib2Zmc2V0IjotNSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

この三角形を構成する組$(N, \epsilon)$を錐(*Cone*)と呼ぶ。

$D$の極限とは、$D$への錐$(L, \eta)$であって、任意の錐の対象$N$に対して一意な仲介射(*Mediating morphism*)$u: N \to L$が存在して、$\mathbf J$の任意の対象$X$に対して$\epsilon_X = \eta_X \circ u$を満たすものである。

[![limit](https://storage.googleapis.com/zenn-user-upload/bd97da2f588d-20250216.png)](https://q.uiver.app/#q=WzAsOCxbMywwLCJcXG1hdGhiZiBDIl0sWzIsMywiRChBKSJdLFs0LDMsIkQoQikiXSxbMCwwLCJcXG1hdGhiZiBKIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbMywyLCJMIl0sWzMsMSwiTiJdLFsxLDIsIkQoZikiLDJdLFs0LDUsImYiXSxbNiwyLCJcXGV0YV9CIiwxXSxbNiwxLCJcXGV0YV9BIiwxXSxbNywxLCJcXGVwc2lsb25fQSIsMix7ImN1cnZlIjoxfV0sWzcsMiwiXFxlcHNpbG9uX0IiLDAseyJjdXJ2ZSI6LTF9XSxbNyw2LCJ1IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEsMiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJvZmZzZXQiOi01LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbNywxLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs3LDIsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

## 普遍性を用いた定義

関手$F: \mathbf C \to \mathbf D$から圏$\mathbf D$の対象Aへの普遍射とは、以下の可換図式上の組$(X, u)$のことだった。

[![opposite_universal_morphism](https://storage.googleapis.com/zenn-user-upload/3cd7ffb5cf32-20250216.png)](https://q.uiver.app/#q=WzAsOSxbMCwwLCJcXG1hdGhiZiBDIl0sWzEsMSwiQSJdLFsyLDEsIkYoWCkiXSxbMiwyLCJGKFkpIl0sWzEsMCwiXFxtYXRoYmYgRCJdLFswLDEsIlgiXSxbMCwyLCJZIl0sWzMsMCwiQSJdLFs0LDAsIkYiXSxbMywyLCJGKGcpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzMsMSwiZiJdLFs2LDUsImciLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiwxLCJ1IiwyXSxbOCw3LCLmma7pgY3lsIQiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7Im9mZnNldCI6NCwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

極限は関手$\Delta: \mathbf C \to \mathbf C^{\mathbf J}$から圏$\mathbf C^{\mathbf J}$の対象$D$への普遍射$(L, \eta)$として表すことができる。

[![limit_universal_morphism](https://storage.googleapis.com/zenn-user-upload/521b9221984d-20250216.png)](https://q.uiver.app/#q=WzAsMTIsWzIsMCwiXFxtYXRoYmYgQyJdLFszLDEsIkQiXSxbNCwxLCJcXERlbHRhKEwpIl0sWzQsMiwiXFxEZWx0YShOKSJdLFszLDAsIlxcbWF0aGJmIENee1xcbWF0aGJmIEp9Il0sWzIsMSwiTCJdLFsyLDIsIk4iXSxbNCwwLCJEIl0sWzUsMCwiXFxEZWx0YSJdLFswLDAsIlxcbWF0aGJmIEoiXSxbMCwxLCJBIl0sWzEsMSwiQiJdLFszLDIsIlxcRGVsdGEodSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGVwc2lsb24iXSxbNiw1LCJ1IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIsMSwiXFxldGEiLDJdLFsxMCwxMSwiZiJdLFs4LDcsIuaZrumBjeWwhCIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFszLDEsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsib2Zmc2V0Ijo0LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

ここで圏$\mathbf C^{\mathbf J}$とは、$\mathbf J$から$\mathbf C$への関手を対象として持ち、それらの間の自然変換を射として持つ関手圏である。ゆえに対象$D$は$\mathbf J \to \mathbf C$の関手である。

また関手$\Delta: \mathbf C \to \mathbf C^{\mathbf J}$は、圏$\mathbf C$の対象$X$を定関手$\Delta_X$に写し、射$f: X \to Y$を$\Delta(f): \Delta_X \Rightarrow \Delta_Y$に写す関手である。すなわち$\Delta(X)=\Delta_X: \mathbf J \to \mathbf C$であり、圏$\mathbf C$上では任意の$J \in \mathbf J$に対して$\Delta(f)_J=f: X \to Y$である。
なお$\Delta$は積の例に登場した対角関手$\mathbf C \to \mathbf C \times \mathbf C$の一般化である。（添え字圏$\mathbf J$に離散圏$\mathbf 2$を使うことで$\mathbf C \to \mathbf C^{\mathbf 2}$を得られる。自明に$\mathbf C^{\mathbf 2} \simeq \mathbf C \times \mathbf C$である）

さて、積の時と同様に、上の普遍射の可換図式が極限のそれと一致することを確認していこう。

まずは$\mathbf C^{\mathbf J}$を圏$\mathbf C$上に書き下してみよう。

[![redundant_cone_limit](https://storage.googleapis.com/zenn-user-upload/efb6147574e6-20250216.png)](https://q.uiver.app/#q=WzAsMTksWzIsMCwiXFxtYXRoYmYgQyJdLFszLDEsIkQiXSxbNCwxLCJcXERlbHRhKEwpIl0sWzQsMiwiXFxEZWx0YShOKSJdLFszLDAsIlxcbWF0aGJmIENee1xcbWF0aGJmIEp9Il0sWzIsMSwiTCJdLFsyLDIsIk4iXSxbNiwwLCJEIl0sWzcsMCwiXFxEZWx0YSJdLFswLDAsIlxcbWF0aGJmIEoiXSxbMCwxLCJBIl0sWzEsMSwiQiJdLFs1LDAsIlxcbWF0aGJmIEMiXSxbNiwxLCJcXERlbHRhX04oQSkiXSxbNywxLCJcXERlbHRhX04oQikiXSxbNiwyLCJcXERlbHRhX0woQSkiXSxbNywyLCJcXERlbHRhX0woQikiXSxbNSwzLCJEKEEpIl0sWzgsMywiRChCKSJdLFszLDIsIlxcRGVsdGEodSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMywxLCJcXGVwc2lsb24iXSxbNiw1LCJ1IiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzIsMSwiXFxldGEiLDJdLFsxMCwxMSwiZiJdLFs4LDcsIuaZrumBjeWwhCIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMywxNCwiXFxEZWx0YV9OKGYpIl0sWzE1LDE2LCJcXERlbHRhX0woZikiLDJdLFsxNywxOCwiRChmKSIsMl0sWzE1LDE3LCJcXGV0YV9BIiwxXSxbMTYsMTgsIlxcZXRhX0IiLDFdLFsxMywxNywiXFxlcHNpbG9uX0EiLDIseyJjdXJ2ZSI6MX1dLFsxNCwxOCwiXFxlcHNpbG9uX0IiLDAseyJjdXJ2ZSI6LTF9XSxbMTQsMTYsIlxcRGVsdGEodSlfe0J9IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEzLDE1LCJcXERlbHRhKHUpX3tBfSIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMywxNiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTMsMTcsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzE0LDE4LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxNSwxOCwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJsYWJlbF9wb3NpdGlvbiI6MjAsIm9mZnNldCI6NSwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

ここで、定関手$\Delta_X$は$\mathbf J$の対象をすべて$\mathbf C$の対象$X$に写すから、$\Delta_L(A) = \Delta_L(B) = L$、かつ$\Delta_N(A) = \Delta_N(B) = N$だ。また$\Delta(u)$は任意の$J \in \mathbf J$に対して$\Delta(u)_J = u$であるから、$\Delta(u)_A = \Delta(u)_B = u$だ。

これらから上の可換図式を整理すると、次の可換図式を得られる。これはまさに、錐から作った極限の図式と同じだ。

[![cone_limit](https://storage.googleapis.com/zenn-user-upload/07ed9ace823b-20250216.png)](https://q.uiver.app/#q=WzAsOCxbMywwLCJcXG1hdGhiZiBDIl0sWzIsMywiRChBKSJdLFs0LDMsIkQoQikiXSxbMCwwLCJcXG1hdGhiZiBKIl0sWzAsMSwiQSJdLFsxLDEsIkIiXSxbMywyLCJMIl0sWzMsMSwiTiJdLFsxLDIsIkQoZikiLDJdLFs0LDUsImYiXSxbNiwyLCJcXGV0YV9CIiwxXSxbNiwxLCJcXGV0YV9BIiwxXSxbNywxLCJcXGVwc2lsb25fQSIsMix7ImN1cnZlIjoxfV0sWzcsMiwiXFxlcHNpbG9uX0IiLDAseyJjdXJ2ZSI6LTF9XSxbNyw2LCJ1IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzEsMiwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJvZmZzZXQiOi01LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbNywxLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs3LDIsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

余談だが、積とは、極限の添え字圏$\mathbf J$に離散圏を使ったもののことだった。
対象が2つしかない離散圏$\mathbf 2$を使えば、次の可換図式を得られる。

[![cone_product](https://storage.googleapis.com/zenn-user-upload/d54261ce0a83-20250216.png)](https://q.uiver.app/#q=WzAsMTcsWzIsMSwiXFxtYXRoYmYgQyJdLFszLDIsIkQiXSxbNCwyLCJcXERlbHRhKEwpIl0sWzQsMywiXFxEZWx0YShOKSJdLFszLDEsIlxcbWF0aGJmIENee1xcbWF0aGJmIDJ9Il0sWzIsMiwiTCJdLFsyLDMsIk4iXSxbMywwLCJEIl0sWzQsMCwiXFxEZWx0YSJdLFswLDEsIlxcbWF0aGJmIDIiXSxbMCwyLCIxIl0sWzEsMiwiMiJdLFs1LDEsIlxcbWF0aGJmIEMiXSxbNiwyLCJOIl0sWzYsMywiTCJdLFs1LDQsIkQoMSkiXSxbNyw0LCJEKDIpIl0sWzMsMiwiXFxEZWx0YSh1KSIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFszLDEsIlxcZXBzaWxvbiJdLFs2LDUsInUiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMiwxLCJcXGV0YSIsMl0sWzE0LDE1LCJcXGV0YV8xIiwxXSxbMTMsMTUsIlxcZXBzaWxvbl8xIiwyLHsiY3VydmUiOjF9XSxbMTMsMTQsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMTQsMTYsIlxcZXRhXzIiLDFdLFsxMywxNiwiXFxlcHNpbG9uXzIiLDAseyJjdXJ2ZSI6LTF9XSxbOCw3LCLmma7pgY3lsIQiLDJdLFszLDEsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsib2Zmc2V0Ijo0LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTMsMTUsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzEzLDE2LCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

離散圏の対象であることを強調するために、$A$を$1$に、$B$を$2$に置き換えている。また離散圏には自明でない射が存在しないので、極限の可換図式から$f$が消えている。

図式$D: \mathbf 2 \to \mathbf C$は、圏$\mathbf C$の中から2つ対象を選ぶ関手であると捉えられるから、この図はまさに積を表しているといえる。

## 記法

- 図式$F : \mathbf{J} \to \mathbf{C}$の極限$(L, \eta)$を$\varprojlim_{j \in \mathbf{J}} F_j$と書くことがある。
    * この場合、図式$F : \mathbf{J} \to \mathbf{C}$の余極限を$\varinjlim_{j \in \mathbf{J}} F_j$と書く。
- より簡潔に$\varprojlim{F_j}$や$\varprojlim{F}$と書くこともある。
    * 同様に余極限を$\varinjlim{F_j}$や$\varinjlim F$と書く。
- またこれらの記号を、そのまま極限の組$(L, \eta)$のうち対象$L$を示すのに使うことがある。
    * すなわち$\varprojlim_{j \in \mathbf{J}} F_j \in \mathrm{ob}(\mathbf{C})$.
- 矢印の向きに注意。極限が左向きで、余極限が右向き。
