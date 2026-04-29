# Assignment 01: Codex Repo Mapping

## Period

Days 1-7

## Goal

Learn how to use Codex to understand unfamiliar codebases without changing production code.

## Source Repos

- `ee-admin-v5`
- `solar_calculator`

## Tasks

1. Clone both source repos locally.
2. Ask Codex to inspect each repo and produce a repo map.
3. Identify the main app framework, package scripts, database layer, deployment files, and test commands.
4. Create two architecture notes:
   - `submissions/01-codex-repo-map/ee-admin-v5-map.md`
   - `submissions/01-codex-repo-map/solar-calculator-map.md`
5. Create one comparison note:
   - `submissions/01-codex-repo-map/repo-comparison.md`

## Required Discoveries

For `ee-admin-v5`, identify:

- Next.js app structure.
- API routes under `src/app/api`.
- Database connection in `src/lib/db.ts`.
- Drizzle schema in `src/db/schema.ts`.
- Railway config in `railway.json` and `nixpacks.toml`.
- Why `DATABASE_URL` matters during build.

For `solar_calculator`, identify:

- Express server entry point in `server.js`.
- Module structure under `src/modules`.
- Database pool under `src/core/database`.
- Migration runner under `database/run_migrations.js`.
- Docker setup in `Dockerfile` and `docker-compose.yml`.
- Playwright navigation test under `tests/navigation.mobile.spec.js`.

## Codex Practice

Use Codex to answer:

- "What is the fastest safe way to understand this repo?"
- "Which files should I read first?"
- "What commands can I run without secrets?"
- "What parts look risky for a new maintainer?"

## Deliverables

- Repo maps.
- Comparison note.
- Command evidence showing at least:
  - `git status`
  - `npm ci` or explanation if skipped
  - `npm run build` or explanation if blocked
  - available test command output

## Acceptance Criteria

- Aqilah can explain both repos in 5 minutes.
- She can name the app entry point, database layer, deployment config, and test surface.
- She can describe what Codex helped with and what she verified herself.

