# Week 14 – TypeScript and Frontend Architecture

## A. Week overview
- **Week number:** 14
- **Week title:** TypeScript and Frontend Architecture
- **Phase:** Month 4 – Frontend and Full‑stack Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Week 13 (React fundamentals) completed; Node.js installed.

## B. Learning objectives
- Write type‑safe code using TypeScript in a React project.
- Configure `tsconfig.json` for strict type checking.
- Apply architectural patterns (Feature‑sliced design, Component‑first) in the frontend.
- Use interfaces and generics to model component props and API contracts.
- Integrate third‑party type definitions (`@types/*`).
- Perform type‑driven refactoring and debugging.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | TypeScript basics – primitives, unions, enums, type inference. |
| 2 | Functions, generics, and advanced types (conditional, mapped). |
| 3 | Setting up a React‑TypeScript project with Vite; `tsconfig` strict mode. |
| 4 | Component props typing, default props, and functional components with generics. |
| 5 | State management typing – `useState`, `useReducer`, context API. |
| 6 | Architectural patterns – feature‑sliced folders, domain‑driven UI, separation of concerns. |
| 7 | Styling with CSS Modules and TypeScript typings (`*.module.css`). |
| 8 | Form handling with typed libraries (`react-hook-form`). |
| 9 | Data fetching – typed API clients with `axios` and `zod` schema validation. |
|10 | Testing TypeScript React components – `@testing-library/react` with type safety. |
|11 | Lab day – refactor the Movie Search SPA (Week 6) to TypeScript and apply feature‑slice architecture. |
|12 | Review & documentation – write `TS_ARCHITECTURE.md` with Mermaid component diagram.

## D. Learning materials
- **Official docs**: <https://www.typescriptlang.org/docs/>, <https://reactjs.org/docs/static-type-checking.html>.
- **Tutorials**:
  - TypeScript Deep Dive (free online book) – <https://basarat.gitbook.io/typescript/>.
  - React‑TypeScript Cheat Sheet – <https://react-typescript-cheatsheet.netlify.app/>.
- **Videos**:
  - "TypeScript for React Developers" – Traversy Media – <https://www.youtube.com/watch?v=Z5iWr6Srsj8>.
  - "Feature Sliced Design – Architecture for Front‑end" – freeCodeCamp – <https://www.youtube.com/watch?v=1br9WHW9EjY>.
- **Exercises**:
  - Exercism TypeScript track – <https://exercism.org/tracks/typescript>.
  - Typescript Playground challenges – <https://www.typescriptlang.org/play>.

## E. Practical laboratories
### Beginner
1. Convert a simple JavaScript component (`Hello.tsx`) to TypeScript with explicit prop types.
### Intermediate
2. Create a typed API client that fetches posts from JSONPlaceholder and validates the response with `zod`.
### Challenge
3. Refactor the Movie Search SPA to TypeScript, organise the code into a feature‑slice folder structure, and add unit tests for the typed components.
### Independent implementation
4. Build a small reusable UI library (Button, Card) with full TypeScript typings and publish it locally (`npm pack`).

## F. Weekly assignment
**Problem statement**: Develop a *Task Board* SPA in React‑TypeScript.
- Use a feature‑slice layout (`src/features/board/`).
- Implement CRUD for tasks with a typed in‑memory store.
- Add drag‑and‑drop reordering using `react-beautiful-dnd` with proper typings.
- Write unit and integration tests (`jest`, `@testing-library/react`).
- Provide a `README.md` and a `REPORT.md` with a Mermaid diagram of the component hierarchy and type relationships.

**Acceptance criteria**
- Application builds with `npm run build` and passes all tests (≥ 80 % coverage).
- TypeScript compiler reports no errors under `strict` mode.
- Documentation includes architecture diagram and rationale.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| TypeScript conversion task (auto‑graded) | 25 % |
| Feature‑slice architecture implementation | 20 % |
| Testing & coverage verification | 20 % |
| Documentation & diagram quality | 20 % |

**Rubric highlights**
- Correct strict TypeScript configuration (10 pts).
- Properly typed components and props (10 pts).
- Clean feature‑slice folder layout (5 pts).
- Comprehensive tests (5 pts).
- Clear architecture diagram (5 pts).

## H. Completion gate
Submit a public repo URL; CI must succeed and overall score ≥ 70 %.

## I. Weekly retrospective
1. Which TypeScript feature helped you the most in catching bugs?
2. How did the feature‑slice architecture affect your code organization?
3. What challenges arose when typing third‑party libraries?
4. What would you improve in your testing strategy for typed components?

---
*Next week:* **Week 15 – Frontend and Backend Integration** (see `syllabus/phase-04/week-15.md`).