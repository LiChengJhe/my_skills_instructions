---
name: frontend-vue-test
description: Vue3 + Vuetify3 + TS playwright e2e
---

## usage
only when:
- user requests playwright/e2e/ui test

## principle
- focus: user flow
- no implementation detail testing
- test must:
  - repeatable
  - independent
  - verifiable

no:
- test for coverage only
- modify prod code (unless allowed)

## workflow
order:
- confirm scope
- define flow
- define expected result
- insufficient → ask
- generate test

## framework
- playwright only

no:
- vitest
- vue-test-utils
- other tools

## coverage
priority:
- happy path
- error
- loading/empty
- form
- critical interaction

common:
- click
- dialog
- table
- search
- pagination

## playwright

selector:
- prefer:
  - getByRole
  - getByLabel
  - getByText
- fallback:
  - getByTestId

avoid:
- vuetify internal class
- dom structure (nth-child)

wait:
- locator assertion (toBeVisible)
- conditional wait
- no hard wait

naming:
- scenario + expected

## output
must include:
- test cases added
- flows covered
- how to run
- testability suggestion