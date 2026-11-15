# SauceDemo Test Plan

## 1. Objective
Test the main features of https://www.saucedemo.com (login, product list, cart, checkout).

## 2. Scope
**In scope:** Login, Products page, Cart, Checkout

**Out of scope:** Performance and security testing

## 3. Test Environment
- Browser: Chrome (latest)
- OS: Windows 11
- Test users: standard_user, locked_out_user

## 4. Test Cases

| ID | Feature | Test Case | Steps | Expected Result | Status |
|----|---------|-----------|-------|-----------------|--------|
| TC01 | Login | Valid login | Enter standard_user and correct password, click Login | Products page opens | | pass
| TC02 | Login | Wrong password | Enter wrong password, click Login | Error message is shown | |
| TC03 | Login | Locked user | Login with locked_out_user | "User has been locked out" message | |
| TC04 | Login | Empty fields | Click Login with empty fields | "Username is required" message | |
| TC05 | Cart | Add one product | Click Add to cart on one item | Cart badge shows 1 | |

## 5. Bug Reports
(Will be added after testing)
