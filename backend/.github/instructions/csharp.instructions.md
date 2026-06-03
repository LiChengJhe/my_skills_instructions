---
description: csharp development guidelines
applyTo: "**/*.cs"
---

### use
- common: copilot-instructions.md
- language: C# only

### style
naming:
- PascalCase: class/method/property
- camelCase: variable/param
- _camelCase: private field

rules:
- meaningful naming
- avoid magic values (extract if needed)
- prefer explicit type (avoid var abuse)

### error
- guard external input / nullable
- no swallow exception
- no exception as flow
- catch: handle / log / rethrow

### linq
- readability first
- avoid long chains
- break complex logic into variables
- no side effects
- beware multiple enumeration
- handle null

### async
- async/await only
- no .Result / .Wait()
- suffix Async
- pass CancellationToken if supported
- no unnecessary Task wrap