# Phase 01 – Programming & Engineering Foundations

Welcome to **Phase 01** of the Software Engineering Academy. This four-week immersive phase establishes the computational, algorithmic, and developer tooling bedrock required for professional software engineering.

---

## Phase Overview

- **Duration:** Weeks 1 – 4 (approx. 18–20 hours/week)
- **Core Focus:** Unix philosophy, Git internal mechanics, idiomatic Python, computational thinking, data structures, and object-oriented software construction.
- **Milestone Project:** [Project 1 – Personal Finance CLI](../../project-library/project-1-spec.md)
- **Phase Completion Gate:** Phase 1 Evaluation & Code Review (see [Phase Gates](../../assessment-collaboration/phase-gates.md))

---

## Weekly Breakdown

| Week | Title | Core Topics | Deliverables |
|:----:|:------|:------------|:-------------|
| **[01](week-01.md)** | **[Git Mechanics & The Unix Philosophy](week-01.md)** | Unix pipes & filters, standard streams, shell scripting, Git DAG, plumbing & porcelain commands | Git `commit-tree` low-level reconstruction, interactive Bash automation script |
| **[02](week-02.md)** | **[Python Fundamentals & Computational Thinking](week-02.md)** | Variables, control flow, functions, collections, decomposition, pattern recognition, unit testing | `notescli` package with CLI arguments, modular functions, and pytest suite |
| **[03](week-03.md)** | **[Problem Solving, Algorithms & Data Structures](week-03.md)** | Big-O complexity analysis, custom linked lists, stacks, queues, trees, searching & sorting | Custom data structure implementations, complexity analysis report |
| **[04](week-04.md)** | **[Object-Oriented Programming & Software Construction](week-04.md)** | Encapsulation, inheritance, polymorphism, `@property`, SOLID principles, Python packaging | Multi-module domain application, complete unit test suite, package build |

---

## Learning Objectives

By the end of Phase 01, learners will be able to:

1. **Master the Command Line & Shell Environment:**
   Compose complex pipelines using standard streams (`stdin`, `stdout`, `stderr`), redirects (`>`, `>>`, `<`), filters (`grep`, `awk`, `sed`, `sort`, `uniq`), and POSIX-compliant shell scripts.
2. **Understand Git Internals:**
   Navigate Git's content-addressable storage model (`blob`, `tree`, `commit`, `tag`), manipulate refs and `HEAD`, and resolve merge conflicts cleanly through branch workflows.
3. **Write Idiomatic, Modular Python:**
   Apply modern Python 3.11+ syntax, type hinting, PEP 8 conventions, structured error handling, and virtual environment dependency isolation.
4. **Analyse and Apply Data Structures:**
   Evaluate time and space complexity using Big-O notation, and select the optimal data structures and algorithmic approaches for real-world constraints.
5. **Apply Object-Oriented & SOLID Principles:**
   Architect software around clean domain models, separation of concerns, and testable interfaces.

---

## Phase Milestone Project

Throughout Weeks 2–4, learners implement **[Project 1 – Personal Finance CLI](../../project-library/project-1-spec.md)**.

- **Objective:** Build a robust, production-ready command-line tool that records financial transactions, tracks categories and budgets, validates input data, persists state cleanly, and exports analytical summaries.
- **Key Constraints:**
  - Pure Python standard library or approved lightweight packages.
  - Strict modular separation (CLI layer, domain business logic, data persistence).
  - ≥ 80% automated unit test coverage with `pytest`.
  - Comprehensive Git history following conventional commits.

---

## Phase Gate & Assessment

Advancement to **Phase 02 (Web Fundamentals)** requires clearing the Phase 01 completion criteria:

1. **Submission of all 4 weekly laboratory assignments** and weekly journal reflections.
2. **Delivery of Project 1** satisfying all acceptance criteria and peer review.
3. **Passing the Phase 01 Gate Examination** (≥ 70% threshold):
   - Conceptual assessment covering Unix, Git mechanics, and computational complexity.
   - Live coding demonstration and technical defense of your Project 1 architecture.

For full rubric definitions and gate schedules, see [Phase Completion Gates](../../assessment-collaboration/phase-gates.md) and [Assessment Framework](../../assessment-collaboration/assessment-framework.md).
