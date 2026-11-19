# Phase 04 – Frontend & Full-Stack Application Engineering

Welcome to **Phase 04** of the Software Engineering Academy. This five-week phase bridges backend services and modern frontend architectures, training learners to build robust, type-safe, full-stack systems using React, TypeScript, rigorous automated testing, and containerized integration.

---

## Phase Overview

- **Duration:** Weeks 12 – 16 (approx. 18–20 hours/week)
- **Core Focus:** Automated backend testing & QA, React component architecture, TypeScript static type checking, frontend state management, REST API integration, multi-container orchestration, and full-stack operational dashboards.
- **Milestone Project:** [Project 4 – Full-stack Business Operations Platform](../../project-library/project-4-spec.md)
- **Phase Completion Gate:** Phase 4 Evaluation & Code Review (see [Phase Gates](../../assessment-collaboration/phase-gates.md))

---

## Weekly Breakdown

| Week | Title | Core Topics | Deliverables |
|:----:|:------|:------------|:-------------|
| **[12](week-12.md)** | **[Testing, Debugging and Backend Quality](week-12.md)** | Unit & integration testing with `pytest`, FastAPI `TestClient`, property-based testing (`hypothesis`), static analysis (`flake8`, `mypy`), CI verification | Comprehensive automated test suite for Book Library API with CI pipeline enforcing linting, type checks, and coverage |
| **[13](week-13.md)** | **[React Fundamentals](week-13.md)** | Component hierarchy, JSX, props, hooks (`useState`, `useEffect`), Context API, React Router, client-side data fetching | Personal Portfolio SPA with multi-route navigation, theme context, dynamic project cards, and GitHub Pages deployment |
| **[14](week-14.md)** | **[TypeScript and Frontend Architecture](week-14.md)** | TypeScript interfaces & generics, feature-slice design, typed state management, drag-and-drop interactions, component testing | Interactive Task Board SPA built with React-TypeScript, typed state store, drag-and-drop task ordering, and Jest test suite |
| **[15](week-15.md)** | **[Frontend and Backend Integration](week-15.md)** | Full-stack architecture, OpenAPI client generation, Axios/Fetch data layer, CORS resolution, multi-service Docker Compose orchestration | Book Review full-stack application connecting React frontend to FastAPI backend with PostgreSQL and integration tests |
| **[16](week-16.md)** | **[Full-stack Application Engineering](week-16.md)** | Production application design, interactive dashboard visualizations (Chart.js), monitoring hooks, Sentry alerting, automated CI/CD builds | Personal Finance Tracker full-stack application with interactive analytics dashboards, metrics endpoints, and multi-container Docker deployment |

---

## Learning Objectives

By the end of Phase 04, learners will be able to:

1. **Implement Rigorous Automated Testing & CI Quality Gates:**
   Author unit, integration, and property-based test suites using `pytest` and `TestClient`, enforcing code quality and type safety via automated GitHub Actions workflows.
2. **Master Declarative UI Construction with React:**
   Develop modular, responsive web interfaces using modern React conventions, custom hooks, context-driven state, and client-side routing.
3. **Ensure End-to-End Type Safety with TypeScript:**
   Apply advanced TypeScript features—generics, discriminated unions, utility types, and strict compiler configurations—to eliminate runtime bugs across frontend applications.
4. **Architect Cohesive Full-Stack Systems:**
   Seamlessly integrate React frontends with FastAPI backends, consuming RESTful APIs, managing asynchronous state, and handling network errors gracefully.
5. **Containerize Multi-Service Applications:**
   Orchestrate multi-tier application architectures consisting of frontend clients, backend APIs, and PostgreSQL databases using Docker and Docker Compose.

---

## Phase Milestone Project

Throughout Weeks 13–16, learners implement **[Project 4 – Full-stack Business Operations Platform](../../project-library/project-4-spec.md)**.

- **Objective:** Develop a comprehensive full-stack web application that enables businesses to manage operations: user authentication, inventory oversight, analytics dashboards, and operational reporting.
- **Key Constraints:**
  - Decoupled React + TypeScript frontend and FastAPI + PostgreSQL backend.
  - JWT authentication with access/refresh token rotation and role-based route gating (`admin`, `manager`, `viewer`).
  - Interactive data dashboards featuring summary metrics and searchable, paginated tabular views.
  - Export capabilities for operational reports (CSV/PDF).
  - Multi-container local orchestration via `docker-compose.yml`.
  - ≥ 80% automated unit and integration test coverage across frontend and backend.

---

## Phase Gate & Assessment

Advancement to **Phase 05 (Professional Software Engineering, Architecture & DevOps)** requires clearing the Phase 04 completion criteria:

1. **Submission of all 5 weekly laboratory assignments** and weekly journal reflections.
2. **Delivery of Project 4** satisfying all acceptance criteria and peer review.
3. **Passing the Phase 04 Gate Examination** (≥ 70% threshold):
   - Conceptual assessment covering test strategies, React lifecycle, TypeScript type systems, and full-stack integration patterns.
   - Live coding demonstration and technical defense of your Project 4 full-stack architecture.

For full rubric definitions and gate schedules, see [Phase Completion Gates](../../assessment-collaboration/phase-gates.md) and [Assessment Framework](../../assessment-collaboration/assessment-framework.md).
