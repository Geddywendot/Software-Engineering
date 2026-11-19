# Phase 06 – Capstone Development & Engineering Evaluation

Welcome to **Phase 06** of the Software Engineering Academy. The capstone represents the culmination of the entire 24-week curriculum: learners conceive, specify, architect, implement, test, secure, deploy, and defend an enterprise-grade software platform that demonstrates mastery across the full software engineering lifecycle.

---

## Phase Overview

- **Duration:** Weeks 21 – 24 (approx. 18–20 hours/week)
- **Core Focus:** Requirements engineering, distributed systems design, domain-driven development, comprehensive test suites, automated cloud deployments, security and performance benchmarking, professional technical documentation, and architectural defense.
- **Milestone Project:** [Capstone – Warehouse and Logistics Operations Management Platform](../../project-library/capstone-spec.md)
- **Phase Completion Gate:** Capstone Defense & Final Engineering Examination (see [Phase Gates](../../assessment-collaboration/phase-gates.md))

---

## Weekly Breakdown

| Week | Title | Core Topics | Deliverables |
|:----:|:------|:------------|:-------------|
| **[21](week-21.md)** | **[Capstone Requirements Engineering and System Design](week-21.md)** | Functional and non-functional requirements elicitation, trade-off analysis, C4/UML diagrams (component, deployment, data flow), ADRs, sprint planning | Complete Requirements & System Design Specification (`REQS.md`, Mermaid architecture diagrams, ADRs, and project plan) |
| **[22](week-22.md)** | **[Capstone Core Implementation](week-22.md)** | Monorepo/polyrepo scaffolding, domain-driven design, core use-case implementation, repository pattern, test-driven development, CI pipeline integration | Functional MVP of the Capstone platform with authenticated core business workflows and automated CI testing |
| **[23](week-23.md)** | **[Capstone Testing, Security, Docker and Deployment](week-23.md)** | Unit, integration & end-to-end testing, property-based testing, static security analysis (`bandit`, `snyk`), production containerization, automated cloud deployment | Production-deployed Capstone system with ≥ 85% test coverage, security audit pass, containerized staging/production, and monitoring dashboards |
| **[24](week-24.md)** | **[Capstone Evaluation, Documentation and Final Examination](week-24.md)** | System post-mortem, load testing with k6/Locust, technical documentation, architectural walkthrough, video demo presentation, final comprehensive evaluation | Final Capstone release package (`README.md`, architecture docs, security & performance audits, retrospective report, and recorded technical demonstration) |

---

## Learning Objectives

By the end of Phase 06, learners will be able to:

1. **Elicit Requirements & Synthesize Complex System Architectures:**
   Translate open-ended business problems into unambiguous functional and non-functional requirements, formal architecture specifications, and documented architectural decision records (ADRs).
2. **Execute Production-Quality Full-Stack Implementation:**
   Build end-to-end distributed systems using clean architecture and domain-driven design, cleanly orchestrating backend microservices, typed frontend user interfaces, and relational persistence.
3. **Validate Rigorously with Testing & Performance Benchmarks:**
   Construct comprehensive test pyramids (unit, integration, end-to-end, and property-based tests) and conduct rigorous load testing with tooling such as k6 or Locust to identify and eliminate latency bottlenecks.
4. **Operate, Secure & Deploy Cloud-Native Systems:**
   Deploy containerized applications to cloud platforms with fully automated GitHub Actions CI/CD pipelines, SSL/TLS encryption, security headers, dependency auditing, and live telemetry dashboards.
5. **Defend Engineering Architecture & Communicate Technical Value:**
   Articulate architectural trade-offs, lead technical code reviews, document operational runbooks, and defend engineering decisions through live technical presentations.

---

## Phase Milestone Project

Throughout Weeks 21–24, learners execute the **[Capstone – Warehouse and Logistics Operations Management Platform](../../project-library/capstone-spec.md)**.

- **Objective:** Design, implement, test, and deploy an enterprise-grade web platform that enables organizations to manage warehouses, inventory, shipments, and logistics operations with multi-tenant data isolation and auditability.
- **Key Constraints:**
  - Multi-tenant architecture with strict data isolation per organization.
  - Decoupled modern stack: FastAPI backend, React + TypeScript frontend, and PostgreSQL database.
  - ≥ 85% automated test coverage across unit, integration, and end-to-end test suites.
  - Automated CI/CD pipeline building, testing, scanning, and deploying to cloud infrastructure.
  - Complete engineering documentation suite: architecture diagrams, OpenAPI specifications, security audit, performance benchmark report, and post-mortem retrospective.

---

## Phase Gate & Assessment

Successful completion of **Phase 06 and Academy Graduation** requires clearing the final evaluation criteria:

1. **Submission of all 4 weekly capstone deliverables** and weekly engineering journal reflections.
2. **Delivery of the Capstone Platform** satisfying all acceptance criteria, functional requirements, and peer review.
3. **Passing the Final Comprehensive Engineering Examination**:
   - Comprehensive conceptual and architectural defense covering all six phases of the curriculum.
   - Live technical demonstration, code walkthrough, and adversarial review of the deployed Capstone system.

For full rubric definitions and gate schedules, see [Phase Completion Gates](../../assessment-collaboration/phase-gates.md) and [Assessment Framework](../../assessment-collaboration/assessment-framework.md).
