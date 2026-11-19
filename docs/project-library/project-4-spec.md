# Project 4 – Full‑stack Business Operations Platform

**Level:** Advanced  
**Relevant weeks:** 13 – 16  
**Estimated effort:** 25‑30 hours

## Problem statement
Develop a comprehensive web application that enables businesses to manage operations: user authentication, inventory oversight, dashboards, and reporting. The frontend will be built with React + TypeScript; the backend with FastAPI + PostgreSQL.

## Target users
- Small‑to‑medium enterprises needing a unified operations dashboard.
- Learners ready to integrate frontend and backend services.

## Functional requirements
1. **User auth** – Register, login, password reset (JWT + refresh tokens).
2. **Dashboard** – Overview cards for inventory levels, recent transactions, alerts.
3. **Inventory UI** – CRUD for products & categories, searchable table, pagination.
4. **Reporting** – Generate CSV/PDF reports of inventory movements.
5. **Role‑based UI** – `admin` sees all pages, `manager` limited to inventory, `viewer` read‑only.
6. **Responsive design** – Works on desktop and tablets.

## Non‑functional requirements
- Type‑safe codebase (TypeScript + Pydantic).
- API versioning (e.g., `/api/v1`).
- Client‑side form validation.
- Unit tests (Jest + React Testing Library) and API tests (`pytest`).
- CI pipeline builds, tests, and produces Docker images.

## User stories (excerpt)
- *As an admin, I can manage user accounts and assign roles.*
- *As a manager, I can view real‑time inventory levels on the dashboard.*
- *As a viewer, I can export a monthly inventory report.*
- *As a developer, I want the frontend to consume a typed OpenAPI client.*

## Acceptance criteria
- All functional requirements implemented.
- End‑to‑end flow works: login → dashboard → inventory CRUD → report download.
- Tests achieve ≥ 80 % coverage for both frontend and backend.
- Documentation includes API spec, component diagram, and deployment guide.

## Architecture proposal
- **Frontend:** React (CRA or Vite) + TypeScript, React Router, Redux Toolkit (or Context) for state.
- **Backend:** FastAPI, Pydantic models, SQLAlchemy ORM, Alembic migrations.
- **API contract:** Generated OpenAPI JSON, consumed by a TypeScript client (`openapi-generator-cli`).
- **Deployment:** Docker Compose with `frontend`, `backend`, `db` services.
- **Pattern:** Separate concerns – UI, API client, service layer.

## Database design (simplified)
```
User(id PK, username, email, password_hash, role, created_at)
Product(id PK, name, sku, description, price, quantity, category_id FK)
Category(id PK, name, description)
InventoryLog(id PK, product_id FK, change INT, timestamp, user_id FK)
```

## API specification (excerpt)
| Method | Path | Auth | Description |
|--------|------|------|-------------|
| POST | `/api/v1/auth/register` | – | Register new user |
| POST | `/api/v1/auth/token` | – | Obtain JWT |
| GET | `/api/v1/dashboard` | JWT | Summary data for dashboard |
| GET | `/api/v1/products` | JWT | List products (supports pagination, filters) |
| POST | `/api/v1/products` | JWT (admin/manager) | Create product |
| GET | `/api/v1/reports/inventory` | JWT | Generate CSV report |

## Security considerations
- Enforce HTTPS in production.
- Use `httpOnly` cookies for refresh tokens or store JWT securely.
- Validate all inputs server‑side; escape output in React.
- Role checks on every endpoint.

## Testing plan
- **Frontend:** Jest unit tests for components, React Testing Library for integration, Cypress for E2E flows.
- **Backend:** `pytest` with `httpx` for API tests, coverage ≥ 80 %.
- **CI:** Run both test suites on each push.

## Deployment requirements
- Dockerfiles for frontend (`node:18-alpine`) and backend (`python:3.11-slim`).
- `docker-compose.yml` orchestrating services.
- CI workflow builds images, pushes to GHCR, and optionally deploys to a staging environment.

## Project milestones
| Milestone | Tasks |
|-----------|-------|
| M1 – Scaffold | Initialise monorepo, set up Docker, create FastAPI starter and React app. |
| M2 – Auth backend | Implement JWT auth, user model, registration/login endpoints. |
| M3 – Frontend auth flow | Build login/register pages, token handling. |
| M4 – Dashboard API & UI | Backend summary endpoint, React dashboard components. |
| M5 – Inventory CRUD | Backend routes, React tables/forms, pagination. |
| M6 – Reporting | CSV export endpoint, download button in UI. |
| M7 – RBAC & security | Role checks, secure cookie handling, CSP headers. |
| M8 – Testing & CI | Write unit/E2E tests, CI pipeline configuration. |
| M9 – Documentation & polish | Architecture diagram, OpenAPI spec, deployment guide. |

## Definition of Done
- All acceptance criteria satisfied.
- CI pipeline passes all checks.
- Documentation is complete and renders.
- Code adheres to linting (`eslint`, `ruff`) and type‑checking (`mypy`, `tsc`).
