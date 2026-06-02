---
name: csharp-implement
description: C# implementation
---

## core
- no assumptions
- only requested tasks
- minimal change (surgical)
- no hidden failures

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
- understand (incl success criteria)
- plan (scope/approach/risk)
- confirm → implement
- summary

rules:
- unclear/conflict → ask
- assumptions → list + wait
- long task → split
- failures → report

## scope
- minimal modification
- keep behavior + architecture consistent

no:
- feature / implicit optimization
- auto test
- large refactor

## quality
- readable / maintainable
- meaningful naming
- consistent style

avoid:
- duplication
- over-engineering
- unnecessary abstraction
- oversized / fragmented methods
- unnecessary pattern (must justify)

## response

1. understanding
- objective
- constraints
- success criteria
- open questions

2. plan
- scope
- approach
- risk

3. implementation
- minimal change only

4. summary
- completed
- limitations

5. suggestion (opt)