---
name: frontend-vue-implement
description: Vue 3 + Vuetify 3 + TypeScript frontend implementation
---

# Frontend Implementation Skill

## 🧠 1. Workflow (Highest Priority)

Execution order:

1. Understand requirements
2. Define success criteria
3. Propose an implementation plan
4. Implement only after confirmation

### Exception Handling

- Unclear / insufficient / conflicting → ask first
- Do not assume requirements (list any necessary assumptions)

### Task Principles

- Only complete explicitly assigned tasks
- Long tasks must be split into phases (checkpoints)
- Failures must be clearly stated

---

## 🎯 2. Scope Control (Mandatory)

- Implement only the requested scope
- Apply minimal changes (surgical approach)

Must NOT:

- Add features
- Extend beyond scope
- Change architecture / API / schema
- Add new packages / UI libraries / state tools
- Modify unrelated files
- Proactively write tests

---

## 🧩 3. Technical Core (Vue / TS / Vuetify)

### Vue / TypeScript

- Composition API + `<script setup lang="ts">`
- Types are required for: props / emits / API / form / table
- Avoid `any`

Rules:

- Do not mutate props
- computed must have no side effects
- watch only for side effects
- Avoid complex logic in templates
- Event handlers → `handleXxx`

---

### Vuetify (Mandatory)

- Must use Vuetify components / layout / utilities
- Must NOT:
  - Rebuild components already provided by Vuetify
  - Replace with custom UI
  - Arbitrarily override internal classes

---

## 🎨 4. UI / Layout

- Use flex / grid (with `gap`)
- CSS must be:
  - scoped
  - minimal custom CSS

Forbidden:

- float
- table layout
- excessive absolute positioning

---

## 🌗 5. Theme (Required, Concise)

- Must support dark / light mode
- Use:
  - Vuetify theme or CSS variables
- Forbidden:
  - Hardcoded colors

Basic requirements:

- Support `prefers-color-scheme`
- Allow switching and persist it (localStorage or state)
- Colors must remain readable (reasonable contrast)

---

## 🔌 6. API / State Handling

Must handle:

- loading
- error
- empty states

Must NOT:

- Swallow errors

Avoid:

- Duplicated API logic
- Race conditions

---

## ♻️ 7. Code Quality

- Readability first
- Clear naming
- Consistent coding style

Avoid:

- Over-engineering / over-abstraction
- Methods that are too long or overly fragmented

---

## 📤 8. Response Format (Fixed)

1. Requirement Understanding
2. Implementation Plan
3. Implementation Details
4. Suggestions (Optional)