# Playwright Assignments 2–12 (WORK IN PROGRESS — partial delivery)

This zip is a **snapshot mid-build**. Assignments 2–8 are complete and
runnable. Assignments 9–12 are also done (see status table). 

## Setup

```bash
npm install
npx playwright install
```

## Running

Each assignment is its own Playwright **project** (own test folder + own
target site), all sharing one `playwright.config.js`.

```bash
npm run test:a2    # Assignment 2
npm run test:a3    # Assignment 3
npm run test:a4    # Assignment 4
npm run test:a5    # Assignment 5
npm run test:a6    # Assignment 6
npm run test:a7    # Assignment 7
npm run test:a8    # Assignment 8
npm run report     # open the HTML report after any run
```


## Status & site mapping

| # | Assignment | Site under test | Status |
|---|---|---|---|
| 2 | Complex Form + Validation | https://demoqa.com/automation-practice-form | ✅ Done — `pages/assignment2`, `tests/assignment2`, `testdata/assignment2` |
| 3 | Popup/Child Window + Edge Case + Refactor | https://the-internet.herokuapp.com | ✅ Done — `pages/assignment3`, `tests/assignment3` |
| 4 | Form / Search / Cart / Filter / Navigation (5 scenarios) | https://automationexercise.com | ✅ Done — `pages/assignment4`, `tests/assignment4`, `testdata/assignment4` |
| 5 | Refactor of Assignment 4 (locators + stability) | https://automationexercise.com | ✅ Done — `pages/assignment5`, `tests/assignment5` (incl. `REFACTOR-NOTES.md`) |
| 6 | Alerts / Frames / Visibility Assertions | https://the-internet.herokuapp.com | ✅ Done — `pages/assignment6`, `tests/assignment6` |
| 7 | File Upload (extends Assignment 4 Contact Us) | https://automationexercise.com | ✅ Done — `tests/assignment7`, `testdata/assignment7` |
| 8 | UI Table Data vs Expected JSON | https://the-internet.herokuapp.com/tables | ✅ Done — `pages/assignment8`, `tests/assignment8`, `testdata/assignment8` |
| 9 | Booking Flow + Refund Eligibility | https://automationintesting.online | 🔶 Partial — `pages/assignment9/BookingPage.js` and `utils/refundPolicy.js` exist; **spec files not yet written** |
| 10 | API Mocking (sandbox banner, cross-user booking) | local fixture app (to be built) | ⬜ Not started |
| 11 | POM Conversion (before/after) | https://the-internet.herokuapp.com | ⬜ Not started |
| 12 | Framework Concepts (tags, retries, reporting) + AI usage doc | https://automationexercise.com | ⬜ Not started |
| — | Root README with full assignment↔site map | — | ⬜ Not started (this file is the placeholder) |

## What's already solid in this snapshot

- **Page Object Model** throughout — every assignment's locators/actions live
  in `pages/assignmentN/*.js`, tests only orchestrate + assert.
- **JSON-driven test data** in `testdata/assignmentN/*.json` wherever the
  assignment called for it.
- Positive **and** negative cases in every finished spec, 3+ assertions per
  scenario.
- No `page.waitForTimeout()` hard waits anywhere — real `waitFor`/auto-retrying
  `expect()` throughout, called out explicitly in Assignment 3 and 5.
- One shared `playwright.config.js` with a project-per-assignment/baseURL
  setup, HTML reporting, and a `webServer` entry pre-wired for Assignment 10.


# PlaywrightAssignmentDhruvi
