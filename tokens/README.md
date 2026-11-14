# Tokens

Own shared semantic design values, their schema, and documented units. Keep values independent
of CSS, React, GPUI, and any application backend. Platform conversion belongs beside its consumer
until multiple consumers justify shared generation tooling.
See [architecture](../docs/ARCHITECTURE.md).

## Palette (draft)

[`palette.json`](palette.json) holds the draft color palette, schema version `0.1.0`. It is a
data file only: no package, generator, or platform consumer exists in this repository yet.

- Two themes (`neutral` on Radix gray, `slate` on Radix slate), each with `light` and `dark`
  modes: 12 scale steps, 10 semantic roles, an accent, and four status colors.
- Every token carries a bilingual rationale (`zh-Hans`, `en-US`) and a `source`:
  `radix:<scale>-<step>` for values taken from a Radix step, `own` for values chosen here.
- The values are a proposal. `verified: true` means only that the value is exactly the
  published Radix value for the cited step; it does not mean contrast, accessibility, or
  rendering has been checked. All own values are `verified: false`.
- `sourceRevision` records the base commit the file was authored against.

## Scales (draft)

[`scales.json`](scales.json) holds the full Radix scale library, schema version `0.1.0`: 31 scales
of 12 steps, each with `light` and `dark` values (sRGB hex), grouped for display, plus a
bilingual per-step usage note (`stepUsage`) that applies to every scale. Values are copied
unchanged from `@radix-ui/colors` 3.0.0; no values are edited or invented. Like `palette.json`
it is data only, and `gray` and `slate` match the steps used by the `neutral` and `slate` themes.
The alpha and Display P3 variants are not included.

Radix step values are taken from `@radix-ui/colors` 3.0.0, MIT License, Copyright (c) 2021 Radix.

## Typography (draft)

[`typography.json`](typography.json) holds the font recommendations and a type scale, schema
version `0.1.0`. It is data only: no font files are included or bundled here.

- `fonts`: seven open-source fonts, each with its upstream source, a bilingual rationale that
  states its limits, and a license record. Every entry is licensed under the SIL Open Font
  License 1.1; the license URL points to the upstream license file, which was fetched and checked
  for the OFL 1.1 text. Where the upstream file carries a copyright line it is recorded; Noto
  Sans SC has none recorded here.
- `roles`: which font to use for UI text, code, display and Chinese accents, with the CSS font
  stack including system fallbacks. A native app that bundles a font must keep the license text.
- `scale`: sizes, line heights and tracking. These are `own` proposals, not verified.
- Whether a font renders correctly in GPUI has not been verified.

## Space, radius and shadow (draft)

[`shape.json`](shape.json) holds the spacing scale (4px base, 12 steps), the corner radius scale
(8 steps) and five elevation levels with separate light and dark shadows, schema version `0.1.0`.
It is data only. Every value is `own` and `verified: false`: a proposal that was not measured
against any reference app and has not been verified in a native UI. Shadows are CSS
`box-shadow` strings; a native consumer maps them to its own shadow model.
