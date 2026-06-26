# ERR-03: Last Name Field Non-Functional But Allows Checkout to Proceed

**Bug ID:** ERR-03
**User Account:** error_user
**Severity:** Critical
**Priority:** Critical
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

The Last Name field on the checkout information page does not accept any input when using the error_user account. Despite the field being non-functional and empty, the checkout flow allows the user to proceed to the finish page without a Last Name value.

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
3. Navigate to cart and click Checkout
4. Attempt to enter a value in the Last Name field (field does not accept input)
5. Click Continue without a Last Name value
6. Observe that the flow proceeds to the order overview page

---

## Expected Behavior

The Last Name field accepts text input. If left empty, the system displays a validation error and prevents progression. The order should not proceed without a Last Name.

---

## Actual Behavior

The Last Name field does not accept any input. Despite being empty, the system allows the user to click Continue and proceed through checkout without a Last Name value.

---

## Evidence
![Screenshot](screenshots/ERR-03-last-name-allows-checkout.jpeg)

---

## Impact

Orders are being submitted with missing required customer data. In a production environment, this would result in incomplete order records, failed deliveries, and broken customer communication. The validation layer is entirely bypassed.
