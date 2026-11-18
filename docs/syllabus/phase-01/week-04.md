# Week 04 – Object‑Oriented Programming, Modules and Software Construction

## A. Week overview
- **Week number:** 4
- **Week title:** Object‑Oriented Programming, Modules and Software Construction
- **Phase:** Month 1 – Computer Science and Programming Foundations
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner‑intermediate
- **Prerequisites:** Weeks 01‑03 completed; solid grasp of Python fundamentals.

## B. Learning objectives
- Design classes using encapsulation, inheritance, and polymorphism.
- Distinguish between class and instance attributes; use `@property` and descriptors.
- Organise code into reusable modules and packages.
- Apply SOLID principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion) in Python.
- Write clean, maintainable code following PEP 8 and project style guidelines.
- Use `unittest` and `pytest` for test‑driven development of OOP code.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | OOP concepts – objects, classes, methods, `self`, `__init__`. |
| 2 | Class vs. instance attributes, encapsulation, name‑mangling (`__var`). |
| 3 | Inheritance – `super()`, method overriding, multiple inheritance pitfalls. |
| 4 | Polymorphism – duck typing, abstract base classes (`abc.ABC`). |
| 5 | Special methods – `__repr__`, `__str__`, `__len__`, `__eq__`, operator overloading. |
| 6 | Property descriptors – `@property`, setters, deleters. |
| 7 | Modules – import statements, relative imports, `__all__`, package structure. |
| 8 | Packaging basics – `setup.cfg` / `pyproject.toml`, entry points, building wheels. |
| 9 | SOLID principles in Python – concrete examples and anti‑patterns. |
|10 | Testing OOP – mocking, fixtures, test organization with `pytest`. |
|11 | Code quality tools – `flake8`, `black`, `isort`, pre‑commit hooks. |
|12 | Lab day – develop a small library `shapes` implementing geometric shapes with inheritance and polymorphism. |
|13 | Review & documentation – write `SHAPES.md` with class diagrams (Mermaid) and usage examples.

## D. Learning materials
- **Official docs**: <https://docs.python.org/3/tutorial/classes.html>, <https://docs.python.org/3/library/importlib.html>.
- **Tutorials**:
  - Real Python – OOP in Python – <https://realpython.com/python3-object-oriented-programming/>
  - PyBites – SOLID Principles – <https://codechalleng.es/bites/solid-principles/>
- **Videos**:
  - Corey Schafer – OOP Tutorial – <https://www.youtube.com/watch?v=ZDa-Z5JzLYM>
  - Tech With Tim – SOLID Principles – <https://www.youtube.com/watch?v=rt4F-73w2Yc>
- **Exercises**:
  - Exercism Python OOP track – <https://exercism.org/tracks/python/exercises>
  - LeetCode OOP problems – <https://leetcode.com/tag/object-oriented/>

## E. Practical laboratories
### Beginner
1. Create a `Person` class with `first_name`, `last_name` attributes and a `full_name()` method.
### Intermediate
2. Implement a class hierarchy `Vehicle -> Car, Truck, Motorcycle` demonstrating inheritance and method overriding.
### Challenge
3. Build a `shapes` package with abstract base class `Shape` and concrete classes `Circle`, `Rectangle`, `Triangle`. Include area/perimeter methods, and a factory function `create_shape(type, **kwargs)`.
### Independent implementation
4. Write unit‑tests for the `shapes` package using `pytest` and achieve 90 % coverage. Provide a `README.md` with installation instructions and usage examples.

## F. Weekly assignment
**Problem statement**: Create a reusable *Task Scheduler* library.
- Design an abstract base class `Scheduler` with methods `schedule(task, delay)` and `run()`.
- Provide two concrete implementations: `InMemoryScheduler` (stores tasks in a list) and `ThreadedScheduler` (executes tasks in separate threads after the delay).
- Include a CLI `schedule-cli` that reads a JSON file of tasks (command, arguments) and schedules them using the chosen scheduler via a command‑line flag.
- Write comprehensive documentation (`SCHEDULER.md`) with class diagrams (Mermaid) and usage examples.
- Add unit‑tests covering both scheduler implementations and CLI parsing.

**Acceptance criteria**
- Library installs via `pip install -e .` and exposes `schedule-cli` entry point.
- Both scheduler classes pass functional tests and handle edge cases (negative delay, invalid task).
- Documentation includes clear diagrams and a 300‑word design rationale.
- Test coverage ≥ 80 %.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| OOP coding exercise – implement `Vehicle` hierarchy (auto‑graded) | 25 % |
| Scheduler library functional test | 30 % |
| Documentation & diagram quality | 20 % |
| Peer code review (optional) | 10 % |

**Rubric highlights**
- Correct use of inheritance and polymorphism (10 pts).
- Proper abstract base class design (5 pts).
- CLI parses arguments robustly (5 pts).
- Documentation includes accurate Mermaid class diagram (5 pts).
- Code style compliance (5 pts).

## H. Completion gate
Submit a public GitHub link to the *Task Scheduler* repository; CI must show all checks passing and the assessment score ≥ 70 %.

## I. Weekly retrospective
1. Which OOP concept was most challenging to implement correctly?
2. How did you decide between inheritance and composition in your designs?
3. What difficulties did you encounter when writing tests for abstract classes?
4. Identify an area of SOLID you would like to explore further.

---
*Next week:* **Week 05 – HTML, CSS and Web Foundations** (see `syllabus/phase-02/week-05.md`).