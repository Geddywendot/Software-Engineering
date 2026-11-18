# Week 05 – HTML, CSS and Web Foundations

## A. Week overview
- **Week number:** 5
- **Week title:** HTML, CSS and Web Foundations
- **Phase:** Month 2 – Web Technologies, Networking and Database Fundamentals
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner
- **Prerequisites:** Completion of Weeks 01‑04, a working development environment with a modern browser.

## B. Learning objectives
- Write semantic HTML5 documents using proper tags and hierarchy.
- Apply CSS3 styling, selectors, box model, layout techniques (Flexbox, Grid).
- Build a responsive page that adapts to mobile, tablet and desktop breakpoints.
- Use browser developer tools to inspect, debug and modify HTML/CSS.
- Understand accessibility basics (ARIA roles, alt text) and best‑practice markup.
- Deploy a static site to GitHub Pages.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | HTML5 anatomy – `<!DOCTYPE>`, `<html>`, `<head>`, `<body>`; semantic elements (`<header>`, `<nav>`, `<section>`, `<article>`, `<footer>`). |
| 2 | Text formatting, lists, tables, forms – proper attribute use, validation. |
| 3 | CSS fundamentals – selectors, specificity, cascade, inheritance. |
| 4 | Box model – margin, border, padding, width/height calculations, `box-sizing`. |
| 5 | Layout with Flexbox – direction, alignment, order, wrapping. |
| 6 | Layout with CSS Grid – rows, columns, grid‑area, implicit grid. |
| 7 | Responsive design – media queries, mobile‑first approach, fluid typography. |
| 8 | Accessibility – semantic markup, ARIA, colour contrast, keyboard navigation. |
| 9 | Browser DevTools – Elements panel, Styles, Computed, Network, Performance. |
|10 | Deploying static assets – GitHub Pages setup, custom domain basics. |
|11 | Lab day – build a personal landing page using HTML/CSS, make it responsive. |
|12 | Review & documentation – write `HTML_CSS_OVERVIEW.md` with code snippets and a Mermaid diagram of the page structure.

## D. Learning materials
- **Official docs**: <https://developer.mozilla.org/en-US/docs/Web/HTML>, <https://developer.mozilla.org/en-US/docs/Web/CSS>.
- **Tutorials**:
  - “HTML & CSS” freeCodeCamp curriculum – <https://www.freecodecamp.org/learn/responsive-web-design/>.
  - “CSS Tricks – A Complete Guide to Flexbox” – <https://css-tricks.com/snippets/css/a-guide-to-flexbox/>.
- **Videos**:
  - Wes Bos – HTML & CSS Crash Course – <https://www.youtube.com/watch?v=UB1O30fR-EE>.
  - Kevin Powell – CSS Grid Full Course – <https://www.youtube.com/watch?v=jV8B24rSN5o>.
- **Exercises**:
  - HTML5 Boilerplate – <https://html5boilerplate.com/> (starter files).
  - CSSBattle – practice CSS layout challenges – <https://cssbattle.dev/>.

## E. Practical laboratories
### Beginner
1. Create `index.html` with a semantic page skeleton and a `<h1>` title.
### Intermediate
2. Add a stylesheet `styles.css` that uses Flexbox to create a navigation bar that collapses on small screens.
### Challenge
3. Build a responsive photo‑gallery page using CSS Grid, including hover effects and a mobile‑first media query.
### Independent implementation
4. Publish the gallery to GitHub Pages and write a short guide (`DEPLOYMENT.md`) describing the steps.

## F. Weekly assignment
**Problem statement**: Design a *Portfolio* site for a developer.
- Must contain sections: About, Projects (grid of cards), Skills (list), Contact (form – static, no backend).
- Use semantic HTML5 and responsive CSS (Flexbox + Grid).
- Include a dark‑mode toggle using CSS custom properties.
- Deploy to GitHub Pages and configure a custom domain (optional).
- Provide a `README.md` with setup instructions and a `REPORT.md` that explains the layout decisions and accessibility considerations.

**Acceptance criteria**
- Site passes the W3C validator (<https://validator.w3.org/>) with ≤ 5 warnings.
- Layout adapts correctly at three breakpoints: < 600 px, 600‑900 px, > 900 px.
- Dark‑mode toggle works without page reload.
- Repository contains a CI workflow that runs `htmlhint` and `csslint` on push.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| CSS layout coding challenge (auto‑graded) | 25 % |
| Accessibility audit (manual) | 20 % |
| Deployment verification & CI checks | 20 % |
| Peer review of another learner’s site (optional) | 10 % |
| Documentation quality | 10 % |

**Rubric highlights**
- Correct semantic markup (10 pts).
- Responsive layout works at all breakpoints (10 pts).
- Dark‑mode implementation using CSS variables (5 pts).
- Accessibility features (ARIA, alt text) present (5 pts).
- CI workflow passes linting (5 pts).
- Documentation clear and complete (5 pts).

## H. Completion gate
Learners must push their repository to GitHub, open a Pull Request to the main curriculum repo, and obtain a score of **≥ 70 %** on the assessment.

## I. Weekly retrospective
1. Which CSS layout method (Flexbox vs. Grid) felt more intuitive for your design?
2. What difficulties did you encounter when making the site responsive?
3. How did the accessibility audit change your markup choices?
4. What would you improve in the deployment process for future projects?

---
*Next week:* **Week 06 – JavaScript and Browser Programming** (see `syllabus/phase-02/week-06.md`).