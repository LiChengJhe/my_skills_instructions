---
name: frontend-vue-code-review
description: Vue3 + Vuetify3 + TS review
---

## principle
- requirement first
- highlight critical only
- classify:
  - must-fix (bug/risk)
  - suggested (quality)
  - optional (opt)

## workflow
order:
- requirement
- core (vue/ts/ui)
- ui/layout
- api/state
- readability
- performance
- testing

## requirement
check:
- meets requirement
- too much / too little
- deviation
- hidden assumptions

fail → must-fix

## core

vue:
- composition api
- script setup + ts
- no prop mutation
- no side effect in computed
- avoid watch abuse
- no complex template logic

ts:
- no overuse any
- must type:
  - props/emits
  - api
  - form/table
- handle nullable
- avoid unsafe assertion

vuetify:
- must use
- no rebuild / replace
- no hardcoded color

## ui
- flex/grid
- scoped css
- minimal custom css

forbidden:
- float
- table layout
- excessive absolute

theme:
- dark/light required
- no hardcoded color
- proper contrast
- support prefers-color-scheme + persist

## api/state
must handle:
- loading / error / empty

check:
- error swallowed?
- race condition?
- duplicated api?

## readability
- clear naming
- reasonable method size
- no duplication
- no over-engineering
- no unnecessary abstraction

## performance
- avoid:
  - unnecessary rerender
  - heavy template logic
  - deep watch abuse

list:
- need pagination / virtual scroll?

## testing
- suggestion only
- priority:
  - happy path
  - error
  - loading/empty
  - form validation
  - critical interaction
  - theme switch + persist

## output

summary:
- conclusion: pass / needs-fix / risk
- key reasons

must-fix:
- bugs / risks / requirement mismatch

suggested:
- quality / typing / structure

optional:
- optimization

testing:
- scenarios only