# 🧪 Swag Labs – Manual Testing Project

![Testing Type](https://img.shields.io/badge/Testing%20Type-Manual%20Testing-blue)
![Test Cases](https://img.shields.io/badge/Test%20Cases-24-informational)
![Test Scenarios](https://img.shields.io/badge/Test%20Scenarios-63-purple)
![Bugs Found](https://img.shields.io/badge/Bugs%20Found-8-red)
![Pass Rate](https://img.shields.io/badge/Pass%20Rate-91.6%25-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)

> A comprehensive **Manual Testing** project on [Swag Labs (SauceDemo)](https://www.saucedemo.com/) — a demo e-commerce web application built for QA practice. This project follows a real-world QA lifecycle covering Requirement Analysis, Test Scenario Design, Test Case Writing, Test Execution, and Bug Reporting.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Application Under Test](#application-under-test-aut)
- [Test Artifacts](#test-artifacts)
- [Modules Tested](#modules-tested)
- [Test Execution Results](#test-execution-results)
- [Bug Report Summary](#bug-report-summary)
- [Tools Used](#tools-used)
- [How to Use This Repository](#how-to-use-this-repository)
- [Author](#author)

---

## 📖 About the Project

This project was created as part of my **Software Testing learning journey**. The goal was to simulate a professional QA process on a real web application — covering everything from reading and analyzing requirements, designing test scenarios, writing structured test cases, executing them, and reporting bugs with proper severity and priority.

**What this project demonstrates:**
- Reading and breaking down functional requirements per module
- Writing **Positive** and **Negative** test scenarios
- Designing detailed, structured test cases with preconditions, steps, expected and actual results
- Executing test cases and logging results accurately
- Identifying and reporting bugs following a standard **Bug Life Cycle**
- Organizing all test documentation in a professional format

---

## 🌐 Application Under Test (AUT)

| Field | Details |
|---|---|
| **Application Name** | Swag Labs |
| **URL** | https://www.saucedemo.com/ |
| **Type** | E-Commerce Web Application (Demo) |
| **Testing Type** | Manual Testing – Functional Testing |
| **Browser** | Google Chrome |
| **Operating System** | Windows 11 |
| **Test Environment** | HP ZBook Laptop – Windows 11 – Chrome Browser |

### Test Users Available

| Username | Type |
|---|---|
| `standard_user` | Valid user – used for most test cases |
| `locked_out_user` | Blocked user – used for negative testing |
| `problem_user` | Buggy behavior user |
| `performance_glitch_user` | Slow performance user |
| `error_user` | Error-prone user |
| `visual_user` | Visual bug user |

> **Password for all users:** `secret_sauce`

---

## 📁 Test Artifacts

| Artifact | Description |
|---|---|
| **Requirement Analysis** | Functional requirements extracted per module before writing any test cases |
| **Test Scenarios** | High-level scenarios covering both Positive and Negative flows |
| **Test Cases** | Detailed cases with preconditions, steps, expected result, actual result, and status |
| **Bug Report** | All found defects with steps to reproduce, severity, priority, and status |
| **Test Summary** | Overall execution metrics per module |

All artifacts are documented in the Excel file: `TASK_SWAG_LABS.xlsx`

---

## 🗂️ Modules Tested

### 1. 🔐 Login Module
**Requirements covered:** Valid login, invalid credentials, empty field validation, locked user behavior.

| Scenarios | Test Cases | Positive | Negative |
|---|---|---|---|
| 12 | 6 | 4 | 8 |

**Key scenarios tested:**
- Login with valid `standard_user` credentials → redirect to inventory page
- Login with invalid username / invalid password → error message appears
- Login with empty username or password → validation message
- Login attempt with `locked_out_user` → account locked error

---

### 2. 🛍️ Products Module
**Requirements covered:** Product display, product info, Add to Cart, Remove, sorting, navigation.

| Scenarios | Test Cases | Positive | Negative |
|---|---|---|---|
| 18 | 5 | 13 | 5 |

**Key scenarios tested:**
- Products list displays after login
- Each product shows name, image, description, price, and Add to Cart button
- Cart icon badge updates after adding a product
- All 4 sorting options work correctly (A→Z, Z→A, Low→High, High→Low)
- Accessing inventory page without login → redirect to login

---

### 3. 🛒 Cart Module
**Requirements covered:** Cart display, product details in cart, remove functionality, navigation.

| Scenarios | Test Cases | Positive | Negative |
|---|---|---|---|
| 10 | 4 | 7 | 3 |

**Key scenarios tested:**
- All added products appear in cart with correct details
- Remove button deletes product from cart and updates cart
- "Continue Shopping" returns user to products page
- "Checkout" button navigates to checkout flow
- Accessing cart without login → redirect to login

---

### 4. 📋 Checkout Information Module
**Requirements covered:** Form validation for First Name, Last Name, Postal Code fields.

| Scenarios | Test Cases | Positive | Negative |
|---|---|---|---|
| 10 | 4 | 6 | 4 |

**Key scenarios tested:**
- All 3 fields accept valid input and user proceeds to next step
- Empty First Name → error message displayed
- Empty Last Name → error message displayed
- Empty Postal Code → error message displayed
- All fields empty + click Continue → error message

---

### 5. 📦 Checkout Overview Module
**Requirements covered:** Order summary display, price calculation, payment/shipping info, cancel and finish.

| Scenarios | Test Cases | Positive | Negative |
|---|---|---|---|
| 13 | 3 | 11 | 2 |

**Key scenarios tested:**
- All selected products appear with name, description, price, quantity
- Item total, tax, and final total displayed and calculated correctly
- Payment and shipping information visible
- "Cancel" returns user to products page
- "Finish" completes the order successfully
- Direct URL access without completing previous steps → access blocked

---

### 6. ✅ Checkout Complete Module
**Requirements covered:** Order confirmation page after completing checkout.

| Scenarios | Test Cases | Positive | Negative |
|---|---|---|---|
| — | 2 | 2 | — |

**Key scenarios tested:**
- Confirmation message displayed after clicking Finish
- Order completion state is visually clear to the user

---

## 📊 Test Execution Results

| Module | Total Test Cases | Passed | Failed | Pass Rate |
|---|---|---|---|---|
| Login | 6 | 5 | 1 | 83.3% |
| Products | 5 | 5 | 0 | 100% |
| Cart | 4 | 3 | 1 | 75% |
| Checkout Information | 4 | 4 | 0 | 100% |
| Checkout Overview | 3 | 3 | 0 | 100% |
| Checkout Complete | 2 | 2 | 0 | 100% |
| **Total** | **24** | **22** | **2** | **91.6%** |

> Total Test Scenarios written: **63** (across all modules)

---

## 🐛 Bug Report Summary

All bugs were tracked using a standard **Bug Life Cycle:**
> `New → Open → Assigned → In Progress → Re-test → Closed`

| Bug ID | Module | Title | Severity | Priority | Status |
|---|---|---|---|---|---|
| BUG-001 | Login | Login with empty fields — validation message not clear | Medium | High | Open |
| BUG-002 | Login | Error message not user-friendly for invalid login | Medium | Medium | Open |
| BUG-003 | Products | Product sorting not applied correctly | Medium | Medium | Open |
| BUG-004 | Cart | Item not removed immediately from cart (requires page refresh) | High | High | Open |
| BUG-005 | Checkout Info | Empty First Name field not highlighted clearly after validation | Low | Medium | Open |
| BUG-006 | Checkout Overview | Total price calculation mismatch (items + tax) | High | High | Open |
| BUG-007 | Checkout Complete | Confirmation message not visually highlighted | Low | Low | Open |
| BUG-008 | Products | Product images loading with delay | Low | Low | Open |

**Bug Severity Distribution:**

| Severity | Count |
|---|---|
| 🔴 High | 2 |
| 🟠 Medium | 3 |
| 🟡 Low | 3 |
| **Total** | **8** |

**Severity Definitions used in this project:**
- 🔴 **High** – Feature broken, significant impact on user experience
- 🟠 **Medium** – Feature partially works but behavior is incorrect
- 🟡 **Low** – Cosmetic or minor UX issue, does not block functionality

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Writing and organizing all test artifacts |
| **Google Chrome** | Test execution environment (browser) |
| **Snipping Tool** | Capturing bug screenshots |
| **GitHub** | Version control and portfolio hosting |

---

## 📂 How to Use This Repository

1. Clone or download this repository
2. Open the file: `TASK_SWAG_LABS.xlsx`
3. Navigate through the sheets in order:
   - **Project Overview** – project summary and environment info
   - **Requirement [Module]** – functional requirements per module
   - **Test Scenarios [Module]** – high-level test scenarios
   - **Test Case [Module]** – detailed test cases with execution results
   - **Bug Report** – all found bugs with full details
   - **Test Summary** – execution results per module
4. You can replicate all tests yourself at [saucedemo.com](https://www.saucedemo.com/) using the credentials listed above

---

## 👤 Author

**Abdelrhman Lotfy**

> 💡 *This project is part of my QA learning portfolio. I am actively building my skills in Manual Testing, working towards becoming a professional QA Engineer.*

---

*⭐ If you found this project useful for your own learning journey, consider giving it a star!*
