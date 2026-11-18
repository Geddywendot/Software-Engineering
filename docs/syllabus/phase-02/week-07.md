# Week 07 – Networking, HTTP, APIs and Internet Architecture

## A. Week overview
- **Week number:** 7
- **Week title:** Networking, HTTP, APIs and Internet Architecture
- **Phase:** Month 2 – Web Technologies, Networking and Database Fundamentals
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner‑intermediate
- **Prerequisites:** Week 06 completed; basic JavaScript and web fundamentals.

## B. Learning objectives
- Explain the OSI and TCP/IP models and locate HTTP within them.
- Describe how DNS resolves domain names to IP addresses.
- Use browser dev tools to inspect network traffic and understand request/response headers.
- Perform CRUD operations against a RESTful API using `fetch`.
- Understand status codes, content negotiation, CORS, and authentication headers (Bearer token).
- Design a simple API contract (OpenAPI/Swagger) for a hypothetical service.

## C. Detailed syllabus
| Day | Topics |
|-----|--------|
| 1 | OSI vs. TCP/IP layers; IP addressing (IPv4/IPv6). |
| 2 | DNS resolution, host files, `dig`/`nslookup` basics. |
| 3 | TCP handshake, UDP vs. TCP, sockets overview. |
| 4 | HTTP fundamentals – methods, status codes, headers, cookies. |
| 5 | HTTPS – TLS handshake, certificates, browser security indicators. |
| 6 | REST principles – resources, URIs, statelessness, idempotence. |
| 7 | CORS – same‑origin policy, preflight requests, `Access-Control-*` headers. |
| 8 | API authentication – API keys, Bearer tokens, basic auth. |
| 9 | Using `fetch` for GET, POST, PUT, DELETE; handling JSON bodies. |
|10 | Error handling – network errors, non‑2xx responses, retries. |
|11 | Lab day – build a small front‑end that consumes the public JSONPlaceholder API (https://jsonplaceholder.typicode.com). |
|12 | Review & documentation – write `NETWORKING_OVERVIEW.md` with a Mermaid sequence diagram of an HTTP request/response cycle.

## D. Learning materials
- **Official docs**: <https://developer.mozilla.org/en-US/docs/Web/HTTP>, <https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API>.
- **Tutorials**:
  - MDN “Introduction to HTTP” – <https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview>.
  - “REST API Tutorial” – <https://restfulapi.net/>.
- **Videos**:
  - Computerphile – How the Internet Works – <https://www.youtube.com/watch?v=7_LPdttKXPc>.
  - Traversy Media – HTTP Crash Course – <https://www.youtube.com/watch?v=iYM2zFP3Zn0>.
- **Exercises**:
  - Postman Playground – send requests to JSONPlaceholder – <https://learning.postman.com/docs/getting-started/introduction/>.
  - curl practice – <https://curl.se/docs/manpage.html>.

## E. Practical laboratories
### Beginner
1. Use `curl` to perform a GET request to `https://api.github.com` and print the HTTP status code.
### Intermediate
2. Write a JS function `fetchPosts()` that retrieves posts from JSONPlaceholder and renders titles in a list.
### Challenge
3. Implement a small client that performs a full CRUD cycle against the JSONPlaceholder `/posts` endpoint, handling errors gracefully.
### Independent implementation
4. Draft an OpenAPI (Swagger) specification (`api.yaml`) for a minimal “Todo” service (GET/POST/PUT/DELETE) and validate it with `swagger-cli`.

## F. Weekly assignment
**Problem statement**: Create a *News Aggregator* front‑end.
- Use the free NewsAPI (https://newsapi.org) to fetch top headlines for a user‑selected country.
- Implement a dropdown to select the country, fetch articles via `fetch`, and display them in a responsive card layout.
- Show loading spinners, handle API errors, and respect the rate limit.
- Write a short OpenAPI contract (`newsapi.yaml`) describing the endpoints you consume.
- Include a `README.md` with setup steps and a `REPORT.md` explaining HTTP flow, CORS handling, and security considerations (API key storage).

**Acceptance criteria**
- Application works in modern browsers without console errors.
- API key is stored in an `.env` file and injected at build time (use a simple script to replace placeholder). No key is committed.
- Linting (`eslint`) passes, and a Jest test validates that the fetch function correctly parses JSON.
- Documentation includes a Mermaid sequence diagram of the request/response.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answers) | 15 % |
| JavaScript fetch coding test (auto‑graded) | 25 % |
| OpenAPI spec creation & validation | 20 % |
| Functional demo of News Aggregator | 30 % |
| Documentation quality | 10 % |

**Rubric highlights**
- Correct use of HTTP methods and status handling (10 pts).
- Secure handling of API key (5 pts).
- Accurate OpenAPI definition (5 pts).
- Responsive UI and loading states (5 pts).
- Linting and testing compliance (5 pts).

## H. Completion gate
Push the repo, open a PR to the curriculum repo, and achieve a minimum score of **70 %**.

## I. Weekly retrospective
1. Which part of the HTTP request/response cycle was most confusing?
2. How did you address CORS issues when calling the API?
3. What improvements could you make to error handling in your fetch logic?
4. Reflect on the usefulness of OpenAPI for communication with teammates.

---
*Next week:* **Week 08 – SQL, Relational Database Design and PostgreSQL** (see `syllabus/phase-02/week-08.md`).