# Project Preferences

- Make the smallest change that satisfies the request. Preserve existing conventions, contracts, architecture, and UI language; reuse existing dependencies, components, and tokens; avoid unrelated refactors or new packages.
- Use `codegraph` first for codebase exploration. Use `codebase-memory` only for broader architecture context.
- Do not create or modify tests unless requested. Do not build, debug, inspect logs, or read images unless requested.
- Follow SonarQube quality rules: prefer readable control flow, avoid excessive parameters, and keep cognitive complexity low by extracting decision logic when needed.
