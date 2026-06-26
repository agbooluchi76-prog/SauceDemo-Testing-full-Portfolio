# Sauce Demo Manual Testing Portfolio

**Tester:** Felicia Agbooluchi
**Application:** [Sauce Demo](https://www.saucedemo.com) (demo e-commerce platform)
**Testing Period:** June 2026
**Type:** Manual QA Testing

---

## Overview

This repository contains a complete manual testing suite for Sauce Demo — a demo e-commerce application built for QA practice. All six user account types were tested independently across login, inventory, cart, checkout, and navigation flows.

**84 test cases executed. 19 bugs found across 6 user accounts.**

---

## Repository Structure

```
SauceDemo-Testing-full-Portfolio/
├── README.md               (this file)
├── TEST-PLAN.md            (test objectives, scope, environment, entry/exit criteria)
├── TEST-CASES.md           (all 83 test cases with expected vs actual results)
└── bug-reports/
    ├── README.md           (bug index with severity table and links)
    ├── STAND-01.md
    ├── LOCK-01.md
    ├── PERF-01.md
    ├── PERF-02.md
    ├── PROB-01.md
    ├── PROB-02.md
    ├── PROB-03.md
    ├── ERR-01.md
    ├── ERR-02.md
    ├── ERR-03.md
    ├── ERR-04.md
    ├── ERR-05.md
    ├── VIS-01.md
    ├── VIS-02.md
    ├── VIS-03.md
    ├── VIS-04.md
    ├── VIS-05.md
    ├── VIS-06.md
    └── VIS-07.md
```

---

## Test Coverage

| User Account | Total TCs | Pass | Fail |
|---|---|---|---|
| standard_user | 16 | 15 | 1 |
| locked_out_user | 1 | 0 | 1 |
| performance_glitch_user | 17 | 15 | 2 |
| problem_user | 14 | 11 | 3 |
| error_user | 17 | 12 | 5 |
| visual_user | 19 | 12 | 7 |
| **Total** | **84** | **65** | **19** |

---

## Bug Summary

| Bug ID | Title | User Account | Severity |
|---|---|---|---|
| [STAND-01](./bug-reports/STAND-01-special-chars-accepted-checkout.md) | Special characters accepted in name and zip code fields | standard_user | High |
| [LOCK-01](./bug-reports/LOCK-01-locked-out-user-login-error.md) | Login blocked with locked-out error | locked_out_user | High |
| [PERF-01](./bug-reports/PERF-01-login-delay-20-30-seconds.md) | Login delay of 20-30 seconds | performance_glitch_user | Medium |
| [PERF-02](./bug-reports/PERF-02-special-chars-accepted-checkout.md) | Special characters accepted in name and zip code fields | performance_glitch_user | High |
| [PROB-01](./bug-reports/PROB-01-image-mismatch-inventory-vs-detail.md) | Image mismatch between inventory and detail page | problem_user | Medium |
| [PROB-02](./bug-reports/PROB-02-3-of-6-items-cannot-add-to-cart.md) | 3 of 6 items cannot be added to cart | problem_user | High |
| [PROB-03](./bug-reports/PROB-03-last-name-field-blocks-checkout.md) | Last Name field blocks checkout progression | problem_user | Critical |
| [ERR-01](./bug-reports/ERR-01-product-description-missing-detail-page.md) | Product description missing on detail page | error_user | Medium |
| [ERR-02](./bug-reports/ERR-02-3-of-6-items-cannot-add-to-cart.md) | 3 of 6 items cannot be added to cart | error_user | High |
| [ERR-03](./bug-reports/ERR-03-last-name-non-functional-allows-checkout.md) | Last Name non-functional but allows checkout | error_user | Critical |
| [ERR-04](./bug-reports/ERR-04-finish-button-not-clickable.md) | Finish button not clickable | error_user | Critical |
| [ERR-05](./bug-reports/ERR-05-special-chars-accepted-checkout.md) | Special characters accepted in name and zip code fields | error_user | High |
| [VIS-01](./bug-reports/VIS-01-image-mismatch-inventory-vs-detail.md) | Image mismatch between inventory and detail page | visual_user | Low |
| [VIS-02](./bug-reports/VIS-02-cart-icon-wrong-position.md) | Cart icon positioned incorrectly | visual_user | Medium |
| [VIS-03](./bug-reports/VIS-03-sort-low-to-high-not-working.md) | Sort low to high not working | visual_user | Medium |
| [VIS-04](./bug-reports/VIS-04-sort-high-to-low-not-working.md) | Sort high to low not working | visual_user | Medium |
| [VIS-05](./bug-reports/VIS-05-checkout-button-wrong-position.md) | Checkout button displayed at wrong position | visual_user | Low |
| [VIS-06](./bug-reports/VIS-06-inventory-price-does-not-match-cart-price.md) | Inventory price does not match cart price | visual_user | High |
| [VIS-07](./bug-reports/VIS-07-special-chars-accepted-checkout.md) | Special characters accepted in name and zip code fields | visual_user | High |

---

## Severity Breakdown

| Severity | Count |
|---|---|
| Critical | 3 |
| High | 10 |
| Medium | 5 |
| Low | 3 |
| **Total** | **19** |

---

## Testing Techniques Applied

- **Positive testing** — standard_user happy path across all core flows
- **Negative testing** — empty fields, invalid passwords, locked account
- **Exploratory testing** — problem_user and visual_user for UI and image defects
- **Boundary testing** — missing postal code during checkout
- **Cross-user testing** — same core test cases applied independently to all 6 user accounts

---

## Environment

| Component | Details |
|---|---|
| URL | https://www.saucedemo.com |
| Browser | Chrome v137.0.7151.79 |
| Device | iPhone XR (iOS 18.5) |
| Network | Stable internet |

---

## Connect

[LinkedIn](https://www.linkedin.com/in/agbo-felicia03)
