# VIS-04: Sort Filter "Price (High to Low)" Does Not Sort Products Correctly

**Bug ID:** VIS-04
**User Account:** visual_user
**Severity:** Medium
**Priority:** Medium
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

When the "Price (High to Low)" sort filter is applied as visual_user, products are not reordered correctly by descending price. The sort has no effect or produces an incorrect order.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: visual_user

---

## Steps to Reproduce

1. Log in as visual_user
2. On the inventory page, click the sort dropdown
3. Select "Price (high to low)"
4. Observe the order of products displayed

---

## Expected Behavior

Products are reordered in descending price order. The most expensive item appears first.

---

## Actual Behavior

Products are not sorted correctly by price. The listing does not follow descending price order after the filter is applied.

---

## Evidence
![Screenshot](screenshots/VIS-04-sort-high-low.jpeg)

---

## Impact

Users relying on price sorting to browse premium products receive inaccurate results. This breaks a core shopping feature and reduces the usability of the product catalogue.
