# Assignment 07: Incident Debugging Lab

## Period

Days 43-52

## Goal

Practice production-style debugging without production access: read symptoms, inspect logs, form hypotheses, run safe checks, and propose a fix.

## Incident Simulations

Complete three incident reports.

### Incident A: Railway Build Failure

Symptom:

```text
Error: DATABASE_URL environment variable is not set
Failed to collect page data for /api/sync/cron
```

Expected investigation:

- Identify repo: likely `ee-admin-v5`.
- Explain build-time env dependency.
- Check `src/lib/db.ts`.
- Check Railway env vars.
- Propose safe fix or config correction.

### Incident B: Mobile Navigation Regression

Symptom:

```text
Playwright test failed: expected URL to match /my-invoice/
```

Expected investigation:

- Identify repo: likely `solar_calculator`.
- Inspect `tests/navigation.mobile.spec.js`.
- Inspect `public/js/navigation.js`.
- Decide whether failure is app behavior or test setup.

### Incident C: Migration Already Applied With Different Checksum

Symptom:

```text
Migration <file>.sql is already recorded with a different checksum.
```

Expected investigation:

- Identify repo: likely `solar_calculator`.
- Inspect `database/run_migrations.js`.
- Explain why editing applied migration files is risky.
- Propose a new migration instead of changing history.

## Required Files

Create:

- `submissions/07-incident-debugging-lab/incident-a-database-url.md`
- `submissions/07-incident-debugging-lab/incident-b-navigation.md`
- `submissions/07-incident-debugging-lab/incident-c-migration-checksum.md`
- `submissions/07-incident-debugging-lab/debugging-playbook.md`

## Codex Practice

For each incident, ask Codex:

- What are the top 3 likely causes?
- What file should I inspect first?
- What command can verify this safely?
- What should I not do?
- What is the smallest safe fix?

## Acceptance Criteria

- Aqilah can write a calm, structured incident report.
- She can show how evidence changes the hypothesis.
- She avoids risky quick fixes.
- She can explain the difference between mitigation and permanent fix.

