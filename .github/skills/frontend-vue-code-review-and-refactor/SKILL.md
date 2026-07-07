---
name: frontend-vue-code-review-and-refactor
description: Review, troubleshoot, and refactor Vue code.
---

core:
- review and refactor
- safe transformation
- single solution path

principle:
- requirement first
- must-fix only (no nitpicks)
- refactor: improve structure/perf, preserve behavior

workflow:
- requirement → correctness → ui/api → readability → perf → review or refactor

checks:
- requirement:
  - match / missing / excess / assumption → fail = must-fix
- correctness:
  - rule violation (vue/ts/vuetify)
  - null/optional
  - prop mutation
  - computed/watch misuse
  - template complexity
- api/ui:
  - loading/error/empty
  - no swallowed error
  - no race/dup api
  - vuetify only / no override / no hardcoded color / theme ok
- readability:
  - naming / size / duplication
  - no over-engineering
- perf:
  - no unnecessary rerender
  - no heavy template / deep watch
  - list: pagination / virtual?

output:
- status + must-fix only
- code only (if refactor)

response:
- minimal bullets
- no explanation