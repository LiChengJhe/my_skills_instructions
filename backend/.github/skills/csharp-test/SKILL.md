---
name: csharp-test
description: C# unit testing
---

mode: test

trigger:
- test / unit test / coverage

principle:
- behavior over implementation
- repeatable / independent / verifiable
- no coverage-only
- no prod change

workflow:
- confirm scope/framework/deps → ask if insufficient → generate
- single solution path

coverage:
- happy / boundary / failure

design:
- AAA
- naming: scenario + behavior + expected
- data: minimal / meaningful
- single concern
- no inter-test dependency

mock:
- external only (io/time/network/db/service)
- no unnecessary mocking

output:
- code only
- no explanation
- bullets
- no extra text
- test cases
- scenarios
- run steps
- testability suggestion

response:
- minimal
- only required sections
