#   End-to-End Manual Testing for an E-Commerce Web Application

### Test Design, Execution & Defect Management for [AutomationExercise.com](https://www.automationexercise.com/) (AEWMT)

![Testing Type](https://img.shields.io/badge/Testing-Manual-blue)
![Test Management](https://img.shields.io/badge/Test%20Management-Jira%20%2B%20Zephyr-0052CC)
![Executed](https://img.shields.io/badge/Test%20Cases%20Executed-25-success)
![Passed](https://img.shields.io/badge/Passed-23-brightgreen)
![Failed](https://img.shields.io/badge/Failed-2-red)
![Bugs](https://img.shields.io/badge/Bugs%20Reported-2-orange)

A complete, end-to-end **manual QA project** performed on the e-commerce practice website **[AutomationExercise.com](https://www.automationexercise.com/)**. The project covers the full testing lifecycle: test planning, test case design, test execution, bug reporting, traceability, and reporting, all managed in **Jira** with **Zephyr (SmartBear Test Management)**.

---

## 🎬 Video Demo

▶️ **[Watch the full project walkthrough](https://drive.google.com/file/d/1tVcrr8EJCioQv1FG9PFhpM85UbHTI7ea/view?usp=sharing)**

---

##  Table of Contents

1. [Project Overview](#project-overview)
2. [Tools & Technologies](#tools--technologies)
3. [Testing Approach](#testing-approach)
4. [Scope & Modules Covered](#-scope--modules-covered)
5. [Test Cases Summary](#test-cases-summary)
6. [Test Execution Results](#test-execution-results)
7. [Bug Reports](#bug-reports)
8. [Traceability](#traceability)
9. [Repository Structure](#repository-structure)
10. [Key Takeaways](#key-takeaways)
11. [Author](#author)

---

##  Project Overview

| Item | Details |
|------|---------|
| **Project Key** | AEWMT |
| **Application Under Test** | https://www.automationexercise.com/ |
| **Testing Type** | Functional Manual Testing (Black-Box) |
| **Test Management** | Jira + Zephyr (SmartBear Test Management) |
| **Browser / OS** | Google Chrome / Windows 11 |
| **Total Test Cases** | 25 |
| **Execution Date** | 31 July 2026 |
| **Total Execution Time** | ~37 minutes |

**Goal:** Validate the core user journeys of the website (registration, login, product browsing, cart, checkout, and payment), identify defects, and improve overall product quality through structured test design and exploratory testing.

---

##  Tools & Technologies

- **Jira**: project tracking, issue/bug management
- **Zephyr (SmartBear Test Management)**: test case creation, test suites, execution cycles, reports
- **Microsoft Excel**: test case and bug report exports
- **Google Chrome DevTools**: inspection and validation during exploratory testing
- **Google Drive**: bug evidence (screen recordings) and project demo video

---

##  Testing Approach

### Black-Box Testing Techniques
Test cases were designed from the user's point of view, without relying on the source code:

- **Equivalence Partitioning**: grouping valid / invalid inputs (e.g., valid vs. invalid mobile numbers, card details)
- **Boundary Value Analysis**: card number length (16 digits), CVC length (3 digits)
- **Positive & Negative Testing**: valid and invalid login, registration with an existing email, invalid payment data
- **Use-Case / Scenario-Based Testing**: end-to-end flows such as *register during checkout* and *download invoice after purchase*
- **Exploratory Testing**: unscripted exploration that uncovered defects not covered by the scripted cases (validation gaps in registration and payment)

### Test Management Workflow
1. Analyze requirements and website features
2. Design test cases for different scenarios (step-by-step, with test data and expected results)
3. Organize test cases into **Test Suites / Folders** by module
4. Execute **25 test scenarios** and record results in Zephyr
5. Log defects in Jira and link them to the failed test cases
6. Generate execution and traceability reports

---

##  Scope & Modules Covered

| Test Suite (Folder) | Test Cases | Focus |
|---------------------|:----------:|-------|
| **User Registration & Account Management** | 6 | Register, login, logout, delete account, validation |
| **Products, Navigation & Page Features** | 6 | Products list/details, search, Contact Us, subscription, Test Cases page |
| **Cart & Product Placement** | 11 | Cart, quantity, checkout, payment, categories, brands, reviews, recommended items, invoice |
| **UI & Page Navigation** | 2 | Scroll up / scroll down behavior |
| **Total** | **25** | |

---

##  Test Cases Summary

###  User Registration & Account Management
| ID | Test Case | Priority |
|----|-----------|:--------:|
| AEWMT-T1 | Register New User | High |
| AEWMT-T2 | Register User with invalid mobile number | Normal |
| AEWMT-T3 | Login with valid data & delete account | High |
| AEWMT-T4 | Login with invalid data | High |
| AEWMT-T5 | Logout User | High |
| AEWMT-T6 | Register User with existing email | High |

###  Products, Navigation & Page Features
| ID | Test Case | Priority |
|----|-----------|:--------:|
| AEWMT-T7 | Contact Us: submit form with attachment | Low |
| AEWMT-T8 | Verify Test Cases page | Normal |
| AEWMT-T9 | Verify all products and product details | High |
| AEWMT-T10 | Search product | High |
| AEWMT-T11 | Verify subscription on Home page | Normal |
| AEWMT-T12 | Verify subscription on Cart page | Normal |

###  Cart & Product Placement
| ID | Test Case | Priority |
|----|-----------|:--------:|
| AEWMT-T13 | Verify adding multiple products to cart | High |
| AEWMT-T14 | Verify product quantity in cart | High |
| AEWMT-T15 | Place order: register while checkout | High |
| AEWMT-T16 | Login before checkout: invalid payment details validation | High |
| AEWMT-T17 | Remove products from cart | High |
| AEWMT-T18 | View category products | Normal |
| AEWMT-T19 | View & cart brand products | Normal |
| AEWMT-T20 | Search products and verify cart after login | High |
| AEWMT-T21 | Add review on product | Normal |
| AEWMT-T22 | Add to cart from recommended items | Normal |
| AEWMT-T23 | Download invoice after purchase order | High |

###  UI & Page Navigation
| ID | Test Case | Priority |
|----|-----------|:--------:|
| AEWMT-T24 | Scroll up using arrow button and scroll down | Low |
| AEWMT-T25 | Scroll up without arrow button and scroll down | Normal |

Each test case includes: **Precondition, Objective, Priority, Component/Labels, step-by-step script with test data and expected results.**

---

##  Test Execution Results

| Metric | Result |
|--------|:------:|
| Total Executed | **25 / 25 (100%)** |
| ✅ Passed | **23** |
| ❌ Failed | **2** |
| Pass Rate | **92%** |
| Total Execution Effort | ~37 min |
| Defects Logged | 2 |

The two failed test cases (**AEWMT-T2** and **AEWMT-T16**) exposed missing input validation and were each linked to a Jira bug.

---

##  Bug Reports

| Bug ID | Title | Module | Severity | Priority | Status |
|--------|-------|--------|:--------:|:--------:|:------:|
| **Bug_01** | User can complete registration using an invalid mobile number format (letters / special characters) | Registration | Medium | High | Open |
| **Bug_02** | Order is placed without validating missing/invalid payment details at checkout | Checkout / Payment | High | High | Open |

### Bug_01: Invalid mobile number accepted
- **Linked test case:** AEWMT-T2
- **Steps:** Signup → fill account details → enter an invalid mobile number (e.g., `abc!@#` or `0000`) → click *Create Account*
- **Expected:** Inline validation error and the form is blocked
- **Actual:** The account is created and the user reaches the *ACCOUNT CREATED!* page

### Bug_02: Payment validation bypassed
- **Linked test case:** AEWMT-T16
- **Steps:** Login → add product → checkout → enter invalid card data (card `1234`, CVC `abc`, blank/past expiry) → *Pay and Confirm Order*
- **Expected:** Transaction is blocked with validation errors
- **Actual:** Invalid data is accepted and the order is confirmed

Every bug report contains: title, description, module, environment, severity, priority, steps to reproduce, expected vs. actual result, reporter, assignee, date, and an attached screen-recording as evidence.

---

##  Traceability

A **Traceability Report** links each test case → execution result → reported issue, ensuring full visibility of coverage and that every failure is tracked to a defect.

| Test Case | Result | Linked Issue |
|-----------|:------:|--------------|
| AEWMT-T2 | ❌ Fail | AEWMT-2 (invalid mobile number) |
| AEWMT-T16 | ❌ Fail | Payment validation defect |
| All other cases | ✅ Pass | None |

---

##  Repository Structure

```
📦 AutomationExercise_Website -Manual-Testing
 ┣ 📂 Test Suites
 ┃ ┣ 📄 User_Registration___Account_Management.xlsx
 ┃ ┣ 📄 Products__Navigation___Page_Features.xlsx
 ┃ ┣ 📄 Cart___Product_Placement.xlsx
 ┃ ┗ 📄 UI___Page_Navigation.xlsx
 ┣ 📂 Bug Reports
 ┃ ┗ 📄 Bug_Report_Manual_Testing_Project_AEW.xlsx
 ┣ 📂 Test execution Reports
 ┃ ┣ 📄 Test_execution_results__summary_.pdf
 ┃ ┣ 📄 Test_execution_results__list_.pdf
 ┃ ┣ 📄 Test_execution_results__detailed_.pdf
 ┃ ┗ 📄 Traceability_Report.pdf
 ┗ 📄 README.md
```

---

##  Key Takeaways

- Designed and executed **25 well-structured test scenarios** across 4 functional suites
- Applied **black-box techniques** and **exploratory testing** to uncover real validation defects
- Achieved a **92% pass rate** and identified **2 reproducible bugs**, one high-severity (payment validation)
- Maintained full **traceability** from test case to execution to defect
- Used professional **Jira + Zephyr** workflows for test management and reporting

---

##  Author

**Ahmed Ayman**: Software QA Engineer 


