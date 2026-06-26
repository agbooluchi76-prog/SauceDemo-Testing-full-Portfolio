# PERF-02: First and Last Name Fields Accept Special Characters; Zip Code Accepts Alphabets

**Bug ID:** PERF-02
**User Account:** performance_glitch_user
**Severity:** High
**Priority:** High
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The checkout form accepts special characters in the First Name and Last Name fields, and accepts alphabetical characters in the Zip Code field. No validation error is thrown. The order completes successfully with invalid input data.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: performance_glitch_user

---

## Steps to Reproduce

1. Log in as performance_glitch_user
2. Add any item to cart
3. Click Checkout
4. Enter special characters (e.g. @#$%) in the First Name field
5. Enter special characters in the Last Name field
6. Enter alphabetical characters (e.g. ABC) in the Zip Code field
7. Click Continue
8. Click Finish

---

## Expected Behavior

The system should validate input fields and display an error message rejecting special characters in name fields and non-numeric characters in the Zip Code field. The order should not proceed.

---

## Actual Behavior

No validation error is displayed. The checkout process completes successfully and the order is confirmed despite invalid input data.

---

## Evidence
![Screenshot](screenshots/PERF-02-special-chars-checkout.jpeg)

---

## Impact

Invalid data passes into the order system without rejection. In a production environment, this would result in corrupted order records, failed deliveries, and potential downstream system errors.
