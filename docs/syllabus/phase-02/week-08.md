# Week 08 – SQL, Relational Database Design and PostgreSQL

## A. Week overview
- **Week number:** 8
- **Week title:** SQL, Relational Database Design and PostgreSQL
- **Phase:** Month 2 – Web Technologies, Networking and Database Fundamentals
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner‑intermediate
- **Prerequisites:** Completion of Week 07; basic command‑line experience.

## B. Learning objectives
- Write SELECT, INSERT, UPDATE, DELETE statements using PostgreSQL syntax.
- Model relational data: entities, attributes, primary/foreign keys, normalization (1NF‑3NF).
- Create tables, indexes, and constraints via `psql`.
- Use `psql` meta‑commands for schema inspection and query planning (`EXPLAIN`).
- Connect to PostgreSQL from Python using `psycopg2` and perform CRUD operations.
- Understand transaction isolation levels and ACID properties.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Introduction to relational databases – tables, rows, columns, primary keys. |
| 2 | SQL basics – SELECT, WHERE, ORDER BY, LIMIT, aliasing. |
| 3 | Filtering – BETWEEN, IN, LIKE, pattern matching, NULL handling. |
| 4 | Aggregation – GROUP BY, HAVING, COUNT, SUM, AVG, MIN, MAX. |
| 5 | Joins – INNER, LEFT, RIGHT, FULL OUTER, self‑joins, cross joins. |
| 6 | Data modification – INSERT, UPDATE, DELETE, RETURNING clause. |
| 7 | Database design – entity‑relationship diagram, normalization, foreign keys. |
| 8 | Indexes – B‑tree, GIN, GiST, when to use them, `EXPLAIN ANALYZE`. |
| 9 | Transactions – BEGIN, COMMIT, ROLLBACK, savepoints, isolation levels. |
|10 | Connecting from Python – `psycopg2` basics, connection pooling, parameterised queries. |
|11 | Lab day – design a simple schema for a blog platform and implement CRUD via Python script. |
|12 | Review & documentation – write `POSTGRESQL_OVERVIEW.md` with ER diagram (Mermaid) and sample queries.

## D. Learning materials
- **Official docs**: <https://www.postgresql.org/docs/current/sql.html>, <https://www.postgresql.org/docs/current/tutorial.html>.
- **Tutorials**:
  - “SQLBolt” interactive lessons – <https://sqlbolt.com/> (covers SELECT‑JOIN basics).
  - “PostgreSQL Tutorial” – <https://www.postgresqltutorial.com/>.
- **Videos**:
  - freeCodeCamp – PostgreSQL Full Course – <https://www.youtube.com/watch?v=qw--VYLpxG4>.
  - Traversy Media – PostgreSQL Crash Course – <https://www.youtube.com/watch?v=qw--VYLpxG4> (same link, but fine).
- **Exercises**:
  - Mode Analytics SQL practice – <https://mode.com/sql-tutorial/>.
  - LeetCode database problems – <https://leetcode.com/tag/database/>.

## E. Practical laboratories
### Beginner
1. Create a `books` table and insert three rows using `psql`.
### Intermediate
2. Write a query that returns authors with at least two books, using GROUP BY and HAVING.
### Challenge
3. Implement a Python script `blog.py` that creates tables (`users`, `posts`), inserts sample data, and performs a join to list posts with author names.
### Independent implementation
4. Produce an ER diagram (Mermaid) for a more complex e‑commerce schema and generate the corresponding SQL DDL statements.

## F. Weekly assignment
**Problem statement**: Build a *Task Tracker* API backed by PostgreSQL.
- Provide endpoints: `GET /tasks`, `POST /tasks`, `PUT /tasks/:id`, `DELETE /tasks/:id` (you may simulate with a simple Python script using `psycopg2` – no web server required).
- Design a normalized schema (`tasks` table with `id`, `title`, `description`, `status`, `created_at`).
- Include unit‑tests that verify CRUD operations.
- Document the schema and sample queries in `SCHEMA.md`.

**Acceptance criteria**
- All CRUD functions work and are covered by tests (≥ 80 % coverage).
- Schema follows 3NF and includes appropriate constraints (PK, NOT NULL).
- `SCHEMA.md` contains a Mermaid ER diagram and a rationale for design choices.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| SQL query writing exercise (auto‑graded) | 20 % |
| Python CRUD script functional test | 30 % |
| Documentation & ER diagram quality | 20 % |
| Peer review (optional) | 15 % |

**Rubric highlights**
- Correct SELECT/JOIN queries (10 pts).
- Proper use of constraints and indexes (5 pts).
- Python script uses parameterised queries to avoid SQL injection (5 pts).
- ER diagram clarity (5 pts).
- Test coverage and passing CI (5 pts).

## H. Completion gate
Submit a GitHub repo URL; CI must pass linting (`flake8`), tests, and the overall assessment score ≥ 70 %.

## I. Weekly retrospective
1. Which SQL clause did you find most powerful for data analysis?
2. What difficulties did you encounter when modelling relationships?
3. How did you ensure your Python code handled database errors safely?
4. What would you change in your schema if the application scaled to millions of rows?

---
*Next week:* **Week 09 – Backend Engineering and FastAPI** (see `syllabus/phase-03/week-09.md`).