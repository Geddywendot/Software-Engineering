# Week 22 – Capstone Core Implementation

## A. Week overview
- **Week number:** 22
- **Week title:** Capstone Core Implementation
- **Phase:** Month 6 – Capstone Development and Engineering Evaluation
- **Estimated hours:** 18‑20 h
- **Difficulty:** Advanced
- **Prerequisites:** Week 21 (Requirements Engineering and System Design) completed.

## B. Learning objectives
- Translate the design artefacts into a working codebase.
- Set up project scaffolding, CI pipeline, and Docker configuration.
- Implement core features iteratively with test‑driven development.
- Apply domain‑driven design and clean architecture principles.
- Conduct regular code reviews and refactoring.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Project bootstrapping – repository layout, monorepo vs polyrepo decision. |
| 2 | Setting up CI pipeline (lint, test, build) – reuse week‑19 workflow. |
| 3 | Implementing authentication & authorization core services. |
| 4 | Building the data access layer – repository pattern with PostgreSQL. |
| 5 | Implementing key business use‑cases (e.g., ticket purchase flow). |
| 6 | Frontend scaffolding – React‑TypeScript with routing and state management. |
| 7 | Integrating frontend with backend APIs using typed service layer. |
| 8 | Writing unit and integration tests for both tiers. |
| 9 | Refactoring session – applying SOLID and design patterns (week‑17). |
|10 | Lab: Deliver a minimally viable product (MVP) covering end‑to‑end ticket purchase. |
|11 | Review of code quality, test coverage, and CI results. |
|12 | Retrospective and planning for next phase.

## D. Learning materials
- **Official docs:** FastAPI, React, Docker, GitHub Actions.
- **Tutorials:** "Building a Full‑Stack App with FastAPI and React" – DigitalOcean (link from week‑16). 
- **Videos:** "TDD in Full‑Stack Development" – Traversy Media: <https://www.youtube.com/watch?v=K6MfpKbm2xk>.
- **Exercises:** Write tests before implementing each feature (test‑first).

## E. Practical laboratories
### Beginner
1. Scaffold the repo with a `backend/` and `frontend/` folder, add basic FastAPI and React starter apps.
### Intermediate
2. Implement the ticket purchase endpoint with proper validation and unit tests.
### Challenge
3. Add optimistic UI updates on the frontend with proper TypeScript typings.
### Independent implementation
4. Set up a CI workflow that runs `pytest`, `npm test`, builds Docker images, and pushes to GHCR.

## F. Weekly assignment
**Problem statement:** Deliver the MVP of the *Scalable Event‑Ticketing Platform*.
- Backend: FastAPI with PostgreSQL, exposing endpoints for events, tickets, orders.
- Frontend: React‑TypeScript UI to browse events and purchase tickets.
- CI/CD: Automated pipeline from week‑19.
- Dockerised deployment via Docker Compose.

**Acceptance criteria**
- End‑to‑end flow works: user can view events, select tickets, place an order, and see confirmation.
- All unit/integration tests pass with ≥ 80 % coverage.
- CI pipeline succeeds on every push.
- Documentation includes setup guide and architecture diagram.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (architecture, TDD) | 15 % |
| Backend core implementation | 30 % |
| Frontend integration | 20 % |
| CI pipeline completeness | 15 % |
| Test coverage & quality | 10 % |
| Documentation | 10 % |

## H. Completion gate
Push the repository; CI must pass all stages and Docker images build.

## I. Weekly retrospective
1. Which feature was most challenging to implement and why?
2. How did TDD affect your development speed and confidence?
3. What bottlenecks appeared in the CI pipeline?
4. How would you improve the MVP for production readiness?

---
*Next week:* **Week 23 – Capstone Testing, Security, Docker and Deployment** (see `syllabus/phase-06/week-23.md`).