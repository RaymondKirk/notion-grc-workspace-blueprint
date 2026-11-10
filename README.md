# Notion GRC workspace blueprint

**Portfolio case study | Synthetic records | November 2026**

This is a buildable design for a small team's AI governance and GRC workspace in Notion. It is adapted from the architecture of my personal BMF workspace: a central dashboard, linked actions and goals, notes, and recurring review views. No personal BMF records or client data are included. This public blueprint is not a deployed client workspace or a downloadable Notion template.

## Problem and design choice

Governance work often breaks across spreadsheets, documents, and reminders. A team needs to answer: What AI uses exist? What risks and controls apply? Who owns the next action? What evidence supports a decision?

The design uses **six linked databases**, each with one job:

| Database | Required fields | Key links |
| --- | --- | --- |
| AI Use Cases | Name, purpose, owner, status, data classification, review date | Risks, Decisions |
| Risks | ID, scenario, impact, likelihood, priority, owner, status | Use Case, Controls, Actions |
| Controls | ID, objective, owner, frequency, status | Risks, Evidence |
| Evidence | ID, description, period, owner, review status, location | Controls, Decisions |
| Actions | Task, owner, due date, priority, status | Risk, Control, Use Case |
| Decisions | Question, outcome, approver, date, next review | Use Case, Evidence |

A control may mitigate several risks, and a risk may have several controls. Evidence belongs to a control and can support a decision. An action tracks work to do; it is never a substitute for evidence that work happened.

## Views that make it usable

- **Intake:** new AI use cases awaiting purpose, data, and owner review.
- **Risk review:** open high-priority risks grouped by owner and due date.
- **Control health:** controls missing current evidence or a named owner.
- **Action queue:** overdue and upcoming tasks, with blockers visible.
- **Decision log:** approvals, conditions, reviewer, and next review date.
- **Executive dashboard:** counts and links to these views, with a clear last-reviewed date. Counts should be labeled live only if driven by actual linked records.

## Example workflow

The [synthetic walkthrough](sample-records.md) follows a fictional internal AI knowledge assistant. It links one use case to a risk, control, evidence request, action, and conditional decision.

1. Product owner submits intended users, data, and exclusions.
2. Risk owner records concrete failure scenarios and assigns priority.
3. Control owner links high-priority risks to controls and defines evidence.
4. Actions track testing; evidence links to actual results once they exist.
5. Approver records a decision with conditions and a review date. Missing evidence cannot be treated as approval.

## Access and quality rules

- Grant edit rights by role; restrict decision and evidence approval to accountable reviewers.
- Keep sensitive documents in approved storage. The Evidence database may hold a restricted link and metadata instead of copying content into a broadly shared page.
- Use stable IDs for risks, controls, and evidence; do not rely only on page titles.
- Require owner, status, and next review date before a record is complete.
- Review overdue actions, stale evidence, and decisions after material changes.
- Before public sharing, remove personal data, internal URLs, access tokens, real names, relations, attachments, and database template content.

## Build sequence and acceptance check

1. Create the six databases and listed properties.
2. Add relations and test navigation in both directions.
3. Add the operational views and executive dashboard.
4. Enter only synthetic records and walk from use case to decision.
5. Verify a viewer cannot edit approvals or open restricted evidence.
6. Ask a new user to find a high-priority risk, its owner, evidence, and next action in under two minutes. This is a proposed usability check, not a measured result.

This blueprint shows how I translate governance requirements into a workspace with record types, ownership, review views, and decision evidence. A shareable Notion demo and a real usability test are future portfolio steps.
