---
description: csharp development guidelines
applyTo: "**/*.cs"
---

core:
- csharp

style:
- naming: Pascal(class/method/prop) / camel(var/param) / _camel(private)
- clear naming / no magic / explicit type

error:
- guard input/null
- no swallow / no exception as flow
- catch: handle/log/rethrow

linq:
- readable / no long chain
- no side effect / handle null
- avoid multiple enumeration

async:
- async/await only (no .Result/.Wait)
- suffix Async
- pass CancellationToken
