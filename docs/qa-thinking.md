# 🧠 How Senior QA Engineers Think

Strong QA is not about creating the most test cases.
It is about validating the right workflows at the right depth based on risk.

## 1. Think in workflows, not isolated features
A feature may pass on its own and still fail as part of a business journey.

Example:
A payment screen can look successful while the backend transaction is duplicated, delayed, or missing from reporting.

That is why senior QA looks at the full path:
**user action → API → backend processing → data storage → visible output**

## 2. Validate data, not just UI
A UI success message is not proof that the system worked correctly.

Always ask:
- was the correct request sent?
- was the correct record created?
- was status updated correctly?
- does the dashboard/report reflect the same truth?

## 3. Prioritize by business risk
Not all bugs matter equally.

In SaaS and FinTech systems, the highest-priority validation areas usually involve:
- money movement
- activation / conversion steps
- subscription state
- dashboard accuracy
- external integrations

## 4. Assume failure conditions exist
Good QA does not only check whether a system works.
It checks how the system behaves when something goes wrong.

Examples:
- duplicate clicks
- retries after timeout
- invalid payloads
- delayed callbacks
- out-of-order updates

## 5. Focus on business impact
Severity is not just technical complexity.
It is the effect on the business and user.

Examples:
- login validation issue → user inconvenience
- duplicate payment issue → financial risk and disputes
- dashboard mismatch → loss of trust and poor decisions

## 6. Use artifacts to support decisions
Spreadsheets, RTMs, and collections are not just documents.
They are evidence used to support one important conclusion:

**Is this system ready for release?**
