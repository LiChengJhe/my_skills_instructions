# Project Preferences

- Scope & Simplicity: make the smallest change that satisfies the request; preserve existing conventions, architecture, and contracts; avoid premature abstractions, over-engineering, unrelated refactors, or new packages.
- Token & Context Efficiency: be direct and concise without conversational filler; in chat, provide targeted diffs or relevant snippets rather than reprinting entire unmodified files; inspect only relevant symbols and line ranges.
- Session Handoff & Continuity: for multi-step tasks across sessions, maintain continuity by ending milestones with a concise handoff summary (completed work, modified files, key technical decisions, and pending next steps); when resuming, continue directly from prior state without redundant re-discovery.
- Exploration & Tooling: use `codegraph` first for codebase exploration; use `codebase-memory` only for broader architecture context.
- Execution Safeguards: do not create or modify tests unless requested; do not build, run, debug, inspect logs, or read images unless requested.
- Code Quality & Clean Code: minimize cognitive complexity via guard clauses and early returns; prioritize immutability (`readonly`/`const`) and single responsibility; eliminate dead code; never hardcode configs, URLs, or magic literals (extract to config files, options, or constants).
- Error Handling & Edge Cases: validate inputs and handle failure paths explicitly; never catch generic exceptions without context; handle empty, boundary, and null inputs gracefully.
- Concurrency & State Safety: guard against race conditions in shared state; ensure thread safety in backend operations and prevent stale async responses from overwriting newer state in UI.
- Ambiguity & Trade-offs: when requirements are underspecified or design trade-offs exist, state assumptions explicitly and outline viable options rather than silently guessing.
- Accuracy & Verification: never assume unverified APIs or types exist—verify declarations in codebase before referencing; trace data flow for root causes; align all affected call sites when modifying shared contracts.
- Git & Commit Hygiene: follow Conventional Commits (`feat:`, `fix:`, `refactor:`, `chore:`); keep commits atomic; never stage secrets, build artifacts, or temporary files.
- Self-Verification: before concluding, verify changes against all specified requirements; check that imports, syntax, and contracts remain intact without regressions.
- Security & Integrity: never hardcode secrets, tokens, or credentials; preserve comments and documentation; produce complete, working code without placeholder omissions (e.g., avoid `// ... existing code`).
