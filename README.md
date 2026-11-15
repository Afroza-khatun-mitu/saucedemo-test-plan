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

| ID | Feature | Test Case | Steps | Expected Result | Status | Comments |
|----|---------|-----------|-------|-----------------|--------|----------|
| TC01 | Login | Valid login | Enter standard_user and correct password, click Login | Products page opens | Pass | |
| TC02 | Login | Wrong password | Enter standard_user and wrong password | Error: username and password do not match |Pass|Error massage shown correctly, but the text is clipped at the top and bottom of the red box.|
| TC03 | Login | Wrong username | Enter wrong username and correct password | Error: username and password do not match |pass | Error massage shown correctly, but the text is clipped at the top and bottom of the red box.|
| TC04 | Login | Both wrong | Enter wrong username and wrong password | Error: username and password do not match |pass |Error massage shown correctly, but the text is clipped at the top and bottom of the red box.|
| TC05 | Login | Both fields empty | Click Login with empty fields | Error: Username is required |pass| |
| TC06 | Login | Username only | Enter username, leave password empty | Error: Password is required |pass| |
| TC07 | Login | Password only | Enter password, leave username empty | Error: Username is required |pass| |
| TC08 | Login | Locked out user | Login with locked_out_user | Error: this user has been locked out |pass | |
| TC09 | Login | Username case sensitive | Enter STANDARD_USER with correct password | Error is shown |pass||
| TC10 | Login | Password case sensitive | Enter standard_user with password in capital letters | Error is shown |pass |suggestion:add a show/hide password(eye)icon so users can check what they typed|
| TC11 | Login | Spaces in username | Enter " standard_user " with spaces, correct password | Error is shown (or note actual behavior) |pass| |
| TC12 | Login | Login with Enter key | Type valid details, press Enter | Products page opens |pass|Enter works when the cursor is in a field.Dose nothing outside the form (expected) |
| TC13 | Login | Close error message | Trigger any error, click X on error box | Error message disappears |pass | |
| TC14 | Login | Login after failed attempt | Try wrong password, then correct password | Products page opens |pass | |
| TC15 | Login | Open page without login | Open saucedemo.com/inventory.html directly | Error: must be logged in, stays on login page |pass | |
| TC16 | Login | Logout | Login, open menu, click Logout | Login page opens |pass | |
| TC17 | Login | Back button after logout | Logout, click browser Back | Products page is not shown |pass | |
| TC18 | Login | problem_user login | Login with problem_user | Products page opens |pass | |
| TC19 | Login | performance_glitch_user login | Login with performance_glitch_user | Products page opens (note how long it took) |pass |take 5 to 6 sec|
| TC20 | Login | Password is hidden | Type in password field | Characters shown as dots |pass | suggestion:add a show/hide password(eye)icon so users can check what they typed|

## 5. Bug Reports
(Will be added after testing)
