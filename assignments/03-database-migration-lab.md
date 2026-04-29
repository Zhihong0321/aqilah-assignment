# Assignment 03: Database And Migration Lab

## Period

Days 15-21

## Goal

Build safe database habits: read schema, write reversible SQL, run migrations locally, and understand data risk.

## Safety Rule

Only use a local database or a disposable test database. Never use production database credentials.

## Tasks

1. Read migration files from both source repos.
2. Explain how each repo tracks or runs migrations.
3. Create a toy local schema for a `maintenance_ticket` table.
4. Write an `up` migration and a rollback note.
5. Use Codex to review the SQL for risk.
6. Run the migration only against a local or disposable database if available.

## Required Files

Create:

- `submissions/03-database-migration-lab/migration-comparison.md`
- `submissions/03-database-migration-lab/001_create_maintenance_ticket.sql`
- `submissions/03-database-migration-lab/rollback-plan.md`
- `submissions/03-database-migration-lab/db-validation.md`

## Required SQL Concept

The table should include:

- `id`
- `repo_name`
- `title`
- `status`
- `priority`
- `created_at`
- `updated_at`

## Codex Practice

Ask Codex to:

- Explain the difference between schema definition and migration file.
- Review the SQL for idempotency.
- Suggest indexes.
- Suggest a rollback plan.

## Acceptance Criteria

- Aqilah can explain `ALTER TABLE`, `CREATE INDEX`, transactions, and rollback risk.
- She can explain why migrations must be reviewed before production.
- She can show command evidence or clearly mark the DB run as `ASSUMED` if no local DB is available.

