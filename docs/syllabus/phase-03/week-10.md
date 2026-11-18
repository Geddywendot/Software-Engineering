# Week 10 – Database Integration, ORM and Migrations

## A. Week overview
- **Week number:** 10
- **Week title:** Database Integration, ORM and Migrations
- **Phase:** Month 3 – Backend Engineering
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Completion of Week 09; a running PostgreSQL instance.

## B. Learning objectives
- Use an ORM (SQLModel/SQLAlchemy) to map Python classes to database tables.
- Perform CRUD operations through the ORM layer.
- Write and apply database migrations with Alembic.
- Understand session management, lazy loading, and eager loading.
- Handle transactions and rollback scenarios in application code.
- Integrate the ORM layer into a FastAPI project.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | ORM concepts – active record vs. data mapper, model definition. |
| 2 | Setting up SQLModel with PostgreSQL – engine, session, BaseModel. |
| 3 | Mapping relationships – one‑to‑many, many‑to‑many, back‑populates. |
| 4 | Querying – filter, order_by, limit, joins, sub‑queries. |
| 5 | Transactions – `session.begin()`, committing, rollbacks, isolation. |
| 6 | Introduction to Alembic – configuration, generating migration scripts. |
| 7 | Writing manual migration scripts – column addition, data migration. |
| 8 | Version control of schema – upgrade/downgrade commands, naming conventions. |
| 9 | Testing ORM code – using `pytest` fixtures and a temporary SQLite DB. |
|10 | Lab day – extend the Todo API (Week 09) to use SQLModel with migrations. |
|11 | Review & documentation – write `ORM_OVERVIEW.md` with ER diagram (Mermaid) and migration flowchart.

## D. Learning materials
- **Official docs**: <https://docs.sqlalchemy.org/en/20/>, <https://fastapi.tiangolo.com/tutorial/sql-databases/>.
- **Tutorials**:
  - "SQLModel Tutorial" – <https://sqlmodel.tiangolo.com/>.
  - Alembic documentation – <https://alembic.sqlalchemy.org/en/latest/>.
- **Videos**:
  - Corey Schafer – SQLAlchemy ORM Basics – <https://www.youtube.com/watch?v=woKYyhLCcnU>.
  - Miguel Grinberg – Flask SQLAlchemy – similar concepts – <https://www.youtube.com/watch?v=Z1RJmh_OqeA>.
- **Exercises**:
  - SQLModel CRUD exercises – <https://github.com/tiangolo/sqlmodel/tree/main/examples>
  - Alembic migration challenges – <https://alembic.sqlalchemy.org/en/latest/tutorial.html>.

## E. Practical laboratories
### Beginner
1. Define a `User` model with `id`, `email`, `hashed_password` and create the table via `SQLModel.metadata.create_all()`.
### Intermediate
2. Write a query to fetch all users whose email domain is `example.com` using ORM filters.
### Challenge
3. Add a many‑to‑many relationship between `User` and `Role` models; write a migration that creates the association table.
### Independent implementation
4. Refactor the Todo API to use SQLModel, add Alembic migrations for schema changes, and write integration tests that run against a temporary Postgres docker container.

## F. Weekly assignment
**Problem statement**: Extend the *Book Library* API (Week 09) to use an ORM and migrations.
- Replace raw SQL with SQLModel models for `Book` and `Author`.
- Implement a many‑to‑many relation (`books_authors`).
- Create Alembic migration scripts for initial schema and a subsequent change (add `published_at` column).
- Write unit‑tests for the new endpoints and a migration test that verifies the schema version.
- Document the migration process in `MIGRATIONS.md` with a Mermaid diagram.

**Acceptance criteria**
- All endpoints work with the ORM and pass tests (≥ 80 % coverage).
- Migrations apply cleanly on a fresh database.
- Documentation includes migration steps and version history.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| ORM implementation task (auto‑graded) | 25 % |
| Alembic migration creation and verification | 20 % |
| Test suite and coverage report | 20 % |
| Documentation quality | 10 % |

**Rubric highlights**
- Correct model definitions and relationships (10 pts).
- Successful migration scripts (5 pts).
- Proper transaction handling in API (5 pts).
- Test coverage and passing CI (5 pts).
- Clear migration documentation (5 pts).

## H. Completion gate
Push the repo, open a PR, and achieve a score of **≥ 70 %**.

## I. Weekly retrospective
1. What difficulties did you encounter when mapping relationships?
2. How did Alembic help keep the database schema under version control?
3. Which part of testing the ORM layer was most challenging?
4. What would you change in your migration workflow for larger teams?

---
*Next week:* **Week 11 – Authentication, Authorisation and Backend Security** (see `syllabus/phase-03/week-11.md`).