# Week 23 – Capstone Testing, Security, Docker and Deployment

## A. Week overview
- **Week number:** 23
- **Week title:** Capstone Testing, Security, Docker and Deployment
- **Phase:** Month 6 – Capstone Development and Engineering Evaluation
- **Estimated hours:** 18‑20 h
- **Difficulty:** Advanced
- **Prerequisites:** Week 22 (Core Implementation) completed.

## B. Learning objectives
- Design and execute comprehensive test strategies (unit, integration, end‑to‑end).
- Conduct security testing (static analysis, dependency scanning, penetration testing basics).
- Optimize Docker images for production and implement multi‑stage builds.
- Deploy the application to a cloud platform (Vercel, Render, or AWS Elastic Beanstalk) using CI/CD.
- Implement monitoring, logging, and rollback procedures.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Test pyramid – unit, integration, E2E; selecting tools (`pytest`, `jest`, `cypress`). |
| 2 | Writing property‑based tests with `hypothesis` (Python) and `fast-check` (JS). |
| 3 | Security static analysis – `bandit`, `npm audit`, `snyk`. |
| 4 | Dependency scanning and updating vulnerable packages. |
| 5 | Docker optimisation – multi‑stage, smallest base, healthchecks. |
| 6 | Docker Compose for production – scaling services, resource limits. |
| 7 | CI workflow extensions for security and performance testing. |
| 8 | Deploying to cloud – configuring environment variables, secrets, zero‑downtime rollout. |
| 9 | Monitoring with Prometheus + Grafana; alerting strategies. |
|10 | Lab: Harden and deploy the capstone MVP to a cloud provider via CI. |
|11 | Review of testing reports, security findings, and deployment logs. |
|12 | Retrospective.

## D. Learning materials
- **Official docs:**
  - `pytest`: <https://docs.pytest.org/en/stable/>
  - `cypress`: <https://docs.cypress.io/>
  - Docker best practices: <https://docs.docker.com/develop/develop-images/dockerfile_best-practices/>
- **Tutorials:**
  - "Security Scanning in CI/CD" – OWASP: <https://owasp.org/www-project-secure-coding-practices/>
  - "Deploy FastAPI with Docker to Render" – Render docs: <https://render.com/docs/fastapi>
- **Videos:**
  - "Full‑Stack CI/CD with GitHub Actions" – Fireship: <https://www.youtube.com/watch?v=Q9X5O5VeOPc>
- **Exercises:**
  - Write a `bandit` scan step in GitHub Actions.
  - Create a Cypress test suite that covers the ticket purchase flow.

## E. Practical laboratories
### Beginner
1. Add unit tests for a FastAPI service using `pytest` and `httpx`.
### Intermediate
2. Set up a Cypress end‑to‑end test that simulates a user buying a ticket.
### Challenge
3. Integrate `snyk` scanning into the CI pipeline and fail the build on high‑severity issues.
### Independent implementation
4. Configure automatic rollbacks in GitHub Actions using Docker image tags and healthcheck failures.

## F. Weekly assignment
**Problem statement:** Complete the *Scalable Event‑Ticketing Platform* with full testing, security hardening, production‑grade Docker images, and cloud deployment.
- Deliverables:
  - Full test suite with ≥ 85 % coverage.
  - Security scan reports with no critical findings.
  - Optimised Docker images and `docker-compose.prod.yml`.
  - CI workflow that builds, tests, scans, and deploys to a chosen cloud provider.
  - Monitoring dashboard (Grafana) showing request latency and error rates.
- Acceptance criteria:
  - Deployment succeeds via CI and the live URL is reachable.
  - All tests pass in CI; security scan passes.
  - Documentation includes deployment diagram and rollback procedure.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (testing & security) | 15 % |
| Test suite implementation & coverage | 30 % |
| Security scanning and remediation | 20 % |
| Docker optimisation & production compose | 15 % |
| Cloud deployment automation | 10 % |
| Documentation & monitoring setup | 10 % |

**Rubric highlights**
- Comprehensive test coverage (15 pts).
- No critical vulnerabilities (10 pts).
- Efficient production Docker images (<150 MB) (5 pts).
- Successful automated deployment (5 pts).
- Clear monitoring dashboard (5 pts).

## H. Completion gate
Merge the PR; CI must show successful deployment to the staging environment.

## I. Weekly retrospective
1. Which testing layer gave the most confidence in the system?
2. How did security scanning affect your dependency choices?
3. What issues arose during Docker optimisation?
4. How would you improve the CI/CD rollout for a larger team?

---
*Next week:* **Week 24 – Capstone Evaluation, Documentation and Final Examination** (see `syllabus/phase-06/week-24.md`).