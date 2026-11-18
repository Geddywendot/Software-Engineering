# Week 20 – Application Security, Observability and Reliability

## A. Week overview
- **Week number:** 20
- **Week title:** Application Security, Observability and Reliability
- **Phase:** Month 5 – Professional Software Engineering, Architecture and DevOps
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate‑Advanced
- **Prerequisites:** Week 19 (CI/CD, GitHub Actions and Deployment) completed.

## B. Learning objectives
- Identify common web application vulnerabilities (OWASP Top 10) and mitigate them.
- Implement security headers, CSP, and rate limiting.
- Add logging, tracing, and metrics to both backend and frontend.
- Use Sentry (or alternative) for error monitoring and alerting.
- Design reliability patterns: circuit breaker, retries, health checks.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | OWASP Top 10 overview; threat modeling basics. |
| 2 | Secure coding practices – input validation, output encoding. |
| 3 | Security headers – Helmet, CSP, HSTS. |
| 4 | Authentication hardening – refresh tokens, token rotation. |
| 5 | Implementing rate limiting (express-rate-limit / fastapi-limiter). |
| 6 | Logging strategies – structured JSON logs (loguru, winston). |
| 7 | Monitoring & metrics – Prometheus client for FastAPI, React performance tools. |
| 8 | Error tracking with Sentry (backend & frontend). |
| 9 | Reliability patterns – circuit breaker (pybreaker), retries, health checks. |
|10 | Lab: Harden the *Personal Finance Tracker* app (Week 16) with security and observability features. |
|11 | Review, documentation, and retrospective.

## D. Learning materials
- **Official docs:**
  - OWASP Top 10: <https://owasp.org/www-project-top-ten/>
  - Helmet (Express) / FastAPI security utilities: <https://fastapi.tiangolo.com/tutorial/security/>.
  - Sentry docs: <https://docs.sentry.io/platforms/python/> and <https://docs.sentry.io/platforms/javascript/>.
- **Tutorials:**
  - "Web Application Security" – PortSwigger Web Security Academy (free labs): <https://portswigger.net/web-security>
- **Videos:**
  - "OWASP Top 10 Explained" – LiveOverflow: <https://www.youtube.com/watch?v=1M3dOdLsK6M>
- **Exercises:**
  - Perform a security scan with `bandit` (Python) and `npm audit` (JS).

## E. Practical laboratories
### Beginner
1. Add Helmet middleware to a FastAPI app (via starlette middleware). 
### Intermediate
2. Instrument the backend with Prometheus metrics and expose `/metrics`.
### Challenge
3. Integrate Sentry into both services, capture unhandled exceptions, and set up alerts.
### Independent implementation
4. Implement a circuit breaker around external API calls (e.g., a third‑party payments API).

## F. Weekly assignment
**Problem statement:** Secure and monitor the *Book Review* full‑stack application (Week 15).
- Apply OWASP mitigations: input validation, security headers, rate limiting.
- Add structured logging (JSON) for all services.
- Export Prometheus metrics and configure Grafana dashboard.
- Integrate Sentry for error reporting.
- Write a reliability plan describing health checks and restart policies.

**Acceptance criteria**
- No high‑severity findings in `bandit` and `npm audit` scans.
- Prometheus metrics endpoint available and Grafana dashboard demonstrates key KPIs.
- Sentry receives at least one test error.
- Documentation includes security checklist and observability diagram.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (OWASP, observability) | 15 % |
| Security hardening implementation | 30 % |
| Logging & metrics setup | 20 % |
| Sentry integration & testing | 15 % |
| Documentation & reliability plan | 10 % |
| Peer review feedback | 10 % |

**Rubric highlights**
- Proper security headers (10 pts).
- Comprehensive logging (10 pts).
- Healthy metrics exposure (5 pts).
- Effective Sentry alerts (5 pts).
- Clear reliability documentation (5 pts).

## H. Completion gate
Submit a public repository; CI must include security scan and metrics verification.

## I. Weekly retrospective
1. Which OWASP category was hardest to mitigate?
2. How did observability change your debugging approach?
3. What trade‑offs did you face between security and performance?
4. How would you extend the reliability plan for a larger system?

---
*Next phase:* **Phase 6 – Capstone Development and Engineering Evaluation** (see `syllabus/phase-06/index.md`).