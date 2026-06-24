# Sauce Demo Test Cases

**Application:** [Sauce Demo](https://www.saucedemo.com)
**Tester:** Felicia Agbooluchi
**Date:** June 2026
**Total Test Cases:** 84 | **Pass:** 65 | **Fail:** 19

---

## Standard User

### Login

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| LOG-01 | Successful login with valid credentials | Browser at login page | 1. Enter username 2. Enter password 3. Click Login | Redirected to /inventory.html. No error displayed. | Redirected to /inventory.html. No error displayed. | Pass |
| LOG-02 | Login with invalid password | Browser at login page | 1. Enter valid username 2. Enter incorrect password 3. Click Login | Error: "Epic sadface: Username and password do not match any user in this service." | Error message displayed correctly. | Pass |
| LOG-03 | Login with empty fields | Browser at login page | 1. Leave fields blank 2. Click Login | Error: "Epic sadface: Username is required." | Error message displayed correctly. | Pass |

### Inventory and Product

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| INV-01 | Add all products to cart | Logged in, on inventory page | 1. Click "Add to cart" for all items 2. Check cart badge | Cart badge shows 6. | Cart badge shows 6. | Pass |
| INV-02 | Sort by price low to high | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (low to high)" | Products in ascending price order. | Products in ascending price order. | Pass |
| INV-03 | Sort by price high to low | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (high to low)" | Products in descending price order. | Products in descending price order. | Pass |
| INV-04 | Sort by Name A-Z | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (A-Z)" | Products in alphabetical order, A first. | Products in alphabetical order, A first. | Pass |
| INV-05 | Sort by Name Z-A | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (Z-A)" | Products in reverse alphabetical order, Z first. | Products in reverse alphabetical order, Z first. | Pass |
| INV-06 | View product details | Logged in, on inventory page | 1. Click product name or image | Navigates to detail page. Product info displays correctly. | Navigates to detail page. Product info displays correctly. | Pass |

### Cart and Checkout

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| CRT-01 | Remove item from cart | 2 items in cart, on cart page | 1. Click "Remove" on one item 2. Observe cart | Item removed. Cart badge decreases by 1. | Item removed. Cart badge decreases by 1. | Pass |
| CHK-01 | Complete checkout with valid details | Cart has at least 1 item | 1. Click Checkout 2. Enter First Name, Last Name, Postal Code 3. Click Continue 4. Click Finish | Order confirmed. "Thank you for your order!" displayed. | Order confirmed. | Pass |
| CHK-02 | Checkout with missing fields | On checkout information page | 1. Leave all fields empty 2. Click Continue | Error: required fields message displayed. | Error displayed correctly. | Pass |
| CHK-03 | Cancel checkout | On checkout information page | 1. Click Cancel | Returned to cart page. Cart contents unchanged. | Returned to cart page unchanged. | Pass |
| CHK-04 | Checkout with special characters in name fields and alphabets in zip code | On checkout information page | 1. Click Checkout 2. Enter special characters in First Name and Last Name 3. Enter alphabets in Zip Code 4. Click Continue 5. Click Finish | Error displayed for invalid data type. | Checkout completed and order confirmed without error. | **Fail** |

### Navigation

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| NAV-01 | Logout functionality | Logged in on any page | 1. Open menu 2. Click Logout | Redirected to login page. Session cleared. | Redirected to login page. Session cleared. | Pass |
| NAV-02 | Continue shopping from cart | On cart page with items | 1. Click "Continue Shopping" | Redirected to inventory page. Cart badge retains count. | Redirected to inventory page. Cart badge retained. | Pass |

---

## Locked Out User

### Login

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| LOG-01 | Login attempt with locked out user | Browser at login page | 1. Enter locked_out_user 2. Enter password 3. Click Login | Redirected to /inventory.html. | Error: "Epic sadface: Sorry, this user has been locked out." User remains on login page. | **Fail** |

---

## Performance Glitch User

### Login

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| LOG-01 | Successful login with valid credentials | Browser at login page | 1. Enter username 2. Enter password 3. Click Login | Redirected to /inventory.html within normal response time. | Redirected to /inventory.html. No error displayed. | Pass |
| LOG-02 | Login with invalid password | Browser at login page | 1. Enter valid username 2. Enter incorrect password 3. Click Login | Error: "Epic sadface: Username and password do not match any user in this service." | Error message displayed correctly. | Pass |
| LOG-03 | Login with empty fields | Browser at login page | 1. Leave fields blank 2. Click Login | Error: "Epic sadface: Username is required." | Error message displayed correctly. | Pass |
| LOG-04 | Performance delay on login | Browser at login page | 1. Login as performance_glitch_user 2. Measure loading time | Login completes within normal response time. | Login takes 20-30 seconds before inventory page loads. | **Fail** |

### Inventory and Product

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| INV-01 | Add product to cart | Logged in, on inventory page | 1. Click "Add to cart" for all items 2. Check cart badge | Cart badge shows 6. | Cart badge shows 6. | Pass |
| INV-02 | Sort by price low to high | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (low to high)" | Products in ascending price order. | Products in ascending price order. | Pass |
| INV-03 | Sort by price high to low | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (high to low)" | Products in descending price order. | Products in descending price order. | Pass |
| INV-04 | Sort by Name A-Z | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (A-Z)" | Products in alphabetical order, A first. | Products in alphabetical order, A first. | Pass |
| INV-05 | Sort by Name Z-A | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (Z-A)" | Products in reverse alphabetical order, Z first. | Products in reverse alphabetical order, Z first. | Pass |
| INV-06 | View product details | Logged in, on inventory page | 1. Click product name or image | Navigates to detail page. Product info displays correctly. | Navigates to detail page. Product info displays correctly. | Pass |

### Cart and Checkout

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| CRT-01 | Remove item from cart | 2 items in cart, on cart page | 1. Click "Remove" on one item 2. Observe cart | Item removed. Cart badge decreases by 1. | Item removed. Cart badge decreases by 1. | Pass |
| CHK-01 | Complete checkout with valid details | Cart has at least 1 item | 1. Click Checkout 2. Enter First Name, Last Name, Postal Code 3. Click Continue 4. Click Finish | Order confirmed. "Thank you for your order!" displayed. | Order confirmed. | Pass |
| CHK-02 | Checkout with missing fields | On checkout information page | 1. Leave all fields empty 2. Click Continue | Error: required fields message displayed. | Error displayed correctly. | Pass |
| CHK-03 | Cancel checkout | On checkout information page | 1. Click Cancel | Returned to cart page. Cart contents unchanged. | Returned to cart page unchanged. | Pass |
| CHK-04 | Checkout with special characters in name fields and alphabets in zip code | On checkout information page | 1. Enter special characters in name fields 2. Enter alphabets in zip code 3. Click Continue 4. Click Finish | Error displayed for invalid data type. | Checkout completed and order confirmed without error. | **Fail** |

### Navigation

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| NAV-01 | Logout functionality | Logged in on any page | 1. Open menu 2. Click Logout | Redirected to login page. Session cleared. | Redirected to login page. Session cleared. | Pass |
| NAV-02 | Continue shopping from cart | On cart page with items | 1. Click "Continue Shopping" | Redirected to inventory page. Cart badge retains count. | Redirected to inventory page. Cart badge retained. | Pass |

---

## Problem User

### Login

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| LOG-01 | Successful login with valid credentials | Browser at login page | 1. Enter username 2. Enter password 3. Click Login | Redirected to /inventory.html. No error displayed. | Redirected to /inventory.html. No error displayed. | Pass |
| LOG-02 | Login with invalid password | Browser at login page | 1. Enter valid username 2. Enter incorrect password 3. Click Login | Error: "Epic sadface: Username and password do not match any user in this service." | Error message displayed correctly. | Pass |
| LOG-03 | Login with empty fields | Browser at login page | 1. Leave fields blank 2. Click Login | Error: "Epic sadface: Username is required." | Error message displayed correctly. | Pass |

### Inventory and Product

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| INV-01 | Add all products to cart | Logged in, on inventory page | 1. Click "Add to cart" for all items 2. Check cart badge | Cart badge shows 6. | 3 out of 6 items cannot be added to cart. | **Fail** |
| INV-02 | Sort by price low to high | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (low to high)" | Products in ascending price order. | Products in ascending price order. | Pass |
| INV-03 | Sort by price high to low | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (high to low)" | Products in descending price order. | Products in descending price order. | Pass |
| INV-04 | Sort by Name A-Z | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (A-Z)" | Products in alphabetical order, A first. | Products in alphabetical order, A first. | Pass |
| INV-05 | Sort by Name Z-A | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (Z-A)" | Products in reverse alphabetical order, Z first. | Products in reverse alphabetical order, Z first. | Pass |
| INV-06 | View product details | Logged in, on inventory page | 1. Click product name or image | Navigates to detail page. Images match inventory page. | Different images displayed on inventory page vs product detail page for 3 items. | **Fail** |

### Cart and Checkout

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| CRT-01 | Remove item from cart | 2 items in cart, on cart page | 1. Click "Remove" on one item 2. Observe cart | Item removed. Cart badge decreases by 1. | Item removed. Cart badge decreases by 1. | Pass |
| CHK-01 | Complete checkout with valid details | Cart has at least 1 item | 1. Click Checkout 2. Enter First Name, Last Name, Postal Code 3. Click Continue 4. Click Finish | Order confirmed. "Thank you for your order!" displayed. | Last Name field does not accept input. Error thrown. Cannot proceed. | **Fail** |
| CHK-02 | Cancel checkout | On checkout information page | 1. Click Cancel | Returned to cart page. Cart contents unchanged. | Returned to cart page unchanged. | Pass |

### Navigation

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| NAV-01 | Logout functionality | Logged in on any page | 1. Open menu 2. Click Logout | Redirected to login page. Session cleared. | Redirected to login page. Session cleared. | Pass |
| NAV-02 | Continue shopping from cart | On cart page with items | 1. Click "Continue Shopping" | Redirected to inventory page. Cart badge retains count. | Redirected to inventory page. Cart badge retained. | Pass |

---

## Error User

### Login

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| LOG-01 | Successful login with valid credentials | Browser at login page | 1. Enter username 2. Enter password 3. Click Login | Redirected to /inventory.html. No error displayed. | Redirected to /inventory.html. No error displayed. | Pass |
| LOG-02 | Login with invalid password | Browser at login page | 1. Enter valid username 2. Enter incorrect password 3. Click Login | Error: "Epic sadface: Username and password do not match any user in this service." | Error message displayed correctly. | Pass |
| LOG-03 | Login with empty fields | Browser at login page | 1. Leave fields blank 2. Click Login | Error: "Epic sadface: Username is required." | Error message displayed correctly. | Pass |

### Inventory and Product

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| INV-01 | Add all products to cart | Logged in, on inventory page | 1. Click "Add to cart" for all items 2. Check cart badge | Cart badge shows 6. | 3 out of 6 items cannot be added to cart. | **Fail** |
| INV-02 | Sort by price low to high | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (low to high)" | Products in ascending price order. | Products in ascending price order. | Pass |
| INV-03 | Sort by price high to low | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (high to low)" | Products in descending price order. | Products in descending price order. | Pass |
| INV-04 | Sort by Name A-Z | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (A-Z)" | Products in alphabetical order, A first. | Products in alphabetical order, A first. | Pass |
| INV-05 | Sort by Name Z-A | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (Z-A)" | Products in reverse alphabetical order, Z first. | Products in reverse alphabetical order, Z first. | Pass |
| INV-06 | View product details | Logged in, on inventory page | 1. Click product name or image | Navigates to detail page. Product info displays correctly. | Product description not displayed on detail page. | **Fail** |

### Cart and Checkout

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| CRT-01 | Remove item from cart | 2 items in cart, on cart page | 1. Click "Remove" on one item 2. Observe cart | Item removed. Cart badge decreases by 1. | Item removed. Cart badge decreases by 1. | Pass |
| CHK-01 | Complete checkout with valid details | Cart has at least 1 item | 1. Click Checkout 2. Enter First Name, Last Name, Postal Code 3. Click Continue 4. Click Finish | Order confirmed. "Thank you for your order!" displayed. | Last Name field does not accept input but allows proceeding to next step. | **Fail** |
| CHK-02 | Checkout with missing fields | On checkout information page | 1. Leave all fields empty 2. Click Continue | Error: required fields message displayed. | Error displayed correctly. | Pass |
| CHK-03 | Proceed to finish order | Cart has at least 1 item | 1. Click Checkout 2. Enter details 3. Click Continue 4. Click Finish | Order confirmed. | Finish button is not clickable. Order cannot be completed. | **Fail** |
| CHK-04 | Cancel checkout | On checkout information page | 1. Click Cancel | Returned to cart page. Cart contents unchanged. | Returned to cart page unchanged. | Pass |
| CHK-05 | Checkout with special characters in name fields and alphabets in zip code | On checkout information page | 1. Enter special characters in name fields 2. Enter alphabets in zip code 3. Click Continue 4. Click Finish | Error displayed for invalid data type. | Checkout completed and order confirmed without error. | **Fail** |

### Navigation

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| NAV-01 | Logout functionality | Logged in on any page | 1. Open menu 2. Click Logout | Redirected to login page. Session cleared. | Redirected to login page. Session cleared. | Pass |
| NAV-02 | Continue shopping from cart | On cart page with items | 1. Click "Continue Shopping" | Redirected to inventory page. Cart badge retains count. | Redirected to inventory page. Cart badge retained. | Pass |

---

## Visual User

### Login

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| LOG-01 | Successful login with valid credentials | Browser at login page | 1. Enter username 2. Enter password 3. Click Login | Redirected to /inventory.html. No error displayed. | Redirected to /inventory.html. No error displayed. | Pass |
| LOG-02 | Login with invalid password | Browser at login page | 1. Enter valid username 2. Enter incorrect password 3. Click Login | Error: "Epic sadface: Username and password do not match any user in this service." | Error message displayed correctly. | Pass |
| LOG-03 | Login with empty fields | Browser at login page | 1. Leave fields blank 2. Click Login | Error: "Epic sadface: Username is required." | Error message displayed correctly. | Pass |

### Inventory and Product

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| INV-01 | Add all products to cart | Logged in, on inventory page | 1. Click "Add to cart" for all items 2. Check cart badge | Cart badge shows 6. | Cart badge shows 6. | Pass |
| INV-02 | Sort by price low to high | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (low to high)" | Products in ascending price order. | Products not sorted correctly by price. | **Fail** |
| INV-03 | Sort by price high to low | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Price (high to low)" | Products in descending price order. | Products not sorted correctly by price. | **Fail** |
| INV-04 | Sort by Name A-Z | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (A-Z)" | Products in alphabetical order, A first. | Products in alphabetical order, A first. | Pass |
| INV-05 | Sort by Name Z-A | Logged in, on inventory page | 1. Click sort dropdown 2. Select "Name (Z-A)" | Products in reverse alphabetical order, Z first. | Products in reverse alphabetical order, Z first. | Pass |
| INV-06 | View product details | Logged in, on inventory page | 1. Click product name or image | Navigates to detail page. Images match inventory page. | Different image displayed on inventory page vs product detail page. | **Fail** |
| INV-07 | Price consistency between inventory and cart across page refreshes | Logged in, items in cart | 1. Note product price on inventory page 2. Add item to cart 3. Navigate to cart 4. Compare prices 5. Refresh inventory page | Prices on inventory and cart pages match. Price is stable on refresh. | Inventory prices change on every refresh. Cart price does not match inventory price. | **Fail** |

### Cart and Checkout

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| CRT-01 | Remove item from cart | 2 items in cart, on cart page | 1. Click "Remove" on one item 2. Observe cart | Item removed. Cart badge decreases by 1. | Item removed. Cart badge decreases by 1. | Pass |
| CHK-01 | Complete checkout with valid details | Cart has at least 1 item | 1. Click Checkout 2. Enter First Name, Last Name, Postal Code 3. Click Continue 4. Click Finish | Order confirmed. "Thank you for your order!" displayed. | Order confirmed. | Pass |
| CHK-02 | Checkout with missing fields | On checkout information page | 1. Leave all fields empty 2. Click Continue | Error: required fields message displayed. | Error displayed correctly. | Pass |
| CHK-03 | Cancel checkout | On checkout information page | 1. Click Cancel | Returned to cart page. Cart contents unchanged. | Returned to cart page unchanged. | Pass |
| CHK-04 | Checkout with special characters in name fields and alphabets in zip code | On checkout information page | 1. Enter special characters in name fields 2. Enter alphabets in zip code 3. Click Continue 4. Click Finish | Error displayed for invalid data type. | Checkout completed and order confirmed without error. | **Fail** |

### Navigation

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| NAV-01 | Logout functionality | Logged in on any page | 1. Open menu 2. Click Logout | Redirected to login page. Session cleared. | Redirected to login page. Session cleared. | Pass |
| NAV-02 | Continue shopping from cart | On cart page with items | 1. Click "Continue Shopping" | Redirected to inventory page. Cart badge retains count. | Redirected to inventory page. Cart badge retained. | Pass |

### UI Elements

| TC ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| EDGE-01 | Cart icon position | Logged in | 1. Observe cart icon position on inventory page | Cart icon positioned correctly in top-right. | Cart icon is incorrectly positioned. | **Fail** |
| EDGE-02 | Checkout button position | Items in cart, on cart page | 1. Navigate to cart page 2. Observe checkout button position | Checkout button positioned at the bottom of the cart page. | Checkout button is incorrectly positioned. | **Fail** |

---

## Test Execution Summary

| User Account | Pass | Fail | Total |
|---|---|---|---|
| standard_user | 15 | 1 | 16 |
| locked_out_user | 0 | 1 | 1 |
| performance_glitch_user | 15 | 2 | 17 |
| problem_user | 11 | 3 | 14 |
| error_user | 12 | 5 | 17 |
| visual_user | 12 | 7 | 19 |
| **Total** | **65** | **19** | **84** |
