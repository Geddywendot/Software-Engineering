# Week 16 – Full‑stack Application Engineering

## A. Week overview
- **Week number:** 16
- **Week title:** Full‑stack Application Engineering
- **Phase:** Month 4 – Frontend and Full‑stack Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate‑Advanced
- **Prerequisites:** Week 15 (Frontend & Backend Integration) completed.

## B. Learning objectives
- Design and implement a production‑ready full‑stack app using React‑TypeScript and FastAPI.
- Apply CI/CD pipelines for automated testing and container deployment.
- Implement environment‑specific configuration (dev, staging, prod).
- Introduce logging, monitoring, and error tracking across the stack.
- Conduct performance profiling and optimisation.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Project planning – feature backlog, service diagram, data model. |
| 2 | Setting up monorepo with Yarn workspaces (frontend & backend). |
| 3 | Refactoring codebase for scalability – module boundaries, services layer. |
| 4 | Implementing CI with GitHub Actions – lint, test, build Docker images. |
| 5 | Secrets management – `.env` files, GitHub Secrets, `python‑dotenv`. |
| 6 | Logging strategies – `loguru` (backend) and `winston` (frontend). |
| 7 | Monitoring – Prometheus metrics exporter in FastAPI, React performance profiling. |
| 8 | Error tracking – Sentry integration for both services. |
| 9 | Performance optimisation – code‑splitting, lazy loading, async endpoints. |
|10 | Security hardening – CSP, Helmet, HTTPS, JWT refresh flow. |
|11 | Lab: Extend the Todo app from Week 15 with user authentication, persistent DB, and CI pipeline. |
|12 | Review, documentation, and retrospective.

## D. Learning materials
- **Official docs:**
  - FastAPI Security: <https://fastapi.tiangolo.com/security/>
  - React Docs – Optimizing Performance: <https://reactjs.org/docs/optimizing-performance.html>
  - GitHub Actions: <https://docs.github.com/en/actions>
- **Tutorials:**
  - "Building a Full‑Stack App with React, FastAPI and Docker" – DigitalOcean Community: <https://www.digitalocean.com/community/tutorials/building-a-full-stack-app-with-react-fastapi-and-docker>
- **Videos:**
  - "CI/CD for Full‑Stack Apps" – Traversy Media: <https://www.youtube.com/watch?v=9CiX87drfYo>
- **Exercises:**
  - Implement a CI workflow that lints, tests, builds, and pushes Docker images to Docker Hub.

## E. Practical laboratories
### Beginner
1. Add `flake8` linting to the FastAPI backend and `eslint` to the React frontend.
### Intermediate
2. Create a GitHub Actions workflow that runs unit tests and builds multi‑arch Docker images.
### Challenge
3. Implement real‑time updates using FastAPI WebSockets and a React hook, with proper type safety.
### Independent implementation
4. Configure Prometheus scraping for the FastAPI service and visualise metrics with Grafana (local Docker compose).

## F. Weekly assignment
**Problem statement:** Build a *Personal Finance Tracker* full‑stack application.
- Backend: FastAPI with PostgreSQL, providing endpoints for accounts, transactions, and reports.
- Frontend: React‑TypeScript dashboard with charts (Chart.js) for spending analysis.
- CI/CD: GitHub Actions pipeline that lints, tests, builds Docker images, and pushes to a registry.
- Monitoring: Integrate Sentry and expose `/metrics` endpoint for Prometheus.

**Acceptance criteria**
- Application deploys via `docker compose up` with three containers (frontend, backend, db).
- All tests pass (`pytest` ≥ 80 % coverage, React tests ≥ 80 %).
- CI pipeline runs on each push and reports status.
- Documentation includes architecture diagram (Mermaid) and deployment guide.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (architecture) | 15 % |
| Backend implementation & security | 25 % |
| Frontend integration & performance | 20 % |
| CI/CD pipeline correctness | 15 % |
| Monitoring & logging setup | 15 % |
| Documentation & diagram quality | 10 % |

**Rubric highlights**
- Secure auth flow (10 pts).
- Correct CI workflow (10 pts).
- Effective monitoring (5 pts).
- Clean codebase separation (5 pts).
- Comprehensive docs (5 pts).

## H. Completion gate
Push the repository to GitHub; CI must succeed and Docker images build without errors.

## I. Weekly retrospective
1. Which CI step was most problematic and why?
2. How did monitoring influence your debugging process?
3. What performance bottlenecks did you encounter in the frontend?
4. How would you improve the deployment strategy for production?

---
*Next phase:* **Phase 5 – Professional Software Engineering, Architecture and DevOps** (see `syllabus/phase-05/index.md`).