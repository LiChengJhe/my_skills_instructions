---
description: General C# Development Guidelines
applyTo: "**/*.cs"
---

# C# Development Guidelines

## 🧠 1. Core Principles (Highest Priority)

- Do not make assumptions about requirements (must list and confirm if necessary)
- Only complete explicitly assigned tasks (no extension)
- Apply minimal changes (surgical approach)
- Do not hide errors or incomplete work

👉 Suggestions may be provided, but:
- Must be clearly labeled as “Suggestion”
- Must not be directly implemented

---

## 🔄 2. Workflow (Mandatory)

Execution order:

1. Understand requirements
2. Define success criteria
3. Propose implementation plan
4. Implement only after confirmation

### Exception Handling

- Unclear / insufficient / conflicting → ask first

### Task Execution

- Long tasks must be divided into phases (checkpoints)
- High-cost operations must be confirmed first (build / full processing / large datasets)
- Failures must be explicitly reported (no skipping)

---

## 🎯 3. Scope Control

- Implement only the requested scope
- Modify only what is necessary

Must NOT:

- Add features / implicit optimizations
- Modify unrelated code
- Introduce new packages / architecture (unless requested)
- Perform large-scale refactoring (unless explicitly required)

---

## 🔍 4. Preconditions for Modification

- Must first understand existing code (context-aware)
- After modification, must maintain:
  - Behavioral consistency
  - Design consistency

---

## 🧩 5. Coding Principles

- Minimalism (simplest viable solution)
- Prioritize: readability / stability / maintainability
- Must follow existing coding style

Avoid:

- Over-engineering / unnecessary abstraction
- Unnecessary method splitting
- Duplicated logic

---

## 🎯 6. Coding Style (Critical)

- Follow existing style (no mixing)

### Naming

- PascalCase → Class / Method / Property
- camelCase → variable / parameter
- `_camelCase` → private field

### Rules

- Names must reflect business meaning
- Avoid magic strings / numbers (extract constants if needed)
- Prefer explicit types (avoid overusing `var`)

---

## ⚠️ 7. Error Handling

- Must guard against:
  - External input
  - Nullable values

Must NOT:

- Swallow exceptions
- Use exceptions for control flow

`catch` must:

- Handle / log / rethrow

---

## 🔍 8. LINQ / Data Handling

- Readability first
- Avoid overly long chains
- Break complex logic into intermediate variables
- No side effects
- Be cautious of multiple enumeration
- Handle null explicitly

---

## ⏱️ 9. Asynchronous Programming

- Use async/await
- Do not use `.Result` or `.Wait()`
- Async methods must end with `Async`
- Pass `CancellationToken` when cancellation is supported
- Avoid unnecessary Task wrapping

---

## 🤖 10. AI Usage Boundaries

- Do not delegate deterministic logic to AI, such as:
  - State handling
  - Retry logic
  - Flow control

---

## 🧪 11. Testing Rules

- Do not write tests by default
- Only write tests when explicitly requested

Tests must:

- Validate business logic (not just outputs)

---

## 📤 12. Response Requirements

- If unclear → ask first
- Before modification → provide a plan
- Output only necessary content
- Suggestions must be in a separate section

---

## ❌ 13. Prohibited Actions (Summary)

- Do not add features / tests
- Do not introduce new packages / architecture
- Do not modify unrelated code
- Do not over-engineer
- Do not modify without understanding context
- Do not hide results or failures