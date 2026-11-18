# Week 18 – Docker and Containerisation

## A. Week overview
- **Week number:** 18
- **Week title:** Docker and Containerisation
- **Phase:** Month 5 – Professional Software Engineering, Architecture and DevOps
- **Estimated hours:** 18‑20 h
- **Difficulty:** Intermediate
- **Prerequisites:** Week 17 (Software Architecture) completed.

## B. Learning objectives
- Understand container concepts, images, layers, and registries.
- Write efficient Dockerfiles for multi‑stage builds.
- Use Docker Compose to orchestrate multi‑service applications.
- Apply best practices for security, size reduction, and caching.
- Debug containers and troubleshoot common issues.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | Container fundamentals – namespaces, cgroups, image layers. |
| 2 | Dockerfile syntax – FROM, RUN, COPY, CMD, ENTRYPOINT, ARG, ENV. |
| 3 | Multi‑stage builds for Node/React and Python/FastAPI. |
| 4 | Docker Compose basics – services, networks, volumes. |
| 5 | Managing environment variables and secrets in containers. |
| 6 | Image optimisation – minimal base images, .dockerignore, layer caching. |
| 7 | Security hardening – non‑root users, read‑only filesystems, scanning with Trivy. |
| 8 | Debugging containers – logs, exec, healthchecks. |
| 9 | Lab: Containerise the Todo app (Week 16) with separate frontend, backend, db services. |
|10 | Review, documentation, and retrospective.

## D. Learning materials
- **Official docs:** <https://docs.docker.com/>
- **Tutorials:**
  - Docker Get Started – Docker: <https://docs.docker.com/get-started/>
  - “Dockerizing a Python Web App” – Real Python: <https://realpython.com/dockerizing-python-web-applications/>
- **Videos:**
  - "Docker Tutorial for Beginners" – Traversy Media: <https://www.youtube.com/watch?v=3c-iBn73dDE>
- **Exercises:**
  - Build a minimal Alpine‑based Node image.
  - Scan an image with Trivy: <https://github.com/aquasecurity/trivy>.

## E. Practical laboratories
### Beginner
1. Write a Dockerfile for a static HTML site.
### Intermediate
2. Create a multi‑stage Dockerfile for a React‑TypeScript app.
### Challenge
3. Refactor the Full‑stack app (Week 16) to use Docker Compose with separate PostgreSQL service, applying security best practices.
### Independent implementation
4. Set up a CI step that builds and pushes the Docker images to Docker Hub.

## F. Weekly assignment
**Problem statement:** Containerise the *Book Review* full‑stack application from Week 15.
- Create Dockerfiles for both FastAPI backend and React‑TypeScript frontend using multi‑stage builds.
- Write a `docker-compose.yml` that defines services: `frontend`, `backend`, `db`.
- Include environment handling for development and production.
- Provide a `README.md` with build and run instructions.

**Acceptance criteria**
- `docker compose up` launches a functional app accessible at `http://localhost:3000`.
- Images are under 200 MB each.
- Security scan reports no critical vulnerabilities.
- Documentation includes a Mermaid diagram of the container architecture.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (container basics) | 15 % |
| Dockerfile correctness & optimisation | 30 % |
| Docker Compose orchestration | 20 % |
| Security hardening & scanning | 15 % |
| Documentation & diagram | 10 % |
| Automated build script | 10 % |

**Rubric highlights**
- Clean multi‑stage Dockerfile (10 pts).
- Proper service isolation and networking (10 pts).
- Secure configuration (5 pts).
- Effective documentation (5 pts).

## H. Completion gate
Push repository; CI must build Docker images and run security scan successfully.

## I. Weekly retrospective
1. Which Dockerfile optimisation gave the biggest size reduction?
2. How did Compose simplify local development?
3. What security considerations emerged when handling secrets?
4. What would you change for a production‑grade deployment?

---
*Next week:* **Week 19 – CI/CD, GitHub Actions and Deployment** (see `syllabus/phase-05/week-19.md`).