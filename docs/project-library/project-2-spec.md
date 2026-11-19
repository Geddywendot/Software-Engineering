# Project 2 – Inventory Management Application

**Level:** Intermediate  
**Relevant weeks:** 5 – 8  
**Estimated effort:** 15‑20 hours

## Problem statement
Build a web‑based inventory management system that allows a small business to keep track of products, categories, and stock levels. Users can add, edit, delete, search and filter items, with data persisted in a relational database.

## Target users
- Small‑business owners or shop floor staff.
- Learners transitioning from static web pages to dynamic data‑driven applications.

## Functional requirements
1. CRUD for **Products** (name, SKU, description, price, stock quantity).
2. CRUD for **Categories** (name, description) with many‑to‑one relationship to products.
3. Search products by name or SKU.
4. Filter products by category and stock status (in‑stock/out‑of‑stock).
5. Simple authentication (username/password) for admin access.
6. Persist data in PostgreSQL (or SQLite for local dev).

## Non‑functional requirements
- Responsive UI (mobile‑friendly).
- Input validation on client and server.
- Secure password storage (bcrypt).
- Unit tests for server routes (≥ 80 % coverage).

## User stories
- *As a manager, I can add a new product so that it appears in the catalogue.*
- *As a staff member, I can search for a product by SKU to check its stock.*
- *As an admin, I can create categories to organise products.*
- *As a manager, I receive a warning when stock falls below a threshold.*

## Acceptance criteria
- All CRUD operations functional via a clean UI.
- Search and filter work instantly without page reload (AJAX/fetch).
- Authentication protects admin pages.
- Automated tests cover models, routes, and authentication.
- Documentation includes API usage and deployment steps.

## Architecture proposal
- **Frontend:** HTML/CSS + vanilla JavaScript (or minimal framework).
- **Backend:** Python FastAPI serving a REST API.
- **Database:** PostgreSQL (Docker container) accessed via SQLAlchemy ORM.
- **Pattern:** MVC – separate concerns (templates, API controllers, models).

## Database design (simplified)
```
Category(id PK, name, description)
Product(id PK, name, sku UNIQUE, description, price NUMERIC, quantity INT, category_id FK)
User(id PK, username UNIQUE, password_hash)
```

## API specification (excerpt)
| Method | Path | Description |
|--------|------|-------------|
| GET | `/api/categories` | List categories |
| POST | `/api/categories` | Create category |
| GET | `/api/products` | List products (supports `search` and `category` query params) |
| POST | `/api/products` | Create product |
| PUT | `/api/products/{id}` | Update product |
| DELETE | `/api/products/{id}` | Delete product |

## Security considerations
- HTTPS enforced in production.
- JWT for session management.
- CSRF protection for state‑changing requests.
- Parameterised queries via ORM to prevent SQL injection.

## Testing plan
- **Backend:** `pytest` with `httpx` for API tests.
- **Frontend:** Jasmine/Karma or simple Selenium end‑to‑end test for UI flows.
- **Integration:** Docker‑compose test environment with real PostgreSQL.

## Deployment requirements
- Dockerfile for backend, Nginx static serve for frontend.
- `docker-compose.yml` orchestrating `frontend`, `backend`, `db` services.
- CI pipeline builds images, runs tests, pushes to Docker Hub.

## Project milestones
| Milestone | Tasks |
|-----------|-------|
| M1 – Setup repo, env, DB | Initialise project, Docker Postgres, FastAPI skeleton |
| M2 – API models & migrations | Define SQLAlchemy models, Alembic migrations |
| M3 – CRUD endpoints | Implement product/category routes |
| M4 – Frontend UI | Build HTML/CSS layout, fetch API integration |
| M5 – Auth & security | Add login, JWT, protect routes |
| M6 – Search/filter | Implement client‑side search and server filters |
| M7 – Tests & CI | Write unit/integration tests, CI workflow |
| M8 – Documentation & polish | Write README, deployment guide |

## Definition of Done
- All functional & non‑functional requirements met.
- CI passes lint, type‑check, tests.
- Deployment scripts work on a fresh machine.
- Comprehensive documentation is present.
