# GitHub Collaboration Workflow

The following workflow standardises how learners collaborate on the repository using GitHub.

## 1. Issue creation
- **Title format:** `Learner‑X – <Brief description>`
- **Labels:** `task`, `learner-1/2/3` (as appropriate).
- **Description:** Include acceptance criteria, resources, and any design sketches.
- Assign the issue to the learner responsible for implementation.

## 2. Feature branch creation
```bash
# From the main branch
git checkout main
git pull origin main
# Create a branch scoped to the learner and task
git checkout -b learner-1/<issue-id>-<short-description>
```
- Use kebab‑case for the branch name.
- Branches are short‑lived; they should be merged or deleted after the PR.

## 3. Implementation & testing
- Write code following the project’s coding standards (see the Engineering Handbook).
- Add unit/integration tests covering new functionality.
- Run locally: `npm test` for frontend, `pytest` for backend.

## 4. Commit
- Write a **meaningful message**:
  - `feat: add inventory filtering UI`
  - `fix: resolve off‑by‑one error in pagination`
- Keep commits atomic; one logical change per commit.

## 5. Pull request
- Push the branch: `git push origin learner-1/<issue-id>-<short-description>`.
- Open a PR targeting `main`.
- Fill the PR template:
  - Summary of changes.
  - Screenshots / API responses.
  - Checklist of tests run.
- **Assign a reviewer** (the designated peer).

## 6. Peer review
- Reviewers must leave at least one **comment** and an **LGTM** (Looks Good To Me) approval.
- Suggest improvements; the author must address all required changes before merging.

## 7. Revision & merge
- After addressing feedback, push additional commits.
- Once approved, the author merges using the **Squash and merge** option to keep a linear history.
- Delete the feature branch on GitHub.

## 8. Documentation update
- Update the relevant module README or the project wiki.
- Add a link to the documentation in the PR description.

## 9. Continuous Integration
- The CI pipeline (see `ci-cd.md`) runs lint, type‑check, tests, and security scans on every PR.
- The merge is only allowed after the CI status is **green**.

## 10. Issue closure
- After successful merge, close the original issue and add a comment linking to the merged PR.

---
*All learners must follow this workflow for every task to ensure traceability and accountability.*