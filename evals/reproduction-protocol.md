# Independent reproduction protocol / 独立复现流程

Use this protocol when testing a material change with a person, agent, or image model that did not make the change. It makes repeatability observable without requiring pixel-identical images.

## Prepare / 准备

1. Choose one permission-cleared photograph that is not already in `examples/` or the four formal checks.
2. Record the Skill version, agent or image model, date, input image, and the exact prompt or mode.
3. Do not supply a showcase output as a style reference. Gallery Score may be requested explicitly.

## Run and assess / 运行与判断

Run the same request three times, preferably with independent sessions. For every result, record pass or fail for these five checks:

| Check / 检查项 | Pass when / 通过条件 |
| --- | --- |
| Source fidelity / 场景识别 | The person, place, or object remains recognisably specific to the input. |
| Derived rest / 来源留白 | The quiet field comes from the source's light, fog, wall, water, sky, or another visible condition. |
| Clear rhythm / 清晰节奏 | One dominant beat and one directional phrase are legible; accents remain limited. |
| Structural change / 结构性转译 | The result is more than colour grading, texture, or a nearly intact photo. |
| No borrowed recipe / 不套模板 | Added forms can be traced to the scene rather than copied from an unrelated example. |

Accept the change when at least two of the three runs pass all five checks. If a run fails, name the failing relationship and make one targeted revision; do not silently select only the best image.

## Publish the record / 发布记录

When sharing a result, include the input's permission status, the run details, the three pass/fail records, and any source attribution required by the image license. This protocol measures hierarchy and behavior, not exact pixels, crop edges, or random texture.
