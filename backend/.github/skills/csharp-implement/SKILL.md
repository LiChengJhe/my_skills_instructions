---
name: csharp-implement
description: C# implementation. Used for adding/modifying/fixing/small refactoring of C# code: clarify requirements → plan → minimal-change implementation → completion summary.
---

# C# Implementation Skill

## 🧠 1) Core Principles (Highest Priority)

- Do not make assumptions about requirements (any necessary assumptions must be listed and confirmed)
- Only complete what the user explicitly requests (no extension or expansion)
- Apply minimal changes (surgical approach)
- Do not hide failures or incomplete work

👉 Suggestions:
- Must be placed in the “Suggestion” section
- Must not be treated as implementation requirements

---

## 🔄 2) Workflow (Mandatory)

Execute in order:

1. Requirement understanding (including success criteria)
2. Implementation planning (scope / approach / risks)
3. Implement only after confirmation
4. Completion summary

If unclear / insufficient / conflicting → ask first, do not write code directly

---

## 🎯 3) Scope Control (Mandatory)

- Modify only the minimum scope required to achieve the task
- Maintain consistency with existing behavior and architecture

Must NOT:

- Add features or implicit optimizations
- Add tests on your own
- Perform large refactoring arbitrarily (unless explicitly required)

---

## 🧩 4) Code Quality (Guidelines)

- Prioritize: readability / maintainability
- Naming follows C# conventions and reflects business meaning
- Keep methods at a reasonable size (avoid overly long or overly fragmented methods)
- Avoid duplicated logic
- Avoid over-engineering / unnecessary abstractions
- Design patterns: use only when they clearly reduce complexity or improve maintainability, and explain why

---

## 📤 5) Response Format (Fixed)

### 1. Requirement Understanding
- Objective:
- Known conditions / constraints:
- Success criteria:
- Open questions (if any):

### 2. Implementation Plan
- Scope of modification:
- Approach:
- Risks / considerations:

### 3. Implementation
- Output only task-related changes (minimal changes)

### 4. Completion Summary
- Completed items:
- Incomplete items / limitations (if any):

### 5. Suggestion (Optional)
- Must not be mixed with implementation