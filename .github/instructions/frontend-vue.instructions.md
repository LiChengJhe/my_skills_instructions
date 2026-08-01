---
description: "Vue 3 + Vuetify 3 + TypeScript conventions."
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

- Stack: follow existing Vue Composition API, `<script setup>`, Vuetify, Pinia, routing, and TypeScript patterns; prefer precise types and immutable props.
- UI: reuse components and tokens/CSS vars; preserve theme, contrast, accessibility, and responsive behavior; avoid needless CSS overrides.
- State: cover relevant loading/error/empty/success states; surface failures; prevent duplicate, stale, or racing requests.