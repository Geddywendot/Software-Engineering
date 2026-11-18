# Week 21 – Capstone Requirements Engineering and System Design

## A. Week overview
- **Week number:** 21
- **Week title:** Capstone Requirements Engineering and System Design
- **Phase:** Month 6 – Capstone Development and Engineering Evaluation
- **Estimated hours:** 18‑20 h
- **Difficulty:** Advanced
- **Prerequisites:** Completion of Phase 5 (Week 20) and a solid grasp of full‑stack development, security, and DevOps.

## B. Learning objectives
- Elicit and document functional and non‑functional requirements for a real‑world software system.
- Translate requirements into high‑level system architecture diagrams (component, deployment, data flow).
- Perform trade‑off analysis (scalability, cost, latency, maintainability).
- Produce Architecture Decision Records (ADRs) to capture key choices.
- Create a detailed project plan (backlog, milestones, sprint cadence).

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Requirement gathering techniques: user stories, use‑case modeling, interview scripts. |
| 2 | Defining functional vs non‑functional requirements; quality attribute scenarios. |
| 3 | Introduction to System Design Primer (GitHub) and how to use it for real projects. |
| 4 | High‑level architecture styles – layered, microservices, event‑driven. |
| 5 | Creating component & deployment diagrams with Mermaid. |
| 6 | Data modeling – ER diagrams, schema evolution, GDPR considerations. |
| 7 | Scalability & reliability patterns – load balancing, caching, circuit breakers. |
| 8 | Security considerations – threat modeling, authentication flows, OWASP checklist. |
| 9 | Writing ADRs – template, example, justification. |
|10 | Lab: Draft the full requirements and a preliminary architecture for the capstone project (choose from a preset list of domains). |
|11 | Review and refinement of artefacts with peer feedback. |
|12 | Retrospective and knowledge consolidation.

## D. Learning materials
- **Official docs / standards:**
  - IEEE 830‑1998 (Software Requirements Specification) – <https://ieeexplore.ieee.org/document/720574> (publicly available abstract).
  - System Design Primer (GitHub): <https://github.com/donnemartin/system-design-primer>.
- **Tutorials / guides:**
  - "How to Write a Good Requirements Document" – Atlassian: <https://www.atlassian.com/software/confluence/guides/create-documentation/requirements>.
  - "Architecture Decision Records" – Michael Nygard: <https://github.com/joelparkerhenderson/architecture_decision_record>.
- **Videos:**
  - "System Design Interview – Basics" – Gaurav Sen: <https://www.youtube.com/watch?v=UzLMfqKXHcI>.
- **Exercises:**
  - Use the *Awesome System Design* checklist (<https://github.com/checkcheckzz/system-design-interview>) to evaluate your design.

## E. Practical laboratories
### Beginner
1. Write three user stories for a chosen capstone domain (e.g., e‑commerce, health tracker).
### Intermediate
2. Produce a Mermaid component diagram covering frontend, API gateway, services, and database.
### Challenge
3. Conduct a threat model using STRIDE and document findings.
### Independent implementation
4. Write a set of ADRs (minimum three) covering language/runtime choice, data store selection, and deployment strategy.

## F. Weekly assignment
**Problem statement:** Produce a complete Requirements & Design package for a *Scalable Event‑Ticketing Platform*.
- Deliverables:
  - **Requirements Specification** (`REQS.md`) covering functional and non‑functional aspects.
  - **Architecture Diagrams** (`ARCHITECTURE.mmd`) using Mermaid for component, deployment, and data flow.
  - **ADRs** (`adr/001-language-runtime.md`, `adr/002-database.md`, `adr/003-deployment.md`).
  - **Project Plan** (`PROJECT_PLAN.md`) with milestones, sprint length, and risk register.
- Constraints:
  - Must support at least 10 000 concurrent users (simulated load).
  - Must guarantee ACID transactions for ticket purchases.
  - Must include a basic security model (JWT auth, role‑based access).
- Acceptance criteria:
  - All artefacts are version‑controlled, reviewed, and pass a peer‑review checklist.
  - Diagrams render correctly on GitHub.
  - ADRs include clear rationale and alternatives considered.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (requirements & design) | 20 % |
| Quality of Requirements Specification | 20 % |
| Architecture diagram correctness & completeness | 20 % |
| ADR depth and justification | 20 % |
| Project plan realism and risk analysis | 10 % |
| Peer‑review feedback incorporation | 10 % |

**Rubric highlights**
- Well‑structured REQS (10 pts).
- Clear, renderable Mermaid diagrams (10 pts).
- Thoughtful ADRs with alternatives (10 pts).
- Realistic milestones and risk mitigation (5 pts).
- Effective incorporation of peer feedback (5 pts).

## H. Completion gate
Submit a public repository URL; CI must run a documentation build (MkDocs) with no errors and all diagrams rendered.

## I. Weekly retrospective
1. Which requirement proved hardest to articulate and why?
2. How did the ADR process influence your design choices?
3. What trade‑offs did you accept for scalability versus simplicity?
4. How confident are you to proceed to full implementation?

---
*Next week:* **Week 22 – Capstone Core Implementation** (see `syllabus/phase-06/week-22.md`).