---
description: csharp development guidelines
applyTo: "**/*.cs"
---

## core
- no assumptions
- only requested tasks
- minimal change (surgical)
- no hidden errors

suggestion:
- separate section only
- must not implement

## output
- default: code only
- no explanation unless asked
- prefer bullets
- no extra text

## workflow
order:
- understand
- success criteria
- plan
- confirm → implement

rules:
- unclear/conflict → ask
- assumptions → list + wait
- long task → split
- high cost → confirm
- failures → report

## scope
- only required scope
- modify minimal

no:
- feature / implicit optimization
- unrelated changes
- new pkg / architecture
- large refactor

## precondition
- must understand context
- preserve:
  - behavior
  - design

## coding
- minimal / readable / stable / maintainable
- follow existing style

avoid:
- over-engineering
- unnecessary abstraction
- unnecessary split
- duplicated logic

## style

naming:
- PascalCase: class/method/property
- camelCase: variable/param
- _camelCase: private field

rules:
- meaningful naming
- avoid magic values (extract if needed)
- prefer explicit type (avoid var abuse)

## error
- guard:
  - external input
  - nullable

no:
- swallow exception
- exception as flow

catch:
- handle / log / rethrow

## linq
- readability first
- avoid long chains
- break into variables
- no side effects
- beware multiple enumeration
- handle null

## async
- async/await only
- no .Result / .Wait()
- suffix Async
- pass CancellationToken if supported
- no unnecessary Task wrap

## testing
- default: none
- only if requested
- validate business logic

## response
1. understanding
2. plan
3. implementation
4. summary
5. suggestion (opt)

## prohibited
- no feature/test/pkg
- no architecture change
- no unrelated changes
- no over-engineering
- no modify without understanding
- no hidden errors