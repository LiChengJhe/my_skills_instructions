---
description: "SQL Server (T-SQL) query safety, performance, and naming conventions."
applyTo: "**/*.sql"
---

- Schema & Naming: always include schema prefixes (e.g., `dbo.TableName`); match existing repository casing and naming conventions.
- Safety: never execute destructive operations (`DELETE`, `UPDATE`, `DROP`, `TRUNCATE`) without explicit `WHERE` clauses and transaction guards (`BEGIN TRAN` ... `COMMIT`).
- Performance: avoid `SELECT *`; specify explicit column lists; ensure predicates in `WHERE` and `JOIN` are sargable (avoid wrapping indexed columns in functions); use `N''` prefix for Unicode literals to prevent implicit conversion and index scans.
- Indexing & Locks: use appropriate indexing for search/join keys; consider non-blocking query hints (e.g. `WITH (NOLOCK)`) only when eventual consistency is acceptable.
- Idempotency: write migration and DDL scripts idempotently (e.g., `IF NOT EXISTS(...)`, `IF OBJECT_ID(...) IS NOT NULL`).
- Security: use parameterized queries or stored procedures; never concatenate user inputs into dynamic SQL (`EXEC(...)` / `sp_executesql`).
