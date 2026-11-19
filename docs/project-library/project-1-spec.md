# Project 1 – Personal Finance CLI

**Level:** Beginner  
**Relevant weeks:** 2 – 4  
**Estimated effort:** 10‑15 hours

## Problem statement
Learners will build a command‑line application that helps individuals track personal finances. The tool must allow users to record transactions, categorize expenses, set budgets, and generate summary reports.

## Target users
- Individuals who want a lightweight, offline way to monitor spending.
- Students learning Python who need a concrete, data‑driven project.

## Functional requirements
1. Record a transaction (date, amount, category, description).
2. Create, edit, delete expense categories.
3. Display a list of transactions with optional filtering by date or category.
4. Calculate total expenses per category and overall.
5. Define a monthly budget per category and warn when exceeded.
6. Export a summary report (plain‑text or CSV).

## Non‑functional requirements
- Runs on any modern Linux/macOS/Windows terminal.
- Persists data locally (JSON or SQLite) with graceful error handling.
- Input validation with clear error messages.
- Unit‑tested core logic (≥ 80 % coverage).

## User stories (example)
- *As a user, I can add a new expense so that I track my spending.*
- *As a user, I can view my total spending for the current month.*
- *As a user, I receive a warning when I exceed my budget for a category.*

## Acceptance criteria
- All functional requirements are implemented.
- The CLI provides a `--help` command with usage details.
- Invalid inputs are caught and reported without crashing.
- Unit tests cover each command path.
- Documentation includes installation instructions and a usage guide.

## Architecture proposal
- **Modules:** `cli.py` (argument parsing), `models.py` (data classes), `storage.py` (persistence), `budget.py` (calculations), `reports.py` (output).
- **Design pattern:** Simple layered architecture – UI → Service → Repository.

## Data design
- **Transaction:** id (int), date (ISO‑8601), amount (float), category_id (int), description (str).
- **Category:** id (int), name (str), monthly_budget (float, optional).
- Storage: JSON file (`data.json`) or SQLite DB (`finance.db`).

## API specification (if using a module‑level API)
| Endpoint | Description |
|----------|-------------|
| `add_transaction(tx: Transaction)` | Persist a new transaction |
| `list_transactions(filter: dict)` | Return transactions matching filter |
| `add_category(cat: Category)` | Persist a new category |
| `get_budget_report(month: str)` | Return totals and budget warnings |

## Security considerations
- No network access; ensure data files are stored with appropriate file permissions.
- Validate and sanitize all user‑provided strings before writing to disk.

## Testing plan
- **Unit tests** for each module using `pytest`.
- **Integration test** exercising the full CLI flow via `subprocess`.
- **Edge cases**: zero/negative amounts, missing fields, duplicate categories.

## Deployment requirements
- Package as a pip‑installable module (`setup.py` or `pyproject.toml`).
- Provide a `requirements.txt` listing Python 3.11+ dependencies.

## Project milestones
| Milestone | Tasks |
|-----------|-------|
| **M1 – Setup** | Initialise repo, create virtual env, define data model. |
| **M2 – Core CLI** | Implement `add_transaction`, `list_transactions`. |
| **M3 – Category & Budget** | Add category management, budget calculations, warnings. |
| **M4 – Persistence** | Implement JSON/SQLite storage, error handling. |
| **M5 – Reporting** | Export CSV, summary printing. |
| **M6 – Tests & Docs** | Write unit tests, create README with usage guide. |
| **M7 – Polish** | Linting (`ruff`), packaging, CI workflow. |

## Definition of Done
- All acceptance criteria satisfied.
- CI pipeline passes lint, type‑check, tests.
- Documentation is complete and renders on GitHub.
- Project is merged to `main` with a clear commit history.
