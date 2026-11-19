# Project 5 – Production Engineering Upgrade

**Level:** Advanced  
**Relevant weeks:** 17 – 20  
**Estimated effort:** 25‑30 hours

## Problem statement
Upgrade the **Full‑stack Business Operations Platform** (Project 4) to a production‑grade system. Introduce containerisation, continuous integration/deployment, security hardening, logging, monitoring, and automated deployment to a cloud platform.

## Target users
- DevOps engineers and senior developers preparing an application for real‑world release.
- Learners who have built a full‑stack app and now need to make it robust, observable, and maintainable.

## Functional requirements (upgrade tasks)
1. **Dockerisation** – Write multi‑stage Dockerfiles for frontend and backend; create a `docker-compose.yml` that defines `frontend`, `backend`, `db`, and a reverse‑proxy (Caddy or Nginx).
2. **CI/CD** – Configure GitHub Actions to lint, test, build Docker images, push to GitHub Container Registry, and deploy to a staging environment.
3. **Security improvements** –
   - Enforce HTTPS with self‑signed certificates (dev) or Let’s Encrypt (prod).
   - Add HTTP security headers via middleware (Helmet/CSP).
   - Scan dependencies with `snyk` or `trivy` and fail builds on high severity findings.
4. **Logging** – Structured JSON logging for backend (`loguru`) and frontend (browser console to remote via Loki or similar).
5. **Monitoring** – Export Prometheus metrics from FastAPI (`prometheus_fastapi_instrumentator`) and expose a Grafana dashboard.
6. **Deployment** – Deploy the stack to a cloud provider (Render, Fly.io, or Vercel’s Serverless containers). Include environment‑specific configuration via Docker secrets or GitHub Actions secrets.
7. **Rollback strategy** – Implement versioned Docker tags and a CI step that rolls back on health‑check failure.

## Non‑functional requirements
- Zero‑downtime deployments using rolling updates.
- Automated tests must pass before any deployment.
- Logs retained for at least 30 days.
- Monitoring alerts for high error rates (> 5 %).
- Documentation must cover the entire CI/CD pipeline and operational runbooks.

## User stories
- *As a devops engineer, I can push a commit and have the CI pipeline automatically build, test, and deploy the app.*
- *As an admin, I receive an alert if a new image contains critical vulnerabilities.*
- *As a developer, I can view live metrics (request latency, error rate) in Grafana.*
- *As an operator, I can rollback to the previous Docker image with a single CI job.*

## Acceptance criteria
- Docker images build locally without errors.
- CI workflow runs on every PR and on `main` pushes, executing lint, tests, security scans, and deployment.
- Application is reachable over HTTPS, with security headers present.
- Structured logs appear in a central log store (e.g., Loki, CloudWatch).
- Prometheus metrics are scraped and visualised in Grafana.
- Rollback mechanism works when a health check fails.
- All documentation (setup, CI, deployment, runbooks) is complete.

## Architecture proposal
- **Frontend Dockerfile** – Node build stage → Nginx serve stage.
- **Backend Dockerfile** – Python build stage (pip install) → Uvicorn/Gunicorn with `uvicorn-gunicorn-fastapi` base.
- **Reverse proxy** – Caddy (auto‑HTTPS) or Nginx handling TLS termination and routing.
- **Orchestration** – Docker Compose for local dev; CI deploys to Fly.io (Docker) or Render (services).
- **Observability stack** – Prometheus (metrics) → Grafana (dashboards), Loki (logs).
- **Security scanning** – Trivy scan step in CI, fail on CRITICAL.

## Database design
No schema changes; migrations from Project 4 are applied via Alembic during container start‑up.

## API specification (no new endpoints, but extensions)
- `/health` – Liveness/readiness probe (returns 200 if DB reachable).
- `/metrics` – Prometheus metrics endpoint.
- `/admin/logs` – Secure endpoint to query recent logs (admin role only).

## Security considerations
- Store secrets (JWT secret, DB password) in Docker secrets / GitHub Actions secrets.
- Enforce `Content‑Security‑Policy` and `Strict‑Transport‑Security` headers.
- Use `OWASP Dependency‑Check` for third‑party libraries.
- Run containers as non‑root users.

## Testing plan
- Extend existing unit and integration tests to cover new security and observability features.
- Add end‑to‑end tests that verify the deployed stack responds over HTTPS.
- CI includes a stage that runs a health‑check script against the staging URL.

## Deployment requirements
- GitHub Actions workflow (`.github/workflows/ci-cd.yml`) with jobs: `lint`, `test`, `security-scan`, `build-push`, `deploy`.
- Docker Compose file for local development (`docker-compose.dev.yml`).
- Production Compose (`docker-compose.prod.yml`) with secret mounts.
- Helm chart optional for Kubernetes.

## Project milestones
| Milestone | Tasks |
|-----------|-------|
| M1 – Containerise app | Write Dockerfiles, test `docker compose up` locally |
| M2 – CI pipeline skeleton | Lint, test, build steps in GitHub Actions |
| M3 – Security hardening | Add headers, HTTPS, Trivy scan |
| M4 – Logging & monitoring | Integrate Loguru, Prometheus, Grafana dashboards |
| M5 – Deployment automation | Configure Fly.io / Render deployment steps |
| M6 – Rollback & health checks | Implement health endpoint, rollback job |
| M7 – Full CI/CD run | Run full pipeline on a feature branch, verify deployment |
| M8 – Documentation & runbooks | Write operational docs, incident response guide |

## Definition of Done
- All upgrade tasks completed.
- CI pipeline passes on every push.
- Production‑grade deployment works and is documented.
- Monitoring and logging are observable.
- Security scans report no critical issues.
