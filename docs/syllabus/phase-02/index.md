# Phase 02 – Web Technologies, Networking & Database Fundamentals

Welcome to **Phase 02** of the Software Engineering Academy. This four-week phase transitions learners from terminal-based computing to the core pillars of web applications and distributed systems: semantic markup, browser programming, internet networking protocols, relational database design, and structured query language.

---

## Phase Overview

- **Duration:** Weeks 5 – 8 (approx. 18–20 hours/week)
- **Core Focus:** Semantic HTML5, responsive CSS3 (Flexbox and Grid), modern JavaScript (ES6+), DOM manipulation, browser networking & HTTP/REST protocols, relational data modeling, and PostgreSQL database administration.
- **Milestone Project:** [Project 2 – Inventory Management Application](../../project-library/project-2-spec.md)
- **Phase Completion Gate:** Phase 2 Evaluation & Code Review (see [Phase Gates](../../assessment-collaboration/phase-gates.md))

---

## Weekly Breakdown

| Week | Title | Core Topics | Deliverables |
|:----:|:------|:------------|:-------------|
| **[05](week-05.md)** | **[HTML, CSS and Web Foundations](week-05.md)** | HTML5 semantic elements, CSS box model, Flexbox, CSS Grid, media queries, accessibility (ARIA), browser dev tools | Developer Portfolio static site deployed to GitHub Pages with responsive layouts and dark-mode toggle |
| **[06](week-06.md)** | **[JavaScript and Browser Programming](week-06.md)** | ES6+ syntax, DOM manipulation, browser event loop, promises, async/await, Fetch API, client-side routing | Movie Explorer single-page application (SPA) consuming TMDB API with dynamic search, modal detail views, and hash routing |
| **[07](week-07.md)** | **[Networking, HTTP, APIs and Internet Architecture](week-07.md)** | OSI & TCP/IP models, DNS resolution, TCP handshake, HTTP methods, headers, status codes, CORS, OpenAPI specification | News Aggregator frontend consuming NewsAPI with rate-limit handling, error states, and OpenAPI (`newsapi.yaml`) contract |
| **[08](week-08.md)** | **[SQL, Relational Database Design and PostgreSQL](week-08.md)** | Relational modeling, normalization (1NF–3NF), DDL/DML, joins, aggregation, PostgreSQL indexing, `psycopg2` Python driver | Task Tracker relational persistence layer with normalized PostgreSQL schema, CRUD test suite (≥ 80% coverage), and `SCHEMA.md` |

---

## Learning Objectives

By the end of Phase 02, learners will be able to:

1. **Master Semantic Markup & Responsive Layouts:**
   Construct accessible, standards-compliant HTML5 documents and responsive styling systems utilizing CSS Flexbox, Grid, custom properties, and responsive breakpoints.
2. **Write Modern Asynchronous JavaScript:**
   Develop client-side web applications using modern ECMAScript standards, DOM manipulation APIs, and asynchronous programming patterns (Promises, `async`/`await`, Event Loop).
3. **Understand Networking Protocols & Web Architecture:**
   Analyze HTTP/HTTPS request-response lifecycles, inspect network traffic and headers via developer tools, resolve CORS issues, and document API interfaces using OpenAPI.
4. **Design Normalized Relational Schemas:**
   Formulate relational database structures adhering to Third Normal Form (3NF), defining primary keys, foreign keys, unique constraints, and performant indexes.
5. **Integrate Relational Databases with Programmatic Code:**
   Execute parameterized SQL queries, manage database connections, and orchestrate ACID-compliant transactions using PostgreSQL and Python database drivers.

---

## Phase Milestone Project

Throughout Weeks 5–8, learners implement **[Project 2 – Inventory Management Application](../../project-library/project-2-spec.md)**.

- **Objective:** Build a web-based inventory management system that allows a small business to keep track of products, categories, and stock levels with persistent data storage in a relational database.
- **Key Constraints:**
  - Semantic, responsive web interface built with clean HTML5, CSS3, and JavaScript.
  - Normalized PostgreSQL database schema establishing relational links between products and categories.
  - Full CRUD operations with search, filtering, and stock-level status tracking.
  - Clean separation between presentation layer, application business logic, and database operations.
  - ≥ 80% automated unit and integration test coverage.

---

## Phase Gate & Assessment

Advancement to **Phase 03 (Backend Engineering)** requires clearing the Phase 02 completion criteria:

1. **Submission of all 4 weekly laboratory assignments** and weekly journal reflections.
2. **Delivery of Project 2** satisfying all acceptance criteria and peer review.
3. **Passing the Phase 02 Gate Examination** (≥ 70% threshold):
   - Conceptual assessment covering web fundamentals, JavaScript event execution, HTTP protocols, and relational schema normalization.
   - Live coding demonstration and technical defense of your Project 2 architecture and database design.

For full rubric definitions and gate schedules, see [Phase Completion Gates](../../assessment-collaboration/phase-gates.md) and [Assessment Framework](../../assessment-collaboration/assessment-framework.md).
