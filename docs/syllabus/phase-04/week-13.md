# Week 13 – React Fundamentals

## A. Week overview
- **Week number:** 13
- **Week title:** React Fundamentals
- **Phase:** Month 4 – Frontend and Full‑stack Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner‑intermediate
- **Prerequisites:** Week 12 completed; basic JavaScript competence.

## B. Learning objectives
- Create React components using function syntax and JSX.
- Manage component state with `useState` and side‑effects with `useEffect`.
- Build component hierarchies and pass props.
- Handle events and form inputs.
- Use React Router for client‑side navigation.
- Apply basic styling with CSS modules or styled‑components.
- Debug React applications with React DevTools.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Project bootstrapping with Vite + React template; folder structure. |
| 2 | JSX fundamentals, expressions, conditional rendering. |
| 3 | Functional components, props, default props, prop‑type checking. |
| 4 | State hook `useState` – primitive and object state.
| 5 | Effect hook `useEffect` – data fetching, cleanup, dependency array. |
| 6 | Event handling – synthetic events, form handling, controlled components. |
| 7 | Component composition – children, composition over inheritance. |
| 8 | React Router – routes, navigation, URL parameters. |
| 9 | Styling – CSS modules, scoped styles, basic theming. |
|10 | Debugging – React DevTools, console, error boundaries. |
|11 | Lab day – build a simple “Movie Search” SPA that consumes the OMDB API. |
|12 | Review & documentation – write `REACT_OVERVIEW.md` with component diagram (Mermaid).

## D. Learning materials
- **Official docs**: <https://reactjs.org/docs/getting-started.html>
- **Tutorials**:
  - FreeCodeCamp React curriculum – <https://www.freecodecamp.org/learn/front-end-libraries/react/>
  - Vite + React starter guide – <https://vitejs.dev/guide/#scaffolding-your-first-project>
- **Videos**:
  - JavaScript Mastery – React Crash Course – <https://www.youtube.com/watch?v=qrJ9u8HYu7w>
  - Traversy Media – React JS Tutorial – <https://www.youtube.com/watch?v=w7ejDZ8SWv8>
- **Exercises**:
  - Scrimba React challenges – <https://scrimba.com/learn/learnreact>
  - CodeSandbox starter templates for practice.

## E. Practical laboratories
### Beginner
1. Create a `HelloReact` component that renders a greeting with a prop.
### Intermediate
2. Build a counter component using `useState` and a button to increment.
### Challenge
3. Implement a weather widget that fetches data from OpenWeatherMap, uses `useEffect` for fetching, and displays loading / error states.
### Independent implementation
4. Refactor the Movie Search SPA to use React Router for a “Details” page and add basic CSS module styling.

## F. Weekly assignment
**Problem statement**: Build a *Personal Portfolio* SPA in React.
- Sections: Home, Projects (grid of cards), Skills, Contact (static form).
- Use React Router for navigation.
- Pull project data from a local JSON file via `fetch`.
- Implement dark‑mode toggle using context and CSS variables.
- Deploy to GitHub Pages using the `gh‑pages` npm package.
- Provide `README.md` with setup, build, and deployment steps, and `REPORT.md` describing component hierarchy (Mermaid) and state management decisions.

**Acceptance criteria**
- Application is fully functional and responsive (mobile‑first).
- Dark‑mode persists across page reloads (localStorage).
- CI workflow runs `npm test` (using Jest + React Testing Library) and passes.
- Documentation includes a component diagram and a 300‑word rationale.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| React component coding test (auto‑graded) | 25 % |
| State management & effect handling challenge | 20 % |
| CI pipeline & deployment verification | 20 % |
| Documentation & diagram quality | 20 % |

**Rubric highlights**
- Correct use of hooks (`useState`, `useEffect`) (10 pts).
- Proper routing and lazy loading (5 pts).
- Responsive design and dark‑mode implementation (5 pts).
- Test coverage ≥ 80 % (5 pts).
- Clear component diagram and rationale (5 pts).

## H. Completion gate
Submit a public repo URL; CI must show a green build and the overall assessment score ≥ 70 %.

## I. Weekly retrospective
1. Which hook did you find most useful and why?
2. What challenges did you encounter when configuring React Router?
3. How would you improve the dark‑mode implementation for accessibility?
4. What testing strategies worked best for your components?

---
*Next week:* **Week 14 – TypeScript and Frontend Architecture** (see `syllabus/phase-04/week-14.md`).