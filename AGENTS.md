# Project Preferences

- Always target the smallest change that fully satisfies the request: touch only necessary files/symbols, preserve repository conventions, public contracts, architecture, and UI language, reuse existing dependencies/components/tokens/patterns, and avoid unrelated cleanup, refactoring, optimization, new packages, or broad refactors.
- Do not create or modify tests unless the user explicitly requests tests; running existing checks is allowed when relevant.
- Do not compile, build, debug, or inspect/analyze project logs unless the user explicitly requests it.
- Do not search for or read image files autonomously; read or analyze only images or screenshots explicitly provided by the user.
- `codegraph` MCP is the primary tool for codebase exploration, file reading, file discovery, and code search.
- Use `codebase-memory` MCP only for broader discovery and architecture context.
- Extract nested ternary operations into independent statements when they reduce readability.
- Avoid functions with too many parameters; group related parameters into an object when appropriate.
- When generating code, keep functions' cognitive complexity low; extract decision logic instead of accumulating conditional branches.
