---
name: csharp-code-review
description: C# Code Review
---

# C# Code Review Skill

## 🧠 1. Review Principles (Highest Priority)

- Prioritize “requirement correctness” first, followed by code quality
- Only highlight **critical issues**, avoid redundancy
- Classify issues into:
  - Must Fix (bugs / risks)
  - Suggested Fix (readability / maintainability)
  - Optional (optimizations)

---

## 🔍 2. Review Workflow (Fixed Order)

1. Requirement alignment
2. Correctness (including error handling / async)
3. Readability
4. Maintainability
5. Performance / resources
6. Testing suggestions

---

## 🎯 3. Requirement Alignment (Most Important)

Check:

- Whether it meets the requirements
- Whether it:
  - Does too much
  - Does too little
  - Deviates from requirements
- Whether there are undocumented assumptions

👉 If this stage fails → mark as **Must Fix** immediately

---

## ✅ 4. Correctness

- Are nulls / boundary cases handled?
- Any logical errors?
- Exception handling:
  - Are exceptions swallowed?
  - Are they handled incorrectly?
- Is async used correctly (avoid blocking)?

---

## 🧩 5. Readability

- Clear naming (aligned with business meaning)
- Methods:
  - Not too long
  - Not overly fragmented
- Can conditional logic be simplified?
- Is LINQ overly complex?
- Does it follow existing coding style?

---

## ♻️ 6. Maintainability

- Any duplicated logic?
- Over-engineering / unnecessary abstraction?
- Does it impact:
  - Existing compatibility?

---

## ⚡ 7. Performance / Resource Usage

- Any:
  - Multiple enumeration (IEnumerable)
  - Unnecessary `ToList` / `ToArray`
  - Blocking async
- Are resources properly released?

---

## 🧪 8. Testing Suggestions

- Provide only test scenarios (do not write test code)
- Prioritize:

  - Happy path
  - Boundary conditions
  - Failure scenarios

---

## 📤 9. Response Format (Fixed)

### Review Summary
- Conclusion: Pass / Needs Fix / Risk Identified
- Key reasons:

---

### Must Fix
- Bugs / risks / requirement mismatch

---

### Suggested Fix
- Readability / maintainability / style

---

### Optional Suggestions
- Non-critical optimizations

---

### Testing Suggestions
- List scenarios only (no test code)