# PERF-01: Login Delay of 20-30 Seconds Before Inventory Page Loads

**Bug ID:** PERF-01
**User Account:** performance_glitch_user
**Severity:** Medium
**Priority:** High
**Status:** Open
**Reproducibility:** Always
**Reported By:** Felicia Agbooluchi
**Date:** 2026-06-23

---

## Summary

Logging in as performance_glitch_user causes a significant delay of 20-30 seconds before the inventory page loads. The login eventually succeeds but the response time is far outside acceptable range.

---

## Environment

- Application: Sauce Demo (https://www.saucedemo.com)
- Browser: Chrome v137.0.7151.79
- Device: iPhone XR (iOS 18.5)
- User Account: performance_glitch_user

---

## Steps to Reproduce

1. Navigate to https://www.saucedemo.com
2. Enter username: performance_glitch_user
3. Enter password: secret_sauce
4. Click Login
5. Measure time elapsed before inventory page loads

---

## Expected Behavior

Login completes and the user is redirected to /inventory.html within a normal response time (typically under 3 seconds).

---

## Actual Behavior

Login takes 20-30 seconds before the inventory page loads. The page eventually loads but with extreme latency.

---

## Evidence
![Screenshot](screenshots/PERF-01-login-delay.jpeg)

---

## Impact

In a production environment, a 20-30 second load time would cause users to abandon the session, resulting in lost conversions. This indicates a serious backend performance issue tied to specific user accounts.
