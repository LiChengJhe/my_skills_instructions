---
name: csharp-code-review
description: C# review
---

### use
- common: copilot-instructions.md
- csharp: csharp.instructions.md
- mode: review only

### principle
- requirement first
- critical only
- classify: must-fix / suggested / optional

### workflow
order:
- requirement
- correctness
- readability
- maintainability
- performance
- testing

### requirement
check:
- meets requirement
- too much / too little
- deviation
- hidden assumptions

fail → must-fix

### review-checks
correctness:
- null / boundary / logic
- exception swallowed / misuse
- async blocking / misuse

readability:
- naming / method size
- condition simplification
- linq complexity
- style consistency

maintainability:
- duplication
- over-engineering / abstraction
- compatibility impact

performance:
- multiple enumeration
- unnecessary ToList/ToArray
- blocking async
- resource release

### testing
- suggestion only
- scenarios: happy / boundary / failure

### output
summary:
- conclusion: pass / needs-fix / risk
- key reasons

must-fix:
- bug / risk / requirement mismatch

suggested:
- readability / maintainability / style

optional:
- optimization

testing:
- scenarios only