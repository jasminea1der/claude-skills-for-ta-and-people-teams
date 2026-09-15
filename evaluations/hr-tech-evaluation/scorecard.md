# HR tech evaluation: scorecard

**Category:** SuccessFactors Recruiting to SmartRecruiters  
**Problem statement owner:** [Name / role]  
**Weights fixed on:** [Date — before first demo]  
**Evaluators:** [Names and roles]

## Scoring anchors

Score what was demonstrated, not what was described.

| Score | Meaning |
| --- | --- |
| 5 | Demonstrated out of the box and better than required |
| 4 | Demonstrated and meets the requirement as written |
| 3 | Meets it with configuration the team can do itself or a minor workaround |
| 2 | Requires vendor services, significant workaround, or partial coverage |
| 1 | Not available or only on the roadmap |
| — | Not covered; add to follow-up, do not guess |

**Evidence flags:** D = demonstrated live; C = claimed only; R = confirmed by reference;
W = confirmed in writing. Any C remaining at decision time is an open risk.

## Must-have gate

Copy the M1–M7 table from `requirements.md` after each vendor has answered in writing and
the relevant owner has reviewed the answer. A vendor that fails any must-have is out,
regardless of weighted score.

| Vendor | M1 | M2 | M3 | M4 | M5 | M6 | M7 | Gate result |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Vendor A |  |  |  |  |  |  |  | All pass / Fail M__ |
| Vendor B |  |  |  |  |  |  |  | All pass / Fail M__ |
| Vendor C |  |  |  |  |  |  |  | All pass / Fail M__ |

## Weighted scoring

Enter `score / evidence flag`; calculate weighted score as `sum(score × weight) / 100`.
Do not treat a gap below roughly 0.3 as meaningful without stronger evidence.

| Rank | Requirement | Weight | Vendor A | Vendor B | Vendor C |
| --- | --- | ---: | --- | --- | --- |
| 1 | Requisition, workflow, correction, and bulk-action usability | 16 |  |  |  |
| 2 | Untrained hiring-manager experience | 12 |  |  |  |
| 3 | Candidate mobile application and scheduling experience | 12 |  |  |  |
| 4 | Reporting and export for unanticipated questions | 11 |  |  |  |
| 5 | Integration documentation, ownership, errors, and sandbox | 11 |  |  |  |
| 6 | Migration fidelity, rehearsal, and reconciliation | 10 |  |  |  |
| 7 | Admin configuration, versioning, and rollback | 8 |  |  |  |
| 8 | Privacy workflows and auditability | 7 |  |  |  |
| 9 | Support model and service commitments | 5 |  |  |  |
| 10 | AI governance and evidence, if applicable | 4 |  |  |  |
| 11 | Commercial transparency and growth pricing | 4 |  |  |  |
| **Total** |  | **100** |  |  |  |

| Vendor | Weighted score /5 | Must-haves | Scores still marked C | Outcome |
| --- | ---: | --- | ---: | --- |
| Vendor A |  |  |  |  |
| Vendor B |  |  |  |  |
| Vendor C |  |  |  |  |

## Evidence notes

Record what was seen, not conclusions about the vendor.

| Requirement | Vendor | Score / flag | Evidence observed | Follow-up / owner |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

## Cost over the contract term

Obtain figures in writing and mark each as quoted, verbal, or estimated.

| Cost item | Vendor A | Vendor B | Vendor C |
| --- | ---: | ---: | ---: |
| Annual licence — current headcount |  |  |  |
| Annual licence — planned headcount |  |  |  |
| Annual licence — planned headcount + 30% |  |  |  |
| Implementation |  |  |  |
| Data migration |  |  |  |
| Integrations / middleware |  |  |  |
| Sandbox / extra environments |  |  |  |
| Training and change support |  |  |  |
| Internal resource (days × loaded cost) |  |  |  |
| Modules likely needed in year 2 |  |  |  |
| **Total over [n] years** |  |  |  |
| Renewal uplift mechanism |  |  |  |
| Exit / export cost |  |  |  |

## Open items before signature

| # | Item | Vendor | Owner | Needed by | Status |
| --- | --- | --- | --- | --- | --- |
| 1 | Security review and pen-test summary |  | Security |  |  |
| 2 | DPA, sub-processors, and transfer mechanism |  | Legal |  |  |
| 3 | Data residency and retention confirmation |  | Legal |  |  |
| 4 | Accessibility evidence for candidate-facing flows |  | Accessibility |  |  |
| 5 | Migration scope, reconciliation, and rehearsal plan |  | Data owner |  |  |
| 6 | Written pricing at planned headcount |  | Finance |  |  |
| 7 | Exit export format, window, and cost |  | Procurement |  |  |

## Weight change log

| Date | Change | Reason | Approved by | Vendors re-scored |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
