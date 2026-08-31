---
name: scene-score
description: "Translate a photograph's rhythm of light, movement, interval, density, and rest into a source-faithful contemporary Scene Score. Use for photo-to-art direction with a gallery-print result; not for generic zine posters, arbitrary collages, or photo filters."
---

# Scene Score

Turn a photograph into an original art print that makes its internal rhythm visible. A Scene Score is not a visual style or a music-themed poster: it is a composition in which scene relationships become visible beats, phrases, and rests. The photograph is evidence; the added graphic score is a translation of that evidence, never a fixed decorative overlay.

Use the built-in `image_gen` workflow. Treat an uploaded photograph as the content source. For a local file, inspect it with `view_image` before the image edit. Preserve the original non-destructively and place project-bound output outside the default generated-images directory.

## Promise and boundary

The finished image should read as a contemporary exhibition print: a photographic anchor set inside an image-wide, source-derived graphic reconstruction. It is not a vintage zine, scrapbook, travel poster, or an infographic.

Default to preserving the photograph's primary subject, spatial relationship, and emotional temperature. Use **distillation** only when the user explicitly asks not to retain photographic pixels; then preserve the scene's factual relationships but author a wholly new image.

Never begin from a stock recipe such as a cream background, an oversized circle, or horizontal stripes. Those forms are allowed when they follow a named source cue. Vary the macro-composition between images so the skill does not collapse into a fixed template.

## Read the scene as a score

Before choosing shapes, identify the roles already present in the photograph:

- **Anchor (melody):** the person, object, place, or relationship that must remain factual.
- **Pulse (beat):** a visible interval or repetition: crossings, windows, waves, branches, footsteps, rain, shelves, or reflections.
- **Phrase (sustained movement):** one direction or value change that carries across the frame: a route, a beam of light, a horizon, a shadow, wind, or gaze.
- **Rest (quiet):** the low-information field that gives the other elements space: fog, wall, sky, water, tabletop, or darkness.
- **Accent:** one small high-salience color or event that changes the rhythm.

Use two or three of these roles, never all of them by default. The score should be felt as a visual rhythm, not illustrated with musical notation.

## Choose the composition mode

Default to **score-led reconstruction**. It should visibly transform the composition at thumbnail scale and be bold enough to read as a finished image rather than a filter:

- **Score-led reconstruction (default):** preserve one photo anchor at roughly 25–45% of the frame. Make two or three scene roles visible: normally one pulse or repeated interval, one sustained phrase, and one rest. They may build a decisive hero geometry, but the image should still read as this scene's visual rhythm rather than a generic poster layout. The anchor may have an aperture-like edge, but its scene geometry should visibly continue outward as graphic fields; it must not read as a pasted sticker. The photo must not run edge-to-edge or dissolve into an almost-full-frame treatment.
- **Amplified score:** use the same score logic, but enlarge one source-derived hero geometry until it carries the thumbnail. It must alter the source silhouette, spatial partition, or major rhythm; contrast, paper grain, fog, and color grading alone do not count. Use when the user wants a bolder, more editorial result.
- **Structural rebuild:** preserve one photo anchor at roughly 25–45% of the frame. Rebuild the remaining frame as one or two source-derived fields plus a small relational mark. Use when the user values direct, legible traceability over maximum graphic impact.
- **Integrated trace:** preserve most of the photograph and add sparse marks within it. Use only when the user asks for a subtle result or maximum photo preservation.
- **Distillation:** remove photographic pixels and retain only source relationships. Use only when the user explicitly asks for a fully new artwork.

The field's contour, palette, and placement must come from the source: a crossing's route, a building's mass, a window's light plane, water's horizon, a garment's silhouette, or another observed force. It must not be a default panel shape.

## Select signals

Identify these internally before generating; map them to the score roles above:

- **Anchor:** the one photo element that must remain factual (person, object, landmark, or relationship).
- **Scene forces:** one to three observable qualities that can become graphics: direction, shadow, reflection, repetition, horizon, interval, weather, growth, or density.
- **Palette logic:** two to four source-derived colors and their roles (field, anchor, accent, ink).
- **Quiet field:** the natural low-information area that can support the composition.

Use [references/translation-grammar.md](references/translation-grammar.md) when deciding how an observed scene force becomes a score mark.

## Build the contract

Before image generation, state a compact contract:

```text
Anchor to retain: <one factual visual anchor>
Scene forces: <1–3 source observations>
Score: <pulse / phrase / rest / accent and the source of each>
Palette: <source-derived field / ink / accent>
Composition: <where the photo anchor and quiet field sit>
Avoid: <untraceable shapes, template defaults, text, logos, etc.>
```

Keep the score intentionally sparse. One clear visual translation is better than five ornamental gestures. Avoid added text by default; if the user asks for copy, use only their exact words and keep it subordinate.

## Choose graphic strength

Default to **balanced** so the translation remains obvious even at thumbnail scale:

- **Quiet:** one source-derived field plus one fine score mark; use when the photograph is already highly graphic.
- **Balanced (default):** two score roles are clearly visible: normally a pulse or interval and a sustained phrase. The photo anchor remains recognisable but is not dominant.
- **Expressive:** two related source-derived fields plus one fine mark; use only when the user asks for a bolder art transformation.

Changing strength changes the visibility of the score, not the ownership of the geometry. A strong result must still pass the same traceability check.

## Generate and inspect

Use an edit/reference image workflow. The generation prompt must name the source role, repeat the anchor invariants, and say how every added graphic relates to a source observation.

Inspect at normal size and thumbnail size. Accept the first image only when all are true:

- The anchor still identifies this specific photograph rather than a generic scene.
- In score-led, amplified, or structural rebuild mode, at least half of the frame is visibly re-authored rather than merely color-graded.
- In score-led reconstruction, at least two distinct scene roles are legible: a pulse/interval, phrase/directional field, or rest; a quiet scene may use one role plus a strong rest.
- The photo and graphic fields visibly interlock: at least one scene geometry continues from photo to graphic, and the anchor does not read as a pasted sticker.
- Every major graphic mark can be traced to a named source relationship.
- The background, hero geometry, and accent color are justified by this photo; none are automatic defaults.
- The result has one clear focal hierarchy and enough quiet space to feel like an art print.
- At the requested strength, the score is visibly distinct from the unedited photo at thumbnail scale.
- The visible difference is structural: identify at least two added or extended scene-derived marks that survive a thumbnail view. Texture, grading, atmospheric haze, and a near-identical crop alone are a failed result.
- It avoids torn paper, fake archival stamps, decorative microtext, logos, and watermark-like marks. Circles, bands, or stripes must be traceable to a named source cue and should not repeat as a fixed formula across different scenes.

If a result fails, make one targeted revision that restores one source relationship or removes one untraceable motif. Do not regenerate merely to obtain random variations.

For a material change to this Skill, run the three scene checks in [evals/scene-score-evals.md](evals/scene-score-evals.md). They test observed relationships and rejection conditions, not pixel matching; do not turn them into a new fixed layout recipe.

## Deliver

Return the final image and a concise Chinese explanation:

- **保留：** <factual anchor>
- **转译：** <source force → graphic mark>

For a project-bound output, also report its saved path and the final prompt. Do not publish, upload, or reuse another creator's example imagery without the user's explicit authorization.
