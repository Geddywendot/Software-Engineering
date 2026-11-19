# Learner Structure

The programme accommodates **exactly three learners**. Each learner is identified by a configurable identifier that they can personalise with their own name and GitHub username.

```yaml
learners:
  - id: learner-1
    name: "<Your Name>"
    github_username: "<your-github>"
  - id: learner-2
    name: "<Your Name>"
    github_username: "<your-github>"
  - id: learner-3
    name: "<Your Name>"
    github_username: "<your-github>"
```

*Instructions for learners*
1. Open this file in the repository (`docs/assessment-collaboration/learner-structure.md`).
2. Replace the placeholder values (`<Your Name>` and `<your-github>`) with your real name and GitHub handle.
3. Commit the changes on a personal feature branch (e.g., `learners/learner-1-profile`) and open a pull request for review.

These identifiers are used throughout the assessment system to attribute contributions, grades, and journal entries to the correct participant.
