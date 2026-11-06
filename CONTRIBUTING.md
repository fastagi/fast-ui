# Contributing

FastUI is currently an architecture scaffold. Start with a small proposal describing the user
interaction, target platform, dependencies, and verification approach.

Keep each change focused. Read the architecture and the relevant directory README. For source
changes, include a runnable example, documented states, supported themes, and verification evidence.
Avoid introducing abstractions or dependencies without an implemented consumer.

Document keyboard, pointer/touch, focus, loading, empty, disabled, and error behavior as applicable.
Native changes require native verification; screenshots alone are not interaction evidence.

Preserve upstream attribution and license notices. Contributions must be compatible with this
repository's MIT license. Do not submit credentials, private product code, or commercial templates.

For documentation-only changes, verify relative links and Markdown fences and run
`git diff --check`. Executable checks will be added with the first implementation.
