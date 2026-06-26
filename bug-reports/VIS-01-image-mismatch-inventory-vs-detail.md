# VIS-01: Image Mismatch Between Inventory Page and Product Detail Page

**Bug ID:** VIS-01
**User Account:** visual_user
**Severity:** Low
**Priority:** Low
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The product image on the inventory page does not match the product image on the detail page for the same item when logged in as visual_user.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: visual_user

---

## Steps to Reproduce

1. Log in as visual_user
2. Observe the product image for Sauce Labs Backpack on the inventory page
3. Click the product name or image to navigate to the product detail page
4. Compare the image on the detail page with the inventory page image

---

## Expected Behavior

The product image on the inventory page should match the product image on the product detail page for the same item.

---

## Actual Behavior

The inventory page displays a completely different image from the one shown on the product detail page for the same product.

---

## Evidence
![Screenshot](screenshots/VIS-01-image-mismatch.jpeg)

---

## Impact

Users cannot verify that the product shown in the listing matches what they are buying. This erodes purchase confidence and would reduce conversions in a production environment.
