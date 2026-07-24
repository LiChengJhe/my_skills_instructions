# Project Rules & Guidelines

## Core Principles

- **Codebase Exploration**: Use CodeGraph MCP / tools for codebase exploration, file reading, file discovery, and code search where available.
- **Task Scope**:
  - Focus strictly on requested tasks with minimal changes.
  - Make no assumptions; if unclear or conflicting, ask for clarification. If making assumptions, list them and wait.
  - Identify main problems first and understand dependencies before modification.
  - Ignore non-critical issues and prioritize blocking issues.
  - Do not perform refactors, feature additions, implicit optimizations, or architectural changes unless requested.
- **Suggestions**: Keep suggestions in a separate section; do not implement unrequested suggestions.
- **Testing**: Do not add or run tests unless explicitly requested.

---

## C# Coding Standards

**Applies to**: `**/*.cs`

### Style & Naming
- Naming convention: PascalCase (classes, methods, properties) / camelCase (variables, parameters) / `_camelCase` (private fields).
- Use clear naming, avoid magic numbers/strings, and use explicit types.
- No reflection.

### Error Handling
- Guard input and check nulls.
- Never swallow exceptions or use exceptions for regular control flow.
- Catch blocks must handle, log, or rethrow properly.

### LINQ
- Keep queries readable without long chains.
- Avoid side effects and handle potential null values.
- Avoid multiple enumeration of enumerables.

### Async / Await
- Use `async`/`await` pattern exclusively (never `.Result` or `.Wait()`).
- Suffix async method names with `Async`.
- Always pass `CancellationToken` where supported.

---

## Vue 3 + Vuetify 3 + TypeScript Standards

**Applies to**: `**/*.{vue,ts,tsx,js,jsx}`

### Core Stack
- Vue 3 + Vuetify 3 (TypeScript, Composition API, `<script setup>`).

### Vue & TypeScript
- Maintain strict type safety (avoid `any`, handle nullables, avoid unsafe assertions).
- Do not mutate props directly.
- `computed`: Keep pure with no side effects.
- `watch`: Use strictly for side effects.
- Templates: Keep clean without complex inline logic.
- Events: Use `handleXxx` naming for handlers and `kebab-case` for emitted events.
- Maintain readable interface/type definitions for props, emits, API responses, forms, and table data.

### UI & Styling
- Rely on Vuetify 3 components (avoid custom overrides or external libraries unless requested).
- Layouts: Use Flexbox/Grid with `gap`.
- CSS: Keep scoped and minimal. Avoid `float`, raw `<table>`, or excessive absolute positioning.

### Theme & Colors
- Use theme tokens and CSS variables (no hardcoded color codes).
- Support dark/light mode switching and state persistence.
- Ensure proper color contrast.

### State & API
- Handle `loading`, `error`, and `empty` states explicitly.
- Do not swallow errors silently.
- Reuse Pinia stores.
- Avoid duplicate API requests or race conditions.
