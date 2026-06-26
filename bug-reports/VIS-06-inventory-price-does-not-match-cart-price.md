# VIS-06: Inventory Page Price Does Not Match Cart Price; Price Changes on Every Page Refresh

**Bug ID:** VIS-06
**User Account:** visual_user
**Severity:** High
**Priority:** High
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

Product prices displayed on the inventory page are unstable and change on every page refresh. The price shown on the inventory page does not match the price shown in the cart for the same product. This creates a financial data integrity failure across the shopping flow.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: visual_user

---

## Steps to Reproduce

1. Log in as visual_user
2. On the inventory page, note the price of Sauce Labs Onesie (observed at $59.91 under Price low to high sort)
3. Refresh the inventory page
4. Observe that the price of Sauce Labs Onesie has changed (e.g. now shows $28.65)
5. Add items to cart and navigate to the cart page
6. Observe that Sauce Labs Fleece Jacket shows $49.99 in the cart but displayed $32.32 on the inventory page
7. Repeat refresh multiple times and observe price continues to change on each load

---

## Expected Behavior

The price displayed on the inventory page should remain consistent across page refreshes. The price shown in the cart should match exactly the price displayed on the inventory page at the time the item was added.

---

## Actual Behavior

Inventory page prices are unstable and regenerate on every page load. Cart page prices remain fixed but do not match what was displayed on the inventory page. The user is shown one price during browsing and charged a different price in the cart.

---

## Evidence
![Screenshot](screenshots/VIS-06-price-mismatch.jpeg)

---

## Impact

This is a financial integrity failure. Users are being shown prices during browsing that do not match what they are charged at checkout. In a production environment, this would expose the business to legal liability, customer complaints, and potential regulatory violations. This is the highest risk bug identified in the visual_user test session.
