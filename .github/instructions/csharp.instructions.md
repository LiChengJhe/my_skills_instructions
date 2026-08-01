---
description: "C# application and library conventions."
applyTo: "**/*.cs"
---

- Match repository framework, nullable/analyzers, formatting, naming, and API conventions.
- Validate external input; preserve exception causes; do not swallow exceptions or use them as normal flow.
- Use non-blocking async and pass `CancellationToken` through meaningful I/O or long-running work.
