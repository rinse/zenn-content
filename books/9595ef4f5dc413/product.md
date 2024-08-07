---
title: "積"
free: false
---

## 定義

積(*product*)とは、任意の圏$\mathbf C$の対象$X_1 \times X_2$と、2つの射$p_1: X_1 \times X_2 \to X_1$と$p_2: X_1 \times X_2 \to X_2$の3つ組で、以下の普遍性を満たすものをいう。

$\mathbf C$の任意の対象$Y$および$f_1: Y \to X_1$ , $f_2: Y \to X_2$が与えられたとき、一意な射$u: Y \to X_1 \times X_2$が存在して、以下の図式を可換にする。

![product](https://storage.googleapis.com/zenn-user-upload/10f64e9d2230-20231028.png)

https://q.uiver.app/#q=WzAsNSxbMSwxLCJZIl0sWzEsMiwiWF8xIFxcdGltZXMgWF8yIl0sWzIsMiwiWF8yIl0sWzAsMiwiWF8xIl0sWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsInUiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbMSwyLCJwXzIiLDJdLFsxLDMsInBfMSJdLFswLDMsImZfMSIsMl0sWzAsMiwiZl8yIl1d

## 普遍性を用いた定義

積とは、対角関手$\Delta: \mathbf C \to \mathbf C \times \mathbf C$から$\mathbf C \times \mathbf C$の対象$(X_1$, $X_2)$への普遍射と表現である。

![product_1](https://storage.googleapis.com/zenn-user-upload/5ae4dd744dd1-20231025.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMCwiXFxtYXRoYmYgQyBcXHRpbWVzIFxcbWF0aGJmIEMiXSxbMiwxLCIoWF8xLCBYXzIpIl0sWzMsMSwiXFxEZWx0YShYKSJdLFszLDIsIlxcRGVsdGEoWSkiXSxbMCwxLCJYIl0sWzAsMiwiWSJdLFszLDIsInUiLDJdLFs0LDMsIlxcRGVsdGEoZykiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNCwyLCJmIl0sWzYsNSwiZyIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImRhc2hlZCJ9fX1dXQ==

ここで対角関手(*Diagonal functor*)$\Delta$とは、$\mathbf C$の対象$X$を$\mathbf C \times \mathbf C$の対象$(X, X)$に、$\mathbf C$の射$f: X \to Y$を$\mathbf C \times \mathbf C$の射$(f, f): (X, X) \to (Y, Y)$に写す関手である。

![Diagonal_functor](https://storage.googleapis.com/zenn-user-upload/1b248d4ce201-20231025.png)

https://q.uiver.app/#q=WzAsOCxbMCwxLCJYIl0sWzEsMSwiWSJdLFswLDAsIlxcbWF0aGJmIEMiXSxbMywwLCJcXG1hdGhiZiBDIFxcdGltZXMgXFxtYXRoYmYgQyJdLFszLDEsIlxcRGVsdGEoWCk9KFgsIFgpIl0sWzUsMywiXFxEZWx0YShZKT0oWSwgWSkiXSxbNSwxLCIoWCwgWSkiXSxbMywzLCIoWSwgWCkiXSxbMCwxLCJmIl0sWzQsNiwiKGlkX1gsIGYpIl0sWzYsNSwiKGYsIGlkX1kpIl0sWzQsNywiKGYsIGlkX1gpIiwyXSxbNyw1LCIoaWRfWSwgZikiLDJdLFs0LDUsIlxcRGVsdGEoZik9KGYsIGYpIiwxXV0=

$\Delta: \mathbf C \to \mathbf C \times \mathbf C$から$\mathbf C \times \mathbf C$の対象$(X_1$, $X_2)$への普遍射$(X, u)$を可換図式上で計算すると、最初の可換図は次のようになる。

![product_2](https://storage.googleapis.com/zenn-user-upload/b0bdeb30b6dd-20231025.png)

https://q.uiver.app/#q=WzAsNyxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMCwiXFxtYXRoYmYgQyBcXHRpbWVzIFxcbWF0aGJmIEMiXSxbMCwxLCJYIl0sWzAsMiwiWSJdLFsyLDEsIihYXzEsIFhfMikiXSxbMywxLCIoWCwgWCkiXSxbMywyLCIoWSwgWSkiXSxbMywyLCJnIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzUsNCwiKHVfMSwgdV8yKSIsMl0sWzYsNSwiKGcsIGcpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzYsNCwiKGZfMSwgZl8yKSJdXQ==

こうすると$\mathbf C \times \mathbf C$の射$u$や$f$が、$\mathbf C$の射$u_1$, $u_2$や$f_1$, $f_2$で構成されていることが分かる。
つまり$\mathbf C$にはこれらの射が存在するということだ。それらを図に書き加えてみよう。

![product_3](https://storage.googleapis.com/zenn-user-upload/66bfc7db3e3b-20231025.png)

https://q.uiver.app/#q=WzAsOSxbMSwwLCJcXG1hdGhiZiBDIl0sWzQsMCwiXFxtYXRoYmYgQyBcXHRpbWVzIFxcbWF0aGJmIEMiXSxbMSwxLCJYIl0sWzEsMiwiWSJdLFs0LDEsIihYXzEsIFhfMikiXSxbNSwxLCIoWCwgWCkiXSxbNSwyLCIoWSwgWSkiXSxbMCwxLCJYXzEiXSxbMiwxLCJYXzIiXSxbMywyLCJnIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzUsNCwiKHVfMSwgdV8yKSIsMl0sWzYsNSwiKGcsIGcpIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiZGFzaGVkIn19fV0sWzYsNCwiKGZfMSwgZl8yKSJdLFsyLDgsInVfMiJdLFsyLDcsInVfMSIsMl0sWzMsOCwiZl8yIiwyXSxbMyw3LCJmXzEiXV0=

圏$\mathbf C$の可換図式は、明らかに積の可換図式と一致している。
上図では、$\mathbf C$の対象$X$が、$X_1$と$X_2$の積であるような対象$X_1 \times X_2$に一致している。

よって確かに、対角関手$\Delta: \mathbf C \to \mathbf C \times \mathbf C$から$\mathbf C \times \mathbf C$の対象$(X_1$, $X_2)$への普遍射は積を表している。

## Haskellでの積

Haskellで積を書いてみよう。
積とは、ある普遍性を満たす、$X_1 \times X_2$と、2つの射$p_1: X_1 \times X_2 \to X_1$と$p_2: X_1 \times X_2 \to X_2$の3つ組だった。

一旦普遍性の条件を忘れて、この3つ組を、まずはペアと名付けよう。
まだ普遍性についての条件を課していないので、これはまだ積とは呼べない。通常、ペアと積とは同一のものを想像すると思うが、ここでは命名の都合で呼び分けさせてもらう。

`p`が$X_1 \times X_2$、`fst`, `snd`が$p_1$, $p_2$に相当する。

```Haskell
class Pair p a b | p -> a, p -> b where
  fst :: p -> a
  snd :: p -> b
```

例えば`(a, b)`は自明に`Pair`のインスタンスだ。

```Haskell
instance Pair (a, b) a b where
  fst (a, _) = a
  snd (_, b) = b
```

ペアではあるが積ではない例として、`(a, b, c)`も見ておこう。

```Haskell
instance Pair (a, b, c) a b where
  fst (a, _, _) = a
  snd (_, b, _) = b
```

他には、自作の積を作れば、これも`Pair`のインスタンスとなる。

```Haskell
data Tup2 a b = Tup2 a b

instance Pair (Tup2 a b) a b where
  fst (Tup2 a _) = a
  snd (Tup2 _ b) = b
```

このように、いくつもの型がペアであり、積にもそうでないものにも、それぞれ複数の型が存在する。
ここで、積を特徴づける普遍性の条件を、Haskellのことばで記述する。

```Haskell
class Pair x a b => Product x a b where
  univ :: Pair y a b => y -> x
```

ペアが積かどうかを、`Product`のインスタンスになるかどうかで確認していこう。
当然、`(a, b)`は積だ。

```Haskell
instance Product (a, b) a b where
  univ y = (fst y, snd y)
```

`(a, b, c)`はペアであるが積ではない。3つ目の要素`c`を得られず、`univ`を実装できないのだ。

一方、自作の積は、確かに積であることを確認できる。

```Haskell
instance Product (Tup2 a b) a b where
  univ y = Tup2 (fst y) (snd y)
```

`Product`型クラスの定義は、積とはどのようなペアからも`univ`を使って得られるようなペアのことである、と主張している。
すなわち、任意の積から任意の積への関数`univ`は、常に同型射である。

```Haskell
iso :: (Product p a b, Product q a b) => p -> q
iso = univ
```

この関数の主張するところは、積は同型を除いて一意だということだ。

https://play.haskell.org/saved/SFhzTtVD
