# HR tech evaluation: requirements

**Category:** SuccessFactors Recruiting replacement  
**Target vendor:** SmartRecruiters (unless an alternative is added to shortlist)  
**Decision type:** Replacement of the incumbent ATS within the broader SuccessFactors HRIS/EC stack  
**Requirements owner:** [Name / role]  
**Date issued to vendors:** [Date]  
**Weights fixed:** [Date — before first demo]

## Problem statement

The current recruiting system does not provide a reliable, low-effort workflow from
approved requisition through offer acceptance in a way that fits the broader SuccessFactors
HRIS/EC environment. The immediate symptoms, affected groups, duration, and cost must be
completed from evidence before demos:

| Question | Current evidence |
| --- | --- |
| What specifically happens that should not? | [e.g. approvals, feedback, reporting, or duplicate entry] |
| Who feels it? | [Recruiters, coordinators, hiring managers, candidates, HRIS/IT] |
| How long has it been happening? | [Date / period] |
| What has already been tried? | [Configuration, training, process change, workaround] |
| What will “fixed” mean in 12 months? | [Measurable outcome and baseline] |
| Cost of leaving it unchanged for two years | [Measured or modelled; label which] |

**Technology test:** confirm whether the root cause is product capability, configuration,
process design, training, ownership, or a combination. A new ATS is not the answer to a
process problem by default.

## Scope and constraints

| Area | Working scope |
| --- | --- |
| In scope now | Requisitions and approvals; candidate application; sourcing and agency submissions; interview scheduling and scorecards; offers; reporting/export; integrations; permissions; migration from SuccessFactors Recruiting; accessibility; support |
| Explicitly out of scope | Payroll; performance; engagement; employee master record, unless an integration requirement depends on it |
| Current system | SAP SuccessFactors Recruiting (within SuccessFactors HRIS / EC) |
| Employees | [Number] |
| Annual hires | [Number] |
| Users | Admin [n]; recruiters [n]; coordinators [n]; hiring managers [n]; interviewers [n] |
| Jurisdictions and data residency | [Countries / restrictions to confirm with legal] |
| Critical integrations | SuccessFactors HRIS / EC, identity provider, calendar/email, background check, assessment, BI/data warehouse, job boards |
| Go-live target | [Date and forcing event] |
| Incumbent notice deadline | [Date] |
| Budget | [Annual and one-off band, or “to be established”] |

## Must-have requirements

A failure disqualifies a vendor. If the team would still buy after a failure, move it to the
weighted table.

| ID | Testable requirement | Owner | Vendor A | Vendor B | Vendor C |
| --- | --- | --- | --- | --- | --- |
| M1 | Supports SSO through [identity provider], role-based access, and prompt deprovisioning. | IT / Security | Pass / Fail | Pass / Fail | Pass / Fail |
| M2 | Supports candidate and employee data residency/transfer requirements for [jurisdictions], subject to legal confirmation. | Legal / Security | Pass / Fail | Pass / Fail | Pass / Fail |
| M3 | Creates an employee record in SuccessFactors HRIS / EC after offer acceptance with the agreed field mapping and no re-keying. | HRIS owner | Pass / Fail | Pass / Fail | Pass / Fail |
| M4 | Provides export of candidates, applications, documents, feedback, audit history, and custom fields in a usable format without prohibited exit cost. | Data owner | Pass / Fail | Pass / Fail | Pass / Fail |
| M5 | Supports the required accessibility standard on candidate-facing application and status flows, with current evidence supplied. | Accessibility / Legal | Pass / Fail | Pass / Fail | Pass / Fail |
| M6 | Provides a documented support and escalation path covering the team’s operating hours, with service commitments supplied in writing. | Operations | Pass / Fail | Pass / Fail | Pass / Fail |
| M7 | Allows confidential requisitions and field/record permissions that prevent unauthorised access to compensation, notes, and protected data. | Security / HR | Pass / Fail | Pass / Fail | Pass / Fail |

## Weighted requirements

Weights total 100 and are provisional until the evaluation group confirms them **before the
first demo**. Score each requirement 1–5 and add an evidence flag: D demonstrated live, C
claimed, R reference-confirmed, W confirmed in writing.

| Rank | Requirement | Group | Tier | Weight | Owner |
| --- | --- | --- | --- | ---: | --- |
| 1 | A recruiter can manage requisition approval, candidate stages, corrections, and bulk actions without vendor services. | Core workflow | Should | 16 | TA operations |
| 2 | A hiring manager with no training can review a shortlist and submit independent feedback from a phone in under three minutes. | User experience | Should | 12 | Hiring manager |
| 3 | A candidate can apply on a phone, upload a document, schedule/reschedule, and see status without unnecessary account friction. | Candidate experience | Should | 12 | Candidate experience |
| 4 | A non-technical user can build and export an unanticipated stage-conversion report by department and month. | Reporting / data | Should | 11 | People analytics |
| 5 | The named integrations have documented APIs/webhooks, clear ownership, error handling, and sandbox access. | Integration | Should | 11 | IT |
| 6 | Migration preserves agreed candidate/application fields, documents, history, and audit evidence, with rehearsal and reconciliation. | Migration | Should | 10 | Data owner |
| 7 | An administrator can change fields, stages, forms, approvals, templates, permissions, and reports with versioning and rollback. | Administration | Should | 8 | System admin |
| 8 | The system supports consent, retention, deletion/access requests, and audit reporting without manual spreadsheet control. | Privacy / governance | Should | 7 | Legal / HR |
| 9 | Support includes defined severity levels, response targets, escalation, documentation, and post-implementation ownership. | Support | Should | 5 | Operations |
| 10 | AI features, if offered, show the workflow, data use, human oversight, audit evidence, and failure handling in writing. | AI governance | Nice | 4 | Legal / Security |
| 11 | Pricing is transparent at current headcount, planned headcount, and planned headcount plus 30%, including implementation and exit. | Commercial | Should | 4 | Finance / Procurement |
| **Total** |  |  |  | **100** |  |

## Longlist screening questions

Use these before demos. A “yes” means the vendor must still prove the requirement; it is not
evidence for the scorecard.

1. Can you support every must-have in our jurisdictions and at our planned scale?
2. Which named integrations are native, partner-built, API-based, or roadmap?
3. What data objects, documents, history, and audit records can be migrated, and who performs
   the work?
4. What is the three-year cost at current headcount, planned headcount, and planned headcount
   plus 30%?
5. What support hours, service commitments, sandbox environments, and exit exports are
   included?
6. Can you provide current accessibility, security, sub-processor, data residency, and AI
   documentation for review?
