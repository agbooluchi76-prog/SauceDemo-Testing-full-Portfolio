# LOCK-01: Login Returns Locked-Out Error Message Instead of Granting Access

**Bug ID:** LOCK-01
**User Account:** locked_out_user
**Severity:** High
**Priority:** Low
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

Logging in with the locked_out_user account returns an error message blocking access. The user cannot reach the inventory page.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: locked_out_user

---

## Steps to Reproduce

1. Navigate to https://www.saucedemo.com
2. Enter username: locked_out_user
3. Enter password: secret_sauce
4. Click Login

---

## Expected Behavior

User is redirected to /inventory.html with no error message displayed.

---

## Actual Behavior

Login is blocked. The following error message is displayed: "Epic sadface: Sorry, this user has been locked out." The user remains on the login page.

---

## Evidence
![Screenshot](screenshots/LOCK-01-screenshot.jpeg)

---

## Impact

The locked_out_user account is completely inaccessible. Any functionality that depends on this account cannot be tested or used.

---

## Note

Priority is logged as Low because this behavior may be intentional for the locked_out_user account type. Severity remains High because a login block is a critical flow failure if unintended.
