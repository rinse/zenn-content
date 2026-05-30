---
title: "自然変換"
free: false
---

自然変換とは関手から関手への矢印であり、$\eta: F \Rightarrow G$ のように表す。

## 定義

圏 $\mathbf C$, $\mathbf D$ と共変関手 $F, G: \mathbf C \to \mathbf D$ が与えられたとき、$F$ から $G$ への自然変換 (*Natural transformation*) $\eta : F \Rightarrow G$ とは、圏 $\mathbf C$ の対象で添え字づけられた圏 $\mathbf D$ の射の族 $\{ \eta_X : F(X) \to G(X) \}_{X \in \mathrm{ob}(\mathbf C)}$ であって、以下の自然性を満たすものである。

すなわち圏 $\mathbf C$ の任意の射 $f : X \to Y$ について、$\eta_Y \circ F(f) = G(f) \circ \eta_X$ が成り立つ。

https://q.uiver.app/#q=WzAsOCxbMiwxLCJGKFgpIl0sWzMsMSwiRihZKSJdLFsyLDIsIkcoWSkiXSxbMywyLCJHKFkpIl0sWzIsMCwiXFxtYXRoYmYgRCJdLFswLDAsIlxcbWF0aGJmIEMiXSxbMCwxLCJYIl0sWzEsMSwiWSJdLFsyLDMsIkcoZikiLDJdLFswLDIsIlxcZXRhX1giLDJdLFsxLDMsIlxcZXRhX1kiXSxbNiw3LCJmIl0sWzAsMSwiRihmKSJdLFswLDMsIlxcY2lyY2xlYXJyb3dyaWdodCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dXQ==

## 表記

このノートでは $F$ から $G$ への自然変換を $\eta: F \Rightarrow G$ のように表す。

自然変換の射の族を $\Rightarrow$ でつなぐ代わりに $\dot{\to}$ や単に $\to$ を使う資料もある。

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
