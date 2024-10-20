---
title: "双関手"
free: false
---

積圏を域に持つような関手を、特別に双関手(*Bifunctor*)と呼ぶ。双関手は典型的には次のような形をしている。

$$
F: \mathbf C \times \mathbf D \to \mathbf E
$$

実質的に圏を2つ取るような関手と考えることもできる。

[![bifunctor](https://storage.googleapis.com/zenn-user-upload/387c58a6f74d-20240818.png)](https://q.uiver.app/#q=WzAsMTIsWzAsMCwiXFxtYXRoYmZ7Q30iXSxbMSwwLCJcXG1hdGhiZntEfSJdLFszLDAsIlxcbWF0aGJme0V9Il0sWzIsMCwiXFxtYXRoYmZ7Q30gXFx0aW1lcyBcXG1hdGhiZntEfSJdLFswLDEsIkMiXSxbMCwyLCJDJyJdLFsxLDEsIkQiXSxbMSwyLCJEJyJdLFsyLDEsIlxcbGFuZyBDLCBEIFxccmFuZyJdLFsyLDIsIlxcbGFuZyBDJywgRCcgXFxyYW5nIl0sWzMsMSwiRihcXGxhbmcgQywgRCBcXHJhbmcpIl0sWzMsMiwiRihcXGxhbmcgQycsIEQnIFxccmFuZykiXSxbNCw1LCJjIiwyXSxbNiw3LCJkIiwyXSxbOCw5LCJcXGxhbmcgYywgZCBcXHJhbmciLDJdLFszLDIsIkYiXSxbMTAsMTEsIkYoXFxsYW5nIGMsIGQgXFxyYW5nICkiLDJdXQ==)

## 疑問

1. 双関手$\mathbf C \times \mathbf D \to \mathbf E$と関手$\mathbf C \to \mathbf E^{\mathbf D}$は同型か？
2. それは（小さい）圏の圏がデカルト閉かという疑問に等しいか？
