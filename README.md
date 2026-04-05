# SaaS Conversion Funnel QA Portfolio

## Overview

This project demonstrates how I test a SaaS conversion funnel for a Stripe-style platform, focusing on end-to-end validation from user sign-up through onboarding, API setup, payment execution, and billing.

The objective is to ensure users can move through the funnel without friction while maintaining data integrity, system reliability, and accurate business outcomes.

This portfolio reflects how QA directly supports **conversion, activation, and revenue-critical workflows**.

---

## Disclaimer

This is a personal QA portfolio project created for demonstration and learning purposes.

All workflows are generalized and do not contain any proprietary or confidential information from real systems.

---

## Funnel Under Test

Visitor → Sign Up → Email Verification → Onboarding → API Key Generation → Sandbox Usage → Payment Execution → Dashboard Validation → Billing / Subscription

---

## Scope

- User onboarding and activation
- API key lifecycle and access control
- Payment processing workflows
- Billing and subscription management
- Data integrity across UI, API, and backend
- Funnel drop-off risk validation

---

## Key QA Focus

- End-to-end system validation (UI → API → DB → Output)
- Transaction integrity and consistency
- Error handling, retries, and edge cases
- Prevention of duplicate or inconsistent data
- User experience impact on conversion and retention
- Validation of business-critical flows (payments, subscriptions)

---

## API Testing Coverage

This project includes API validation for key SaaS funnel workflows, simulating how a Stripe-style platform is tested from onboarding through payment and billing.

### API Scope Covered

- Customer creation
- Duplicate user validation
- Payment intent creation
- Payment confirmation
- Payment status retrieval
- Subscription creation and retrieval

### API Testing Approach

- Assertions on HTTP status codes and response structure
- Validation of critical fields (IDs, status, amount, currency)
- Chaining of dynamic data using variables:
  - `customer_id`
  - `payment_intent_id`
  - `subscription_id`
- End-to-end API flow validation rather than isolated endpoint testing
- Negative testing (duplicate requests, invalid inputs)

### Example End-to-End API Flow

1. Create customer  
2. Validate duplicate email handling  
3. Create payment intent using `customer_id`  
4. Confirm payment using `payment_intent_id`  
5. Retrieve payment status  
6. Create subscription  
7. Validate subscription data  

---

## Test Artifacts

- Test Strategy (risk-based approach)
- Funnel Overview and workflow mapping
- Manual Test Cases (Excel-based execution tracker)
- API Test Scenarios and Postman Collection
- RTM (Requirement Traceability Matrix)
- Defect Summary
- Sample Test Data

---

## Tools & Approach

- Manual Testing (functional, regression, exploratory)
- API Testing using Postman (with assertions and chaining)
- Data validation across system layers
- Risk-based prioritization
- End-to-end funnel validation

---

## Repository Structure

docs/ → Test strategy, RTM, risk analysis
test-cases/ → Manual and API test cases (OpenMRS-style tracker)
postman/ → API collections with assertions and chaining
sample-data/ → Test data for positive and negative scenarios


---

## Why This Portfolio Matters

In SaaS platforms, failures in the funnel directly impact:

- User conversion
- Activation success
- Payment completion
- Revenue generation
- Customer retention

This project demonstrates how I approach testing systems where **quality issues translate directly into business impact**.

---

## About Me

Senior QA Engineer with 20+ years of experience across payments, SaaS, IoT, and enterprise systems.

I specialize in validating systems end-to-end, ensuring data integrity, workflow accuracy, and reliable business outcomes.

I have successfully transitioned across industries by quickly understanding system architecture, workflows, and critical business logic, and applying risk-based testing to ensure production readiness.
