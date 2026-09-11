---
description: "SQL Server (T-SQL) query safety, performance, and naming conventions."
applyTo: "**/*.sql"
---

- Schema & Naming: always include schema prefixes (e.g., `dbo.TableName`); match existing casing conventions.
- Safety: never execute destructive statements (`DELETE`, `UPDATE`, `DROP`) without explicit `WHERE` and transaction guards (`BEGIN TRAN` ... `COMMIT`).
- Performance: avoid `SELECT *`; ensure `WHERE`/`JOIN` predicates are sargable (no function calls on indexed columns); prefix Unicode strings with `N''` to prevent index scans.
- Idempotency: write migration and DDL scripts idempotently (`IF NOT EXISTS(...)`, `IF OBJECT_ID(...) IS NOT NULL`).
