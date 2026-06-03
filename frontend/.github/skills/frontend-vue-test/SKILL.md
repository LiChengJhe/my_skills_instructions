---
name: frontend-vue-test
description: Vue3 + Vuetify3 + TS playwright e2e
---

### core
- use common rules from copilot-instructions.md
- use frontend rules from frontend-vue.instructions.md
- this skill = Playwright E2E only

### usage
only when:
- user requests playwright / e2e / ui test

### principle
- test user flow, not implementation
- repeatable / independent / verifiable
- no coverage-only tests
- no prod code change unless allowed

### workflow
order:
- confirm scope
- define flow + expected result
- insufficient → ask
- generate test

### framework
- playwright only
- no vitest / vue-test-utils / other tools

### coverage
priority:
- happy / error / loading-empty / form / critical interaction

common:
- click / dialog / table / search / pagination

### playwright
selector:
- prefer: getByRole / getByLabel / getByText
- fallback: getByTestId
- avoid: vuetify internal class / nth-child

wait:
- use locator assertion / conditional wait
- no hard wait

naming:
- scenario + expected

### output
- test cases added
- flows covered
- how to run
- testability suggestion