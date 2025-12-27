---
title: "随伴はKan拡張である"
free: false
---

## 定理

$F \dashv G : \mathbf C \to \mathbf D$が存在するならば、$F$に沿った$1_C$の絶対左Kan拡張が存在する。

### 証明

$\eta: 1_\mathbf C \Rightarrow G \circ F$, $\epsilon: F \circ G \Rightarrow 1_\mathbf D$とすると、以下の三角形を描ける。これが絶対左Kan拡張であることを示す。すなわち、圏$\mathbf U$と関手$K : \mathbf C \to \mathbf U$を任意に取って、$K \circ G$が$F$に沿った$K \circ 1_\mathbf C$の左Kan拡張であることを示す。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-2df6516e.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiXFxtYXRoYmYgRCJdLFsxLDEsIlxcbWF0aGJmIEMiXSxbMCwyLCIxX1xcbWF0aGJmIEMiXSxbMSwyLCJHIiwyXSxbMCwxLCJGIiwyXSxbMyw0LCJcXGV0YSIsMix7Im9mZnNldCI6Miwic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfSwiZWRnZV9hbGlnbm1lbnQiOnsic291cmNlIjpmYWxzZSwidGFyZ2V0IjpmYWxzZX19XV0=)

次のひし形合成を考えたときに、任意の$\theta : K \circ 1_\mathbf C \Rightarrow S \circ F$に対して、$\theta = (\tau \ast F) \circ (K \ast \eta)$を満たすような自然変換$\tau : K \circ G \Rightarrow S$が一意に存在することを示す。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-df46cc32.png)](https://q.uiver.app/#q=WzAsOCxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiXFxtYXRoYmYgRCJdLFsxLDEsIlxcbWF0aGJmIEMiXSxbMSwyLCJcXG1hdGhiZiBVIl0sWzIsMCwiXFxtYXRoYmYgQyJdLFsyLDEsIlxcbWF0aGJmIEQiXSxbMywxLCJcXG1hdGhiZiBDIl0sWzMsMiwiXFxtYXRoYmYgVSJdLFswLDIsIjFfXFxtYXRoYmYgQyJdLFsxLDIsIkciLDFdLFswLDEsIkYiLDJdLFsyLDMsIksiXSxbMSwzLCJTIiwyXSxbNCw1LCJGIiwyXSxbNiw3LCJLIl0sWzUsNywiUyIsMl0sWzQsNiwiMV9cXG1hdGhiZiBDIl0sWzgsOSwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJlZGdlX2FsaWdubWVudCI6eyJzb3VyY2UiOmZhbHNlLCJ0YXJnZXQiOmZhbHNlfX1dLFsxNiwxNSwiXFx0aGV0YSIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMCwidGFyZ2V0IjoyMH19XSxbOSwxMiwiXFx0YXUiLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjAsInRhcmdldCI6MjB9LCJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XV0=)

この$\tau : K \circ G \Rightarrow S$を以下のように定義する：

$$
\tau \coloneqq (S \ast \epsilon) \circ (\theta \ast G)
$$

この式は、以下のひし形合成を表す。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-e11075d6.png)](https://q.uiver.app/#q=WzAsNCxbMCwxLCJcXG1hdGhiZiBEIl0sWzEsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIFUiXSxbMiwxLCJcXG1hdGhiZiBEIl0sWzAsMSwiRyJdLFsxLDIsIksiXSxbMSwzLCJGIiwyXSxbMywyLCJTIiwyXSxbMCwzLCIxX1xcbWF0aGJmIEQiLDJdLFs1LDMsIlxcdGhldGEiLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV0sWzEsOCwiXFxlcHNpbG9uIiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dXQ==)

$\theta = (\tau \ast F) \circ (K \ast \eta)$を確認する。
$(\tau \ast F) \circ (K \ast \eta)$は以下のひし形である。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-0a9f6f33.png)](https://q.uiver.app/#q=WzAsNSxbMSwxLCJcXG1hdGhiZiBEIl0sWzIsMCwiXFxtYXRoYmYgQyJdLFs0LDAsIlxcbWF0aGJmIFUiXSxbMywxLCJcXG1hdGhiZiBEIl0sWzAsMCwiXFxtYXRoYmYgQyJdLFswLDEsIkciXSxbMSwyLCJLIl0sWzEsMywiRiIsMl0sWzMsMiwiUyIsMl0sWzAsMywiMV9cXG1hdGhiZiBEIiwyXSxbNCwwLCJGIiwyXSxbNCwxLCIxX1xcbWF0aGJmIEMiXSxbNiwzLCJcXHRoZXRhIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwfX1dLFsxLDksIlxcZXBzaWxvbiIsMix7InNob3J0ZW4iOnsidGFyZ2V0IjoyMH19XSxbMTEsMCwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV1d)

[unit-counit恒等式](./adjunction-unit-counit)より$(\epsilon \ast F) \circ (F \ast \eta) = \mathrm{Id}_F$であるから、上の図式は以下の図式に等しい。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-77750ab5.png)](https://q.uiver.app/#q=WzAsMyxbMCwwLCJcXG1hdGhiZiBDIl0sWzIsMCwiXFxtYXRoYmYgVSJdLFsxLDEsIlxcbWF0aGJmIEQiXSxbMCwxLCJLIl0sWzAsMiwiRiIsMl0sWzIsMSwiUyIsMl0sWzMsMiwiXFx0aGV0YSIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMH19XV0=)

よって$\theta = (\tau \ast F) \circ (K \ast \eta)$が確認できた。

次に$\tau$の一意性を確認する。
$\tau' : K \circ G \Rightarrow S$が存在して、$\theta = (\tau' \ast F) \circ (K \ast \eta)$を満たすと仮定する。つまり以下の図式が$\theta : K \Rightarrow S \circ F$に等しいと仮定する。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-a45685a1.png)](https://q.uiver.app/#q=WzAsNCxbMSwxLCJcXG1hdGhiZiBEIl0sWzIsMCwiXFxtYXRoYmYgQyJdLFszLDEsIlxcbWF0aGJmIFUiXSxbMCwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiRyJdLFszLDAsIkYiLDJdLFszLDEsIjFfXFxtYXRoYmYgQyJdLFswLDIsIlMiLDJdLFsxLDIsIksiXSxbNiwwLCJcXGV0YSIsMix7InNob3J0ZW4iOnsic291cmNlIjoyMH19XSxbMSw3LCJcXHRhdSciLDIseyJzaG9ydGVuIjp7InRhcmdldCI6MjB9fV1d)

$\tau'$の図式に、unit-counit恒等式を書き足す。$(\eta \ast G) \circ (G \ast \epsilon) = \mathrm{Id}_G$であるから、次の図式は$\tau'$に等しい。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-585f6a2f.png)](https://q.uiver.app/#q=WzAsNSxbMiwxLCJcXG1hdGhiZiBEIl0sWzMsMCwiXFxtYXRoYmYgQyJdLFs0LDEsIlxcbWF0aGJmIFUiXSxbMSwwLCJcXG1hdGhiZiBDIl0sWzAsMSwiXFxtYXRoYmYgRCJdLFswLDIsIlMiLDJdLFsxLDIsIksiXSxbMCwxLCJHIl0sWzMsMSwiMV9cXG1hdGhiZiBDIl0sWzMsMCwiRiIsMV0sWzQsMywiRyJdLFs0LDAsIjFfXFxtYXRoYmYgRCIsMl0sWzEsNSwiXFx0YXUnIiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFszLDExLCJcXGVwc2lsb24iLDIseyJzaG9ydGVuIjp7InRhcmdldCI6MjB9fV0sWzgsMCwiXFxldGEiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV1d)

仮定より$(\tau' \ast F) \circ (K \ast \eta) = \theta$であるから、図式の右側を$\theta$で置き換えられる。
この図式はまさに$\tau$の定義と同一であるから、$\tau' = \tau$が示せた。

[![diagram](/images/book/9595ef4f5dc413/kan-extension-adjunction/diagram-e11075d6.png)](https://q.uiver.app/#q=WzAsNCxbMCwxLCJcXG1hdGhiZiBEIl0sWzEsMCwiXFxtYXRoYmYgQyJdLFszLDAsIlxcbWF0aGJmIFUiXSxbMiwxLCJcXG1hdGhiZiBEIl0sWzAsMSwiRyJdLFsxLDIsIksiXSxbMSwzLCJGIiwyXSxbMywyLCJTIiwyXSxbMCwzLCIxX1xcbWF0aGJmIEQiLDJdLFs1LDMsIlxcdGhldGEiLDAseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9fV0sWzEsOCwiXFxlcHNpbG9uIiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dXQ==)

証明終わり。

## 逆

上の主張は逆も成り立つ。しかしながら、逆はもう少し弱い主張で十分である。

すなわち、$F$に沿った$1_C$の左Kan拡張$\lang \mathrm{Lan}_F 1_\mathbf C, \eta \rang$が存在して、$F$が$\lang \mathrm{Lan}_F 1_\mathbf C, \eta \rang$と交換するならば、$G : \mathbf D \to \mathbf C$が存在して、$F \dashv G$が成り立つ。
