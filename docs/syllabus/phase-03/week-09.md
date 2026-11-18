# Week 09 – Backend Engineering and FastAPI

## A. Week overview
- **Week number:** 9
- **Week title:** Backend Engineering and FastAPI
- **Phase:** Month 3 – Backend Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Weeks 01‑08 completed; comfortable with Python and PostgreSQL.

## B. Learning objectives
- Build a RESTful API using FastAPI.
- Define request/response models with Pydantic.
- Perform input validation and automatic documentation (OpenAPI/Swagger).
- Implement dependency injection for database sessions.
- Secure endpoints with JWT authentication.
- Write async endpoints and understand ASGI.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | FastAPI overview, installation, project structure. |
| 2 | Path operations – `@app.get`, `@app.post`, path parameters, query parameters. |
| 3 | Pydantic models – data validation, serialization, nested models. |
| 4 | Automatic docs – OpenAPI schema, Swagger UI, ReDoc. |
| 5 | Async support – `async def`, `await`, using `httpx` for external calls. |
| 6 | Dependency injection – `Depends`, database session provider. |
| 7 | Database integration – using `SQLModel` (or `SQLAlchemy`) with PostgreSQL. |
| 8 | Authentication – OAuth2 password flow, JWT creation/verification. |
| 9 | Authorization – role‑based access control, `Security` dependencies. |
|10 | Error handling – custom exception handlers, validation errors. |
|11 | Testing – `TestClient`, fixture setup, integration tests. |
|12 | Lab day – build a small Todo API with CRUD, auth, and PostgreSQL persistence. |
|13 | Review & documentation – write `FASTAPI_OVERVIEW.md` with request/response diagrams (Mermaid). 

## D. Learning materials
- **Official docs**: <https://fastapi.tiangolo.com/>.
- **Tutorials**:
  - "FastAPI Tutorial – Full Course" – freeCodeCamp – <https://www.youtube.com/watch?v=0sOvCWFmrtA>.
  - Real Python – FastAPI Basics – <https://realpython.com/fastapi-python-web-apis/>.
- **Videos**:
  - "FastAPI Crash Course" – Traversy Media – <https://www.youtube.com/watch?v=7t2alSnE2-I>.
- **Exercises**:
  - FastAPI official tutorial exercises – <https://fastapi.tiangolo.com/tutorial/>.
  - TestDriven.io FastAPI projects – free sections – <https://testdriven.io/blog/fastapi-crud/>.

## E. Practical laboratories
### Beginner
1. Create a simple FastAPI app that returns "Hello, FastAPI!" at `/`.
### Intermediate
2. Add a `/items/{item_id}` GET endpoint returning a Pydantic model with validation.
### Challenge
3. Implement a JWT‑protected `/users/me` endpoint that returns the authenticated user profile.
### Independent implementation
4. Build a full Todo API with async CRUD operations, PostgreSQL storage (using `SQLModel`), and unit‑tests with `pytest` and `httpx.AsyncClient`.

## F. Weekly assignment
**Problem statement**: Develop a *Book Library* API.
- Endpoints: `GET /books`, `POST /books`, `GET /books/{id}`, `PUT /books/{id}`, `DELETE /books/{id}`.
- Each book has `id`, `title`, `author`, `published_year`, `isbn`.
- Use PostgreSQL for persistence and Pydantic for schema validation.
- Secure write operations (`POST`, `PUT`, `DELETE`) with JWT auth.
- Provide OpenAPI documentation and a `README.md` with usage examples.

**Acceptance criteria**
- All endpoints function as specified and return appropriate status codes.
- Authentication is required for mutating endpoints.
- Test suite achieves ≥ 80 % coverage.
- Documentation includes a Mermaid sequence diagram of a typical request/response flow.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| FastAPI coding task – CRUD API (auto‑graded) | 30 % |
| JWT authentication implementation test | 20 % |
| Documentation & diagram quality | 15 % |
| Peer review (optional) | 10 % |
| Test coverage report | 10 % |

**Rubric highlights**
- Correct FastAPI routing and async usage (10 pts).
- Proper Pydantic validation and response models (5 pts).
- Secure JWT implementation (5 pts).
- Comprehensive test suite (5 pts).
- Clear OpenAPI docs and Mermaid diagram (5 pts).

## H. Completion gate
Push the repository, open a PR, and obtain an assessment score ≥ 70 %.

## I. Weekly retrospective
1. Which FastAPI feature (dependency injection, async, docs) was most valuable?
2. What challenges did you face when integrating PostgreSQL?
3. How did JWT handling affect your API design?
4. What would you improve in your testing strategy for async endpoints?

---
*Next week:* **Week 10 – Database Integration, ORM and Migrations** (see `syllabus/phase-03/week-10.md`).