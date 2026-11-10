# Synthetic walkthrough records

All names, IDs, and entries below are examples. No control test or approval is represented as completed.

| Database | Sample record | Fields and links |
| --- | --- | --- |
| AI Use Cases | UC-001 — Internal policy assistant | Owner: Product; status: Intake; data: approved internal policies only; next review: before pilot; links to R-001 and D-001 |
| Risks | R-001 — Restricted document disclosure | Impact: High; likelihood: Medium; priority: High; owner: Security; status: Open; links to UC-001, C-001, A-001 |
| Controls | C-001 — Enforce source permissions | Owner: Security; frequency: each material change; status: Proposed; links to R-001 and E-001 |
| Evidence | E-001 — Negative access test results | Owner: Security; period: pilot readiness; review status: Requested; location: blank until the test exists; links to C-001 and D-001 |
| Actions | A-001 — Run denied-access test cases | Owner: Security; due: before pilot; priority: High; status: To do; links to R-001 and C-001 |
| Decisions | D-001 — May the pilot launch? | Outcome: Pending; approver: Executive sponsor; date: blank; condition: review E-001 and other launch gates; links to UC-001 and E-001 |

**Trace:** UC-001 → R-001 → C-001 → E-001, with A-001 tracking the test and D-001 blocked until evidence is reviewed. This trace makes a governance claim inspectable instead of hiding it in a status label.
