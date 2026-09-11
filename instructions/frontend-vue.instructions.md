---
description: "Vue 3 + Vuetify 3 + TypeScript conventions."
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

- Component Boundaries: reuse existing Vuetify components, design tokens, and Pinia stores without inventing ad-hoc abstractions.
- Reactivity & Cleanup: preserve reactivity (never destructure `props` without `toRefs`); clean up timers and event listeners in `onUnmounted`.
- TypeScript & Contracts: explicitly declare `defineEmits` and props with strict types; avoid `any` or loose type assertions (`as any`).
- Template & Styling: use stable, unique `:key` in `v-for`; use template refs (`useTemplateRef`/`ref`) instead of direct DOM manipulation; always use `<style scoped>`.
- State & Async: handle loading, error, and empty states; guard against racing async responses overwriting newer state.
- Tests: follow existing Playwright structure; prefer accessible locators and web-first assertions over arbitrary timeouts.