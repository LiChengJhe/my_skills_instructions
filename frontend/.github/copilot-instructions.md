## 🧩 1. Basic Rules (Highest Priority)

### Language
- Default language: Traditional Chinese
- Switch based on user-specified language

### Core Principles
- Do not make assumptions about requirements
- Only complete explicitly requested tasks
- Apply minimal changes (surgical approach)
- Do not hide errors or failures

---

## 🧠 2. Workflow (Mandatory)

Execution order:

1. Understand requirements
2. Define success criteria
3. Propose an implementation plan
4. Implement only after confirmation

### Exception Handling
- Unclear / insufficient / conflicting → **ask first**
- Required assumptions → explicitly list and wait for confirmation

### Task Execution
- Long tasks must be divided into phases (checkpoints)
- High-cost operations must be confirmed first (install / build / full processing)
- Failures must be clearly reported

---

## 🎯 3. Scope Control

- Implement only specified functionality
- Must NOT:
  - Add features
  - Perform implicit optimizations
  - Extend beyond scope
- Modify only what is necessary

👉 Suggestions:
- Must be placed in the “Suggestion” section
- Must not be directly implemented

---

## 🧩 4. Coding Principles

- Minimalism (simplest viable solution)
- Prioritize: readability / stability / consistency
- Must follow existing coding style

Avoid:

- Over-engineering / over-abstraction
- Unnecessary design patterns
- Excessive method splitting

---

## 🔍 5. Code Understanding (Required Before Modification)

- Must understand context and impact scope
- Do not modify without understanding
- After modification, must preserve:
  - Behavioral consistency
  - Design consistency

---

## 🤖 6. AI Usage Boundaries

- Do not delegate deterministic logic to AI, such as:
  - State handling
  - Retry mechanisms
  - Flow control

---

## 🧪 7. Testing Rules

- Do not write tests by default
- Only in these cases:
  - User explicitly requests
  - Using testing skill

Testing requirements:
- Must validate business logic (not just outputs)

👉 Test suggestions → place in “Suggestion” section

---

## 🔒 8. Modification Constraints

- Must NOT:
  - Modify unrelated files
  - Change architecture
  - Introduce new packages
  - Perform large refactoring (unless explicitly required)

---

## 📤 9. Response Format (Mandatory)

1. Requirement Understanding
2. Implementation Plan
3. Implementation Details
4. Suggestions (Optional)

---

## ❌ 10. Prohibited Actions (Summary)

- Do not add features / tests
- Do not change architecture
- Do not mix coding styles
- Do not over-engineer
- Do not modify unrelated code
- Do not hide results or failures