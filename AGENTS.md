# Project Preferences

- Scope & Simplicity: make the smallest change that satisfies the request; preserve existing conventions, architecture, and contracts; apply design patterns pragmatically to resolve concrete complexity (e.g., creation, decoupling, or polymorphism), but avoid speculative over-engineering, premature abstractions, unrelated refactors, or new packages.
- Token & Context Efficiency: communicate in Traditional Chinese (繁體中文); be direct and concise without conversational filler; in chat, provide targeted diffs or relevant snippets rather than reprinting entire unmodified files; inspect only relevant symbols and line ranges.
- Session Handoff & Continuity: for multi-step tasks across sessions, maintain continuity by ending milestones with a concise handoff summary (completed work, modified files, key technical decisions, and pending next steps); when resuming, continue directly from prior state without redundant re-discovery.
- Exploration & Tooling: use `codegraph` first for codebase exploration; use `codebase-memory` only for broader architecture context.
- Execution Safeguards: do not create or modify tests unless requested; do not build, run, debug, or inspect logs unless requested; never run destructive commands without explicit confirmation.
- Code Quality & Clean Code: minimize cognitive complexity via guard clauses and early returns; prioritize immutability (`readonly`/`const`) and single responsibility; eliminate dead code; never hardcode configs, URLs, or magic literals (extract to config files, options, or constants).
- Error Handling & Edge Cases: validate inputs and handle failure paths explicitly; never catch generic exceptions without context; handle empty, boundary, and null inputs gracefully.
- Concurrency & State Safety: guard against race conditions in shared state; ensure thread safety in backend operations and prevent stale async responses from overwriting newer state in UI.
- Ambiguity & Trade-offs: when requirements are underspecified or design trade-offs exist, state assumptions explicitly and outline viable options rather than silently guessing.
- Accuracy & Verification: verify declarations in codebase before referencing (never assume unverified APIs exist); align all affected call sites; verify changes satisfy all requirements without syntax or contract regressions.
- Security & Integrity: never hardcode secrets, tokens, or credentials; preserve comments and documentation; produce complete, working code without placeholder omissions (e.g., avoid `// ... existing code`).
