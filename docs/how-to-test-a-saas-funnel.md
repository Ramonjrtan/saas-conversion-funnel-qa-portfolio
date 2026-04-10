# 🧪 How to Test a SaaS Funnel

A SaaS funnel should be tested as a connected business journey, not as a list of unrelated pages.

## Step 1: Identify the core conversion path
Define the highest-value user journey.

For this project:
**Sign Up → Verify Email → Onboard → Generate API Key → Use Sandbox → Execute Payment → Validate Dashboard → Manage Billing**

## Step 2: Map the system layers
For each step, identify:
- UI behavior
- API calls
- backend processing
- stored data
- visible outputs or dashboards

## Step 3: Validate success and failure paths
Do not stop at happy path coverage.
Also test:
- invalid sign-up data
- expired verification links
- incomplete onboarding
- failed payments
- duplicate requests
- retry / timeout behavior

## Step 4: Check downstream truth
The most common hidden defects happen when a system appears successful in one layer but fails in another.

Verify that:
- API status matches backend state
- backend state matches dashboard data
- dashboard data matches billing outcomes

## Step 5: Review business impact
Ask what each failure would do to:
- conversion
- revenue
- retention
- trust
- operational visibility

## Step 6: Convert findings into a QA recommendation
The final output is not just a bug list.
It is a release-readiness view supported by evidence.
