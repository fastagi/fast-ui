# Architecture

## Boundaries

FastUI owns reusable UI source, design values, documentation, and examples.
The separate website consumes versioned public artifacts; it owns discovery UX, accounts,
collections, payments, and administration. Users must not need that service to run components.

```text
tokens + themes
      |
      +--> web implementation ------> web examples
      +--> mobile implementation ---> mobile examples
      +--> desktop implementation --> desktop examples
                  |
          versioned source + resource metadata
                  |
          website and downstream applications
```

These are ownership boundaries, not mandatory packages or separate deployment units.
No runtime dependencies or package manifests are introduced in this initial milestone.

## Design model

Style defines shape, typography, density, elevation, and motion. Theme chooses semantic colors
and light/dark values. Platform defines implementation and interaction behavior.
Supported combinations must be declared explicitly; not every style/theme/platform combination
is automatically supported. Respect reduced motion and system appearance where implemented.

Tokens begin as a small, versioned, serializable schema with documented units and semantic roles.
Choose the concrete schema with the first working theme, not a speculative compiler.
Platform mappings explicitly resolve colors, lengths, fonts, and motion. CSS cannot be imported
into GPUI; React DOM components cannot be treated as native mobile implementations.

## Implementation strategy

- Web first: React, TypeScript, Tailwind CSS, and selected shadcn/ui primitives.
- Mobile later: React Native / Expo, using native interaction behavior.
- Desktop later: Rust, GPUI, and compatible GPUI Kit components.

These are intended stacks, not installed dependencies. Pin and verify compatible versions when
implementing each target. Basic components own interaction and presentation; composed patterns
receive data and callbacks rather than importing product-specific APIs or authentication.
Extract shared packages only when actual consumers justify them.

## Source and distribution

Platform directories are the authoritative component source. Examples consume that same source.
Registry metadata references resources; it does not become a second hand-maintained source copy.
Generated installable outputs must be reproducible and carry explicit versions and dependencies.

Web distribution can target the shadcn registry format. Mobile and Rust use their own validated
installation mechanisms; sharing catalog metadata does not establish installer compatibility.
Do not introduce a custom CLI or MCP server until existing distribution cannot meet a real need.

The website pins a library release and uses matching preview artifacts and installation metadata.
A native recording must be labeled as a recording. Simulated web previews are not native evidence.

## Verification and release

Each implemented resource records source revision, dependencies, supported targets, and evidence.
Verify keyboard/focus, input methods, accessibility, themes, resize behavior, and reduced motion
where relevant. Measure performance in release/production builds with workload and hardware stated.
A first release requires one runnable vertical slice; folders alone do not establish readiness.

## Licensing

Original code is MIT licensed. Retain upstream licenses and notices for copied code and assets.
Do not copy commercial templates or private website source into this repository.
Document upstream provenance alongside adapted components.
