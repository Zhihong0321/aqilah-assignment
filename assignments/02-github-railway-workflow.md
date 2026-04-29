# Assignment 02: GitHub And Railway Workflow

## Period

Days 8-14

## Goal

Practice normal developer workflow: branch, commit, pull request, environment variables, deployment checks, and rollback thinking.

## Tasks

1. Create a new branch in this assignment repo named `aqilah/02-github-railway-workflow`.
2. Create a fake Railway deployment checklist for both source repos.
3. Document the environment variables each repo needs.
4. Explain what should happen before a deploy, during deploy, and after deploy.
5. Create a simulated incident note: "Build fails because `DATABASE_URL` is missing."

## Required Files

Create:

- `submissions/02-github-railway-workflow/railway-checklist-ee-admin-v5.md`
- `submissions/02-github-railway-workflow/railway-checklist-solar-calculator.md`
- `submissions/02-github-railway-workflow/github-pr-checklist.md`
- `submissions/02-github-railway-workflow/missing-database-url-incident.md`

## Required Content

For `ee-admin-v5`, include:

- Build command: `npm run build`.
- Start command: `npm start`.
- Healthcheck path: `/api/health`.
- Required env examples: `DATABASE_URL`, `JWT_SECRET`, `UNIAPI_KEY`.
- Note that a dummy `DATABASE_URL` can allow build collection, but real runtime needs a valid database.

For `solar_calculator`, include:

- Build command: `npm run build`.
- Start command: `npm start`.
- Database migration command: `npm run db:migrate -- <migration.sql>`.
- Docker local setup using `docker-compose.yml`.
- Note that production PostgreSQL uses SSL when `NODE_ENV=production`.

## Codex Practice

Ask Codex to:

- Review the deployment files.
- Identify missing or risky deployment assumptions.
- Draft a PR checklist.
- Draft a rollback checklist.

## Deliverables

- Four markdown files.
- At least one Git commit.
- Pull request description using the template in this repo.

## Acceptance Criteria

- Aqilah can explain the difference between build-time and runtime environment variables.
- She can explain how to inspect Railway logs before guessing a fix.
- She can create a clean PR and describe validation evidence.

