# VIS-05: Checkout Button Displayed at Top Instead of Bottom of Cart Page

**Bug ID:** VIS-05
**User Account:** visual_user
**Severity:** Low
**Priority:** Low
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The Checkout button on the cart page is displayed in the wrong position when logged in as visual_user. It appears at the top of the page instead of the expected bottom position.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: visual_user

---

## Steps to Reproduce

1. Log in as visual_user
2. Add any item to cart
3. Click the cart icon to navigate to the cart page
4. Observe the position of the Checkout button

---

## Expected Behavior

The Checkout button is positioned at the bottom of the cart page, consistent with standard e-commerce layout conventions.

---

## Actual Behavior

The Checkout button is displayed at the top of the cart page instead of the bottom. It is not in its expected position.

---

## Evidence
![Screenshot](screenshots/VIS-05-checkout-button-position.jpeg)

---

## Impact

The unexpected button position disrupts the standard user flow and creates a confusing cart experience. Users accustomed to standard e-commerce layouts would struggle to locate the Checkout button where expected.
