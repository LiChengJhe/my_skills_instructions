---
name: frontend-vue-implement
description: Vue3 + Vuetify3 + TS implementation
---

## workflow
order:
- understand
- success criteria
- plan
- confirm → implement

rules:
- unclear/conflict → ask
- no assumptions (list if needed)
- only requested tasks
- long task → split
- failures → report

## scope
- minimal change (surgical)
- only required scope

no:
- feature creep
- scope expansion
- architecture/api/schema change
- new pkg/ui/state
- unrelated modification
- auto test generation

## core

vue:
- composition api
- script setup + ts
- no prop mutation

computed:
- derived only
- no side effects

watch:
- side effects only

template:
- no complex logic

event:
- handler: handleXxx
- emit: kebab-case

ts:
- must type:
  - props/emits
  - api
  - form/table

- no any (explain if used)
- handle nullable
- avoid unsafe assertion

vuetify:
- must use
- no rebuild / replace
- no override internal styles

## ui
- flex/grid + gap
- scoped css
- minimal custom css

forbidden:
- float
- table layout
- excessive absolute

## theme
- dark/light required
- use theme / css vars
- no hardcoded color
- support prefers-color-scheme + persist
- ensure contrast

## api/state
must handle:
- loading
- error
- empty

rules:
- no silent error
- avoid duplication
- avoid race condition

## quality
- readable
- clear naming
- consistent style

avoid:
- over-engineering
- over-abstraction
- oversized / fragmented methods

## response
1. understanding
2. plan
3. implementation
4. suggestions (opt)