# Week 01 – Git Mechanics & The Unix Philosophy

## A. Week overview
- **Week number:** 1
- **Week title:** Git Mechanics & The Unix Philosophy
- **Phase:** Month 1 – Computer Science and Programming Foundations
- **Estimated hours:** 18‑20 h
- **Difficulty:** Beginner
- **Prerequisites:** None (fresh environment with Git and a Linux terminal installed)

## B. Learning objectives
- Explain the Unix philosophy and how it shapes tool design.
- Manipulate standard streams (`stdin`, `stdout`, `stderr`) and perform redirection.
- Write simple Bash scripts that combine commands with pipes and process substitution.
- Describe Git’s internal data model: objects, refs, HEAD, and the commit graph.
- Perform basic Git operations: add, commit, branch, merge, rebase, and resolve conflicts.
- Document a Git workflow with commit messages that follow a conventional style.

## C. Detailed syllabus
| Day | Topics & Sub‑topics |
|-----|---------------------|
| 1   | **Unix philosophy** – “Do one thing and do it well”, composability, text as data. |
| 2   | **Shell fundamentals** – Bash prompt, command lookup, exit status, quoting. |
| 3   | **Standard streams** – `>` `>>` `<` `2>` `&>`; using `tee`; logging. |
| 4   | **Pipes & redirection** – chaining `|`, `|&`, process substitution `$(…)`, heredocs. |
| 5   | **Shell scripting** – variables, conditionals, loops, functions, script execution permissions. |
| 6   | **Git basics** – repository layout (`.git`), working tree vs. index vs. HEAD. |
| 7   | **Git objects** – blobs, trees, commits, tags; `git cat‑file`. |
| 8   | **Branching mechanics** – `git branch`, `git checkout`, detached HEAD. |
| 9   | **Merging** – fast‑forward, three‑way merge, `git merge --no‑ff`. |
|10   | **Merge conflicts** – conflict markers, `git mergetool`, manual resolution. |
|11   | **Rebasing** – `git rebase`, interactive rebase, when to use. |
|12   | **History rewriting** – `git commit --amend`, `git reset`, `git reflog`. |
|13   | **Collaboration basics** – remote add, `git push`, `git fetch`, `git pull --rebase`. |
|14   | **Commit message conventions** – imperative style, referencing issues. |
|15   | **Lab day** – hands‑on exercises (see section E). |
|16   | **Review & documentation** – write a technical explanation of the Git commit graph for the repo. |

## D. Learning materials
- **Official docs**: 
  - Unix & Bash – <https://www.gnu.org/software/bash/manual/bash.html>
  - Git – <https://git-scm.com/docs>
- **Tutorials**:
  - “The Linux Command Line” (free PDF) – <https://learncodethehardway.org/unix/> 
  - “Pro Git” – Chapter 1‑3 – <https://git-scm.com/book/en/v2>
- **Videos**:
  - Git Basics – freeCodeCamp (YouTube) – <https://www.youtube.com/watch?v=RGOj5yH7evk>
  - Bash Scripting – Corey Schafer – <https://www.youtube.com/watch?v=oxuRxtrO2Ag>
- **Exercises**:
  - Codecademy Bash (free tier) – <https://www.codecademy.com/learn/learn-the-command-line>
  - Git Immersion – <http://gitimmersion.com/>

## E. Practical laboratories
### Beginner
1. Create a directory, initialize a Git repo, add a `README.md`, and make the first commit.
### Intermediate
2. Write a Bash script that reads a text file, counts word frequencies, and writes the result to a new file using pipelines.
### Challenge
3. Simulate a collaborative workflow: clone the repo, create two branches, make conflicting edits to the same line, and resolve the conflict using `git mergetool`.
### Independent implementation
4. Produce a Markdown file `git‑internals.md` that explains, with diagrams (Mermaid), the relationship between blobs, trees, commits, and refs.

## F. Weekly assignment
**Problem statement**: Build a small personal notes repository.
- Create a Git repo `notes`.
- Add at least three Markdown files (`ideas.md`, `tasks.md`, `journal.md`).
- Each file must be created/updated via a Bash script that appends a timestamped entry.
- Use branches to add a new feature (`ideas‑feature`) and merge it back, demonstrating conflict resolution.
- Produce a `report.md` documenting the commit graph (use `git log --graph`) and explaining each step.

**Requirements**
- Bash script must be POSIX‑compatible and include error handling.
- All commits must follow the Conventional Commits format (e.g., `feat: add ideas script`).
- The repo must be pushed to a private branch on your GitHub fork (optional).

**Acceptance criteria**
- Repository contains the three notes files and the script.
- At least two merge commits (one with a conflict) exist.
- `report.md` includes a clear diagram (Mermaid code block) and a 300‑word explanation.

## G. Assessment
| Item | Weight |
|------|--------|
| Conceptual Q&A (5 short answer) | 15 % |
| Bash scripting exercise (auto‑graded) | 25 % |
| Git conflict‑resolution practical test | 30 % |
| Technical explanation document (`report.md`) | 20 % |
| Peer review of a teammate’s repo (optional) | 10 % |

**Rubric highlights**
- Correct use of streams and redirection (5 pts).
- Script handles missing files gracefully (5 pts).
- Merge conflict resolution without data loss (10 pts).
- Explanation demonstrates understanding of Git internals (10 pts).

## H. Completion gate
Learners must submit a public GitHub link to the `notes` repository and pass the assessment rubric with a minimum of **70 %** overall.

## I. Weekly retrospective
1. Which Unix command surprised you the most and why?
2. What difficulties did you encounter when resolving the merge conflict?
3. How could your Bash script be improved for robustness?
4. What concepts from Git internals do you still find unclear?

---
*Next week:* **Week 02 – Python Fundamentals and Computational Thinking** (see `syllabus/phase-01/week-02.md`).