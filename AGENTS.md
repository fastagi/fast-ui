# FastUI — Agent Instructions

This is the public UI library, not the FastBuild scaffold or the website product.
Use FastUI as the visible brand and fast-ui as the repository identifier.

Read README.md, docs/ARCHITECTURE.md, and the nearest directory README before changes.
Preserve unrelated work. Do not import sibling repository source or copy private product code.

The current repository is documentation and ownership scaffolding only. Do not claim packages,
components, platform support, benchmark results, or deployment exist before verification.

Use modules before packages. Add a package manifest and lockfile only with an actual runnable
implementation. Do not create a universal widget wrapper, plugin engine, CSS interpreter,
or custom renderer. Prefer existing framework primitives and compose them.

Shared tokens contain serializable design values; platform code owns mapping, units, gamut,
font fallback, accessibility, and interaction differences. Website business data never belongs here.
Registry outputs must match the source and dependency versions actually demonstrated.

Before importing third-party assets or code, preserve their licenses and attribution.
Never commit credentials, personal data, node_modules, build outputs, or private configurations.

Documentation checks: verify local links, fences, and whitespace with git diff --check
(and inspect untracked files). No tests that merely assert documentation wording.
For code, run focused checks for the affected platform. Native UI requires real device/window
verification; browser previews do not prove native compatibility. Report untested platforms.
