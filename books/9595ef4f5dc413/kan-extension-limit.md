---
title: "極限はKan拡張である"
free: false
---

## 定理

$G : \mathbf{C} \to \mathbf{D}$ の $F : \mathbf{1} \to \mathbf{D}$ に沿った右Kan拡張を考える。

![](https://storage.googleapis.com/zenn-user-upload/ecf0a4f8b1f5-20250303.png)

この時$\lang R(\ast), \eta \rang$は圏$\mathbf{D}$における極限である。

## 証明

$\mathbf{C}$が次のような構造を備えているとする。

![](https://storage.googleapis.com/zenn-user-upload/3c4652d18de5-20250303.png)

これを$R \circ F$と$G$によって圏$\mathbf{D}$に写すと、次の可換図式を書ける。

![](https://storage.googleapis.com/zenn-user-upload/2a7515e19451-20250303.png)

ここで$F$は$\mathbf{C} \to \mathbf{1}$への関手であり、$\mathbf{1}$は対象が$\ast$, 射が$\mathrm{id}_\ast : \ast \to \ast$しかない圏であるから、$R(F(A)) = R(F(B)) = R(\ast)$かつ$R(F(f)) = R(\mathrm{id}_\ast)$が成り立つ。
よって上図を下のように整理できる。

![](https://storage.googleapis.com/zenn-user-upload/f40055345b0f-20250303.png)

Kan拡張の普遍性により、別の関手$S : \mathbf{1} \to \mathbf{D}$と自然変換$\theta : S \circ F \Rightarrow G$があったとき、自然変換$\tau : R \Rightarrow S$が一意に存在して、$\theta = \eta \circ (\tau \ast F)$ を満たすのであった。

![](https://storage.googleapis.com/zenn-user-upload/8ba1d0f87661-20250303.png)

この$S$, $\theta$, $\tau$を圏$\mathbf{D}$の図式に書き加えると、次のようになる。

![](https://storage.googleapis.com/zenn-user-upload/df268cb6ec49-20250303.png)

これは極限の定義に一致するため、$\lang R(\ast), \eta \rang$は極限である。
