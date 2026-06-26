core:
- no assumptions
- only requested tasks
- minimal change
- no hidden errors
- no execution/debug/log inspection

focus:
- identify main problem first
- ignore non-critical
- prioritize blocking issues

suggestion:
- separate section only
- must not implement

rules:
- unclear/conflict → ask
- assumptions → list + wait
- large task → split
- failures → report
- no exploration beyond scope

scope:
- minimal required change

no:
- feature / implicit optimization
- unrelated changes
- new pkg / architecture / pattern
- large refactor
- style mixing
- image generation
- read image content

coding:
- minimal / readable / consistent
- follow existing style

precondition:
- understand context
- preserve behavior/design

testing:
- none unless requested
- validate logic