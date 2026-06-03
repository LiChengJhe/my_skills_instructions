---
name: frontend-vue-code-review
description: Vue3 + Vuetify3 + TS review
---

### core
- use common rules from copilot-instructions.md
- use frontend rules from frontend-vue.instructions.md
- this skill = review only

### principle
- requirement first
- critical only
- classify: must-fix / suggested / optional

### workflow
order:
- requirement
- correctness
- ui/layout
- api/state
- readability
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
- vue/ts/vuetify rule violations
- null/optional handling
- prop mutation
- computed/watch misuse
- template complexity

api-state:
- loading/error/empty handled
- no swallowed error
- no race / duplicated api

ui-theme:
- vuetify used
- no rebuild/custom replacement
- no hardcoded color
- dark/light + contrast

readability:
- naming / method size
- no duplication
- no over-engineering
- no unnecessary abstraction

performance:
- no unnecessary rerender
- no heavy template logic
- no deep watch abuse
- list: pagination / virtual scroll?

### testing
- suggestion only
- scenarios: happy / error / loading-empty / form / critical interaction / theme persist

### output
summary:
- conclusion: pass / needs-fix / risk
- key reasons

must-fix:
- bug / risk / requirement mismatch

suggested:
- quality / typing / structure

optional:
- optimization

testing:
- scenarios only
