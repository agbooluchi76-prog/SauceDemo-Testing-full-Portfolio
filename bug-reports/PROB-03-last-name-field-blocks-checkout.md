# PROB-03: Last Name Field Not Interactive During Checkout; Blocks Progression

**Bug ID:** PROB-03
**User Account:** problem_user
**Severity:** Critical
**Priority:** Critical
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The Last Name field on the checkout information page does not accept any input when using the problem_user account. Because the field is required, the user cannot continue past the checkout information step and the entire checkout flow is blocked.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: problem_user

---

## Steps to Reproduce

1. Log in as problem_user
2. Add any item to cart
3. Navigate to cart and click Checkout
4. Attempt to enter a value in the Last Name field
5. Click Continue

---

## Expected Behavior

The Last Name field accepts text input. The user can complete the checkout information form and proceed to the order overview page.

---

## Actual Behavior

The Last Name field does not accept any input. An error is thrown and the user cannot proceed past the checkout information page. The checkout flow is completely blocked.

---

## Evidence
![Screenshot](screenshots/PROB-03-last-name-blocks-checkout.jpeg)

---

## Impact

The problem_user account cannot complete any purchase. The entire checkout flow is broken for this user type. In a production environment, this would mean zero completed orders for affected users.
