# Sauce Demo Test Plan

**Project:** Manual QA Testing of Sauce Demo (Swag Labs)
**Tester:** Felicia Agbooluchi
**Date:** June 2026
**Version:** 1.0

---

## 1. Introduction

### Objective
Validate core functionality, negative paths, and edge cases of [saucedemo.com](https://www.saucedemo.com) — a demo e-commerce platform.

### Scope
The following areas are covered in this test plan:

- Login and session management
- Product listing and sorting
- Product details page
- Add/remove items from cart
- Checkout flow (information, overview, completion)
- Logout and navigation
- User type matrix (standard, locked_out, problem, performance_glitch, error, visual)

### Out of Scope

- Performance load testing
- Security penetration testing
- Payment gateway (simulated only)

---

## 2. Test Environment

| Component | Details |
|---|---|
| URL | https://www.saucedemo.com |
| Browser | Chrome v137.0.7151.79 |
| Device | iPhone XR (iOS 18.5) |
| Network | Stable internet |

---

## 3. Test Data

| Username | Password | Expected Behavior |
|---|---|---|
| standard_user | secret_sauce | Checkout flow - accepted special characters |
| locked_out_user | secret_sauce | Login blocked; user is locked out |
| problem_user | secret_sauce | Image mismatches; not all items add to cart |
| performance_glitch_user | secret_sauce | Extreme login latency (20-30 seconds) |
| error_user | secret_sauce | Missing product descriptions; not all items add to cart; checkout broken |
| visual_user | secret_sauce | Image mismatches; UI element misplacement; price instability |

---

## 4. Entry and Exit Criteria

### Entry Criteria
- Test environment is accessible
- All credentials are valid and functional
- No blocking defects on login or critical path

### Exit Criteria
- All High priority tests executed and passed
- Medium and Low tests executed with known issues logged
- At least one full regression run completed

---

## 5. Testing Techniques Used

| Technique | Description |
|---|---|
| Positive testing | Standard user happy path: login, add to cart, checkout, logout |
| Negative testing | Empty fields, invalid passwords, locked user |
| Exploratory testing | problem_user and visual_user for UI and image inconsistencies |
| Boundary testing | Missing postal code during checkout |
| User-based testing | Each of 6 user accounts tested against the same core test cases |

---

## 6. Test Coverage

| Feature | Test Cases | Users Covered |
|---|---|---|
| Login | LOG-01, LOG-02, LOG-03, LOG-04 | All 6 users |
| Inventory and sorting | INV-01 to INV-07 | All 6 users |
| Cart | CRT-01 | All applicable users |
| Checkout | CHK-01 to CHK-05 | All applicable users |
| Navigation | NAV-01, NAV-02 | All applicable users |
| UI elements | EDGE-01, EDGE-02 | visual_user |

---

## 7. Deliverables

- Test plan (this document)
- Executed test cases ([TEST-CASES.md](./TEST-CASES.md))
- Bug reports ([bug-reports/README.md](./bug-reports/README.md))
- Test execution summary (pass/fail per test case, included in TEST-CASES.md)

---

## 8. Test Execution Summary

| Status | Count |
|---|---|
| Pass | 64 |
| Fail | 19 |
| **Total** | **83** |
