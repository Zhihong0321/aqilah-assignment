# Assignment 05: ee-admin-v5 Maintenance Lab

## Period

Days 29-35

## Goal

Practice safe maintenance work on a Next.js admin repo with database-backed pages and sync features.

## Source Context

`ee-admin-v5` includes:

- Next.js app router.
- TypeScript and React.
- API routes under `src/app/api`.
- Drizzle schema under `src/db/schema.ts`.
- PostgreSQL pool under `src/lib/db.ts`.
- Bubble sync and migration utilities.
- Railway deployment config.

## Tasks

1. Create a maintenance map for one module:
   - recommended module: `users`, `payments`, `seda`, `sync`, or `catalog`.
2. Pick one low-risk improvement from `FEATURE-TRACKER.md`.
3. Do not implement in the real repo. Instead, write a proposed fix plan in this assignment repo.
4. Create a small mock function or pseudo-test that proves the logic.
5. Ask Codex to review your plan for production risk.

## Recommended Homework Scenario

Use the array-field file sync item from `FEATURE-TRACKER.md`:

- Understand the issue: Bubble may return array fields as comma-separated strings.
- Write a small parser function in this assignment repo.
- Test inputs:
  - single URL string
  - comma-separated URL string
  - array of URLs
  - empty/null input
  - malformed URL

## Required Files

Create:

- `submissions/05-ee-admin-maintenance-lab/module-map.md`
- `submissions/05-ee-admin-maintenance-lab/proposed-fix-plan.md`
- `submissions/05-ee-admin-maintenance-lab/array-url-parser.js`
- `submissions/05-ee-admin-maintenance-lab/array-url-parser-test-notes.md`
- `submissions/05-ee-admin-maintenance-lab/risk-review.md`

## Codex Practice

Ask Codex to:

- Trace the relevant production files.
- Explain the bug in plain language.
- Propose the smallest safe fix.
- Generate test cases.
- Review the patch for hidden production risk.

## Acceptance Criteria

- Aqilah can explain the module flow and where data enters/leaves.
- She can design a fix without touching production.
- She can identify edge cases and test them.
- She can explain what she would need before making the real repo change.

