---
title: "コンマ圏は普遍性を満たす"
free: false
---

## 定理

コンマ圏$F \downarrow G$を考える。このとき関手$P_0$, $P_1$, 自然変換 $\eta : F \circ P_0 \Rightarrow G \circ P_1$ が存在する。

![](https://storage.googleapis.com/zenn-user-upload/b021b190e6d5-20250324.png)

このとき、同じ条件を満たす任意の4つ組$\lang \mathbf{X}, Q_0, Q_1, \theta \rang$に対して関手$H : \mathbf{X} \to F \downarrow G$が一意に存在して、以下の条件を満たす。

$$
\begin{split}
Q_0 =& P_0 \circ H  \\
Q_1 =& P_1 \circ H \\
\theta =& \eta \ast H
\end{split}
$$

[![](https://storage.googleapis.com/zenn-user-upload/2a39166cba0c-20250324.png)](https://q.uiver.app/#q=WzAsMTgsWzMsMSwiRiBcXGRvd25hcnJvdyBHIl0sWzQsMSwiXFxtYXRoYmZ7RX0iXSxbNCwyLCJcXG1hdGhiZntDfSJdLFszLDIsIlxcbWF0aGJme0R9Il0sWzIsMCwiWCJdLFs1LDAsIlgiXSxbNywxLCJcXG1hdGhiZntFfSJdLFs3LDIsIlxcbWF0aGJme0N9Il0sWzYsMiwiXFxtYXRoYmZ7RH0iXSxbOCwwLCJYIl0sWzksMiwiXFxtYXRoYmZ7RH0iXSxbMTAsMSwiXFxtYXRoYmZ7RX0iXSxbMTAsMiwiXFxtYXRoYmZ7Q30iXSxbMCwxLCJGIFxcZG93bmFycm93IEciXSxbMSwxLCJcXG1hdGhiZntFfSJdLFsxLDIsIlxcbWF0aGJme0N9Il0sWzAsMiwiXFxtYXRoYmZ7RH0iXSxbMCwwLCJcXG1hdGhiZntDYXR9Il0sWzAsMSwiUF8xIl0sWzEsMiwiRyJdLFswLDMsIlBfMCIsMl0sWzMsMiwiRiIsMl0sWzMsMSwiXFxldGEiLDEseyJsZXZlbCI6Mn1dLFs0LDAsIkgiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNCwzLCJRXzAiLDIseyJjdXJ2ZSI6MX1dLFs0LDEsIlFfMSIsMCx7ImN1cnZlIjotMX1dLFs1LDYsIlFfMSIsMCx7ImN1cnZlIjotMX1dLFs2LDcsIkciXSxbNSw4LCJRXzAiLDIseyJjdXJ2ZSI6MX1dLFs4LDYsIlxcdGhldGEiLDAseyJsZXZlbCI6Mn1dLFs4LDcsIkYiLDJdLFsxMCwxMiwiRiIsMl0sWzExLDEyLCJHIl0sWzEwLDExLCJcXGV0YSBcXGFzdCBIIiwwLHsibGV2ZWwiOjJ9XSxbOSwxMCwiUF8wIFxcY2lyYyBIIiwyLHsiY3VydmUiOjF9XSxbOSwxMSwiUF8xIFxcY2lyYyBIIiwwLHsiY3VydmUiOi0xfV0sWzEzLDE0LCJQXzEiXSxbMTQsMTUsIkciXSxbMTMsMTYsIlBfMCIsMl0sWzE2LDE1LCJGIiwyXSxbMTYsMTQsIlxcZXRhIiwxLHsibGV2ZWwiOjJ9XV0=)

## 証明

関手$P_0 : F \downarrow G \to \mathbf{D}$は以下のように定義する。
$P_1 : F \downarrow G \to \mathbf{E}$も同じように定義する。

$$
\begin{split}
P_0 :& \lang D, E, f \rang \mapsto D \\
P_0 :& \lang d, e \rang \mapsto d \\
\end{split}
$$

また自然変換$\eta : F \circ P_0 \Rightarrow G \circ P_1 $は以下のように定義する。

$$
\eta_{\lang D, E, f \rang} \overset{def}{=} f
$$

TODO: 普遍性の条件はどのように確かめればいいのだろうか？

## アイデア

関手$F : \mathbf{D} \to \mathbf{C}$, $G : \mathbf{E} \to \mathbf{C}$を考える。

![](https://storage.googleapis.com/zenn-user-upload/ba1e951d8a30-20250323.png)

この形から普遍性を満たすものを考えたとき、最初に思い浮かぶのは[引き戻し](./pullback)である。

つまりこういう関手$H$が一意に存在して、$Q_0 = P_0 \circ H$, $Q_1 = P1_1 \circ H$をそれぞれ満たしてくれるやつがいたらいいなと思うわけである。

[![](https://storage.googleapis.com/zenn-user-upload/e8d5a6f418ed-20250323.png)](https://q.uiver.app/#q=WzAsNSxbMiwyLCJcXG1hdGhiZntDfSJdLFsxLDIsIlxcbWF0aGJme0R9Il0sWzIsMSwiXFxtYXRoYmZ7RX0iXSxbMSwxLCJcXG1hdGhiZntEfSBcXHRpbWVzX1xcbWF0aGJme0N9IFxcbWF0aGJme0V9Il0sWzAsMCwiXFxtYXRoYmZ7WH0iXSxbMSwwLCJGIiwyXSxbMiwwLCJHIl0sWzMsMSwiUF8wIiwyXSxbMywyLCJQXzEiXSxbMywwLCJcXGNpcmNsZWFycm93bGVmdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs0LDMsIkgiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNCwxLCJRXzAiLDIseyJjdXJ2ZSI6MX1dLFs0LDIsIlFfMSIsMCx7ImN1cnZlIjotMX1dXQ==)

しかしながら各対象が圏であり、各射が関手であることを思い出すと、（圏同型より圏同値のほうが有用であるように）この可換性の条件は強すぎるように思われる。

普遍性とは、何か条件を決めて、その条件を満たす者たちの中で一番えらいやつのことだ。そこで条件として自然変換を採用しよう。

コンマ圏$F \downarrow G$は、この条件を満たす圏である。

[![](https://storage.googleapis.com/zenn-user-upload/07e585589c3c-20250323.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJGIFxcZG93bmFycm93IEciXSxbMSwwLCJcXG1hdGhiZntFfSJdLFsxLDEsIlxcbWF0aGJme0N9Il0sWzAsMSwiXFxtYXRoYmZ7RH0iXSxbMCwxLCJQXzEiXSxbMSwyLCJHIl0sWzAsMywiUF8wIiwyXSxbMywyLCJGIiwyXSxbMywxLCJcXGV0YSIsMSx7ImxldmVsIjoyfV1d)

関手$P_0 : F \downarrow G \to \mathbf{D}$は以下のように定義される。
$P_1 : F \downarrow G \to \mathbf{E}$も同じように定義する。

$$
\begin{split}
P_0 :& \lang D, E, f \rang \mapsto D \\
P_0 :& \lang d, e \rang \mapsto d \\
\end{split}
$$

[![](https://storage.googleapis.com/zenn-user-upload/e667976fc504-20250323.png)](https://q.uiver.app/#q=WzAsMTAsWzAsMCwiRiBcXGRvd25hcnJvdyBHIl0sWzEsMCwiXFxtYXRoYmZ7RX0iXSxbMSwxLCJcXG1hdGhiZntDfSJdLFswLDEsIlxcbWF0aGJme0R9Il0sWzIsMCwiRiBcXGRvd25hcnJvdyBHIl0sWzMsMCwiXFxtYXRoYmZ7RH0iXSxbMiwxLCJcXGxhbmcgRCwgRSwgZiBcXHJhbmciXSxbMywxLCJEIl0sWzMsMiwiRCciXSxbMiwyLCJcXGxhbmcgRCcsIEUnLCBmJyBcXHJhbmciXSxbMCwxLCJQXzEiXSxbMSwyLCJHIl0sWzAsMywiUF8wIiwyXSxbMywyLCJGIiwyXSxbMywxLCJcXGV0YSIsMSx7ImxldmVsIjoyfV0sWzQsNSwiUF8wIl0sWzYsOSwiXFxsYW5nIGQsIGUgXFxyYW5nIiwyXSxbNyw4LCJkIiwyXV0=)

次に自然変換$\eta : F \circ P_0 \Rightarrow G \circ P_1$について考える。
各成分について愚直に書き出すと次のような図式が得られる。

[![](https://storage.googleapis.com/zenn-user-upload/b6ad051eb366-20250323.png)](https://q.uiver.app/#q=WzAsOSxbMCwxLCJGIFxcZG93bmFycm93IEciXSxbMSwxLCJcXG1hdGhiZntFfSJdLFsxLDIsIlxcbWF0aGJme0N9Il0sWzAsMiwiXFxtYXRoYmZ7RH0iXSxbMywwLCJcXG1hdGhiZntDfSJdLFszLDEsIkYoUF8wKFxcbGFuZyBELCBFLCBmIFxccmFuZykpIl0sWzMsMiwiRyhQXzEoXFxsYW5nIEQsIEUsIGYgXFxyYW5nKSkiXSxbNCwxLCJGKFBfMChcXGxhbmcgRCcsIEUnLCBmJyBcXHJhbmcpKSJdLFs0LDIsIkcoUF8xKFxcbGFuZyBEJywgRScsIGYnIFxccmFuZykpIl0sWzAsMSwiUF8xIl0sWzEsMiwiRyJdLFswLDMsIlBfMCIsMl0sWzMsMiwiRiIsMl0sWzMsMSwiXFxldGEiLDEseyJsZXZlbCI6Mn1dLFs1LDYsIlxcZXRhX3tcXGxhbmcgRCwgRSwgZiBcXHJhbmd9IiwyXSxbNyw4LCJcXGV0YV97XFxsYW5nIEQnLCBFJywgZicgXFxyYW5nfSJdLFs1LDcsIkYoUF8wKFxcbGFuZyBkLCBlIFxccmFuZykpIl0sWzYsOCwiRyhQXzEoXFxsYW5nIGQsIGUgXFxyYW5nKSkiLDJdLFs1LDgsIlxcY2lyY2xlYXJyb3dsZWZ0IiwxLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoibm9uZSJ9LCJoZWFkIjp7Im5hbWUiOiJub25lIn19fV1d)

$P_0$, $P_1$の定義を思い出して図式を整理すると次のようになる。

[![](https://storage.googleapis.com/zenn-user-upload/0044035a3ac4-20250323.png)](https://q.uiver.app/#q=WzAsOSxbMCwxLCJGIFxcZG93bmFycm93IEciXSxbMSwxLCJcXG1hdGhiZntFfSJdLFsxLDIsIlxcbWF0aGJme0N9Il0sWzAsMiwiXFxtYXRoYmZ7RH0iXSxbMywwLCJcXG1hdGhiZntDfSJdLFszLDEsIkYoRCkiXSxbMywyLCJHKEUpIl0sWzQsMSwiRihEJykiXSxbNCwyLCJHKEUnKSJdLFswLDEsIlBfMSJdLFsxLDIsIkciXSxbMCwzLCJQXzAiLDJdLFszLDIsIkYiLDJdLFszLDEsIlxcZXRhIiwxLHsibGV2ZWwiOjJ9XSxbNSw2LCJcXGV0YV97XFxsYW5nIEQsIEUsIGYgXFxyYW5nfSIsMl0sWzcsOCwiXFxldGFfe1xcbGFuZyBEJywgRScsIGYnIFxccmFuZ30iXSxbNSw3LCJGKGQpIl0sWzYsOCwiRyhlKSIsMl0sWzUsOCwiXFxjaXJjbGVhcnJvd2xlZnQiLDEseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJub25lIn0sImhlYWQiOnsibmFtZSI6Im5vbmUifX19XV0=)

コンマ圏の定義に照らして、圏$\mathbf{C}$の射$f : F(D) \to G(E)$は、まさにこの可換性を満たす射であるから、$\eta_{\lang D, E, f \rang}$を$f$で定義する。

$$
\eta_{\lang D, E, f \rang} \mapsto f
$$

これでコンマ圏$F \downarrow G$について、$P_0$, $P_1$, $\eta$を定義できた。

[![](https://storage.googleapis.com/zenn-user-upload/07e585589c3c-20250323.png)](https://q.uiver.app/#q=WzAsNCxbMCwwLCJGIFxcZG93bmFycm93IEciXSxbMSwwLCJcXG1hdGhiZntFfSJdLFsxLDEsIlxcbWF0aGJme0N9Il0sWzAsMSwiXFxtYXRoYmZ7RH0iXSxbMCwxLCJQXzEiXSxbMSwyLCJHIl0sWzAsMywiUF8wIiwyXSxbMywyLCJGIiwyXSxbMywxLCJcXGV0YSIsMSx7ImxldmVsIjoyfV1d)

このコンマ圏が同じ条件を満たす組に対して普遍性を満たすので、コンマ圏が重要だというわけである。
