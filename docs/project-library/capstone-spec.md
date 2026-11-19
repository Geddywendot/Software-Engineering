# Capstone – Warehouse and Logistics Operations Management Platform

**Level:** Advanced  
**Relevant weeks:** 21 – 24  
**Estimated effort:** 30‑40 hours

## Problem statement
Design and implement an end‑to‑end web platform that enables organisations to manage warehouses, inventory, shipments, and logistics operations. The system must support multi‑tenant data isolation, complex inventory workflows, reporting, and auditability.

## Target users
- Logistics managers overseeing multiple warehouses.
- Operations teams handling stock transfers and shipments.
- Business analysts generating performance reports.

## Functional modules (high‑level)
1. **User Management** – Registration, authentication (JWT), role‑based access (`admin`, `manager`, `operator`).
2. **Organisation Management** – Each organisation has its own isolated data set.
3. **Warehouse Management** – Create, configure, and view warehouses (location, capacity).
4. **Product Management** – Central catalogue of SKUs, descriptions, units of measure.
5. **Inventory Transactions** – Receipts, issues, adjustments, with audit trail.
6. **Stock Transfers** – Move goods between warehouses, enforce transactional consistency.
7. **Shipment Management** – Create shipments, assign carrier, track status.
8. **Shipment Tracking** – Integration with carrier APIs (mocked) for real‑time updates.
9. **Barcode Generation** – Generate printable barcodes/QR codes for products and pallets.
10. **Reporting** – Inventory levels, turnover, shipment performance, audit logs.
11. **Audit Logs** – Immutable records of all state‑changing actions.
12. **Notifications** – Email/SMS alerts for low stock, transfer failures, shipment milestones.

## Technical requirements
- **Frontend:** React + TypeScript, React Router, Redux Toolkit (or TanStack Query) for state management.
- **Backend:** FastAPI (Python) with Pydantic models, SQLAlchemy ORM, Alembic migrations.
- **Database:** PostgreSQL (Docker) with schema supporting multi‑tenant isolation (tenant_id column on all core tables).
- **Containerisation:** Docker Compose for local dev, Helm chart for Kubernetes (optional).
- **CI/CD:** GitHub Actions pipeline that lints, type‑checks, runs unit/integration tests, builds images, and deploys to a staging environment.
- **Observability:** Prometheus metrics, Grafana dashboards, structured logging (Loguru).
- **Security:** OWASP‑based hardening, CSP, HSTS, rate limiting, secret management via GitHub secrets.

## Non‑functional requirements
- High availability (rolling updates, health checks).
- Data consistency – all inventory mutations performed within ACID transactions.
- Scalability – support adding new warehouses without code changes.
- Performance – API response < 200 ms for typical queries under load.
- Documentation – comprehensive README, API spec (OpenAPI), architecture diagram (Mermaid), deployment guide.

## User stories (sample)
- *As an admin, I can create a new organisation and assign a manager.*
- *As a manager, I can view real‑time stock levels across all my warehouses.*
- *As an operator, I can record a receipt of 500 units of SKU 12345 into Warehouse A.*
- *As a logistics coordinator, I can generate a shipment, attach a carrier, and track its progress.*
- *As an auditor, I can query the immutable log of every inventory change.*

## Acceptance criteria
- All modules functional and integrated.
- Multi‑tenant isolation enforced at the database query level.
- End‑to‑end tests (Cypress) cover major user flows.
- CI pipeline passes all stages on `main`.
- Deployment scripts provision the stack on a cloud VM or Kubernetes cluster.
- Documentation includes architecture diagram, API contract, and runbooks.

## Architecture proposal
- **Frontend** compiled with Vite, served via Nginx.
- **Backend** runs under Uvicorn/Gunicorn, exposing OpenAPI and Prometheus endpoints.
- **Gateway** – optional API gateway (e.g., Traefik) for routing and TLS termination.
- **Database** – single PostgreSQL instance with row‑level security policies for tenant isolation.
- **Observability stack** – Prometheus ⇒ Grafana, Loki for logs.

## Database design (core tables)
```
Organization(id PK, name, created_at)
User(id PK, username, email, password_hash, role, organization_id FK)
Warehouse(id PK, name, location, capacity, organization_id FK)
Product(id PK, sku UNIQUE, name, description, uom, organization_id FK)
InventoryTransaction(id PK, product_id FK, warehouse_id FK, quantity INT, type ENUM('receipt','issue','adjustment','transfer'), timestamp, performed_by FK)
StockTransfer(id PK, source_warehouse_id FK, dest_warehouse_id FK, product_id FK, quantity INT, status ENUM('pending','in_progress','completed','failed'), created_at, completed_at)
Shipment(id PK, reference, carrier, status, origin_warehouse_id FK, destination_address, created_at, delivered_at)
AuditLog(id PK, user_id FK, action, table_name, record_id, timestamp, details JSONB)
Notification(id PK, user_id FK, channel ENUM('email','sms'), message, sent_at)
```

## API specification (high‑level excerpt)
| Method | Path | Auth | Description |
|--------|------|------|-------------|
| POST | `/api/v1/auth/register` | – | Register new user |
| POST | `/api/v1/auth/token` | – | Obtain JWT |
| GET | `/api/v1/warehouses` | JWT | List warehouses for current organisation |
| POST | `/api/v1/inventory/transactions` | JWT (manager/operator) | Record inventory movement |
| POST | `/api/v1/stock-transfers` | JWT (manager) | Initiate transfer between warehouses |
| GET | `/api/v1/shipments/{id}` | JWT | Retrieve shipment details |
| GET | `/api/v1/reports/inventory` | JWT (admin/manager) | Generate CSV/Excel report |

## Security considerations
- Row‑level security policies in PostgreSQL to restrict data by `organization_id`.
- JWT with short‑lived access tokens and refresh tokens stored httpOnly.
- Input validation via Pydantic; escape output on the frontend.
- Rate limiting per tenant.
- Dependency scanning and container image vulnerability checks.

## Testing plan
- **Unit tests** for services and models (`pytest`).
- **Integration tests** with a test Postgres container (`testcontainers`).
- **E2E tests** using Cypress covering registration, login, inventory transactions, transfers, and reporting.
- **Security tests**: verify RBAC enforcement, test for SQL injection attempts.

## Deployment requirements
- Docker Compose files for dev (`docker-compose.dev.yml`) and prod (`docker-compose.prod.yml`).
- GitHub Actions workflow that builds images, runs tests, pushes to GHCR, and deploys to staging via SSH or Fly.io.
- Helm chart for Kubernetes (optional). 
- Helm values allow overriding secrets from GitHub Actions.

## Project milestones
| Milestone | Tasks |
|-----------|-------|
| M1 – Initialise repo & infra | Create monorepo, Docker Compose, CI skeleton |
| M2 – Core backend models & auth | Implement multi‑tenant auth, basic CRUD |
| M3 – Frontend scaffolding | Set up React‑TS project, routing, auth flow |
| M4 – Warehouse & product modules | API endpoints, UI components |
| M5 – Inventory transactions | ACID transaction handling, audit logging |
| M6 – Stock transfers & shipments | Complex workflows, external carrier mock |
| M7 – Reporting & barcode generation | CSV export, barcode/QR generation library |
| M8 – Observability & security | Prometheus, Loki, security headers, scanning |
| M9 – CI/CD & deployment | Full pipeline, staging deployment, rollback |
| M10 – Documentation & final polish | Architecture diagram, runbooks, user guide |

## Definition of Done
- All functional modules implemented and integrated.
- CI pipeline passes all checks on `main`.
- Deployment to a staging environment is successful and documented.
- Tests achieve ≥ 85 % coverage across backend and frontend.
- Comprehensive documentation (README, API spec, architecture diagram, runbooks) is present.
- Project is ready for evaluation in weeks 21‑24.
