# Week 03 – Problem Solving, Algorithms and Data Structures

## A. Week overview
- **Week number:** 3
- **Week title:** Problem Solving, Algorithms and Data Structures
- **Phase:** Month 1 – Computer Science and Programming Foundations
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner‑intermediate
- **Prerequisites:** Completion of Weeks 01‑02, comfortable with basic Python syntax.

## B. Learning objectives
- Decompose real‑world problems into algorithmic steps.
- Analyse algorithmic complexity using Big‑O notation.
- Implement common data structures (lists, stacks, queues, linked lists, trees, graphs) in Python.
- Write recursive and iterative solutions for sorting and searching.
- Evaluate trade‑offs of different data structures for given workloads.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Problem‑solving methodology – decomposition, abstraction, pattern recognition. |
| 2 | Introduction to algorithmic complexity – time vs. space, Big‑O basics, best/average/worst case. |
| 3 | Linear data structures – arrays (Python lists) and their operations. |
| 4 | Stacks and queues – implementation with `list` and `collections.deque`. |
| 5 | Linked lists – singly‑linked implementation, traversal, insertion, deletion. |
| 6 | Trees – binary tree concepts, traversals (pre‑order, in‑order, post‑order) using recursion. |
| 7 | Graph basics – adjacency list representation, BFS and DFS algorithms. |
| 8 | Sorting algorithms – insertion sort, selection sort, bubble sort (O(n²)). |
| 9 | Efficient sorts – merge sort and quicksort (O(n log n)). |
|10 | Searching – linear search vs. binary search (requires sorted data). |
|11 | Recursion depth, tail‑recursion, stack overflow prevention. |
|12 | Lab day – implement a mini library `algos.py` covering the above structures and algorithms. |
|13 | Review & documentation – write a Markdown file `algorithms‑overview.md` with Mermaid diagrams of a binary tree and a graph. |

## D. Learning materials
- **Official docs**: <https://docs.python.org/3/tutorial/datastructures.html>
- **Tutorials**:
  - “Algorithms, Part I” (Stanford, free) – <https://online.stanford.edu/courses/soe-ycsalgorithms1>
  - “Big O Cheat Sheet” – <https://www.bigocheatsheet.com/>
- **Videos**:
  - Abdul Bari – Data Structures and Algorithms Playlist – <https://www.youtube.com/playlist?list=PLlrxD0HtieHjc6AqSj5lZyM8bTQJ8gHk>
- **Exercises**:
  - HackerRank “Data Structures” – <https://www.hackerrank.com/domains/tutorials/10-days-of-python>
  - LeetCode Easy – <https://leetcode.com/tag/algorithm/>

## E. Practical laboratories
### Beginner
1. Implement a stack using a Python list with `push`, `pop`, `peek` operations.
### Intermediate
2. Write a function `reverse_linked_list(head)` that reverses a singly‑linked list in‑place.
### Challenge
3. Implement BFS and DFS traversals for an undirected graph; output the order of visited nodes.
### Independent implementation
4. Create a module `algos.py` containing:
   - `insertion_sort`, `merge_sort`, `binary_search`
   - `Stack`, `Queue`, `LinkedList`, `BinaryTree`
   - Unit‑tests for each implementation using `unittest`.

## F. Weekly assignment
**Problem statement**: Build a *Contact Manager* command‑line tool.
- Store contacts (name, email, phone) in a JSON file.
- Support commands: `add`, `list`, `search <query>`, `delete <id>`.
- Use a binary search tree (self‑implemented) to store contacts in memory for fast lookup.
- Provide unit‑tests covering all CLI operations.
- Document the data‑structure choice and complexity analysis in `REPORT.md`.

**Acceptance criteria**
- All commands work and persist changes to the JSON file.
- Tree insertion and search are O(log n) on average.
- Test coverage ≥ 85 %.
- `REPORT.md` contains Mermaid diagram of the BST and a 300‑word justification.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| Coding task – implement `reverse_linked_list` (auto‑graded) | 25 % |
| Full CLI functional test | 30 % |
| Documentation & complexity analysis | 20 % |
| Peer review (optional) | 10 % |

**Rubric highlights**
- Correct implementation of data structures (15 pts).
- Accurate Big‑O analysis in report (10 pts).
- Robust error handling (10 pts).
- Clean, PEP 8‑compliant code (5 pts).

## H. Completion gate
Submit a public GitHub link to the *Contact Manager* repo; CI must pass all checks and the overall assessment score ≥ 70 %.

## I. Weekly retrospective
1. Which algorithm was most intuitive, and which required the most debugging?
2. How did recursion affect your problem‑solving approach?
3. What challenges did you face when visualising data structures?
4. Identify one data‑structure you would like to explore deeper.

---
*Next week:* **Week 04 – Object‑Oriented Programming, Modules and Software Construction** (see `syllabus/phase-01/week-04.md`).