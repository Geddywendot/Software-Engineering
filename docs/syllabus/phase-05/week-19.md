# Week 19 – CI/CD, GitHub Actions and Deployment

## A. Week overview
- **Week number:** 19
- **Week title:** CI/CD, GitHub Actions and Deployment
- **Phase:** Month 5 – Professional Software Engineering, Architecture and DevOps
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Week 18 (Docker and Containerisation) completed.

## B. Learning objectives
- Design CI pipelines with GitHub Actions for linting, testing, building, and deploying.
- Implement automated Docker image builds and pushes to a registry.
- Deploy applications to a cloud platform (Vercel, Render or AWS Elastic Beanstalk) using CI.
- Configure environment‑specific variables and secret management.
- Apply versioning and release tagging strategies.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Overview of CI/CD concepts; GitHub Actions architecture.
| 2 | Writing workflow YAML: jobs, steps, actions, matrix builds.
| 3 | Linting and testing stages for both frontend and backend.
| 4 | Building multi‑stage Docker images in CI.
| 5 | Pushing images to Docker Hub / GitHub Container Registry securely.
| 6 | Deploying a Docker Compose stack to a remote VM via SSH.
| 7 | Deploying a static front‑end to Vercel/GitHub Pages from CI.
| 8 | Environment protection rules, review apps, and approvals.
| 9 | Lab: Create a full CI pipeline for the *Book Review* app (Week 15).
|10 | Review, documentation, and retrospective.

## D. Learning materials
- **Official docs:**
  - GitHub Actions: <https://docs.github.com/en/actions>
  - Docker Hub: <https://docs.docker.com/docker-hub/> 
- **Tutorials:**
  - "CI/CD with GitHub Actions for Docker" – freeCodeCamp: <https://www.freecodecamp.org/news/github-actions-docker-ci-cd/>
- **Videos:**
  - "GitHub Actions Tutorial for Beginners" – Traversy Media: <https://www.youtube.com/watch?v=R8_veQiYbxo>
- **Exercises:**
  - Build a workflow that lints, tests, builds a Docker image and pushes to GHCR.

## E. Practical laboratories
### Beginner
1. Create a simple workflow that runs `npm ci` and `npm test` on push.
### Intermediate
2. Extend the workflow to build a Docker image for the backend and push to GHCR using a secret token.
### Challenge
3. Implement a deployment job that SSH‑es into a remote server and runs `docker compose up -d`.
### Independent implementation
4. Set up a release workflow that creates a Git tag, builds artifacts, and publishes release notes.

## F. Weekly assignment
**Problem statement:** Build a CI/CD pipeline for the *Personal Finance Tracker* app (Week 16).
- Include linting, unit tests, Docker image builds for both services, and deployment to a cloud VM via Docker Compose.
- Use GitHub Secrets for credentials and environment variables.
- Provide a `deployment.md` describing the process and a `workflow.yml` checked into `.github/workflows/`.

**Acceptance criteria**
- Pipeline runs on every push to `main` and passes all stages.
- Images are pushed to GitHub Container Registry.
- Deployment job successfully brings up the app on a remote VM (can be simulated with a local VM).
- Documentation is clear and reproducible.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (CI/CD theory) | 15 % |
| Workflow correctness & completeness | 30 % |
| Secure secret handling | 15 % |
| Deployment automation | 20 % |
| Documentation quality | 10 % |
| Peer review feedback | 10 % |

**Rubric highlights**
- Correct workflow syntax (10 pts).
- Successful image build & push (10 pts).
- Secure secret usage (5 pts).
- Deployment automation works end‑to‑end (5 pts).
- Clear docs and diagrams (5 pts).

## H. Completion gate
Merge the PR containing the workflow; CI must report success on the merge commit.

## I. Weekly retrospective
1. Which CI step was most error‑prone and why?
2. How did secret management affect your pipeline design?
3. What improvements would you make to the deployment strategy?
4. How confident are you in rolling out a production release using this pipeline?

---
*Next week:* **Week 20 – Application Security, Observability and Reliability** (see `syllabus/phase-05/week-20.md`).