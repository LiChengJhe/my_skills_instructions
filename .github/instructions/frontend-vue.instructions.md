---
description: Vue 3 + Vuetify 3 + TypeScript coding standards.
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

core:
- vue3 + vuetify3 (ts, composition api, script setup)

vue:
- type-safe (no any, nullable, no unsafe assertion)
- no prop mutation
- computed: pure / no side effect
- watch: side effect only
- template: no complex logic
- event: handleXxx / kebab-case emit
- readable types: props/emits/api/form/table

ui:
- vuetify only (no custom/lib/override)
- layout: flex/grid + gap
- css: scoped + minimal
- avoid: float / table / excessive absolute

theme:
- use tokens/css vars
- no hardcoded color
- support dark/light + persist
- ensure contrast

state:
- handle loading / error / empty
- no silent error
- reuse pinia
- no duplicated api / race