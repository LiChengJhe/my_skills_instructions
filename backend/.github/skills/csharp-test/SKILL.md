---
name: csharp-test
description: C# unit testing
---

### use
- common: copilot-instructions.md
- csharp: csharp.instructions.md
- mode: test only

### usage
only when:
- user requests test / unit test / coverage

### principle
- behavior over implementation
- repeatable / independent / verifiable
- no coverage-only tests
- no prod code change unless approved

### workflow
order:
- confirm scope / framework / dependency
- insufficient → ask
- generate test

### coverage
priority:
- happy / boundary / failure

### design
- AAA
- name: scenario + behavior + expected
- data: minimal / meaningful
- single concern per test
- no inter-test dependency

mock:
- external only: IO / time / network / db / service
- no mock for sake of mocking

### output
- test cases added
- scenarios covered
- how to run
- testability suggestion
