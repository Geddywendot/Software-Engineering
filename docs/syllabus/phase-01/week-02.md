# Week 02 – Python Fundamentals and Computational Thinking

## A. Week overview
- **Week number:** 2
- **Week title:** Python Fundamentals and Computational Thinking
- **Phase:** Month 1 – Computer Science and Programming Foundations
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner
- **Prerequisites:** Week 01 completed, working Git repo, Linux terminal.

## B. Learning objectives
- Write syntactically correct Python scripts using variables, data types, and control flow.
- Demonstrate proper use of functions, parameters, return values, and docstrings.
- Apply basic computational‑thinking techniques: decomposition, pattern recognition, abstraction, and algorithm design.
- Use built‑in data structures (list, tuple, dict, set) effectively.
- Perform input/output operations, handle exceptions, and write unit‑tests with `unittest`.
- Document code following PEP 8 and the project's Contributing guidelines.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Python installation, REPL, script execution, `#!/usr/bin/env python3` shebang. |
| 2 | Variables, types, literals, string formatting (`f"..."`). |
| 3 | Control flow – `if/elif/else`, truthiness, ternary operator. |
| 4 | Loops – `for`, `while`, `break`, `continue`, `else` clause on loops. |
| 5 | Functions – definition, positional/keyword arguments, default values, `*args`, `**kwargs`. |
| 6 | Data structures – lists (comprehensions), tuples, dictionaries, sets, common methods. |
| 7 | File I/O – `open`, context managers, reading/writing text & CSV. |
| 8 | Error handling – `try/except/else/finally`, custom exceptions. |
| 9 | Modules & packages – `import`, `from ... import`, creating a package, `__init__.py`. |
|10 | Testing – `unittest` basics, assertions, test discovery, coverage with `pytest‑cov`. |
|11 | Code style – PEP 8, `flake8`, docstrings, type hints with `typing`. |
|12 | Lab day – build a small CLI utility (see section E). |
|13 | Review & documentation – write a technical explanation of Python’s memory model (objects, reference counting, garbage collection). |

## D. Learning materials
- **Official docs**: <https://docs.python.org/3/tutorial/>, <https://docs.python.org/3/library/>.
- **Tutorials**:
  - “Automate the Boring Stuff with Python” (free online chapters) – <https://automatetheboringstuff.com/>
  - “Python for Everybody” – Chapter 1‑5 – <https://www.py4e.com/>.
- **Videos**:
  - Corey Schafer – Python Basics playlist – <https://www.youtube.com/playlist?list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU>
- **Exercises**:
  - Exercism Python track (free) – <https://exercism.org/tracks/python>
  - LeetCode Easy Python problems – <https://leetcode.com/tag/python/>

## E. Practical laboratories
### Beginner
1. Write `hello.py` that prints "Hello, World!" and accepts an optional name argument.
### Intermediate
2. Create a script `wordcount.py` that reads a text file, counts word frequencies, and outputs the top 10 words in JSON format.
### Challenge
3. Implement a simple calculator REPL that supports `+ - * /` and variable assignment, handling invalid input gracefully.
### Independent implementation
4. Build a small package `notescli` with a command `add-note <file> <text>` that appends a timestamped entry to a markdown file, includes unit‑tests, and is installable via `pip install -e .`.

## F. Weekly assignment
**Problem statement**: Develop a personal *Task Tracker* CLI.
- Must support commands: `add`, `list`, `done`, `remove`.
- Persist tasks in a JSON file `tasks.json` in the repository root.
- Include unit‑tests covering each command.
- Use type hints and follow PEP 8.
- Provide a `README.md` with usage examples.

**Acceptance criteria**
- All commands work as specified and handle edge cases (e.g., marking a non‑existent task as done).
- Test coverage ≥ 80 %.
- Code passes `flake8` linting.
- Repository includes a `pyproject.toml` (or `setup.cfg`) defining the console script entry point.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| Coding exercise – `wordcount.py` (auto‑graded) | 25 % |
| CLI implementation test (functional) | 30 % |
| Documentation & code style review | 20 % |
| Peer code review (optional) | 10 % |

**Rubric highlights**
- Correct use of functions and arguments (10 pts).
- Proper error handling and user feedback (10 pts).
- Unit‑tests demonstrate understanding of test‑driven development (10 pts).
- README clearly explains installation and usage (5 pts).
- Code style compliance (5 pts).

## H. Completion gate
Submit a public GitHub link to the *Task Tracker* repository; CI must show all checks passing and the assessment score ≥ 70 %.

## I. Weekly retrospective
1. Which Python feature felt most natural, and which was hardest to grasp?
2. How did you approach designing your CLI’s argument parsing?
3. What improvements could you make to your testing strategy?
4. Identify any remaining gaps in your understanding of Python’s memory model.

---
*Next week:* **Week 03 – Problem Solving, Algorithms and Data Structures** (see `syllabus/phase-01/week-03.md`).