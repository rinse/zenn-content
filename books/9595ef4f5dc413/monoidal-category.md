---
title: "モノイダル圏"
free: false
---

## 定義

モノイダル圏(*Monoidal category*)とは、以下の構造を備えた圏$\mathbf{C}$をいう:

1. モノイダル積と呼ばれる双関手$\otimes: \mathbf{C} \times \mathbf{C} \to \mathbf{C}$
2. 単位対象$I$
3. 結合子(*Associator*)と呼ばれる、$\otimes$の結合律を保証する自然同型$\alpha$
    * 任意の対象$A$, $B$, $C$に対して$\alpha_{A, B, C}: (A \otimes B) \otimes C \simeq A \otimes (B \otimes C)$
4. 左単位律を保証する自然同型$\lambda$
    * 任意の対象$A$に対して$\lambda_A: I \otimes A \simeq A$
5. 右単位律を保証する自然同型$\rho$
    * 任意の対象$A$に対して$\rho_A: A \otimes I \simeq A$

あるいは圏$\mathbf{C}$と上の5つを合わせた6つ組$(\mathbf{C}, \otimes, I, \alpha, \lambda, \rho)$をモノイダル圏と呼ぶ。簡単に3つ組$(\mathbf{C}, \otimes, I)$をモノイダル圏と呼ぶ場合もある。

このとき自然変換$\alpha$, $\lambda$, $\rho$はコヒーレンス条件(*Coherence condition*)を満たす。すなわち以下の図式を可換にしなければならない。

![Coherence1](https://storage.googleapis.com/zenn-user-upload/381d63f3ba37-20231227.png)

https://q.uiver.app/#q=WzAsMTIsWzUsMSwiKEEgXFxvdGltZXMgKEIgXFxvdGltZXMgQykpIFxcb3RpbWVzIEQiXSxbNSwyLCJBIFxcb3RpbWVzICgoQiBcXG90aW1lcyBDKSBcXG90aW1lcyBEKSJdLFszLDEsIigoQSBcXG90aW1lcyBCKSBcXG90aW1lcyBDKSBcXG90aW1lcyBEIl0sWzUsMywiQSBcXG90aW1lcyAoQiBcXG90aW1lcyAoQyBcXG90aW1lcyBEKSkiXSxbMywzLCIoQSBcXG90aW1lcyBCKSBcXG90aW1lcyAoQyBcXG90aW1lcyBEKSJdLFswLDEsIkEiXSxbMSwxLCJCIl0sWzAsMywiQSBcXG90aW1lcyBCIl0sWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMCwyLCJBJyJdLFsxLDIsIkInIl0sWzEsMywiQScgXFxvdGltZXMgQiciXSxbMiwwLCJcXGFscGhhX3tBLCBCLCBDfSBcXG90aW1lcyBcXG1hdGhybXtpZH1fRCJdLFswLDEsIlxcYWxwaGFfe0EsQiBcXG90aW1lcyBDLCBEfSJdLFsyLDQsIlxcYWxwaGFfe0EgXFxvdGltZXMgQiwgQywgRH0iLDJdLFs0LDMsIlxcYWxwaGFfe0EsIEIsIEMgXFxvdGltZXMgRH0iLDJdLFsxLDMsIlxcbWF0aHJte2lkfV9BIFxcb3RpbWVzIFxcYWxwaGFfe0IsIEMsIER9Il0sWzUsNiwiZiJdLFs5LDEwLCJmJyJdLFs3LDExLCJmIFxcb3RpbWVzIGYnIl1d

![Coherence2](https://storage.googleapis.com/zenn-user-upload/30d53ffacc05-20231227.png)

https://q.uiver.app/#q=WzAsNCxbMCwxLCIoQSBcXG90aW1lcyBJKSBcXG90aW1lcyBCIl0sWzIsMSwiQSBcXG90aW1lcyAoSSBcXG90aW1lcyBCKSJdLFsxLDIsIkEgXFxvdGltZXMgQiJdLFswLDAsIlxcbWF0aGJme0N9Il0sWzAsMSwiXFxhbHBoYV97QSwgSSwgQn0iXSxbMCwyLCJcXHJob19BIFxcb3RpbWVzIFxcbWF0aHJte2lkfV9CIiwyXSxbMSwyLCJcXG1hdGhybXtpZH1fQSBcXG90aW1lcyBcXGxhbWJkYV9CIl1d

## モノイド対象

モノイダル圏$(\mathbf{C}, \otimes, I, \alpha, \lambda, \rho)$が与えられたとき、$\mathbf{C}$の対象$M$および2つの射$\mu: M \otimes M \to M$, $\eta: I \to M$の3つ組$(M, \mu, \eta)$をモノイド対象と呼ぶ。

このとき射$\mu$, $\eta$は以下の図式を可換にしなければならない。

![Coherence3](https://storage.googleapis.com/zenn-user-upload/39f424fa2398-20231228.png)

https://q.uiver.app/#q=WzAsMTAsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMCwxLCIoTSBcXG90aW1lcyBNKSBcXG90aW1lcyBNIl0sWzIsMSwiTSBcXG90aW1lcyAoTSBcXG90aW1lcyBNKSJdLFswLDIsIk0gXFxvdGltZXMgTSJdLFsyLDIsIk0gXFxvdGltZXMgTSJdLFsxLDMsIk0iXSxbMCw0LCJNIFxcb3RpbWVzIEkiXSxbMSw0LCJNIFxcb3RpbWVzIE0iXSxbMiw0LCJJIFxcb3RpbWVzIE0iXSxbMSw1LCJNIl0sWzEsMiwiXFxhbHBoYV97TSwgTSwgTX0iXSxbMSwzLCJcXG11IFxcb3RpbWVzIFxcbWF0aHJte2lkfV9NIiwyXSxbMiw0LCJcXG1hdGhybXtpZH1fTSBcXG90aW1lcyBcXG11Il0sWzMsNSwiXFxtdSIsMl0sWzQsNSwiXFxtdSJdLFs2LDcsIlxcbWF0aHJte2lkfV9NIFxcb3RpbWVzIFxcZXRhIl0sWzgsNywiXFxldGEgXFxvdGltZXMgXFxtYXRocm17aWR9X00iLDJdLFs2LDksIlxccmhvX00iLDJdLFs4LDksIlxcbGFtYmRhX00iXSxbNyw5LCJcXG11Il1d

## 強モノイダル圏

モノイダル圏$(\mathbf{C}, \otimes, I, \alpha, \lambda, \rho)$のうち、自然同型$\alpha$, $\lambda$, $\rho$のいずれもが恒等射であるとき、これを特に強モノイダル圏(*Strict monoidal category*)と呼ぶ。

## 記法

- モノイダル圏のことを、モノイド圏やテンソル圏(*Tensor category*)とも呼ぶ
- モノイダル積のことを、テンソル積とも呼ぶ
