---
title: "モノ射とエピ射"
free: false
---

## モノ射

モノ射 (*Monic morphism*) とは、圏論における単射をいう。
集合の圏上では、モノ射は単射に一致する。

### 定義

$f$がモノ射であるとは、$f$が任意の射$g_1$, $g_2$に対して$f \circ g_1 = f \circ g_2 \implies g_1 = g_2$を満たすことをいう。これを左簡約可能という。
モノ射$f$をしばしば$f: X \hookrightarrow Y$と書く。

![monic_morphism](https://storage.googleapis.com/zenn-user-upload/ef831ef81d16-20240104.png)
https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMSwiQyJdLFsxLDIsImdfMSIsMCx7ImN1cnZlIjotMX1dLFsxLDIsImdfMiIsMix7ImN1cnZlIjoxfV0sWzIsMywiZiIsMCx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Imhvb2siLCJzaWRlIjoidG9wIn19fV1d

### 記法

モノ射を$f: X \rightarrowtail Y$と書く資料も存在するが、このノートではフック付きの矢印を用いて$f: X \hookrightarrow Y$と書く。

## エピ射

エピ射 (*Epic morphism*) とは、圏論における全射をいう。
集合の圏上では、エピ射は全射に一致する。

### 定義

$f$がエピ射であるとは、$f$が任意の射$g_1$, $g_2$に対して$g_1 \circ f = g_2 \circ f \implies g_1 = g_2$を満たすことをいう。これを右簡約可能という。
エピ射$f$をしばしば$f: X \twoheadrightarrow Y$と書く。

![epic_morphism](https://storage.googleapis.com/zenn-user-upload/87dcdb5dd322-20240104.png)
https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzIsMSwiQyJdLFsxLDIsImYiLDAseyJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJlcGkifX19XSxbMiwzLCJnXzEiLDAseyJjdXJ2ZSI6LTF9XSxbMiwzLCJnXzIiLDIseyJjdXJ2ZSI6MX1dXQ==

### 余談

全射を英語でsurjectiveというが、語根のsur-はラテン語由来で「上に」を意味する。エピ射のepi-はギリシャ語由来で、これも「上に」を意味する。
域が余域を覆うようなイメージなのだろう。
