# Desktop

Reserved ownership for reusable Rust / GPUI UI components and patterns, composed with GPUI Kit.
Window setup and product workflows belong in examples or consumer applications, not shared controls.

Map tokens explicitly; preserve desktop focus, shortcuts, input methods, resizing, and platform
behavior. Do not import fastbuild-desktop source or build a framework-neutral renderer.

Add Cargo manifests and tested dependency versions with the first runnable component example.
No desktop crate or verified platform support exists yet. See [architecture](../docs/ARCHITECTURE.md).
