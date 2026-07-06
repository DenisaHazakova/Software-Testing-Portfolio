# TEST SCENARIO: SHOPPING CART FEATURE

## 1. DESCRIPTION:

As a registered e-shop customer, I want to be able to add items to my shopping cart and change their quantity, so that I can conveniently purchase multiple items at once.

## 2. BUSINESS RULES:

- The maximum quantity for any single product in the cart is 10 units.
- If the cart is empty, the "Proceed to Checkout" button is inactive (disabled).
- The cart price must automatically update after a quantity change.

---

## 3. POSITIVE SCENARIOS

| ID    | Test Scenario                                                                         | Priority |
| :---- | :------------------------------------------------------------------------------------ | :------- |
| TC-01 | Verify that e-shop customer can successfully buy selected products at quantity of 10. | High     |

## 4. NEGATIVE SCENARIOS

| ID    | Test Scenario                                                                                 | Priority |
| :---- | :-------------------------------------------------------------------------------------------- | :------- |
| TC-02 | Verify that e-shop customer has button "Proceed to Checkout" disabled when the cart is empty. | High     |

## 5. EDGE CASE SCENARIOS

| ID    | Test Scenario                                                        | Priority |
| :---- | :------------------------------------------------------------------- | :------- |
| TC-03 | Verify that e-shop customer cannot add 11 units of selected product. | High     |
