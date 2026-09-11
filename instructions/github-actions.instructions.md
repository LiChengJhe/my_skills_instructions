---
description: "GitHub Actions workflow conventions and security."
applyTo: "**/.github/workflows/*.{yml,yaml}"
---

- Permissions & Security: explicitly declare top-level `permissions:` (e.g. `contents: read`); never expose or print unmasked secrets in run logs.
- Concurrency Control: configure `concurrency:` with `cancel-in-progress: true` on PR workflows to terminate superseded runs and conserve runner minutes.
- Execution Timeouts: specify explicit `timeout-minutes:` on every job to prevent stalled workflows from exhausting quotas.
- Caching: leverage ecosystem-native caching (`actions/setup-dotnet`, `actions/setup-node` with `cache:`) to minimize build durations.
