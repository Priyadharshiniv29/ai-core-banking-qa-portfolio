# AI Prompt Library – Banking QA

## 1. Purpose

This document contains reusable AI prompts designed to support functional testing activities for a fictional core banking application.

The prompts are designed to assist QA engineers with requirement analysis, test scenario generation, test case preparation and defect analysis.

AI-generated outputs must always be reviewed and validated by the QA engineer.

---

## 2. Prompt 01 – Requirement Analysis

### Objective
Identify missing, ambiguous and incomplete banking requirements.

### Prompt

Act as a Senior Core Banking QA Engineer.

Analyse the following requirement:

A customer can transfer money from a savings account to another bank account. The transfer must be rejected if sufficient funds are not available.

Business assumption:
- Minimum account balance: €5,000.
- Transfers are processed through a batch job.
- Customers receive transaction notifications.

Identify:
1. Functional requirements.
2. Missing business rules.
3. Ambiguous requirements.
4. Positive scenarios.
5. Negative scenarios.
6. Integration dependencies.

Do not invent missing business rules. List assumptions separately.

### QA Validation
The QA engineer must verify that AI has correctly identified the business rules and has not introduced unsupported assumptions.

---

## 3. Prompt 02 – Test Scenario Generation

### Objective
Generate comprehensive test scenarios from approved banking requirements.

### Prompt

Act as an experienced banking QA engineer.

Generate test scenarios for outward fund transfers from savings accounts.

Consider:
- Available balance validation.
- Minimum balance validation.
- Pending transactions.
- Insufficient funds.
- Batch processing.
- Receiving bank rejection.
- Duplicate rejection messages.
- Customer notifications.
- System failure and recovery.

Categorise scenarios into positive, negative, boundary and integration testing.

Identify missing requirements separately.

### QA Validation
Check whether all important business conditions are covered and whether expected outcomes follow the approved requirements.

---

## 4. Prompt 03 – Detailed Test Case Generation

### Objective
Convert approved test scenarios into detailed test cases.

### Prompt

Generate detailed functional test cases for outward fund transfers.

Use the following format:

- Test Case ID
- Test Scenario
- Preconditions
- Test Data
- Execution Steps
- Expected Result
- Test Type
- Priority

Include positive, negative and boundary test cases.

Do not assume behaviour that is not specified in the business requirements.

### QA Validation
Review preconditions, test data, execution steps and expected results for correctness.

---

## 5. Prompt 04 – Boundary Value Analysis

### Objective
Identify boundary conditions for transfer amount validation.

### Prompt

Act as an ISTQB-certified QA engineer.

Account balance: €15,000.

Minimum required balance: €5,000.

Assume the remaining account balance must be greater than or equal to the minimum balance.

Calculate:
1. Maximum permitted transfer amount.
2. Boundary value.
3. Value immediately below the boundary.
4. Value immediately above the boundary.

Generate test cases with expected results.

### QA Validation
Independently verify the calculations and expected results against the stated business rule.

---

## 6. Prompt 05 – Defect Analysis

### Objective
Prepare clear and reproducible defect reports.

### Prompt

Act as a senior banking QA engineer.

Analyse the following defect:

A customer initiates an outward fund transfer of €8,000. The receiving bank rejects the transaction. The transaction status is updated to REJECTED, but the reserved amount is not released.

Generate:
- Defect title.
- Preconditions.
- Steps to reproduce.
- Actual result.
- Expected result.
- Severity.
- Business impact.

Do not invent technical root causes.

### QA Validation
Confirm that the defect is reproducible and that severity is assigned according to actual business impact.

---

## 7. Prompt 06 – SQL Validation Assistance

### Objective
Generate SQL queries to validate banking transaction data.

### Prompt

Act as a banking database testing specialist.

Assume fictional tables for customer accounts and fund transfers.

Help generate SQL queries to validate:
- Account ledger balance.
- Available balance.
- Reserved amount.
- Transaction status.
- Duplicate transaction references.

Explain each query and its expected output.

Do not assume actual database table names or schemas. Ask for the schema if required.

### QA Validation
Review SQL logic, table relationships and expected results before execution.

---

## 8. Prompt 07 – AI Output Quality Review

### Objective
Identify incorrect or incomplete AI-generated test cases.

### Prompt

Act as a Senior QA Reviewer.

Review the following AI-generated test cases against the approved banking requirements.

Identify:
- Incorrect expected results.
- Missing test scenarios.
- Duplicate scenarios.
- Invalid test data.
- Missing boundary conditions.
- Unsupported assumptions.

Provide corrected test cases and explain each correction.

Do not automatically accept the original AI output.

### QA Validation
The QA engineer makes the final decision on test case acceptance.

---

## 9. Responsible AI Usage

- Do not upload confidential banking information.
- Use fictional test data.
- Validate AI-generated outputs independently.
- Never assume AI-generated SQL is safe to execute.
- Keep business rules and assumptions separate.
- Do not claim AI-generated work as independently executed testing.

## 10. Conclusion

This prompt library demonstrates how Generative AI can support traditional banking QA activities while keeping the QA engineer responsible for quality, accuracy and business-rule validation.
