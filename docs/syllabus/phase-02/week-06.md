# Week 06 – JavaScript and Browser Programming

## A. Week overview
- **Week number:** 6
- **Week title:** JavaScript and Browser Programming
- **Phase:** Month 2 – Web Technologies, Networking and Database Fundamentals
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner‑intermediate
- **Prerequisites:** Week 05 completed; modern browser installed.

## B. Learning objectives
- Write vanilla ES6+ JavaScript that runs in the browser.
- Manipulate the DOM using selectors, events, and element creation.
- Understand the event loop, call stack, and asynchronous patterns (callbacks, promises, async/await).
- Use browser dev tools for debugging JavaScript.
- Consume a public REST API with `fetch` and handle JSON data.
- Apply module bundling with native ES modules.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | JavaScript basics – variables (`let`, `const`), data types, operators, template literals. |
| 2 | Control flow – `if/else`, ternary, loops (`for`, `while`), `switch`. |
| 3 | Functions – declarations, expressions, arrow functions, default parameters, rest/spread. |
| 4 | Scope, closures, the `this` keyword, lexical vs. dynamic binding. |
| 5 | DOM fundamentals – `document.querySelector`, element creation, attributes, classes. |
| 6 | Events – event listeners, delegation, propagation (`capture`, `bubble`). |
| 7 | Asynchronous JavaScript – callbacks, `setTimeout`, `setInterval`. |
| 8 | Promises – creation, chaining, error handling, `Promise.all`. |
| 9 | Async/Await – syntax, error handling with `try/catch`. |
|10 | Fetch API – GET, POST, handling response status, JSON parsing. |
|11 | ES Modules – `import`/`export`, static vs. dynamic imports. |
|12 | Lab day – build a small weather widget that fetches data from a free API. |
|13 | Review & documentation – write `JS_OVERVIEW.md` with code snippets and a Mermaid flowchart of the event loop.

## D. Learning materials
- **Official docs**: <https://developer.mozilla.org/en-US/docs/Web/JavaScript>.
- **Tutorials**:
  - “You Don’t Know JS” (free on GitHub) – <https://github.com/getify/You-Dont-Know-JS>.
  - freeCodeCamp “JavaScript Algorithms and Data Structures” – <https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/>.
- **Videos**:
  - Traversy Media – Modern JavaScript Crash Course – <https://www.youtube.com/watch?v=hdI2bqOjy3c>.
  - The Net Ninja – JavaScript ES6 Tutorial – <https://www.youtube.com/playlist?list=PL4cUxeGkcC9jLYyp2Aoh6hcWuxFDX6PBJ>.
- **Exercises**:
  - Codewars “JavaScript” kata – <https://www.codewars.com/kata/search/javascript>.
  - JavaScript30 – 30 vanilla JS projects – <https://javascript30.com/>.

## E. Practical laboratories
### Beginner
1. Write `hello.js` that logs “Hello, World!” and runs in the browser console.
### Intermediate
2. Create an interactive to‑do list: add, toggle complete, and delete items, persisting state in `localStorage`.
### Challenge
3. Build a weather widget that fetches data from the OpenWeatherMap free API, displays current temperature, and updates every hour.
### Independent implementation
4. Refactor the widget into an ES module `weather.js` and import it from `main.js`. Add unit‑tests with Jest (runs in Node with `jsdom`).

## F. Weekly assignment
**Problem statement**: Develop a *Movie Explorer* SPA.
- Use the TMDB free API to search movies by title.
- Display results in a responsive grid with poster, title, rating.
- Clicking a movie opens a modal with detailed information (overview, release date, etc.).
- Implement client‑side routing using the URL hash (`#search`, `#movie/ID`).
- Write a `README.md` describing the architecture and how to obtain an API key.

**Acceptance criteria**
- Search works and debounces input (300 ms).
- Modal opens without page reload and can be closed with ESC.
- Application is responsive (mobile‑first).
- Linting (`eslint`) passes, and a Jest test suite covers at least the search utility function.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| JavaScript coding challenge – to‑do list (auto‑graded) | 20 % |
| Weather widget functional test | 20 % |
| Movie Explorer SPA demonstration | 30 % |
| Documentation & code quality | 15 % |

**Rubric highlights**
- Correct use of `fetch` and error handling (10 pts).
- Proper DOM manipulation without libraries (10 pts).
- Asynchronous code written with `async/await` (5 pts).
- Responsive UI and accessibility (5 pts).
- Linting and testing compliance (5 pts).

## H. Completion gate
Push the repository to GitHub, enable GitHub Pages for the demo, and achieve an assessment score of **≥ 70 %**.

## I. Weekly retrospective
1. Which asynchronous pattern (callback, promise, async/await) felt most natural?
2. What challenges did you face when handling API errors and rate limits?
3. How did you ensure the UI remained responsive during data fetches?
4. What would you improve in your module structure for larger projects?

---
*Next week:* **Week 07 – Networking, HTTP, APIs and Internet Architecture** (see `syllabus/phase-02/week-07.md`).