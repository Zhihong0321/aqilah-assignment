# Assignment 06: solar_calculator Maintenance Lab

## Period

Days 36-42

## Goal

Practice maintaining an Express app with modules, PostgreSQL, static frontend files, Docker, and Playwright tests.

## Source Context

`solar_calculator` includes:

- `server.js` as the Express entry point.
- Feature modules under `src/modules`.
- Database pools under `src/core/database`.
- Migration runner under `database/run_migrations.js`.
- Tailwind CSS build.
- Playwright navigation tests.
- Docker local environment.

## Tasks

1. Map one module:
   - recommended module: `SolarCalculator`, `Invoicing`, `Health`, `Voucher`, or `ActivityReport`.
2. Create a small maintenance improvement in this assignment repo.
3. Write a test or validation note.
4. Create a mock incident report from a realistic log message.

## Recommended Homework Scenario

Use the solar calculator validation logic:

- Read `src/modules/SolarCalculator/services/solarCalculatorService.js`.
- Identify the input validation rules.
- Recreate a simplified validation function in this assignment repo.
- Add tests for invalid bill amount, invalid sun peak hour, invalid morning usage, and invalid SMP price.

## Required Files

Create:

- `submissions/06-solar-calculator-maintenance-lab/module-map.md`
- `submissions/06-solar-calculator-maintenance-lab/calculator-validation.js`
- `submissions/06-solar-calculator-maintenance-lab/calculator-validation-test.md`
- `submissions/06-solar-calculator-maintenance-lab/mock-incident-report.md`

## Codex Practice

Ask Codex to:

- Explain the Express route-to-service flow.
- Identify what input validation protects.
- Suggest edge cases.
- Help create a small test script.
- Interpret one fake stack trace.

## Acceptance Criteria

- Aqilah can explain route, service, repository, and database roles.
- She can reproduce business rules in a safe sandbox.
- She can separate frontend errors, backend errors, and database errors.

