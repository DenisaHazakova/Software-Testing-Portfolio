# TEST SCENARIO: Login Authentication

## 1. DESCRIPTION

Verify the functionality of the web application's login process. The system must ensure secure user authentication, handle successful logins correctly, and respond appropriately to invalid inputs or security threats.

## 2. BUSINESS RULES

- **Account Lockout:** The account is locked after 5 consecutive failed login attempts.
- **Session Expiry:** The session expires after 30 minutes of inactivity.
- **Case Sensitivity:** Passwords are case-sensitive.
- **Email Format:** The email must be in a valid format (e.g., user@domain.com).

---

## 3. POSITIVE SCENARIOS

| ID    | Test Scenario                                                                              | Priority |
| :---- | :----------------------------------------------------------------------------------------- | :------- |
| TC-01 | Verify that a user can successfully log in with valid credentials                          | High     |
| TC-02 | Verify that a user can log in when the "remember me" checkbox is selected                  | Medium   |
| TC-03 | Verify that a user can log in when the "remember me" checkbox is unchecked                 | Medium   |
| TC-04 | Verify that a user can view the password when "show password" is toggled on                | Medium   |
| TC-05 | Verify that a user can navigate to the password recovery flow                              | Medium   |
| TC-06 | Verify that a user remains logged in during active usage beyond 30 minutes                 | Medium   |
| TC-07 | Verify that a user can mask the password when "hide password" is toggled                   | Low      |
| TC-08 | Verify that a user can successfully log in with plus-addressing (e.g., user+test@mail.com) | Low      |

## 4. NEGATIVE SCENARIOS

| ID    | Test Scenario                                                                         | Priority |
| :---- | :------------------------------------------------------------------------------------ | :------- |
| TC-09 | Verify that a user cannot log in when the email field is empty                        | High     |
| TC-10 | Verify that a user cannot log in when the password field is empty                     | High     |
| TC-11 | Verify that a user cannot log in with an invalid email format                         | High     |
| TC-12 | Verify that a user cannot log in with a correct email and incorrect password          | High     |
| TC-13 | Verify that a user cannot log in with an unregistered email                           | High     |
| TC-14 | Verify that a user cannot log in with incorrect password casing                       | High     |
| TC-15 | Verify that a user cannot log in when the account is locked (after 5 failed attempts) | High     |
| TC-16 | Verify that a user cannot access protected pages after a 30-minute session expiry     | High     |
| TC-17 | Verify that a user cannot log in when both fields are empty                           | Medium   |

## 5. EDGE CASE SCENARIOS

| ID    | Test Scenario                                                                     | Priority |
| :---- | :-------------------------------------------------------------------------------- | :------- |
| TC-18 | Verify immediate account lockout on the 5th consecutive failed attempt            | High     |
| TC-19 | Verify counter reset when a correct password is entered on the 4th attempt        | Medium   |
| TC-20 | Verify re-authentication requirement at the exact 30-minute inactivity mark       | Medium   |
| TC-21 | Verify login with mixed-case email (email matching should be case-insensitive)    | Medium   |
| TC-22 | Verify behavior when leading/trailing whitespace is included in fields            | Medium   |
| TC-23 | Verify session extension when activity occurs just before the 30-minute threshold | Medium   |
| TC-24 | Verify toggle control stability during multiple rapid clicks                      | Low      |
| TC-25 | Verify submission failure when the email field contains only whitespace           | Low      |
| TC-26 | Verify login behavior with extremely long strings (exceeding field limits)        | Low      |
