---
title: "Catamorphism"
free: false
---

## 定義

[F-代数](./f-algebra.md)とその始代数$(I, i)$を考える。

このとき始代数の性質より、対象$I$から任意の対象への準同型が存在する。この準同型の族をCatamorphismと呼び、$\mathrm{cata}$と書く。

[![catamorphism](https://storage.googleapis.com/zenn-user-upload/dd267b882263-20240805.png)](https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDEsIkYoSSkiXSxbMCwyLCJGKEEpIl0sWzEsMiwiQSJdLFsxLDEsIkkiXSxbMSw0LCJpIiwwLHsib2Zmc2V0IjotMX1dLFs0LDMsIlxcbWF0aHJte2NhdGF9X0EiXSxbMiwzLCJhIiwyXSxbMSwyLCJGKFxcbWF0aHJte2NhdGF9X0EpIiwyXSxbNCwxLCJpXnstMX0iLDAseyJvZmZzZXQiOi0xfV1d)

## プログラミングへの応用

$\mathrm{cata}_A$はF-代数の準同型であるから、$\mathrm{cata}_A \circ i = a \circ F(\mathrm{cata}_A)$を満たす。
$i$は同型射であるから、自明に$\mathrm{cata}_A \circ i = a \circ F(\mathrm{cata}_A) \circ i^{-1} \circ i$であり、同型射がモノ射かつエピ射であることを思い出して[右簡約](monic-and-epic-morphisms#エピ射)を行うと$\mathrm{cata}_A = a \circ F(\mathrm{cata}_A) \circ i^{-1}$が成り立つ。

すなわち下の図式が可換になる。

[![simple-catamorphism](https://storage.googleapis.com/zenn-user-upload/57dfd8063086-20240805.png)](https://q.uiver.app/#q=WzAsNSxbMCwwLCJcXG1hdGhiZntDfSJdLFswLDIsIkYoSSkiXSxbMCwzLCJGKEEpIl0sWzIsMywiQSJdLFswLDEsIkkiXSxbNCwzLCJcXG1hdGhybXtjYXRhfV9BIl0sWzIsMywiYSIsMl0sWzEsMiwiRihcXG1hdGhybXtjYXRhfV9BKSIsMl0sWzQsMSwiaV57LTF9IiwyXV0=)

この図式の意味するところは、F-代数$(A, a)$が与えられれば$\mathrm{cata}_A: I \to A$が一意に定まるということである。

Catamorphismはプログラミングの文脈では**畳み込み**と呼ばれ、広く用いられている。

HaskellではCatamorphismは次のように表現することができる。

```Haskell
-- Iの定義。命名はFの不動点であることから
newtype Fix f = InF { outF :: f (Fix f) }

cata :: Functor f => (f a -> a) -> Fix f -> a
cata a = a . fmap (cata a) . outF
```

この`cata`は、関手に下記の`ListF`を用いたとき`foldr`と同型になる。

```Haskell
data ListF a b = Nil | Cons a b deriving (Functor)

foldr :: (a -> b -> b) -> b -> [a] -> b
```
