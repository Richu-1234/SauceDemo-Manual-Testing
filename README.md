# Sauce Demo – Manual Testing Project

A complete manual QA project on the **Sauce Demo** e-commerce website, covering the full testing process: test planning, test scenarios, test cases, execution with evidence, defect tracking in Jira, and a test summary report.

**Application under test:** https://www.saucedemo.com/ (a public practice website)

---

## Project at a glance

| Item | Result |
|---|---|
| Test scenarios | 41 |
| Test cases | 45 |
| Test cases executed | 45 |
| Passed | 42 |
| Failed | 3 |
| Pass rate | 93.3% |
| Defects logged in Jira | 3 (SDQ-1, SDQ-2, SDQ-3) |
| Testing type | Manual, black-box |
| Environment | Windows, Google Chrome |
| Tools | Jira, Microsoft Excel, Microsoft Word, GitHub |

---

## Repository structure

| Folder | Contents |
|---|---|
| [01_Test_Plan](01_Test_Plan) | Test Plan: scope, approach, environment, entry and exit criteria, risks, schedule |
| [02_Test_Scenarios](02_Test_Scenarios) | 41 test scenarios, each mapped to its test cases |
| [03_Test_Cases](03_Test_Cases) | 45 test cases with preconditions, test data, steps, expected and actual results |
| [04_Test_Execution](04_Test_Execution) | Test Execution Report (status, evidence and Bug ID for every test case) and a `Screenshots` folder |
| [05_Defect_Reports](05_Defect_Reports) | Bug list exported from Jira, the raw export, and Jira screenshots (board, dashboard, bug details) |
| [06_Test_Summary_Report](06_Test_Summary_Report) | Final Test Summary Report |

---

## Scope

**Modules tested**

1. Login
2. Products / Inventory
3. Product Sorting
4. Shopping Cart
5. Checkout Information
6. Checkout Overview
7. Order Confirmation
8. Navigation and Logout

**Out of scope:** performance, security, backend and database testing, payment gateway testing, cross-browser testing and mobile testing.

---

## Testing approach

- **Types of testing:** functional, positive, negative, UI and exploratory testing.
- **Design techniques:** equivalence partitioning (for example valid user, locked-out user, wrong password, empty fields) and error guessing (for example a capitalised username).
- **Test data:** the test users listed on the Sauce Demo login page (`standard_user`, `locked_out_user`, `problem_user`, `performance_glitch_user`, `error_user`, `visual_user`).
- **Traceability:** every scenario lists its test cases, every test case lists its scenario, and every failed test case has a Jira Bug ID.

---

## Defects found

| Bug ID | Test case | Summary | Severity | Priority | Status |
|---|---|---|---|---|---|
| SDQ-1 | TC_PROD_005 | Incorrect product images displayed for problem_user | Medium | Medium | In Progress |
| SDQ-2 | TC_PROD_006 | Product details page shows a different product than the one clicked for problem_user | High | Medium | In Progress |
| SDQ-3 | TC_PROD_007 | Product images and prices differ from standard_user for visual_user | Medium | Medium | In Progress |

The defects were logged in a Jira space named **Sauce Demo QA** (key `SDQ`) using the Kanban template. Each bug has steps to reproduce, expected and actual results, a screenshot, labels and a comment. Screenshots of the board, dashboard and each bug are in [05_Defect_Reports](05_Defect_Reports).

The bugs remain *In Progress* because Sauce Demo is a public practice site whose defects cannot be fixed, so no retest was possible.

---

## Key observations

- All main flows (login, browsing, sorting, cart, checkout and order confirmation) passed with `standard_user`.
- Negative login cases behaved correctly, including the locked-out user.
- All three defects appeared only with the `problem_user` and `visual_user` accounts, which are built-in demo accounts with deliberate issues.

---

## Limitations and notes

- Testing was done by one tester, on Google Chrome and Windows only.
- Eighteen additional test cases were identified but not executed in this cycle. They are listed in the Test Summary Report and are not counted in the 45 test cases.
- AI tools were used to help draft some of the test cases and documents. All test execution, screenshots, results and bug reports are my own work, based on what I observed on the application.

---

## Planned next steps

- API testing with Postman
- SQL practice for QA
- Test automation with Selenium

These will be added as separate repositories.

---

## Author

**Richu Maria Sijee**
B.Tech student preparing for a career in software testing.
GitHub: [Richu-1234](https://github.com/Richu-1234)

