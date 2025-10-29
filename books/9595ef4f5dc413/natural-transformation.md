---
title: "自然変換"
free: false
---

## 定義

自然変換(*Natural transformation*)とは、圏$\mathbf C$, $\mathbf D$と共変関手$F, G: \mathbf C \to \mathbf D$が与えられたとき、圏$\mathbf C$の任意の対象$X$, $Y$における各関手の像$F(f): F(X) \to F(Y)$, $G(g): G(X) \to G(Y)$に対して、射$\eta_X: F(X) \to G(X)$, $\eta_Y: F(Y) \to G(Y)$を与えるものであり、以下を満たす:

- 圏$\mathbf C$の任意の対象$X, Y$に対して、$\hom_D$上の射$\eta_Y \circ F(f) = G(f) \circ \eta_X$

すなわち以下の図式を可換にする。

[![](https://storage.googleapis.com/zenn-user-upload/eeca522e6379-20251029.png)](https://q.uiver.app/#q=WzAsOCxbMywxLCJGKEEpIl0sWzQsMSwiRihCKSJdLFszLDIsIkcoQSkiXSxbNCwyLCJHKEIpIl0sWzMsMCwiXFxtYXRoYmYgRCJdLFswLDAsIlxcbWF0aGJmIEMiXSxbMCwxLCJBIl0sWzEsMSwiQiJdLFsyLDMsIkcoZikiLDJdLFswLDIsIlxcZXRhX1giLDJdLFsxLDMsIlxcZXRhX1kiXSxbNiw3LCJmIl0sWzAsMSwiRihmKSJdLFswLDMsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==)

このノートでは、$\mathbf C$の対象で添え字づけられる自然変換を、$\eta: F \Rightarrow G$のように表す。

## 表記

自然変換の射の族を、$\Rightarrow$でつなぐ代わりに$\dot{\to}$や単に$\to$を使う資料もある。

### Haskellでの表現

Haskellで表すと次のようになる。
ここには書かれていないが、`f`や`g`には関手であるという制限がある。
また自然変換に`~>`という記号を用いたのは、`->`や`=>`が使えないからだ。^[1 [UnicodeSyntax](https://downloads.haskell.org/ghc/latest/docs/users_guide/exts/unicode_syntax.html#extension-UnicodeSyntax)を使う手もあるが、→や⇒は`->`や`=>`の代替であるし、上に点のついた矢印(rightward arrow with a dot above)も見つからないので、これを使うことにした。より良い記号が見つかれば今後はそれを使っていくことにする。]

```Haskell
type f ~> g = forall a. f a -> g a
infixr 1 ~>
```

https://play.haskell.org/saved/lpdybL9a

具体的な自然変換としては、例えば次のようなものがある。
`Data.Maybe`モジュールに含まれている[listToMaybe](https://hackage.haskell.org/package/base-4.19.0.0/docs/Data-Maybe.html#v:listToMaybe)の型は、次の通りだ。

```Haskell
listToMaybe :: [a] -> Maybe a
```

これを上で定義した自然変換の演算子で表せば、次の通りとなる。

```Haskell
listToMaybe :: [] ~> Maybe
```
