---
title: "米田拡張"
free: false
---

米田拡張 (*Yoneda extension*) とは、[米田埋め込み](./yoneda-embedding)に沿った関手の[Kan拡張](./kan-extension)のことである。

$\mathbf{C}$を[小さい圏](./largeness-of-categories)とする。関手$F : \mathbf{C} \to \mathbf{D}$の米田拡張とは、米田埋め込み$H_- : \mathbf{C} \to \mathbf{Set}^{\mathbf{C}^{\mathrm{op}}}$に沿った$F$の左Kan拡張$\mathrm{Lan}_{H_-} F$である。

[![](https://storage.googleapis.com/zenn-user-upload/45039f4d02b0-20250314.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZntDfSJdLFsyLDEsIlxcbWF0aGJme0R9Il0sWzAsMSwiXFxtYXRoYmZ7U2V0fV57XFxtYXRoYmZ7Q31eXFxtYXRocm17b3B9fSJdLFswLDEsIkYiXSxbMCwyLCJIXy0iLDJdLFsyLDEsIlxcbWF0aHJte0xhbn1fe0hfLX0gRiIsMl0sWzMsNSwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJ0YXJnZXQiOmZhbHNlfX1dXQ==)

## 米田拡張と米田埋め込みの合成は元の関手に一致する

すなわち以下が成り立つ。

$$
\mathrm{Lan}_{H-} F \circ H_- \simeq F
$$

## 記法

- $F$の米田拡張$\mathrm{Lan}_{H_-} F$は、$\tilde F$と書かれることもある。
