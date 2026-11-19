# Phase 03 – Backend Engineering & API Development

Welcome to **Phase 03** of the Software Engineering Academy. This phase focuses on designing, architecting, and securing production-grade backend web services using Python, FastAPI, relational object-relational mappers (ORMs), automated database migrations, and robust authentication mechanisms.

---

## Phase Overview

- **Duration:** Weeks 9 – 11 (approx. 18–20 hours/week)
- **Core Focus:** Asynchronous Server Gateway Interface (ASGI), FastAPI application architecture, Pydantic schema validation, SQLModel/SQLAlchemy ORM integration, Alembic schema migrations, OAuth2 password flow, JWT authentication, and role-based access control (RBAC).
- **Milestone Project:** [Project 3 – Multi-user Inventory API](../../project-library/project-3-spec.md)
- **Phase Completion Gate:** Phase 3 Evaluation & Code Review (see [Phase Gates](../../assessment-collaboration/phase-gates.md))

---

## Weekly Breakdown

| Week | Title | Core Topics | Deliverables |
|:----:|:------|:------------|:-------------|
| **[09](week-09.md)** | **[Backend Engineering and FastAPI](week-09.md)** | ASGI architecture, FastAPI path operations, Pydantic request/response schemas, dependency injection, automatic OpenAPI/Swagger docs | Book Library RESTful API with validated CRUD endpoints, Pydantic models, and interactive API documentation |
| **[10](week-10.md)** | **[Database Integration, ORM and Migrations](week-10.md)** | SQLModel & SQLAlchemy ORM, relational mapping (one-to-many, many-to-many), session lifecycle, schema versioning with Alembic | Extended Book Library API with relational ORM entities, automated Alembic migration scripts, and migration test suite |
| **[11](week-11.md)** | **[Authentication, Authorisation and Backend Security](week-11.md)** | Password hashing (`bcrypt`), OAuth2 password bearer flow, JWT token creation & verification, RBAC scopes, OWASP mitigations | Production-hardened Book Library API with JWT auth, role-gated endpoints (`admin`), rate limiting, and `SECURITY_REPORT.md` |

---

## Learning Objectives

By the end of Phase 03, learners will be able to:

1. **Construct High-Performance REST APIs with FastAPI:**
   Architect modular backend services leveraging ASGI asynchronous execution, FastAPI routers, path/query parameters, and dependency injection systems.
2. **Enforce Type-Safe Data Contracts with Pydantic:**
   Define rigorous request and response schemas, validate incoming payloads, eliminate injection vectors, and auto-generate comprehensive OpenAPI documentation.
3. **Master Database Object-Relational Mapping (ORM):**
   Model complex relational domain entities and relationships using SQLModel and SQLAlchemy, optimizing query performance and managing session contexts cleanly.
4. **Automate Database Schema Evolution:**
   Manage production database schema changes using Alembic migrations, tracking revision trees and validating upgrade/downgrade rollbacks.
5. **Implement Industry-Standard Authentication & RBAC:**
   Secure backend endpoints with cryptographically secure password hashing (`bcrypt`), JWT token lifecycles (access and refresh tokens), and granular role-based permissions.

---

## Phase Milestone Project

Throughout Weeks 9–11, learners implement **[Project 3 – Multi-user Inventory API](../../project-library/project-3-spec.md)**.

- **Objective:** Create a secure, multi-tenant RESTful API for managing inventory across multiple organizations, featuring authentication, role-based access control, and full CRUD operations on PostgreSQL.
- **Key Constraints:**
  - Multi-tenant architecture ensuring strict data isolation per organization.
  - JWT authentication with secure password hashing and role scopes (`admin`, `manager`, `viewer`).
  - Full request validation and serialization using Pydantic models.
  - Relational persistence with SQLModel/SQLAlchemy and versioned Alembic migrations.
  - Comprehensive automated test coverage using `pytest` and FastAPI `TestClient`.

---

## Phase Gate & Assessment

Advancement to **Phase 04 (Frontend & Full-Stack Engineering)** requires clearing the Phase 03 completion criteria:

1. **Submission of all 3 weekly laboratory assignments** and weekly journal reflections.
2. **Delivery of Project 3** satisfying all acceptance criteria and peer review.
3. **Passing the Phase 03 Gate Examination** (≥ 70% threshold):
   - Conceptual assessment covering ASGI architecture, ORM query mechanics, token-based authentication, and API security.
   - Live coding demonstration and technical defense of your Project 3 API design and schema migration strategy.

For full rubric definitions and gate schedules, see [Phase Completion Gates](../../assessment-collaboration/phase-gates.md) and [Assessment Framework](../../assessment-collaboration/assessment-framework.md).
