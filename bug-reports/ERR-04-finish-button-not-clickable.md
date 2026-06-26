# ERR-04: Finish Button Not Functional on Order Overview Page

**Bug ID:** ERR-04
**User Account:** error_user
**Severity:** Critical
**Priority:** Critical
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

On the order overview page during checkout as error_user, the Finish button is not clickable. The user cannot complete the order.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: error_user

---

## Steps to Reproduce

1. Log in as error_user
2. Add any item to cart
3. Click Checkout
4. Enter First Name and Postal Code (Last Name field does not accept input per ERR-03)
5. Click Continue to reach the order overview page
6. Click the Finish button

---

## Expected Behavior

The Finish button is clickable. Clicking it completes the order and redirects the user to /checkout-complete.html with the message "Thank you for your order!"

---

## Actual Behavior

The Finish button is not clickable. The user is stuck on the order overview page and cannot complete the purchase.

---

## Evidence
![Screenshot](screenshots/ERR-04-finish-button-not-clickable.jpeg)

---

## Impact

Even users who navigate past the broken Last Name field (ERR-03) cannot complete a purchase. The checkout flow has no successful exit path for error_user. Zero orders can be completed.
