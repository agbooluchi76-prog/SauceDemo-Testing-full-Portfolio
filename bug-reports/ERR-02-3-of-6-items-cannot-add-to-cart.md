# ERR-02: 3 Out of 6 Items Cannot Be Added to Cart

**Bug ID:** ERR-02
**User Account:** error_user
**Severity:** High
**Priority:** High
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

When attempting to add all 6 products to the cart as error_user, only 3 items can be successfully added. The remaining 3 items cannot be added to the cart.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: error_user

---

## Steps to Reproduce

1. Log in as error_user
2. On the inventory page, click "Add to cart" for all 6 items
3. Observe the cart badge count

---

## Expected Behavior

All 6 items are added to the cart. Cart badge displays 6.

---

## Actual Behavior

Only 3 out of 6 items can be added to the cart. The remaining 3 items fail to add. Cart badge does not reach 6.

---

## Evidence
![Screenshot](screenshots/ERR-02-items-cannot-add-to-cart.jpeg)

---

## Impact

Users cannot purchase half the product catalogue. This is a direct revenue loss. In a production environment, this would block sales for 50% of available inventory.
