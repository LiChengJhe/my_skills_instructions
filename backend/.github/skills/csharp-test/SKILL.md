---
name: csharp-test
description: C# unit testing
---

## usage
only when:
- user requests test / unit test / coverage

## principle
- test behavior (not implementation)
- test must:
  - repeatable
  - independent
  - verifiable

no:
- coverage-only tests
- modify prod code (unless approved)

## output
- default: code only
- no explanation unless asked
- prefer bullets
- no extra text

## workflow
order:
- confirm scope (target / behavior / expected)
- confirm framework (follow project / ask)
- confirm dependency (mock / stub / integration)
- insufficient → ask
- generate test

## coverage
priority:
- happy path
- boundary
- failure

## design

aaa:
- arrange
- act
- assert

naming:
- scenario + behavior + expected

data:
- minimal / meaningful

rules:
- single concern per test
- no inter-test dependency

mock:
- only external:
  - IO / time / network / db / service
- no mock for sake of mocking

## output-required
- test cases added
- scenarios covered
- how to run
- testability suggestion