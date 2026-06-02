---
description: Vue3 + Vuetify3 + TS guidelines
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
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
- no:
  - extra features
  - scope expansion
  - unrelated modification

suggestion:
- separate section only
- must not implement

## tech
- vue3 composition api
- script setup + ts
- no any (explain if used)

## typing
- must type:
  - props / emits
  - api response
  - form model
  - table row

rules:
- handle nullable/optional
- avoid type assertion

## vue
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

## ui (vuetify)
- must use vuetify
- no custom replacement
- no other ui lib

## layout
- use vuetify utilities
- flex/grid + gap
- scoped css

forbidden:
- float
- table layout
- excessive absolute

## theme
- support dark/light
- use theme / css vars
- no hardcoded color

## api/state
- must handle:
  - loading
  - error
  - empty

- no silent error
- reuse pinia if exists

## response
1. understanding
2. plan
3. implementation
3. suggestions (opt)

## prohibited
- no feature creep
- no new pkg/ui/state
- no unrelated changes
- no over-engineering
- no hidden errors