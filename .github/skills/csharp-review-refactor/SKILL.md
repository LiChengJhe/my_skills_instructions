---
name: csharp-review-refactor
description: Review, troubleshoot, and refactor C# code.
---

mode: review / refactor

principle:
- requirement first
- critical only
- classify: must-fix / suggested / optional
- refactor: preserve behavior, improve readability and maintainability

workflow:
- review: requirement → correctness → readability → maintainability → perf → test
- refactor: identify issues → plan refactoring → confirm → implement
- single solution path

checks:
- requirement: match / excess / missing / assumption → fail = must-fix
- correctness:
  - null / boundary / logic
  - exception misuse / swallowed
  - async misuse / blocking
- readability:
  - naming / size / condition / linq / style
- maintainability:
  - duplication / over-engineering / compatibility
- perf:
  - multiple enum
  - unnecessary ToList/ToArray
  - blocking async
  - resource release

testing:
- suggestion only (for review)
- validate logic (for refactor)
- happy / boundary / failure

output:
- code only
- no explanation
- bullets
- no extra text
- summary: pass / needs-fix / risk + reasons
- must-fix: bug / risk / requirement
- suggested: quality
- optional: optimization
- refactor-plan: proposed changes and benefits

response:
- minimal
- only required sections