# Phase 05 – Professional Software Engineering, Architecture & DevOps

Welcome to **Phase 05** of the Software Engineering Academy. This four-week phase elevates software engineering from functional code to enterprise-grade systems engineering: clean architecture patterns, production containerization, automated CI/CD pipelines, application security hardening, observability, and cloud deployment.

---

## Phase Overview

- **Duration:** Weeks 17 – 20 (approx. 18–20 hours/week)
- **Core Focus:** SOLID design principles at system scale, Clean Architecture / Hexagonal patterns, GoF design patterns, multi-stage Docker builds, GitHub Actions CI/CD automation, cloud deployment, OWASP Top 10 hardening, structured logging, Prometheus metrics, and Sentry monitoring.
- **Milestone Project:** [Project 5 – Production Engineering Upgrade](../../project-library/project-5-spec.md)
- **Phase Completion Gate:** Phase 5 Evaluation & Code Review (see [Phase Gates](../../assessment-collaboration/phase-gates.md))

---

## Weekly Breakdown

| Week | Title | Core Topics | Deliverables |
|:----:|:------|:------------|:-------------|
| **[17](week-17.md)** | **[Software Architecture, SOLID and Design Patterns](week-17.md)** | Clean Architecture, hexagonal design, Repository & Unit-of-Work patterns, creational/structural/behavioral GoF patterns, Architecture Decision Records (ADRs) | Clean Architecture Blog Platform backend with strict domain separation, Repository pattern, and documented ADRs |
| **[18](week-18.md)** | **[Docker and Containerisation](week-18.md)** | Container internals, multi-stage Dockerfiles, image layer caching, Docker Compose multi-service orchestration, secrets management | Production-optimized multi-stage Docker setup for full-stack application (frontend, backend, database, reverse proxy) |
| **[19](week-19.md)** | **[CI/CD, GitHub Actions and Deployment](week-19.md)** | CI/CD pipelines, matrix testing, GHCR container registry publishing, automated cloud deployments, semantic versioning | End-to-end GitHub Actions workflow automating linting, testing, Docker image publishing, and remote cloud deployment |
| **[20](week-20.md)** | **[Application Security, Observability and Reliability](week-20.md)** | OWASP Top 10 mitigation, CSP & security headers, structured JSON logging, Prometheus metrics, Grafana dashboards, Sentry alerting, health checks | Hardened and observable full-stack application with security headers, rate limiting, Prometheus metrics exporter, and Sentry error tracking |

---

## Learning Objectives

By the end of Phase 05, learners will be able to:

1. **Architect Maintainable Systems Using Clean & SOLID Patterns:**
   Decouple enterprise applications into clean architectural boundaries (entities, use cases, interface adapters), applying Repository and Unit-of-Work patterns to isolate business logic from infrastructure.
2. **Build Lightweight, Secure Container Images:**
   Author optimized multi-stage Dockerfiles that minimize layer size, eliminate build tooling from runtime images, run as non-root users, and orchestrate complex environments via Docker Compose.
3. **Automate Continuous Integration & Continuous Deployment:**
   Engineer resilient GitHub Actions pipelines that lint, test, build, scan, and deploy microservices and web applications to cloud environments upon merge.
4. **Apply Threat Modeling & Defense-in-Depth Security:**
   Harden web applications against OWASP Top 10 vulnerabilities, enforce Content Security Policies (CSP) and HTTP security headers, and integrate automated dependency vulnerability scanners (`trivy`, `snyk`, `bandit`).
5. **Implement Comprehensive Telemetry & Observability:**
   Instrument frontend and backend applications with structured logging, Prometheus metric endpoints, health check probes, and distributed error reporting via Sentry.

---

## Phase Milestone Project

Throughout Weeks 17–20, learners implement **[Project 5 – Production Engineering Upgrade](../../project-library/project-5-spec.md)**.

- **Objective:** Upgrade the Full-stack Business Operations Platform (Project 4) to a production-grade system featuring containerization, automated CI/CD pipelines, security hardening, structured logging, monitoring, and cloud deployment.
- **Key Constraints:**
  - Multi-stage Docker builds for frontend, backend, and reverse proxy (Caddy/Nginx) with production compose profiles.
  - Fully automated GitHub Actions workflow executing linting, unit/integration testing, security scans, and container image publishing to GitHub Container Registry.
  - Security hardening implementing HTTPS, HTTP security headers, and automated vulnerability scanning with failure gates for critical vulnerabilities.
  - Comprehensive observability stack including structured JSON logs, `/metrics` Prometheus endpoint, and Sentry error reporting.

---

## Phase Gate & Assessment

Advancement to **Phase 06 (Capstone Development & Engineering Evaluation)** requires clearing the Phase 05 completion criteria:

1. **Submission of all 4 weekly laboratory assignments** and weekly journal reflections.
2. **Delivery of Project 5** satisfying all acceptance criteria and peer review.
3. **Passing the Phase 05 Gate Examination** (≥ 70% threshold):
   - Conceptual assessment covering clean architecture principles, containerization internals, CI/CD pipeline design, and application security.
   - Live demonstration and technical defense of your Project 5 production infrastructure, deployment pipeline, and observability telemetry.

For full rubric definitions and gate schedules, see [Phase Completion Gates](../../assessment-collaboration/phase-gates.md) and [Assessment Framework](../../assessment-collaboration/assessment-framework.md).
