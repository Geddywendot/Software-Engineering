# Project 3 – Multi‑user Inventory API

**Level:** Intermediate‑Advanced  
**Relevant weeks:** 9 – 12  
**Estimated effort:** 20‑25 hours

## Problem statement
Create a secure, multi‑tenant RESTful API for managing inventory across multiple users/organizations. The API must support authentication, role‑based access, and full CRUD operations on products stored in PostgreSQL.

## Target users
- Warehouse managers and staff needing programmatic access to inventory data.
- Developers learning backend API design, security, and testing.

## Functional requirements
1. **User management** – Register, login, logout (JWT‑based auth).
2. **Roles** – `admin`, `manager`, `viewer` with scoped permissions.
3. **Organizations** – Each user belongs to an organization; data isolation per organisation.
4. **Products** – CRUD endpoints with fields: name, SKU, description, price, quantity, organisation_id.
5. **Input validation** – Pydantic models enforce types and constraints.
6. **Pagination** – List endpoints support `limit`/`offset`.
7. **Automated testing** – Unit and integration tests covering auth, RBAC, and CRUD.

## Non‑functional requirements
- Stateless API using JWT.
- PostgreSQL persistence with SQLAlchemy ORM and Alembic migrations.
- Rate limiting (e.g., 100 requests/min per user).
- Comprehensive OpenAPI spec generated automatically.
- Logging of all request attempts and errors.

## User stories
- *As a manager, I can create a product for my organization so that inventory reflects new stock.*
- *As a viewer, I can list products but cannot modify them.*
- *As an admin, I can add users to my organization and assign roles.*
- *As a client application, I can retrieve a paginated list of products via the API.*

## Acceptance criteria
- All endpoints functional and secured according to role.
- OpenAPI documentation accessible at `/docs`.
- Test suite achieves ≥ 85 % coverage.
- CI pipeline runs lint, type‑check, and tests on each push.
- Documentation includes API contract (OpenAPI JSON) and usage examples.

## Architecture proposal
- **FastAPI** – primary framework.
- **Auth** – OAuth2 password flow with JWT, `fastapi-users` optional.
- **Database** – PostgreSQL in Docker, accessed via SQLAlchemy.
- **Migrations** – Alembic scripts.
- **Service layer** – Separate business logic from route handlers.
- **Dependency injection** – FastAPI `Depends` for DB session and current user.

## Database design (simplified)
```
Organization(id PK, name, created_at)
User(id PK, username UNIQUE, email UNIQUE, password_hash, role, organization_id FK)
Product(id PK, name, sku UNIQUE, description, price NUMERIC, quantity INT, organization_id FK)
```

## API specification (excerpt)
| Method | Path | Auth | Description |
|--------|------|------|-------------|
| POST | `/auth/register` | – | Register a new user |
| POST | `/auth/token` | – | Obtain JWT |
| GET | `/organizations` | JWT (admin) | List organisations |
| POST | `/products` | JWT (admin/manager) | Create product |
| GET | `/products` | JWT (any) | List products (filters: `search`, `org_id` ) |
| PATCH | `/products/{id}` | JWT (admin/manager) | Update product |
| DELETE | `/products/{id}` | JWT (admin) | Delete product |

## Security considerations
- Store passwords with `bcrypt`/`argon2`.
- Validate JWT signature and expiry on each request.
- Enforce organization‑level data isolation in queries.
- Use parameterised ORM queries to prevent SQL injection.
- Rate limiting via `slowapi` or similar middleware.

## Testing plan
- **Unit tests** for services and models (`pytest`).
- **Integration tests** using `httpx.AsyncClient` against a test DB.
- **Security tests**: verify unauthorized access is rejected, role restrictions enforced.
- **Load tests** (optional) with `locust` for endpoint performance.

## Deployment requirements
- Dockerfile for FastAPI app.
- `docker-compose.yml` with `app` and `db` services.
- CI workflow builds Docker image, runs tests, pushes to GHCR.
- Helm chart (optional) for Kubernetes deployment.

## Project milestones
| Milestone | Tasks |
|-----------|-------|
| M1 – Repo & env | Initialise repo, set up virtualenv, create Docker Compose with Postgres |
| M2 – Auth & models | Implement User, Org, Product models, JWT auth flow |
| M3 – CRUD endpoints | Build product routes with RBAC checks |
| M4 – Migrations | Alembic scripts for schema evolution |
| M5 – Testing | Write unit & integration tests, configure CI |
| M6 – Rate limiting & logging | Add middleware, configure structured logs |
| M7 – Documentation | Generate OpenAPI spec, write usage guide |
| M8 – Polish & deployment | CI/CD pipeline, Helm chart, production README |

## Definition of Done
- All acceptance criteria satisfied.
- CI passes all stages.
- Documentation is complete and rendered on GitHub.
- Code follows linting (`ruff`) and type‑checking (`mypy`).
