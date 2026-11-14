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
