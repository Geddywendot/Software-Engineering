# Week 15 – Frontend and Backend Integration

## A. Week overview
- **Week number:** 15
- **Week title:** Frontend and Backend Integration
- **Phase:** Month 4 – Frontend and Full‑stack Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Week 14 (TypeScript & Frontend Architecture) completed; FastAPI basics covered in Week 9.

## B. Learning objectives
- Build a full‑stack application connecting a React‑TypeScript frontend to a FastAPI backend.
- Implement RESTful API calls with proper TypeScript typings.
- Manage CORS, authentication tokens, and error handling across the stack.
- Deploy the integrated app locally using Docker Compose.
- Write end‑to‑end tests that span both frontend and backend.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Review of HTTP, status codes, and JSON payloads. |
| 2 | Designing API contracts – OpenAPI spec basics. |
| 3 | Setting up FastAPI project with Pydantic models. |
| 4 | Creating TypeScript interfaces for API responses. |
| 5 | Implementing CRUD endpoints in FastAPI. |
| 6 | Consuming the API from React using `axios` with interceptors. |
| 7 | Handling authentication – JWT issuance in FastAPI, storage in React (HttpOnly cookies). |
| 8 | Error propagation and global error UI components. |
| 9 | Dockerizing FastAPI and React services. |
|10 | Docker Compose orchestration and local networking. |
|11 | Lab: Build a simple *Todo* full‑stack app. |
|12 | Review, documentation, and retrospective.

## D. Learning materials
- **Official docs:**
  - FastAPI: <https://fastapi.tiangolo.com/>
  - React TypeScript: <https://reactjs.org/docs/static-type-checking.html>
  - Docker Compose: <https://docs.docker.com/compose/>
- **Tutorials:**
  - Full‑Stack FastAPI + React tutorial – freeCodeCamp: <https://www.freecodecamp.org/news/build-a-full-stack-web-application-with-fastapi-and-react/>.
- **Videos:**
  - "FastAPI & React – Full Stack Tutorial" – Tech With Tim: <https://www.youtube.com/watch?v=0sYrS9tef8g>.
- **Exercises:**
  - Build a minimal FastAPI CRUD service (FastAPI docs tutorial).
  - Create TypeScript API client (React docs example).

## E. Practical laboratories
### Beginner
1. Write a Pydantic model for a `Note` object and expose a `GET /notes` endpoint.
### Intermediate
2. In React, build a typed service layer that fetches notes and displays them in a list.
### Challenge
3. Add JWT‑based authentication: protect the FastAPI routes and store the token securely in the React app.
### Independent implementation
4. Extend the app with a real‑time feature using WebSockets (`fastapi-socketio` + React hook).

## F. Weekly assignment
**Problem statement:** Create a *Book Review* full‑stack application.
- Backend: FastAPI with PostgreSQL (SQLAlchemy) exposing CRUD for books and reviews.
- Frontend: React‑TypeScript UI to browse books, submit reviews, and view average ratings.
- Use Docker Compose to run both services and a PostgreSQL container.
- Write integration tests with `pytest` (backend) and `cypress` (frontend).

**Acceptance criteria**
- All API endpoints conform to the OpenAPI spec and are type‑checked in the frontend.
- Docker Compose `up` launches a functional app reachable at `http://localhost:3000`.
- Test suite achieves ≥ 80 % coverage.
- Documentation includes API contract (`openapi.json`) and architecture diagram.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (API design) | 15 % |
| Backend implementation (auto‑graded) | 25 % |
| Frontend integration (type safety) | 20 % |
| Docker Compose orchestration | 15 % |
| End‑to‑end testing | 15 % |
| Documentation quality | 10 % |

**Rubric highlights**
- Correct OpenAPI spec (10 pts).
- Proper TypeScript typings for all API calls (10 pts).
- Secure JWT handling (5 pts).
- Docker Compose works without manual tweaks (5 pts).
- Comprehensive test coverage (5 pts).
- Clear architecture diagram (5 pts).

## H. Completion gate
Submit a public GitHub repository URL; CI must pass all tests and Docker build.

## I. Weekly retrospective
1. Which part of the integration caused the most friction?
2. How did type safety improve debugging across the stack?
3. What security considerations emerged when handling tokens?
4. What would you change in your Docker workflow for production?

---
*Next week:* **Week 16 – Full‑stack Application Engineering** (see `syllabus/phase-04/week-16.md`).