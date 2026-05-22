---
name: csharp-test
description: C# unit testing. Use only when the user explicitly requests writing/adding tests, generating unit tests, or test cases.
---

# C# Testing Skill

## 🧠 1) Usage Conditions (Mandatory)

Use this skill only when the user explicitly requests one of the following:

- Write tests / add tests
- Generate unit tests / test cases / test coverage
- Or explicitly specifies using this skill

---

## 🎯 2) Core Principles (Highest Priority)

- Test behavior, not implementation details
- Tests must be:
  - Repeatable
  - Independent
  - Have clear, verifiable outcomes
- Do not write meaningless tests just for coverage
- Do not modify production code arbitrarily (unless approved by the user or required for testability)

---

## 🔄 3) Execution Workflow (Fixed)

1. Confirm test scope (class/method/behavior, expected results)
2. Confirm test framework (follow project standard; ask if not specified)
3. Confirm dependency handling (whether mock / stub / integration is needed)
4. If information is insufficient → ask questions first
5. Then generate test code

---

## 🧩 4) Test Design (Scenario Coverage)

Prioritize covering:

- Happy path
- Boundary conditions
- Failure scenarios (exceptions / failed results / invalid inputs)

---

## ⚙️ 5) Test Style & Conventions

- Use Arrange / Act / Assert (AAA)
- Test naming must describe: scenario + behavior + expected result
- Test data should be concise and meaningful

Avoid:

- Multiple unrelated assertions in a single test
- Dependencies between tests

### Mocking Rules (Minimal)

- Only mock external dependencies or uncontrollable behaviors:
  - IO / time / network / database / external services
- Do not mock for the sake of mocking

---

## 📤 6) Completion Output (Required)

Must include:

- What test cases were added
- What scenarios are covered
- How to run the tests
- Testability issues or improvement suggestions (in a “Suggestion” section)