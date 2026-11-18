# Week 12 – Testing, Debugging and Backend Quality

## A. Week overview
- **Week number:** 12
- **Week title:** Testing, Debugging and Backend Quality
- **Phase:** Month 3 – Backend Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Week 11 completed; functional FastAPI backend.

## B. Learning objectives
- Write unit, integration, and functional tests using `pytest` and FastAPI `TestClient`.
- Apply test‑driven development (TDD) to backend features.
- Use coverage tools (`pytest-cov`) to measure code coverage.
- Debug FastAPI applications with `pdb`, VS Code debugger, and logging.
- Implement property‑based testing with `hypothesis`.
- Apply linting (`flake8`/`black`) and static analysis (`mypy`, `bandit`).

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Testing philosophy – unit vs. integration vs. end‑to‑end. |
| 2 | Setting up `pytest` – fixtures, `conftest.py`, test discovery. |
| 3 | Writing unit tests for pure functions and services. |
| 4 | Testing FastAPI routes with `TestClient`. |
| 5 | Mocking external calls using `unittest.mock` and `pytest-mock`. |
| 6 | Property‑based testing with `hypothesis`. |
| 7 | Measuring coverage – `pytest-cov`, interpreting reports. |
| 8 | Debugging techniques – `pdb`, VS Code breakpoints, logging best practices. |
| 9 | Continuous integration – configuring GitHub Actions for test, lint, coverage. |
|10 | Lab day – refactor the Todo API to be fully covered with tests and CI workflow. |
|11 | Review & documentation – write `TESTING_OVERVIEW.md` with a Mermaid flowchart of the test pipeline.

## D. Learning materials
- **Official docs**: <https://docs.pytest.org/en/stable/>, <https://fastapi.tiangolo.com/tutorial/testing/>.
- **Tutorials**:
  - Real Python – Testing FastAPI – <https://realpython.com/fastapi-testing/>.
  - “Python Testing with pytest” – freeCodeCamp – <https://www.youtube.com/watch?v=etosV2IWBF0>.
- **Videos**:
  - Corey Schafer – Testing in Python – <https://www.youtube.com/watch?v=etosV2IWBF0>.
- **Exercises**:
  - `pytest` kata – <https://github.com/ehmatthes/pcc/tree/master/03_05_testing>
  - `hypothesis` tutorial – <https://hypothesis.readthedocs.io/en/latest/>.

## E. Practical laboratories
### Beginner
1. Write a unit test for a pure function `add(a, b)` using `assert`.
### Intermediate
2. Create a fixture that provides a temporary SQLite database for integration tests.
### Challenge
3. Use `hypothesis` to test a function that validates email addresses against many edge cases.
### Independent implementation
4. Add a full test suite to the Book Library API covering models, routes, and authentication, achieving ≥ 90 % coverage. Include a GitHub Actions workflow that runs tests, lints, and uploads coverage to Codecov.

## F. Weekly assignment
**Problem statement**: Enhance the *Book Library* API with a comprehensive test suite.
- Write unit tests for all service functions.
- Write integration tests for each endpoint using FastAPI `TestClient`.
- Include property‑based tests for input validation.
- Configure a CI pipeline (`.github/workflows/ci.yml`) that runs:
  - `pytest --cov=app`
  - `flake8`
  - `mypy`
  - `bandit -r .`
- Document the testing strategy in `TESTING_STRATEGY.md` with a Mermaid diagram of the CI pipeline.

**Acceptance criteria**
- Test coverage ≥ 90 % (excluding `tests/`).
- CI pipeline passes on every push.
- Documentation clearly explains how to run tests locally and interpret results.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 10 % |
| Unit testing implementation (auto‑graded) | 20 % |
| Integration test suite for API | 30 % |
| Property‑based testing task | 15 % |
| CI pipeline and documentation | 15 % |
| Peer review (optional) | 10 % |

**Rubric highlights**
- Correct test structure and fixtures (10 pts).
- High coverage and passing CI (10 pts).
- Effective use of `hypothesis` (5 pts).
- Clear CI YAML and documentation (5 pts).
- Linting and static analysis compliance (5 pts).

## H. Completion gate
Submit the repo URL; the CI must show a green build and the assessment score must be ≥ 70 %.

## I. Weekly retrospective
1. Which testing technique (unit, integration, property‑based) gave you the most confidence?
2. What difficulties did you encounter when mocking database interactions?
3. How did the CI pipeline affect your development workflow?
4. What improvements would you make to your test coverage strategy?

---
*Next week:* **Week 13 – React Fundamentals** (see `syllabus/phase-04/week-13.md`).