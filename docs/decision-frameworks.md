# 🎯 QA Decision Frameworks

This guide shows how to decide what to test first, how deep to test, and how to translate findings into release recommendations.

## 1. Risk-based testing
Start with the flows that create the highest business risk.

### Test first
- payment execution
- billing and subscription changes
- onboarding completion blockers
- API key generation and access control
- dashboard figures used for decisions or customer visibility

### Why
If these fail, the system may still look usable while causing revenue leakage, conversion loss, or data inconsistency.

## 2. When to write detailed vs high-level test cases

### Use detailed test cases when:
- the workflow is business-critical
- the logic is stateful or integration-heavy
- multiple systems must stay consistent
- the result affects money, compliance, or trust

### Use higher-level test cases when:
- validating low-risk UI behavior
- covering cosmetic or simple content checks
- the area changes frequently and needs lighter maintenance

## 3. Production validation priority
If time is limited, prioritize in this order:

1. login / account access
2. onboarding completion
3. payment / subscription workflow
4. data persistence and API correctness
5. dashboard / report accuracy

## 4. Release recommendation logic
A release should not be recommended when any of the following are true:
- duplicate payment is possible
- billing state is incorrect or inconsistent
- dashboard figures do not match underlying data
- critical workflow blockers prevent user completion
- API responses create unreliable downstream behavior

## 5. Example severity thinking

### Critical
Defects that can cause financial loss, duplicate charges, major outages, or invalid business state.

### High
Defects that significantly break workflow accuracy, reporting trust, or core user completion.

### Medium
Defects that degrade the experience or require workaround but do not corrupt the core transaction state.

### Low
Minor usability or presentation issues with limited business impact.
