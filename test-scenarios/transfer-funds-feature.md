# TEST SCENATRIO: BANK APP TRANSFER REFUNDS FEATURE

## 1. DESCRIPTION

As a bank account holder, I want to be able to transfer funds to another account within the same bank, so that I can pay bills or send money to friends.

## 2. BUSINESS RULES

- Transfer Limits: The minimum transfer amount is 1.00 EUR. The maximum daily transfer limit is 5,000.00 EUR.
- Insufficient Funds: A transfer cannot be processed if the account balance is less than the transfer amount.
- Account Status: Transfers can only be made from active accounts. Blocked or frozen accounts cannot initiate transfers.

---

## 3. POSITIVE SCENARIOS

| ID    | Test Scenario                                                                                                 | Priority |
| :---- | :------------------------------------------------------------------------------------------------------------ | :------- |
| TC-01 | Verify that account holder can transfer amount of 10.00 EUR to another account when his balance is 20.00 EUR. | Medium   |
| TC-02 | Verify that account holder can transfer 4,000.00 EUR to another account when his balance is 4,001.00 EUR.     | Medium   |
| TC-03 | Verify that account holder can check whether they have active account after log in.                           | High     |

## 4. NEGATIVE SCENARIOS

| ID    | Test Scenario                                                                                                                                                                    | Priority |
| :---- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------- |
| TC-04 | Verify that account holder who has blocked account is not allowed to proceed any transfer.                                                                                       | High     |
| TC-05 | Verify that account holder is notified by error message when trying to proceed transfer of 5,001.00 EUR.                                                                         | High     |
| TC-06 | Verify that account holder is notified by error message "Your account balance is lower than the transfer" when attempts of transfer 100.00 EUR with account balance of 1.00 EUR. |

## 5. EDGE CASE SCENARIOS

| ID    | Test Scenario                                                                                                                                                                                              | Priority |
| :---- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------- |
| TC-07 | Verify that account holder can proceed a transfer succesfully of amount 1.01 EUR.                                                                                                                          |
| TC-08 | Verify that account holder is notified by error message "You exceeded maximum daily transfer of 5,000 EUR" after attempts to create one transfer of 3,000 EUR at 8:00 UTC and then 3,000 EUR at 18:00 UTC. |
| TC-09 | Verify that account holder is notified by error message "Your account balance needs to be higher than your transfer amount" when attempts transfer of 10.00 EUR and their account balance is 10.00 EUR.    |
