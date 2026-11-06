# FastUI

A cross-platform UI exploration library for AI-assisted development: design foundations,
themes, components, and interaction patterns with inspectable source.

**Status: architecture scaffold only.** There are no installable packages or implemented
components yet. Web is the first implementation target; mobile and desktop are planned.
No performance or cross-platform compatibility claims have been verified.

## Repository map

| Directory | Responsibility |
| --- | --- |
| [tokens](tokens/README.md) | Shared semantic design values and future platform exports |
| [themes](themes/README.md) | Named visual styles, palettes, and light/dark variants |
| [web](web/README.md) | React components and composed interaction patterns |
| [mobile](mobile/README.md) | Planned React Native / Expo implementations |
| [desktop](desktop/README.md) | Planned Rust / GPUI implementations |
| [examples](examples/README.md) | Runnable consumers and reproducible demonstrations |
| [registry](registry/README.md) | Versioned resource metadata and distribution outputs |
| [docs](docs/ARCHITECTURE.md) | Architecture, integration guidance, and design rules |

The website, accounts, and administration belong to the separate `fast-ui-site` product
repository. This library must work without its backend or the FastBuild scaffold.

## Design direction

Share design intent across platforms, not a universal renderer. Each implementation respects
its platform's focus, keyboard, pointer, touch, accessibility, and window behavior.

- **Style:** typography, shape, density, elevation, and motion language.
- **Theme:** semantic color choices and light/dark appearance within a style.
- **Platform:** an independently implemented and verified UI target.

Start with [the architecture](docs/ARCHITECTURE.md) and [the first milestone](docs/ROADMAP.md).
Contributions follow [CONTRIBUTING.md](CONTRIBUTING.md). Original contributions use the
[MIT license](LICENSE); third-party code retains its own required notices.
