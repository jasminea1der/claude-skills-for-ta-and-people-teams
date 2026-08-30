# Weighted scorecard: [Category, e.g. Applicant Tracking System]

**Owner:** [Name, role] | **Weights fixed on:** [Date — before first demo] |
**Evaluators:** [Names and roles]

---

## The problem we are solving

[Two or three sentences, written before any vendor was seen. What is broken, who feels it,
what "fixed" looks like and how it would be measured. This is the tiebreak when totals are
close — if a vendor wins on points but does not obviously solve this, say so.]

**Scope:** [Category and modules in scope now] | **Replacement of:** [Incumbent, or "first
system"] | **Users:** [Admin / recruiter / manager / employee counts] |
**Employees:** [Number] | **Jurisdictions:** [List] | **Go-live target:** [Date] |
**Incumbent notice deadline:** [Date]

---

## Scoring anchors

The same anchors apply to every requirement and every evaluator. Score what was
demonstrated, not what was described.

| Score | Meaning |
| --- | --- |
| 5 | Demonstrated, out of the box, and better than we asked for |
| 4 | Demonstrated and meets the requirement as written |
| 3 | Meets it with configuration we can do ourselves, or with a minor workaround |
| 2 | Only with vendor professional services, significant workaround, or partial coverage |
| 1 | Not available, or only on the roadmap |
| — | Not covered in the session — carry to the follow-up list, do not guess |

**Evidence flag** on every score: **D** demonstrated live, **C** claimed only, **R**
confirmed by a reference, **W** confirmed in writing. A requirement still marked C at
decision time is an open risk, not a score.

---

## Must-have requirements (pass/fail — no weight)

A vendor that fails any of these is out, regardless of total score. If a failure here would
not actually stop the purchase, the requirement belongs in the weighted table instead.

| # | Must-have | Owner | [Vendor A] | [Vendor B] | [Vendor C] |
| --- | --- | --- | --- | --- | --- |
| M1 | [Requirement, written testably] | [Name] | Pass / Fail | | |
| M2 | | | | | |
| M3 | | | | | |
| M4 | | | | | |
| M5 | | | | | |
| M6 | | | | | |

---

## Weighted requirements

Weights sum to 100 and were set before the first demo. Requirements are ranked within each
group, most important first.

| # | Requirement | Group | Tier | Weight | [Vendor A] | [Vendor B] | [Vendor C] |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | [Requirement] | [e.g. Workflow] | Should | [n] | [score / flag] | | |
| 2 | | | | | | | |
| 3 | | | | | | | |
| 4 | | | | | | | |
| 5 | | | | | | | |
| 6 | | | | | | | |
| 7 | | | | | | | |
| 8 | | | | | | | |
| 9 | | | | | | | |
| 10 | | | | | | | |
| 11 | | | | | | | |
| 12 | | | | | | | |
| | **Total weight** | | | **100** | | | |

Suggested groups, each carrying its own share of the 100: core workflow for the primary
users, reporting and data access, integration, administration and configurability,
end-user experience, implementation and support, security and compliance, commercial. Adapt
the groups to the category; keep the weights explicit at group level so the shape of the
decision is visible at a glance.

### Weighted scores

| Vendor | Weighted score /5 | Must-haves | Scores still marked "claimed" |
| --- | --- | --- | --- |
| [Vendor A] | | All pass / Fails M[n] | [count] |
| [Vendor B] | | | |
| [Vendor C] | | | |

*Weighted score = Σ(score × weight) ÷ 100. Report to one decimal place and do not treat a
gap of less than roughly 0.3 as meaningful — inside that range the vendors are equivalent
on the evidence held, and the decision should turn on references, implementation
confidence, exit terms or total cost.*

---

## Evidence notes by requirement

[For each requirement where scores differ by two or more points between vendors, or between
evaluators, record what was actually seen. This is what makes the scorecard defensible six
months later when someone asks why a vendor scored what it did.]

| # | Vendor | Score | What we saw |
| --- | --- | --- | --- |
| [n] | [Vendor] | [n] | [Observation from the demo, trial or reference call] |

---

## Cost over the contract term

Licence plus everything else. Year one is not the comparison; the term is.

| Item | [Vendor A] | [Vendor B] | [Vendor C] |
| --- | --- | --- | --- |
| Annual licence — today's headcount | | | |
| Annual licence — at plan headcount | | | |
| Implementation (vendor) | | | |
| Data migration | | | |
| Integrations / middleware | | | |
| Sandbox / additional environments | | | |
| Training | | | |
| Modules likely needed in year 2 | | | |
| Internal resource (days × cost) | | | |
| **Total over [n] years** | | | |
| Renewal uplift mechanism | | | |
| Exit / export cost | | | |

*Mark each figure as quoted in writing, verbal, or estimated. Estimated figures go in the
assumptions block below.*

---

## Reference call summary

| Vendor | References taken | Consistent positives | Consistent concerns | Score changes made |
| --- | --- | --- | --- | --- |
| [Vendor A] | [n, and whether vendor-sourced] | | | |
| [Vendor B] | | | | |
| [Vendor C] | | | | |

---

## Open items before signature

| # | Item | Vendor | Owner | Needed by | Status |
| --- | --- | --- | --- | --- | --- |
| 1 | [Capability claimed but not demonstrated] | | | | |
| 2 | [Security review] | | | | |
| 3 | [DPA and sub-processor list to legal] | | | | |
| 4 | [Written confirmation of pricing at plan headcount] | | | | |
| 5 | [Data residency confirmation] | | | | |

---

## Assumptions

| Assumption | Where it affects the score | How to replace it with fact |
| --- | --- | --- |
| [e.g. headcount growth of x% over the term] | Cost comparison | [Finance plan] |
| [e.g. integration to [system] is native] | Requirement [n] | [Written confirmation] |

---

## Weight change log

Weights are set before the first demo and are not changed afterwards — a weight that moves
after a demo makes the scorecard justify a preference rather than test it. If a demo
genuinely reveals a requirement nobody had considered, add it here as a new line, then
re-score every vendor against it including those already seen.

| Date | Change | Reason | Who approved | Vendors re-scored |
| --- | --- | --- | --- | --- |
| | | | | |

*An empty log is the expected state.*
