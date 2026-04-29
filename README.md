# Aqilah 60-Day Coding AI Onboarding Plan

This repo is the safe assignment workspace for Aqilah's first 60 days in the IT department.

The goal is not to make production changes here. The goal is to train her to use Codex responsibly so she can help maintain, debug, update, and improve the real company repos after she has proven the workflow.

## Real Repos She Is Training For

- `ee-admin-v5`: Next.js 15, React 19, TypeScript, Drizzle ORM, PostgreSQL, Bubble sync, Railway deployment.
- `solar_calculator`: Express, Node.js, PostgreSQL, Docker, Tailwind CSS, Playwright tests, Railway-style deployment.

## 60-Day Outcome

By the end of this plan, Aqilah should be able to:

- Clone and inspect a repo safely.
- Use Codex to map unfamiliar code without blindly trusting it.
- Run build, lint, test, and database checks.
- Understand Railway deployment basics and environment variables.
- Diagnose common production issues from logs and error messages.
- Write small fixes with Codex and verify them locally.
- Create GitHub branches, commits, and pull requests with clear summaries.
- Handle database migrations carefully with backup and rollback thinking.
- Explain what changed, why it changed, and how it was validated.

## Ground Rules

- Never use production secrets in this assignment repo.
- Never push directly to production branches.
- Never run destructive SQL on production databases.
- All assignments are homework simulations unless a manager explicitly approves real repo work.
- Every task must include evidence: command output, screenshots, test results, or a short investigation note.
- Codex can write code, but Aqilah must review, run, and explain it.

## Assignment Flow

Each assignment follows this format:

1. Read the assignment brief.
2. Create a branch in this repo.
3. Use Codex to inspect, plan, and implement the task.
4. Save notes, evidence, and answers under `submissions/<assignment-id>/`.
5. Commit the work.
6. Open a pull request for review.

## Weekly Schedule

| Period | Focus | Assignment |
| --- | --- | --- |
| Days 1-7 | Codex basics and repo mapping | `assignments/01-codex-repo-map.md` |
| Days 8-14 | GitHub workflow and safe DevOps | `assignments/02-github-railway-workflow.md` |
| Days 15-21 | PostgreSQL and migrations | `assignments/03-database-migration-lab.md` |
| Days 22-28 | Testing and debugging | `assignments/04-testing-debugging-lab.md` |
| Days 29-35 | `ee-admin-v5` maintenance simulation | `assignments/05-ee-admin-maintenance-lab.md` |
| Days 36-42 | `solar_calculator` maintenance simulation | `assignments/06-solar-calculator-maintenance-lab.md` |
| Days 43-52 | Production-style incident simulations | `assignments/07-incident-debugging-lab.md` |
| Days 53-60 | Final capstone | `assignments/08-capstone-maintainer-trial.md` |

## Required Submission Files

Each assignment submission should include:

- `notes.md`: what she asked Codex, what she learned, and what she decided.
- `evidence.md`: commands run, test output, screenshots if useful, and validation result.
- `reflection.md`: what went well, what was confusing, and what she would do differently.
- Any code, SQL, docs, or test files created for the assignment.

Use `templates/assignment-submission-template.md` for each assignment.

## Evaluation

Use `rubric.md` to review each assignment.

The most important grading areas are:

- Safety: no production risk.
- Understanding: she can explain the code and data flow.
- Verification: she runs the right checks.
- Git hygiene: clean branch, clear commits, good PR summary.
- Codex judgment: she uses AI as a partner, not as an unquestioned authority.

