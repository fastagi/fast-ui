# Registry

Own resource metadata and future reproducible distribution outputs. A resource describes identity,
platform, style/theme compatibility, dependencies, source revision, examples, license, and evidence.
The exact schema will be introduced alongside the first installable resource.

Component source remains in its platform directory. Do not hand-maintain copies here.
Web exports may target shadcn registry consumers; mobile and Rust need separately validated
installation instructions. Catalog membership is not proof of cross-platform support.

There is no registry endpoint, CLI, or MCP server yet. See [architecture](../docs/ARCHITECTURE.md).
