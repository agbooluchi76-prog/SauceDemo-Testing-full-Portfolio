# VIS-02: Cart Icon Positioned Incorrectly (Center Instead of Top-Right)

**Bug ID:** VIS-02
**User Account:** visual_user
**Severity:** Medium
**Priority:** Medium
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The cart icon is displayed in the wrong position on the page when logged in as visual_user. It appears in the center of the page instead of the expected top-right position.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: visual_user

---

## Steps to Reproduce

1. Log in as visual_user
2. Observe the position of the cart icon on the inventory page

---

## Expected Behavior

The cart icon is positioned in the top-right corner of the navigation bar, consistent with standard e-commerce UI conventions.

---

## Actual Behavior

The cart icon is improperly positioned and does not appear in the top-right corner. It is displaced from its expected location.

---

## Evidence
![Screenshot](screenshots/VIS-02-cart-icon-position.jpeg)

---

## Impact

Users cannot reliably locate the cart icon. This disrupts the standard navigation flow and creates a confusing user experience. In a production environment, this would increase friction and reduce cart-to-checkout conversion rates.
