---
description: "Vue 3 + Vuetify 3 + TypeScript conventions."
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

- Component Boundaries: keep changes within existing Vue component/store/API boundaries; reuse Vuetify components, tokens, and Pinia helpers; avoid adding new packages.
- Reactivity & Cleanup: preserve reactivity (never destructure `props` without `toRefs`); always clean up timers, intervals, and DOM listeners in `onUnmounted`.
- Contracts & Types: explicitly declare `defineEmits` with typed payloads; avoid `any` or loose type assertions (`as any`); provide explicit types for props and API payloads.
- Template & Styling: use stable, unique `:key` in `v-for`; use Vue template refs (`useTemplateRef` / `ref`) instead of direct DOM manipulation (`document.querySelector`); scope component styles with `<style scoped>` to prevent CSS leakage.
- Security: never render unescaped user content with `v-html` without explicit sanitization (e.g. DOMPurify) to prevent XSS.
- State Resilience: cover loading, error, empty, and success states; surface failures cleanly; prevent duplicate or racing requests from overwriting newer state.
- Tests: follow existing Playwright structure; prefer accessible/stable locators and web-first assertions; test observable user flows without arbitrary timeouts.