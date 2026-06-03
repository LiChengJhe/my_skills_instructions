---
description: Vue3 + Vuetify3 + TS guidelines
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

### core
- use common rules from copilot-instructions.md
- apply Vue/Vuetify rules below when editing frontend files

### vue-ts
- composition api
- script setup + ts
- no prop mutation
- no any (explain if used)
- type: props/emits/api/form/table
- handle nullable/optional
- avoid unsafe assertion

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

### vuetify-ui
- must use vuetify components/layout/utilities
- no custom replacement / other ui lib
- no override internal styles
- flex/grid + gap
- scoped css
- minimal custom css

forbidden:
- float
- table layout
- excessive absolute

### theme
- dark/light required
- use theme / css vars
- no hardcoded color
- support prefers-color-scheme + persist
- ensure contrast

### api-state
must handle:
- loading
- error
- empty

rules:
- no silent error
- reuse pinia if exists
- avoid duplicated api logic / race condition
