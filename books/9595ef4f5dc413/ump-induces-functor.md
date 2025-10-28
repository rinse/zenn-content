---
title: "普遍射による関手の誘導"
free: false
---

## 普遍射による関手の誘導

任意の対象に対して普遍射が存在するとき、関手が定まる。

圏$\mathbf C$, $\mathbf D$, 関手$F : \mathbf C \to \mathbf D$を考える。
$F$から任意の$D \in \mathrm{ob}(\mathbf D)$への普遍射が存在するとき、関手$G : \mathbf D \to \mathbf C$が存在する。

以下では代表として$F$から$D$への普遍射$\langle C, h \rangle$を図示している。

![](https://storage.googleapis.com/zenn-user-upload/54168918d9bd-20250914.png)

$F$から$D$への普遍射$\langle C, h \rangle$に対して、対応関係$G$を次のように定める。

$$
\begin{aligned}
G(D) &\coloneqq C \\
G(d) &\coloneqq c
\end{aligned}
$$

ただし、$d$は$d \circ h' = h \circ F(G(d))$を満たすような射である。
（普遍射の性質より任意の$f : F(C') \to D$に対して$h \circ F(c)$となるような$c : C' \to C$が一意に存在するため、$d \circ h' = h \circ F(G(d))$となるような射$G(d)$）が一意に存在する。

![](https://storage.googleapis.com/zenn-user-upload/e95971453eb0-20250914.png)

このような対応関係$G$は関手になる。

$G(d) \circ G(d') = G(d \circ d')$を示す。
いま、$F$から任意の$D \in \mathrm{ob}(\mathbf D)$に対して普遍射が存在するため、$D'$に対しても$D$と同じ議論ができる。

![](https://storage.googleapis.com/zenn-user-upload/df2623f1cc85-20250914.png)

圏$\mathbf D$の可換図式に注目すると、次の式が得られる：

$$
d \circ d' \circ h'' = h \circ F(G(d)) \circ F(G(d'))
$$

$F$から$\mathbf D$への普遍射$\langle G(D), h \rangle$より、圏$\mathbf D$の射$d \circ d \circ h''$について、圏$\mathbf C$の射$G(d \circ d)$が一意に存在して、$d \circ d \circ h'' = h \circ F(G(d \circ d'))$を満たす。

![](https://storage.googleapis.com/zenn-user-upload/fbf1c12210ee-20250914.png)

よって以下が示せた。

$$
\begin{aligned}
d \circ d' \circ h'' &= h \circ F(G(d)) \circ F(G(d')) \\
&= h \circ F(G(d) \circ G(d')) \\
\end{aligned}
$$

一意性により、$G(d) \circ G(d') = G(d \circ d')$である。証明終わり。

https://q.uiver.app/#q=WzAsNDgsWzAsMSwiXFxtYXRoYmYgQyJdLFswLDMsIkMnIl0sWzAsMiwiQyJdLFsxLDEsIlxcbWF0aGJmIEQiXSxbMSwyLCJEIl0sWzIsMiwiRihDKSJdLFsyLDMsIkYoQycpIl0sWzksMSwiXFxtYXRoYmYgRCJdLFs4LDEsIlxcbWF0aGJmIEMiXSxbOCwyLCJHKEQpIl0sWzgsMywiRyhEJykiXSxbOSwyLCJEIl0sWzEwLDIsIkYoRyhEKSkiXSxbMTAsMywiRihHKEQnKSkiXSxbOSwzLCJEJyJdLFsxLDAsIlxcbWF0aGNsYXB7XlxcZm9yYWxsIEQsIF5cXGZvcmFsbCBmLCBee1xcZXhpc3RzIX0gaCwgZj0gaCBcXGNpcmMgRihjKX0iXSxbOCw0LCJHKEQnJykiXSxbOSw0LCJEJyciXSxbMTAsNCwiRihHKEQnJykpIl0sWzksMCwiXFxtYXRoY2xhcHtHKGQpIFxcY2lyYyBHKGQnKSA9IEcoZCBcXGNpcmMgZCcp44KS56S644GX44Gf44GEfSJdLFsxMiwyLCJHKEQpIl0sWzEyLDMsIkcoRCcnKSJdLFsxMywyLCJEIl0sWzEzLDMsIkQnJyJdLFsxNCwyLCJGKEcoRCkpIl0sWzE0LDMsIkYoRyhEJycpKSJdLFsxMiwxLCJcXG1hdGhiZiBDIl0sWzEzLDEsIlxcbWF0aGJmIEQiXSxbOCw3LCJHKEQpIl0sWzgsOCwiRyhEJykiXSxbOSw3LCJEIl0sWzEwLDcsIkYoRyhEKSkiXSxbMTAsOCwiRihHKEQnJykpIl0sWzksOCwiRCcnIl0sWzQsMSwiXFxtYXRoYmYgQyJdLFs1LDEsIlxcbWF0aGJmIEQiXSxbNCwyLCJHKEQpIl0sWzQsMywiRyhEJykiXSxbNSwyLCJEIl0sWzYsMiwiRihHKEQpKSJdLFs1LDMsIkQnIl0sWzYsMywiRihHKEQnKSkiXSxbOSw1LCJcXG1hdGhjbGFwe+WkluWBtOOBruWPr+aPm+Wbs+W8j+OBq+azqOebruOBmeOCi30iXSxbNSwwLCJcXG1hdGhjbGFwe2QgXFxjaXJjIGgnID0gaCBcXGNpcmMgRihHKGQpKX0iXSxbMTMsMCwiXFxtYXRoY2xhcHtkIFxcY2lyYyBkJyBcXGNpcmMgaCcnID0gaCBcXGNpcmMgRihHKGQgXFxjaXJjIGQnKSl9Il0sWzksNiwiXFxtYXRoY2xhcHtkIFxcY2lyYyBkJyBcXGNpcmMgaCcnID0gaCBcXGNpcmMgRihHKGQpKSBcXGNpcmMgRihHKGQnKSl9Il0sWzE0LDUsIlxcbWF0aGNsYXB7aCBcXGNpcmMgRihHKGQpKSBcXGNpcmMgRihHKGQnKSkgPSBoIFxcY2lyYyBGKEcoZCBcXGNpcmMgZCcpKX0iXSxbMTQsNiwiXFxtYXRoY2xhcHvkuIDmhI/mgKfjgYvjgonjgIFHKGQpIFxcY2lyYyBHKGQnKSA9IEcoZCBcXGNpcmMgZCcpfSJdLFsxLDIsImMiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNSw0LCJoIiwyXSxbNiw1LCJGKGMpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzYsNCwiZiJdLFs2LDQsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7Im9mZnNldCI6NCwic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzAsMywiRiJdLFs4LDcsIkYiXSxbMTAsOSwiRyhkKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMywxMiwiRihHKGQpKSIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxMiwxMSwiaCIsMl0sWzEzLDE0LCJoJyJdLFsxMywxMSwiXFxjaXJjbGVhcnJvd3JpZ2h0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzE2LDEwLCJHKGQnKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dLFsxNywxNCwiZCciXSxbMTgsMTMsIkYoRyhkJykpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzE4LDE3LCJoJyciXSxbMTgsMTQsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsxNCwxMSwiZCJdLFsyMywyMiwiZCBcXGNpcmMgZCciXSxbMjUsMjQsIkYoRyhkIFxcY2lyYyBkJykpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzI0LDIyLCJoIiwyXSxbMjYsMjcsIkYiXSxbMjEsMjAsIkcoZCBcXGNpcmMgZCcpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzMxLDMwLCJoIiwyXSxbMzIsMzEsIkYoRyhkKSkgXFxjaXJjIEYoRyhkJykpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzMyLDMzLCJoJyciXSxbMzMsMzAsImQnIFxcY2lyYyBkIl0sWzMyLDMwLCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMjUsMjIsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsyNSwyMywiaCcnIl0sWzM0LDM1LCJGIl0sWzM3LDM2LCJHKGQpIiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzM5LDM4LCJoIiwyXSxbNDAsMzgsImQiXSxbNDEsMzksIkYoRyhkKSkiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNDEsNDAsImgnIl0sWzQxLDM4LCJcXGNpcmNsZWFycm93cmlnaHQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMzUsMzQsIkcoRCkgXFxjb2xvbmVxcSBDIFxcXFwgRyhkKSBcXGNvbG9uZXFxIGMiLDAseyJvZmZzZXQiOi0zfV0sWzI5LDI4LCJHKGQpIFxcY2lyYyBHKGQnKSIsMCx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dXQ==
