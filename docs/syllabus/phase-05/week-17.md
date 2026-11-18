# Week 17 – Software Architecture, SOLID and Design Patterns

## A. Week overview
- **Week number:** 17
- **Week title:** Software Architecture, SOLID and Design Patterns
- **Phase:** Month 5 – Professional Software Engineering, Architecture and DevOps
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate‑Advanced
- **Prerequisites:** Week 16 (Full‑stack Application Engineering) completed.

## B. Learning objectives
- Apply SOLID principles to design maintainable codebases.
- Identify and implement common design patterns (Factory, Strategy, Observer, Repository).
- Create high‑level architecture diagrams using UML/Component diagrams.
- Evaluate trade‑offs between monolithic, microservice, and serverless architectures.
- Document architectural decisions using ADR (Architecture Decision Records).

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Review of SOLID principles with concrete JavaScript/TypeScript examples. |
| 2 | Creational patterns – Factory, Builder, Singleton. |
| 3 | Structural patterns – Adapter, Facade, Composite. |
| 4 | Behavioral patterns – Strategy, Observer, Command. |
| 5 | Repository & Unit‑Of‑Work patterns for data access. |
| 6 | Introduction to Domain‑Driven Design (bounded contexts, aggregates). |
| 7 | Architectural styles – Layered, Hexagonal, Clean Architecture. |
| 8 | Microservices vs monolith vs serverless – scalability, deployment, data consistency. |
| 9 | Writing Architecture Decision Records (ADR). |
|10 | Lab: Refactor the Todo app (Week 16) to use Repository pattern and SOLID principles. |
|11 | Review & documentation – create UML component diagram (Mermaid). |
|12 | Retrospective and knowledge check.

## D. Learning materials
- **Official docs / standards:**
  - SOLID principles – Wikipedia: <https://en.wikipedia.org/wiki/SOLID> (verified).
  - Design Patterns – Refactoring.Guru: <https://refactoring.guru/design-patterns> (free).
- **Tutorials:**
  - "Clean Architecture" – freeCodeCamp article: <https://www.freecodecamp.org/news/clean-architecture-explained/>.
- **Videos:**
  - "SOLID Principles in TypeScript" – Academind: <https://www.youtube.com/watch?v=rtmFCcjEgEw>.
  - "Design Patterns in JavaScript" – Traversy Media: <https://www.youtube.com/watch?v=v9fre-G2a1M>.
- **Exercises:**
  - Refactoring.Guru interactive quizzes for each pattern.
  - ADR templates – <https://github.com/joelparkerhenderson/architecture_decision_record>.

## E. Practical laboratories
### Beginner
1. Identify violations of SOLID in a given code snippet and rewrite them.
### Intermediate
2. Implement the Factory and Strategy patterns in a TypeScript utility library.
### Challenge
3. Refactor the Week 16 full‑stack app to use Repository and Service layers, applying at least three design patterns.
### Independent implementation
4. Produce an ADR series documenting major architectural choices for a hypothetical e‑commerce platform.

## F. Weekly assignment
**Problem statement:** Design and implement a *Blog Platform* backend using FastAPI that follows Clean Architecture.
- Separate layers: entities, use‑cases, adapters (FastAPI routers, persistence).
- Apply Repository pattern for PostgreSQL access via SQLModel.
- Use SOLID principles throughout the code.
- Document architecture with a Mermaid component diagram and three ADRs.

**Acceptance criteria**
- Code compiles with `mypy` strict mode and passes all `pytest` tests (≥ 80 % coverage).
- ADRs clearly justify choices (e.g., ORM vs raw SQL, async vs sync).
- Diagram included in `ARCHITECTURE.md`.
- CI pipeline runs lint, type‑check, tests.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (SOLID & patterns) | 15 % |
| Backend architecture implementation | 30 % |
| ADR documentation quality | 15 % |
| Test coverage & quality | 20 % |
| Diagram & documentation | 10 % |
| Peer review feedback incorporation | 10 % |

**Rubric highlights**
- Correct application of at least three design patterns (15 pts).
- Clean separation of concerns per Clean Architecture (15 pts).
- Comprehensive ADRs (10 pts).
- High test coverage (10 pts).
- Clear diagram (5 pts).

## H. Completion gate
Submit a public repository; CI must pass all checks and architecture diagram render correctly.

## I. Weekly retrospective
1. Which design pattern gave the most value in your implementation?
2. How did SOLID principles affect code readability?
3. What challenges did you face when writing ADRs?
4. How would you adapt the architecture for scaling to millions of users?

---
*Next week:* **Week 18 – Docker and Containerisation** (see `syllabus/phase-05/week-18.md`).