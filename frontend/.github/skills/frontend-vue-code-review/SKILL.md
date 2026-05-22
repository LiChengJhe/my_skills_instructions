---
name: frontend-vue-code-review
description: Vue 3 + Vuetify 3 + TypeScript frontend code review
---

# Frontend Code Review Skill

## 🧠 1. Review Principles (Highest Priority)

- Prioritize **requirement correctness** first, then technical quality
- Only highlight **critical issues**, avoid noise
- Classify issues into:
  - Must Fix (bugs / risks)
  - Suggested Fix (quality / maintainability)
  - Optional (optimization)

---

## 🔍 2. Review Workflow (Fixed Order)

1. Requirement alignment
2. Core technologies (Vue / TS / Vuetify)
3. UI / Layout
4. API / State handling
5. Readability / Maintainability
6. Performance
7. Testing suggestions

---

## 🎯 3. Requirement Alignment (Most Important)

Check:

- Whether it meets requirements
- Whether it:
  - Does too much
  - Does too little
  - Deviates from requirements
- Whether there are undocumented assumptions

👉 If this stage fails → directly mark as **Needs Fix**

---

## 🧩 4. Core Technology Checks

### Vue

- Must use:
  - Composition API
  - `<script setup lang="ts">`
- Must NOT:
  - Mutate props
- Avoid:
  - Side effects in computed
  - Overuse of watch
  - Complex logic in template

---

### TypeScript

- Do not overuse `any`
- Must define types for:
  - props / emits
  - API responses
  - form / table data
- Nullable must be handled properly
- Avoid unsafe assertions

---

### Vuetify (Mandatory)

- Must use Vuetify components / layout / utilities
- Must NOT:
  - Rebuild existing components
  - Replace with custom UI
- Must NOT hardcode colors (use theme / tokens)

---

## 🎨 5. UI / Layout

- Use flex / grid (avoid float / table)
- CSS:
  - Must be scoped
  - Minimize custom CSS
- Must NOT:
  - Use excessive absolute positioning

### Theme Checks

- Support dark / light mode
- No hardcoded colors
- Maintain proper contrast
- Support `prefers-color-scheme` + persistence

---

## 🔌 6. API / State Handling

Must handle:

- loading
- error
- empty states

Check:

- Are errors swallowed?
- Are there race conditions?
- Is API logic duplicated?

---

## ♻️ 7. Readability / Maintainability

- Clear naming
- Methods are not too long and not overly fragmented
- No duplicated logic
- No over-engineering

Check:

- Does it impact props / emits / API compatibility?
- Any unnecessary abstraction (composable / patterns)?

---

## ⚡ 8. Performance

- Avoid:
  - Unnecessary re-renders
  - Heavy computation in templates
  - Overuse of deep watch
- list / table:
  - Should pagination / virtual scroll be applied?

---

## 🧪 9. Testing Suggestions (Playwright)

- Provide suggestions only (do not write test code)
- Prioritize:

  - Happy path
  - Error scenarios
  - loading / empty states
  - Form validation
  - Critical interactions

- Theme testing:
  - Dark / light switching
  - Preference persistence

---

## 📤 10. Response Format (Fixed)

### Review Summary
- Conclusion: Pass / Needs Fix / Risk Identified
- Key reasons:

---

### Must Fix
- Critical issues (bugs / risks / requirement mismatch)

---

### Suggested Fix
- Readability / typing / Vuetify / structural improvements

---

### Optional Suggestions
- Non-critical optimizations

---

### Testing Suggestions
- List scenarios only (do not write test code)