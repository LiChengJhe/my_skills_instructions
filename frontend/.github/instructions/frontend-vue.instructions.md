---
description: Vue 3 + Vuetify 3 + TypeScript Frontend Development Guidelines
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

# Vue Frontend Development Guidelines

## 🧠 1. Workflow (Highest Priority)

- Before implementation, must:
  1. Understand requirements
  2. Define success criteria
  3. Provide a brief plan (scope / approach / success criteria)

- If there are issues:
  - Unclear / insufficient / conflicting → **ask first**
  - Do not make assumptions (list assumptions if necessary)

- Task principles:
  - Only perform what is requested
  - Long tasks must be split into phases (checkpoints)
  - Failures must not be hidden and must be clearly stated

---

## 🎯 2. Implementation Scope Control

- Implement only required functionality
- Apply “surgical changes” (minimal modification)
- Do not modify unrelated code
- Do not expand functionality

👉 Suggestions may be provided, but:
- Must be in a separate section
- Must not be directly implemented

---

## 🧩 3. Technical Fundamentals

- Vue 3 Composition API
- `<script setup lang="ts">`
- TypeScript is required
- Avoid `any` (must explain if used)

---

## 🧾 4. Typing Rules (All Must Be Typed)

Must define types for:

- props / emits
- API responses
- form models
- table rows

Additional notes:

- nullable / optional must be explicitly handled
- Avoid excessive type assertions

---

## ⚙️ 5. Vue Usage Rules

- Do not mutate props
- computed:
  - For derived state only
  - Must not have side effects
- watch:
  - Only for side effects
- template:
  - Avoid complex logic
- event naming:
  - `handleXxx`

---

## 🎨 6. UI / Vuetify Principles (Mandatory)

- **Must use Vuetify components and its official layout / utilities**
- Do not recreate components already provided by Vuetify
- Do not replace Vuetify with custom UI
- Do not introduce other UI libraries (unless explicitly requested)

---

## 📐 7. Layout / CSS

- Prefer Vuetify utilities
- Use flex / grid (with gap)
- CSS must be scoped

Forbidden:

- float
- table layout
- excessive absolute positioning

---

## 🌗 8. Theme (Required)

- Must support dark / light mode
- Use:
  - Vuetify theme or CSS variables
- Forbidden:
  - Hardcoded colors

---

## 🔌 9. API / State Handling

- Must handle:
  - loading / error / empty states
- Do not swallow errors
- If Pinia is already used → must reuse it

---

## 🤖 10. AI Usage Constraints

- Do not delegate deterministic logic to AI, such as:
  - Conditional logic
  - Flow control

---

## 📤 11. Response Format (Fixed)

1. Requirement Understanding
2. Implementation Plan
3. Implementation
4. Suggestions (Optional)

---

## ❌ Prohibited Actions (Summary)

- Do not add features
- Do not introduce new packages / UI / state tools
- Do not modify unrelated code
- Do not over-engineer
- Do not hide errors