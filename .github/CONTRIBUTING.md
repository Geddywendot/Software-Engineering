# Contributing Guidelines

We welcome contributions from all three learners and the broader community. Please follow these steps when contributing:

1. **Fork the repository** (if you are not a direct collaborator).
2. **Create a feature branch** named `feat/<short-description>`.
3. **Make your changes** – add lessons, assignments, documentation, or code.
4. **Run the documentation build locally** (`mkdocs build`) to ensure no broken links.
5. **Commit with a clear message** and push the branch.
6. **Open a Pull Request** targeting `main`.
7. Ensure the PR passes all CI checks and that the PR template is filled out.

### Code Style
- Use 2‑space indentation for Markdown and YAML.
- Keep line length ≤ 120 characters.
- Follow the existing naming conventions for files and directories.

### Review Process
- At least one learner must review the PR before merging.
- Address any feedback and ensure the documentation builds without errors.

### Release Process
- The `main` branch is the source for GitHub Pages.
- Merges to `main` automatically trigger a site rebuild via GitHub Actions.
