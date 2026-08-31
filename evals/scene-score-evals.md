# Scene Score evaluation set / 场景乐谱评测集

Use this set after a material change to `SKILL.md`, the translation grammar, or an image-generation workflow. It guards the method's observable behaviour; it does not prescribe a layout or demand pixel-matched output.

在 `SKILL.md`、转译规则或图像生成流程出现实质改动后使用本评测集。它保护的是可观察的行为，不规定固定版式，也不要求像素级一致。

## How to assess / 如何判断

For each prompt, inspect the generated image at normal and thumbnail size. Pass only if all named factual anchors remain identifiable, the required scene-derived relationships are visible, and the rejection conditions are absent.

每条测试都要在正常尺寸与缩略图尺寸下查看。只有当事实锚点仍可辨认、要求的源场景关系清晰可见、且不触发拒绝条件时才通过。

## 01 · Rain street / 雨街

**Source / 原图：** [`rain-street-source.jpg`](../examples/rain-street-source.jpg)

**Input condition / 输入场景：** A wet evening street with one umbrella walker, a zebra crossing, a bus in the distance, a shop window, and rain mist.

**Request / 请求：** Use `$scene-score` in score-led reconstruction mode. Preserve the walker and bus relationship. Make the crossing the pulse, the route toward the bus a phrase, rain mist the rest, and one shop light the accent.

**Must observe / 必须看到：**

- The walker, bus, wet crossing, and shop remain specific to this street.
- At least two crossing intervals extend or reappear as a source-derived pulse.
- One route-like phrase visibly carries the eye toward the bus.

**Reject / 拒绝：** a near-identical filtered photo; an unrelated circle or stripe recipe; a pasted photographic sticker with disconnected graphics.

**v0.2.1 evidence / v0.2.1 证据：** [`rain-street-score.png`](../examples/rain-street-score.png) · [run note](v0.2.1-validation.md)

## 02 · Stair hall / 阶梯大厅

**Source / 原图：** [`stair-hall-source.jpg`](../examples/stair-hall-source.jpg)

**Input condition / 输入场景：** A concrete stair hall with an ascending person, repeated treads, a diagonal handrail, tall window bays, and one warm exit light.

**Request / 请求：** Use `$scene-score` in amplified score mode. Preserve the person on the stairs. Make the treads an ascending pulse, the handrail an upward phrase, concrete a rest, and the exit light one accent.

**Must observe / 必须看到：**

- The person, stair direction, and handrail remain legible.
- The repeated treads become a major source-derived interval that changes the thumbnail silhouette or spatial partition.
- A single directional phrase continues the handrail's rise.

**Reject / 拒绝：** a generic architectural poster; equal decorative bars with no relation to the treads; dark grading alone presented as transformation.

**v0.2.1 evidence / v0.2.1 证据：** [`stair-hall-score.png`](../examples/stair-hall-score.png) · [run note](v0.2.1-validation.md)

## 03 · Misty ginkgo / 雾湖银杏

**Source / 原图：** [`misty-ginkgo-source.jpg`](../examples/misty-ginkgo-source.jpg)

**Input condition / 输入场景：** A foggy lake, gold ginkgo on the right, small boat, distant hills, and rust reeds in the foreground.

**Request / 请求：** Use `$scene-score` in score-led reconstruction mode. Preserve the trunk, boat, hills, and lake horizon. Make leaf and reed density the pulse, wake and horizon the phrase, and fog the rest.

**Must observe / 必须看到：**

- The trunk, boat, distant hills, and lake remain identifiable.
- Leaf or reed density visibly clusters, thins, or disperses; it must not become equal bars.
- At least one translucent, source-aligned water field or offset horizon survives at thumbnail size.

**Reject / 拒绝：** a full flat canopy silhouette; identical reeds; only fog, paper grain, or colour grading added to the original landscape.

**v0.2.1 evidence / v0.2.1 证据：** [`misty-ginkgo-score.jpg`](../examples/misty-ginkgo-score.jpg) · [run note](v0.2.1-validation.md)

## 04 · Perfume still life / 香水静物

**Source / 原图：** [`perfume-still-life-source.png`](../examples/perfume-still-life-source.png)

**Input condition / 输入场景：** An amber perfume bottle on a pale tabletop, paper sheet, dried branch, warm window light, and a diagonal cast shadow.

**Request / 请求：** Use `$scene-score` in expressive Gallery Score mode. Preserve the bottle, stopper, paper, branch, and the light/shadow relationship. Make window shafts the pulse, the diagonal light the phrase, tabletop or wall the rest, and the bottle colour the accent.

**Must observe / 必须看到：**

- The bottle, paper, branch, and window-light direction remain specific to this still life.
- A source-derived quiet field visibly occupies roughly 40–60% of the frame.
- Projected light becomes a major rhythm, and the score fields visibly reorganize at least half the frame.
- A circular accent appears only when it is traceable to the stopper, reflection, or another factual circular source.

**Reject / 拒绝：** a nearly intact product photo with a warm filter; arbitrary vertical stripes; an unrelated decorative circle; a quiet field that has no relationship to wall, tabletop, or light.

**v0.2.1 evidence / v0.2.1 证据：** [showcase result](../examples/perfume-still-life-score.png) · [independent repeat run](results/perfume-still-life-gallery-score-v0.2.1.png) · [run note](v0.2.1-validation.md)

## Record / 记录

For each run, record the source, final prompt, accepted image, and one sentence naming the two structural changes. If a test fails, make one targeted revision and record the rejected condition rather than adding a universal rule for every future scene.

每次运行应记录原图、最终提示词、接受的成图，以及一句话说明两处结构性变化。若失败，只做一次针对性修改并记录触发的拒绝条件，不要把单次失败扩写成适用于所有场景的规则。
