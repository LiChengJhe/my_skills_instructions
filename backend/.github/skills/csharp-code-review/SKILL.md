---
name: csharp-code-review
description: C# review
---

## principle
- requirement first
- highlight critical only
- classify:
  - must-fix (bug/risk)
  - suggested (quality)
  - optional (opt)

## workflow
order:
- requirement
- correctness
- readability
- maintainability
- performance
- testing

## requirement
check:
- meets requirement
- too much / too little
- deviation
- hidden assumptions

fail → must-fix

## correctness
check:
- null / boundary handled
- logic correct
- exception:
  - swallowed?
  - misuse?
- async:
  - blocking?
  - incorrect usage?

## readability
- clear naming (business aligned)

method:
- not too long
- not over-fragmented

check:
- simplify condition?
- linq too complex?
- follow existing style?

## maintainability
- duplicated logic?
- over-engineering / abstraction?
- compatibility impact?

## performance
check:
- multiple enumeration
- unnecessary ToList/ToArray
- blocking async
- resource release

## testing
- suggestion only
- priority:
  - happy path
  - boundary
  - failure

## output

summary:
- conclusion: pass / needs-fix / risk
- key reasons

must-fix:
- bug / risk / requirement mismatch

suggested:
- readability / maintainability / style

optional:
- optimization

testing:
- scenarios only