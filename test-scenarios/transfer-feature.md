# TEST SCENARIO: BANK APP TRANSFERS FEATURE

## 1. DESCRIPTION

As a bank account holder, I want to be able to transfer funds to another account within the same bank, so that I can pay bills or send money to friends.

## 2. BUSINESS RULES

- Transfer Limits: The minimum transfer amount is 1.00 EUR. The maximum daily transfer limit is 5,000.00 EUR.
- Insufficient Funds: A transfer cannot be processed if the account balance is less than the transfer amount.
- Account Status: Transfers can only be made from active accounts. Blocked or frozen accounts cannot initiate transfers.

---

## 3. POSITIVE SCENARIOS

| ID    | Test Scenario                                                                          | Priority |
| :---- | :------------------------------------------------------------------------------------- | :------- |
| TC-01 | Verify that a transfer of 10.00 EUR is successful when the balance is 20.00 EUR.       | Medium   |
| TC-02 | Verify that a transfer of 4,000.00 EUR is successful when the balance is 4,001.00 EUR. | High     |
| TC-03 | Verify that a transfer of 1.00 EUR (minimum amount) is successful.                     | High     |

## 4. NEGATIVE SCENARIOS

| ID    | Test Scenario                                                                                           | Priority |
| :---- | :------------------------------------------------------------------------------------------------------ | :------- |
| TC-04 | Verify that a transfer cannot be initiated from a blocked account.                                      | High     |
| TC-05 | Verify that an error message is displayed when attempting to transfer 5,001.00 EUR.                     | High     |
| TC-06 | Verify that an error message is displayed when attempting to transfer amount exceeding account balance. | High     |

## 5. EDGE CASE SCENARIOS

| ID    | Test Scenario                                                                            | Priority |
| :---- | :--------------------------------------------------------------------------------------- | :------- |
| TC-07 | Verify that a daily transfer of 5,000 EUR (maximum daily limit) is successful.           | High     |
| TC-08 | Verify that a second transfer is blocked if cumulative daily transfers exceed 5,000 EUR. | High     |
| TC-09 | Verify that a transfer of -10.00 EUR is not succesful.                                   | High     |
