## AI Tools

- ChatGPT
- Claude
- Gemini
- Copilot
- GitHub Copilot

## Test Scenario prompt example

**Role**

You are a senior QA engineer with extensive experience in writing test scenarios for web applications. You have deep knowledge of authentication systems, security testing, and both functional and non-functional testing practices.

**Context**

We are building a web application that includes a Login Authentication feature. The application serves regular end users who access it through a browser. The login feature must handle both successful authentication attempts, and is a critical security touchpoint in the system.

**Expected output**

Generate a comprehensive set of test scenarios for the Login / Authentication feature. Cover the following scenarios types:

- positive scenarios (valid, expected user behaviour)
- negative scenarios (invalid inputs, wrong credentials)
- edge case scenarios (boundary conditions, unusual but possible situations) for each scenario, write a clear statement using this formula: "Verify that [user] can/cannot [action] when [condition]"

**Input data**

- feature: login/ authentication
- fields: email address, password
- actions available: submit login form, show/hide password, "remember me" checkbox, "forgot password" link

**Business rules**

- account locks after 5 consecutive failed login attempts
- session expires after 30minutes of inactivity
- password is case-sensitive
- email must be in valid format (e.g. user@domain.com)

**Constraints**

- do not write test steps o test cases - scenarios only
- each scenario must be single, self-contained statement
- do not repeat the same scenario in different wording
- include at least 3 scenarios per type (positive, negative, edge case)

**Format**

Return the scenarios as numbered list, grouped under three headings: positive scenarios, negative scenarios, edge case scenarios
Example:

## **Positive scenarios**

1. Verify that...
2. Verify that...

## **Negative Scenarios**

3. Verify that...
4. Verify that...

## **Edge Cases**

5. Verify that...
6. Verify that...
