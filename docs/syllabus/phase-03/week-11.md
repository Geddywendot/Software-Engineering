# Week 11 – Authentication, Authorisation and Backend Security

## A. Week overview
- **Week number:** 11
- **Week title:** Authentication, Authorisation and Backend Security
- **Phase:** Month 3 – Backend Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Week 10 completed; FastAPI project with database integration.

## B. Learning objectives
- Implement password hashing with `bcrypt`/`passlib`.
- Build OAuth2 password flow with JWT tokens in FastAPI.
- Design role‑based access control (RBAC) using FastAPI `Security` dependencies.
- Apply security best practices: input validation, rate limiting, CORS, HTTPS.
- Use OWASP Top 10 as a checklist for common backend vulnerabilities.
- Perform security testing with tools like `bandit` and `pytest‑security`.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Password hashing – `bcrypt`, salting, `passlib.context.CryptContext`. |
| 2 | OAuth2 password flow – token endpoint, `OAuth2PasswordBearer`. |
| 3 | JWT creation/verification – `pyjwt`, expiration, refresh tokens. |
| 4 | Dependency injection for current user – `Depends(get_current_user)`. |
| 5 | Role‑based access – defining `User` roles, `Security` scopes. |
| 6 | Securing FastAPI – CORS middleware, HTTPS enforcement, security headers. |
| 7 | Rate limiting – using `slowapi` or custom middleware. |
| 8 | Input validation – Pydantic sanitisation, preventing injection attacks. |
| 9 | OWASP Top 10 overview – injection, broken authentication, sensitive data exposure. |
|10 | Static analysis – `bandit`, `safety` for dependencies. |
|11 | Lab day – secure the Todo API with JWT auth and RBAC. |
|12 | Review & documentation – write `SECURITY_OVERVIEW.md` with authentication flow diagram (Mermaid).

## D. Learning materials
- **Official docs**: <https://fastapi.tiangolo.com/tutorial/security/>, <https://pyjwt.readthedocs.io/en/latest/>.
- **Tutorials**:
  - "FastAPI Security – OAuth2 with JWT" – <https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/>.
  - OWASP Top 10 – <https://owasp.org/www-project-top-ten/>.
- **Videos**:
  - "FastAPI Authentication" – Traversy Media – <https://www.youtube.com/watch?v=0sOvCWFmrtA>.
  - "OWASP Top 10 explained" – FreeCodeCamp – <https://www.youtube.com/watch?v=5gZ9Ns8ftQY>.
- **Exercises**:
  - Secure coding challenges on `hackthebox` (auth section) – <https://www.hackthebox.eu/> (free tier).
  - `bandit` scanning on sample code – <https://bandit.readthedocs.io/en/latest/>.

## E. Practical laboratories
### Beginner
1. Implement a password hashing utility function and verify hash matches.
### Intermediate
2. Add an `/auth/token` endpoint to the Todo API that returns a JWT for valid credentials.
### Challenge
3. Protect the `POST /tasks` endpoint so only users with role `admin` can create tasks.
### Independent implementation
4. Write a middleware that limits each IP to 100 requests per hour; test it with `locust` load testing script.

## F. Weekly assignment
**Problem statement**: Secure the *Book Library* API.
- Implement user registration (`/auth/register`) with hashed passwords.
- Add login endpoint (`/auth/login`) returning JWT access and refresh tokens.
- Protect write endpoints (`POST/PUT/DELETE /books`) with role‑based access (`admin`).
- Include rate limiting and security headers.
- Provide a `SECURITY_REPORT.md` documenting threat model, mitigations, and a Mermaid diagram of the auth flow.

**Acceptance criteria**
- All security mechanisms work; unauthorized requests receive 401/403.
- Rate limiting returns 429 after threshold.
- `bandit` scan shows ≤ 2 low‑severity issues.
- Documentation and threat model are complete.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| JWT implementation test (auto‑graded) | 25 % |
| Role‑based endpoint protection functional test | 20 % |
| Rate‑limit and security header verification | 15 % |
| Documentation & threat model quality | 15 % |

**Rubric highlights**
- Correct password hashing and verification (10 pts).
- Secure JWT handling (expiration, secret management) (10 pts).
- Proper RBAC enforcement (5 pts).
- Effective rate limiting (5 pts).
- Thorough security report (5 pts).

## H. Completion gate
Submit the repo URL; CI must pass security scans and achieve ≥ 70 % assessment score.

## I. Weekly retrospective
1. Which security measure was hardest to implement correctly?
2. How did you ensure tokens are stored and transmitted safely?
3. What improvements would you make to your rate‑limiting strategy?
4. Which OWASP risk do you consider most critical for your API?

---
*Next week:* **Week 12 – Testing, Debugging and Backend Quality** (see `syllabus/phase-03/week-12.md`).