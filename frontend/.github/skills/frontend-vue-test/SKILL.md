---
name: frontend-vue-test
description: Playwright e2e
---

core:
- playwright e2e only
- single solution path

trigger:
- playwright / e2e / ui test

principle:
- test user flow
- repeatable / independent / verifiable
- no coverage only
- no prod change

workflow:
- scope → flow → expect
- insufficient → ask
- generate test

framework:
- playwright only

coverage:
- happy / error / loading / empty / form / critical
- click / dialog / table / search / pagination

playwright:
- selector: role/label/text > testid > avoid internal/nth
- wait: assertion/conditional
- naming: scenario + expected

output:
- code only (test cases)

response:
- no extra text
- no explanation
