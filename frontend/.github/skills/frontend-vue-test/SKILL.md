---
name: frontend-vue-test
description: Vue 3 + Vuetify 3 + TypeScript Playwright testing
---

# Frontend Playwright Testing Skill

## 🧠 1. Usage Conditions (Mandatory)

Use this skill only when the user explicitly requests:

- Writing tests / adding tests
- Playwright / E2E / UI / workflow testing

---

## 🎯 2. Testing Principles (Highest Priority)

- Focus on **user interaction flows**
- Do not test implementation details
- Tests must be:
  - Repeatable
  - Independent
  - Have clear, verifiable outcomes

Must NOT:

- Write tests solely for coverage
- Arbitrarily modify production code (unless explicitly allowed)

---

## 🧩 3. Execution Workflow

1. Confirm test scope
2. Define user interaction flow
3. Define expected results
4. If information is insufficient → ask first
5. Then generate test code

---

## ⚙️ 4. Testing Framework (Fixed)

- Must use **Playwright**
- Must NOT use:
  - Vitest
  - Vue Test Utils
  - Other testing tools (unless explicitly required)

---

## 🔍 5. Test Coverage (Core Scenarios)

Prioritize:

- Happy path
- Error scenarios
- loading / empty states
- Forms and critical interactions

Examples:

- click
- dialog
- table
- search
- pagination

---

## 🧪 6. Playwright Implementation Rules

### Selector (Stability First)

Prefer:

- `getByRole`
- `getByLabel`
- `getByText`
- `getByTestId`

Avoid:

- Vuetify internal classes
- DOM structure dependencies (e.g., `nth-child`)

---

### Waiting Strategy

- Use locator assertions (e.g., `toBeVisible`)
- Use conditional waits (not time-based)
- Do not rely on hardcoded timeouts as primary mechanism

---

### Naming

- Test names must describe:
  - Scenario + expected result

---

## 📤 7. Output Requirements

Must include:

- What test cases were added
- What user flows are covered
- How to run the tests
- Testability suggestions (if any)