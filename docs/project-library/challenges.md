# Critical‑Thinking Engineering Challenges

The following scenarios are deliberately open‑ended.  Learners must analyse the problem, propose a design, identify trade‑offs, and document their solution.  Instructor reference solutions are provided in `reference-solutions/` for grading and guidance.

## 1. Multi‑tenant Data Isolation
- **Problem:** Design a strategy to ensure that data belonging to one organisation cannot be accessed by users of another organisation.
- **Constraints:** Must work with PostgreSQL, support role‑based access, and be enforceable at the database layer.
- **Questions to investigate:**
  - Row‑level security (RLS) vs. application‑level filters?
  - Performance impact of RLS policies.
  - How to handle admin users who need cross‑tenant visibility?

## 2. Concurrent Stock Updates
- **Problem:** Multiple users may update the quantity of the same product simultaneously (e.g., receiving stock while issuing items).
- **Constraints:** Must prevent lost updates and ensure accurate inventory counts.
- **Questions:**
  - Optimistic vs. pessimistic locking?
  - Use of `SELECT … FOR UPDATE`?
  - Impact on API latency.

## 3. Database Transaction Consistency
- **Problem:** A stock transfer involves debiting one warehouse and crediting another. Ensure the operation is atomic.
- **Constraints:** Must survive server crashes and maintain ACID guarantees.
- **Questions:**
  - How to structure the transaction in SQLAlchemy?
  - What isolation level is appropriate?
  - How to handle partial failures (e.g., network loss during commit).

## 4. Audit Trails
- **Problem:** Every change to inventory must be recorded immutably for regulatory compliance.
- **Constraints:** High write volume, ability to query recent changes efficiently.
- **Questions:**
  - Append‑only table vs. event‑sourcing model?
  - Use of `jsonb` for change details.
  - Retention policy and archiving strategy.

## 5. Authentication & Authorisation
- **Problem:** Implement a secure authentication system with role‑based permissions across the platform.
- **Constraints:** Must support JWT access tokens, refresh tokens, and password reset flows.
- **Questions:**
  - Where to store refresh tokens securely?
  - How to invalidate tokens on password change?
  - Scope vs. role claims in JWT.

## 6. API Reliability
- **Problem:** Ensure the API remains responsive under load and gracefully degrades when dependent services fail.
- **Constraints:** Must meet an SLA of 99.9 % uptime.
- **Questions:**
  - Implementing circuit‑breaker pattern?
  - Rate limiting strategy per tenant.
  - Health‑check endpoints and monitoring.

## 7. Database Indexing
- **Problem:** Identify the most critical indexes for the inventory tables to support fast look‑ups.
- **Constraints:** Indexes increase write overhead; need balance.
- **Questions:**
  - Which columns to index (e.g., `sku`, `organization_id`, `warehouse_id`)?
  - Composite vs. single‑column indexes.
  - How to monitor index usage (pg_stat_user_indexes).

## 8. Performance Bottlenecks
- **Problem:** The dashboard experiences latency spikes when loading large inventory tables.
- **Constraints:** Must retain real‑time data freshness.
- **Questions:**
  - Pagination vs. infinite scroll?
  - Caching strategies (Redis, HTTP cache headers).
  - Query optimisation (materialised views, denormalisation).

## 9. Data Backup & Recovery
- **Problem:** Design a backup strategy that supports point‑in‑time recovery for the PostgreSQL database.
- **Constraints:** Limited storage budget, minimal downtime.
- **Questions:**
  - Physical base‑backup + WAL archiving?
  - Cloud‑based automated backups vs. custom scripts.
  - Testing restoration procedures.

## 10. Scaling from One Warehouse to Many
- **Problem:** The system must evolve from a single‑warehouse deployment to supporting hundreds of warehouses across regions.
- **Constraints:** Must not require major schema changes.
- **Questions:**
  - Sharding strategy (by organisation, by geographic region)?
  - Multi‑region deployments and data latency.
  - Impact on API design and query patterns.

---
*Reference solutions* are stored in `docs/project-library/reference-solutions/` for instructors.
