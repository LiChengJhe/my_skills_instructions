---
description: "C# application and library conventions."
applyTo: "**/*.cs"
---

- Contracts & Evolution: preserve C# public APIs, schemas, and architecture contracts; avoid breaking changes to serialization property names or required fields when extending DTOs.
- Async & Cancellation: use non-blocking async and propagate `CancellationToken` through all I/O calls; never block on async code (avoid `.Result`, `.Wait()`, or `async void`).
- Resource Management: ensure `IDisposable` and `IAsyncDisposable` instances are deterministically released with `using` declarations.
- Data Access & Performance: use `AsNoTracking()` for read-only EF Core queries; project columns with `.Select()`; prevent N+1 queries by avoiding database calls in loops.
- Concurrency & Transactions: use thread-safe collections (`ConcurrentDictionary`, `SemaphoreSlim`) for shared state; wrap multi-entity state changes in database transactions.
- Reflection & Typing: avoid reflection; rely on static typing, generics, interfaces, or source generators instead.
- Null Safety: respect nullable reference annotations (`#nullable enable`); do not suppress warnings with `!` without runtime validation.
- Security: use parameterized queries or EF Core LINQ exclusively; never concatenate user input into raw SQL, LDAP, or system commands.
- Logging & Exceptions: use structured logging message templates (never string interpolation `$"..."`); preserve stack traces with `throw;` (never `throw ex;`).
- Tests: follow existing test framework and fixtures; test observable behavior rather than internal implementation; mock external boundaries only when necessary.
