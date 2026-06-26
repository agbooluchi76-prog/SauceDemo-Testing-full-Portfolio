# PROB-01: Image Mismatch Between Inventory Page and Product Detail Page

**Bug ID:** PROB-01
**User Account:** problem_user
**Severity:** Medium
**Priority:** Medium
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The product image displayed on the inventory page does not match the image shown on the product detail page for the same item. The problem_user account consistently shows wrong images on the inventory listing.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: problem_user

---

## Steps to Reproduce

1. Log in as problem_user
2. Observe the product image for Sauce Labs Backpack on the inventory page
3. Click the product name or image to navigate to the product detail page
4. Compare the image displayed on the detail page with the inventory page image

---

## Expected Behavior

The product image on the inventory page should match the product image on the detail page for the same item.

---

## Actual Behavior

The inventory page displays a completely different image from the one shown on the product detail page for the same product.

---

## Evidence
![Screenshot](screenshots/PROB-01-image-mismatch.jpeg)

---

## Impact

Users cannot trust that the product they see on the listing is the product they are buying. This breaks purchase confidence and would directly impact conversion rates in a production environment.
