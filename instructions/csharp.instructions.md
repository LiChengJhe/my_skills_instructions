---
description: "C# application and library conventions."
applyTo: "**/*.cs"
---

- Contracts & DTOs: avoid breaking serialization names or required fields when extending DTOs.
- Async & Cancellation: propagate `CancellationToken` through all I/O calls; never block on async code (`.Result`, `.Wait()`, `async void`).
- Data Access & Performance: use `AsNoTracking()` for read-only EF Core queries; project with `.Select()`; prevent N+1 queries in loops.
- Concurrency & Typing: avoid reflection (use static typing, generics, or source generators); use thread-safe collections (`ConcurrentDictionary`, `SemaphoreSlim`) for shared state.
- Null Safety: respect nullable reference annotations; do not suppress warnings with `!` without runtime validation.
- Logging & Exceptions: use structured logging templates (never string interpolation `$"..."`); preserve stack traces with `throw;` (never `throw ex;`).
- Tests: follow existing test framework; test observable behavior rather than internal implementation.
