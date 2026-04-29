# Assignment 04: Testing And Debugging Lab

## Period

Days 22-28

## Goal

Learn to reproduce a problem, create a small test, run it, and use Codex to debug without guessing.

## Tasks

1. Run the existing `solar_calculator` navigation test.
2. Read `tests/navigation.mobile.spec.js`.
3. Ask Codex to explain what behavior the test protects.
4. Add a new simulated Playwright test in this assignment repo, not the production repo.
5. Create a debug report for one failing scenario.

## Required Files

Create:

- `submissions/04-testing-debugging-lab/navigation-test-notes.md`
- `submissions/04-testing-debugging-lab/failing-scenario-report.md`
- `submissions/04-testing-debugging-lab/sample-playwright-test.spec.js`

## Simulated Test Idea

Create a small test that checks a fake navigation menu:

- Home link exists.
- Invoice link exists.
- Clicking Back returns to the expected page.
- Missing user role hides an admin-only item.

This does not need to run against the real app unless a mentor approves.

## Codex Practice

Ask Codex to:

- Explain the Playwright test line by line.
- Suggest what to test next.
- Help interpret a failing test output.
- Explain whether a failure is a test bug, app bug, or environment issue.

## Acceptance Criteria

- Aqilah can run `npm run test:navigation` in `solar_calculator`.
- She can explain what the 5 existing navigation tests validate.
- She can write a small test and explain what it proves.

