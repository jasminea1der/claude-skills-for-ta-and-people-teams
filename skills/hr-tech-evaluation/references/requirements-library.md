# Requirements library

Checklists to build a requirements document from. Use them as prompts, not as a form to
complete — a requirements list with ninety lines nobody argued about is worse than one
with thirty that were each fought for.

Two rules apply throughout. **Every requirement must be testable**: written so you can
watch a demo and say yes or no. And **every requirement must be attributable**: someone
named wants it, for a stated reason. An unattributed requirement is usually a demo
souvenir.

---

## Contents

- [How to use this file](#how-to-use-this-file)
- [Writing a requirement that can be scored](#writing-a-requirement-that-can-be-scored)
- [Part 1 — Cross-category requirements everyone forgets](#part-1--cross-category-requirements-everyone-forgets)
  - [1. Data migration from the incumbent](#1-data-migration-from-the-incumbent)
  - [2. Reporting, analytics and getting your own data out](#2-reporting-analytics-and-getting-your-own-data-out)
  - [3. Integration with the rest of the stack](#3-integration-with-the-rest-of-the-stack)
  - [4. Permissions and the access model](#4-permissions-and-the-access-model)
  - [5. Candidate and employee-facing experience](#5-candidate-and-employee-facing-experience)
  - [6. Accessibility](#6-accessibility)
  - [7. Support model and service levels](#7-support-model-and-service-levels)
  - [8. Implementation resource from your own team](#8-implementation-resource-from-your-own-team)
  - [9. Configuration, administration and change](#9-configuration-administration-and-change)
  - [10. Security, privacy and residency](#10-security-privacy-and-residency)
  - [11. Localisation and multi-entity structure](#11-localisation-and-multi-entity-structure)
  - [12. Notifications, comms and templates](#12-notifications-comms-and-templates)
  - [13. Environments, releases and roadmap](#13-environments-releases-and-roadmap)
  - [14. AI and automated decision-making](#14-ai-and-automated-decision-making)
  - [15. The exit path](#15-the-exit-path)
- [Part 2 — Requirements by category](#part-2--requirements-by-category)
  - [Applicant tracking (ATS)](#applicant-tracking-ats)
  - [Core HR / HRIS](#core-hr--hris)
  - [Payroll](#payroll)
  - [Performance and goals](#performance-and-goals)
  - [Engagement and listening](#engagement-and-listening)
  - [Sourcing and CRM](#sourcing-and-crm)
  - [Assessment and selection](#assessment-and-selection)
- [Part 3 — Requirements that usually should not be must-haves](#part-3--requirements-that-usually-should-not-be-must-haves)

---

## How to use this file

1. Read the cross-category section (Part 1) first, before the category section. It carries
   the requirements that decide whether a system is liveable in year two, and they are the
   ones vendors are least often asked about, so they differentiate most.
2. Read the category section for the product in scope, plus any adjacent category the
   purchase touches — an ATS that will hold offers touches core HR; a performance tool that
   feeds pay touches HRIS.
3. Convert each relevant line into a requirement in the user's own words, with a named
   owner and a tier.
4. Discard what does not apply. A short list that reflects this organisation beats a
   complete list that reflects the library.

---

## Writing a requirement that can be scored

| Weak | Testable |
| --- | --- |
| Good reporting | A recruiter can build and export a stage-conversion report by department and month without raising a ticket |
| Easy for hiring managers | A hiring manager with no training can submit an interview scorecard from a phone in under three minutes |
| Integrates with our HRIS | On offer acceptance, the candidate record creates an employee record in [HRIS] including [named fields], without re-keying |
| Configurable workflows | An admin can add an approval step to one department's requisition flow without vendor involvement |
| Good candidate experience | A candidate can apply on a phone without creating an account, and can see their status afterwards |
| Strong security | SSO via [our identity provider], SCIM provisioning, and role-based access with field-level restriction on comp data |

The pattern: **who does what, in what conditions, to what standard.** Where a requirement
resists that shape, it is usually a preference rather than a requirement — keep it, but
tier it honestly.

---

## Part 1 — Cross-category requirements everyone forgets

### 1. Data migration from the incumbent

The single most common source of implementation overrun, and almost never scored.

- Which objects migrate: candidates, applications, employees, historic records, documents,
  notes, interview feedback, offers, comp history, org history, audit trail.
- At what fidelity — does a historic application keep its stages, dates, source, rejection
  reason and feedback, or does it arrive as a name and a CV?
- How far back, and is there a volume or age cut-off that changes the price?
- Who does the work: vendor, partner, or your team? Get it named, with days.
- What is the mapping process when the incumbent's fields have no equivalent, and who
  decides the mapping?
- How many migration rehearsals are included, and can you inspect the output before
  cutover?
- Attachments and documents — signed contracts, right-to-work evidence, offer letters.
  These are frequently excluded from the headline migration and separately priced.
- What happens to data you are legally required to retain but do not want to migrate.
- Reconciliation: how you prove after cutover that nothing was lost.

Ask the migration questions of a **reference customer who came from your incumbent**, not
only of the vendor.

### 2. Reporting, analytics and getting your own data out

The test is not whether they have dashboards. Every product has dashboards. The test is
whether you can answer a question they did not anticipate.

- Can a non-technical user build a new report, or does every new question become a ticket?
- Which fields are reportable? Custom fields, free-text notes and historic values are
  frequently not.
- Point-in-time and trend reporting: can you see what the pipeline looked like on a past
  date, or only its current state? This decides whether you can report on trends at all.
- Scheduled reports, and delivery to a named recipient or shared location.
- Export formats, row limits and whether export is throttled.
- API access to your own data for a warehouse or BI tool: read access, rate limits,
  historic backfill, and whether it costs extra.
- Whether analytics is a separately licensed module, and what the base licence includes.
- Audit trail: who changed what, when, and can you export it.
- Data dictionary — does one exist, and will they give it to you before signature?

In the demo, ask for a report you have not pre-briefed. That single request separates
products more reliably than any feature list.

### 3. Integration with the rest of the stack

- For each named system: what direction does data flow, how often, and what triggers it?
- Is the integration native, via a middleware partner, or a documented API you would build
  against? Each has a different cost and a different owner when it breaks.
- Is the API real and documented today, or roadmap? Ask for the public documentation link
  in the demo and read it.
- Rate limits, sandbox API access, and webhook support for event-driven flows.
- SSO with your identity provider, and SCIM or equivalent for user provisioning and
  deprovisioning. Deprovisioning matters more than provisioning and is asked about less.
- Calendar and email integration, including how it behaves for users on a different mail
  platform.
- Who owns the integration when it breaks at 8am, and what the support path is when two
  vendors each say it is the other's problem.
- What happens to the integration when either side upgrades.

### 4. Permissions and the access model

The requirement that surfaces late, usually as a crisis, when someone sees something they
should not have.

- Role granularity: how many roles, and can you create your own?
- Field-level permissions — comp, notes, demographic data, performance ratings, documents.
- Record-level scoping by department, entity, country, business unit or manager hierarchy.
- Can a hiring manager see other departments' candidates? Can a manager see a skip-level's
  record? Defaults matter; ask what they are.
- Interview feedback visibility: who sees whose, and when. Whether feedback can be hidden
  until submitted, which affects whether the feedback is independent.
- Restricted or confidential requisitions and confidential employee records.
- Delegated access for leave cover, and how it is revoked.
- Access for external parties — agencies, contractors, background check providers.
- Audit of permission changes, and periodic access review support.

### 5. Candidate and employee-facing experience

The largest user population by far, and the one whose opinion is least represented in the
buying group. Test it on a phone, in the demo, live.

- Application without account creation, and how long an application actually takes.
- Mobile behaviour end to end, including document upload from a phone.
- Status visibility, and whether the candidate can see or do anything after applying.
- Self-scheduling, rescheduling, and what happens when someone cancels.
- Communication tone and whether templates are editable by you, including branding.
- Employee self-service: what an employee can do without asking HR, and how discoverable it
  is for someone who logs in twice a year.
- Language options for candidates and employees.
- Data rights: how a candidate or employee exercises access, correction or deletion
  requests, and how much manual work that creates for your team.

### 6. Accessibility

- Which standard the organisation is held to, contractually or legally. State it in the
  requirement — the answer differs by jurisdiction and sector.
- Ask for the vendor's accessibility conformance documentation and the date of the last
  audit, for the **candidate or employee-facing** surfaces specifically. Vendors often hold
  documentation for the admin product only.
- Keyboard navigation and screen reader behaviour on the application flow and self-service.
- Whether known accessibility defects are published, and the remediation commitment.
- If you have internal accessibility expertise, get them into one demo. If not, note it as
  a gap for legal or your DEI lead to review; do not rate it on the vendor's word alone.

### 7. Support model and service levels

- Support hours against your working hours in every region you operate in.
- Channels: ticket, chat, phone, named contact. What is included at your licence tier
  versus what costs extra.
- Response and resolution targets by severity, and how severity is defined — the definition
  is where the value sits.
- Escalation path, and who your named account contact is after implementation ends.
- Whether implementation and ongoing support are the same team. They usually are not, and
  the handover is where quality drops.
- Is there a customer community, documentation and self-serve training, and is it current?
- Ask a reference specifically: what happened the last time something broke badly.

### 8. Implementation resource from your own team

Vendors quote their days. The days that sink projects are yours.

- Named roles required from your side and the hours per week for each, across the whole
  implementation: project owner, systems admin, HR ops, IT, security, data owner, testers.
- Who makes configuration decisions, and how many decisions there are.
- Testing effort expected from you, including UAT and payroll parallel runs.
- Training: who builds and delivers it internally, for how many people, in how many
  languages.
- Change management and comms — usually entirely yours.
- Whether the person who will administer the system afterwards exists and has capacity. If
  the answer is "we'll work it out", that is a risk for the decision paper.
- The realistic elapsed timeline given your cycles — you cannot cut over payroll mid-year
  end, or launch performance mid-cycle, whatever the plan says.

### 9. Configuration, administration and change

- What an admin can change without the vendor: fields, workflows, stages, forms,
  approvals, templates, permissions, reports.
- What requires professional services, and at what rate.
- Whether configuration is per-entity or global, which matters in multi-country groups.
- How complex configuration is versioned, tested and rolled back.
- Whether a change made in a sandbox can be promoted, or must be rebuilt by hand.
- How many admins you would realistically need, and whether any certification is required.

### 10. Security, privacy and residency

Route the answers to security and legal — this list gets the questions asked early, not
answered by you.

- Certifications held and their scope and date; ask for the report, not the badge.
- Penetration test cadence and whether a summary is shareable.
- Hosting locations, data residency options, and where support staff access data from.
- Sub-processor list, and notification terms when it changes.
- Encryption at rest and in transit; key management.
- Breach notification terms and timelines.
- Retention and deletion controls, including per-jurisdiction candidate data retention.
- Data processing agreement and transfer mechanisms — legal's call, not yours.
- Whether their security review can start before the shortlist closes. If security cannot
  clear a vendor, they are not a candidate, and finding that out after the decision is the
  expensive path.

### 11. Localisation and multi-entity structure

- Which countries the product genuinely supports versus which it can be made to work in.
  Ask for named live customers in each of your jurisdictions.
- Legal entity structure, cost centres, and multiple employment relationships.
- Language support for admin, employee and candidate surfaces separately — they often
  differ.
- Local statutory fields, reporting and document requirements.
- Date, name, address and identifier formats that do not assume one country's conventions.
- Works council or employee representation features where relevant — consultation records,
  restricted data views.

### 12. Notifications, comms and templates

- Which emails and notifications the system sends, to whom, and which you can switch off.
- Template editing, branding, and whether editing requires the vendor.
- Sending domain and deliverability — whether mail comes from your domain.
- Bulk communication, and whether it respects your consent and preference model.
- Reminder and nudge logic, especially for the perennial problem of hiring manager or
  reviewer inaction.
- SMS or messaging channels if relevant, including cost per message.

### 13. Environments, releases and roadmap

- Is there a sandbox? Does it cost extra? Can it be refreshed from production, and how
  often?
- Release cadence, whether upgrades are optional, and how much notice you get.
- How breaking changes to APIs and integrations are communicated.
- Deprecation policy for features you depend on.
- Roadmap: ask what shipped in the last twelve months, not what is coming. Shipped history
  is evidence; roadmap is intent. Never score a roadmap item as a capability — if it is not
  in the product at signature, it is a risk line in the decision paper.

### 14. AI and automated decision-making

Treat each claimed feature as a requirement, and get these in writing:

- What it does, described as a workflow, and whether it can be switched off per feature.
- Whether it makes, ranks, scores or influences a decision about a person.
- Training data provenance, and whether your data trains their models — with an opt-out
  and what the opt-out costs in capability.
- Bias auditing: who audited, when, against what, and what will be shared with you.
- Human oversight: where the human sits by design, what they see, and how an output is
  overridden and recorded.
- Explainability sufficient to answer a candidate or employee who challenges an outcome.
- Accuracy claims — ask what they were measured against and on whose data.
- Model change management: what happens when they update the model under you.

Regulatory obligations for employment-related automated decisions vary by jurisdiction and
change frequently. Verify the current position by search at runtime and hand it to legal;
do not state obligations from memory.

### 15. The exit path

Ask before you enter, while you still have leverage.

- What data you can export, in what format, at what fidelity, including documents and
  audit history.
- Whether export is self-serve or a paid vendor service, and how long it takes.
- The window after termination in which you can still extract, and their deletion
  commitment afterwards.
- Whether historic records remain readable without the product — an export you cannot
  interpret is not an export.
- Notice period, and what happens to integrations and configuration you built.
- Ask a reference who left a previous vendor what the extraction actually cost them.

---

## Part 2 — Requirements by category

Each list assumes Part 1 has already been applied. These are the category-specific lines.

### Applicant tracking (ATS)

**Requisition and approval**
- Requisition creation, approval chains by cost centre or seniority, and delegation.
- Budget or headcount linkage, if approvals depend on it.
- Reopening, cloning, and multi-hire requisitions.

**Pipeline and workflow**
- Stage configuration per role type or department, and whether stages can differ.
- Bulk actions: moving, rejecting, messaging, and correcting a bulk action taken in error.
- Duplicate detection and merging, including candidates who reapply years later.
- Silver medallist handling and re-engagement of past applicants.
- Agency portal, submission ownership and duplicate claims.
- Referral capture, tracking and payment trigger.
- Internal mobility: whether internal applicants are handled distinctly and privately.

**Interviewing**
- Scheduling, including panels across time zones, and self-scheduling.
- Interviewer load balancing and availability.
- Structured scorecards per stage, and whether they can be mandatory.
- Preventing interviewers from seeing others' feedback before submitting.
- Interview kit distribution — questions and guidance in front of the interviewer.

**Offers**
- Offer approval workflow, versioning and comparison against band.
- E-signature, and whether it is native or a separately licensed integration.
- Handover to onboarding and HRIS, including exactly which fields move.

**Sourcing and content**
- Careers site: hosted or your own, editable, indexable by job aggregators.
- Job board posting and whether individual board costs are passed through.
- Campaign, source and spend tracking through to hire.

**Compliance and reporting**
- Configurable candidate data retention per jurisdiction, with automatic deletion.
- Consent capture and re-consent.
- Voluntary demographic data capture, held separately from the assessment record.
- Statutory reporting relevant to your jurisdictions.
- Time in stage, conversion, source effectiveness, hiring manager responsiveness, offer
  decline reasons.

### Core HR / HRIS

- Employee record model: what is core, what is custom, and whether custom fields are
  reportable and API-accessible.
- Effective dating and history — the requirement that decides whether you can ever report
  on a past state. Test it explicitly: show me this org chart as at a date last year.
- Org structure, multiple reporting lines, matrix, and future-dated changes.
- Position management, if you manage headcount by position rather than person.
- Contract types: permanent, fixed-term, part-time, contractor, intern, multiple concurrent
  jobs.
- Absence and leave: policy configuration by country, accrual rules, carryover, public
  holiday calendars.
- Document management, e-signature, right-to-work and visa expiry tracking with alerts.
- Onboarding and offboarding workflows including task assignment to IT and facilities.
- Compensation records, currency handling, and pay change history with approval.
- Benefits administration, if in scope, and provider integrations by country.
- Manager and employee self-service depth, and what still requires an HR ticket.
- Mass change tooling — reorganisations, transfers, uplifts — and how to undo one.
- Workforce reporting, headcount definitions, FTE versus headcount, and reconciliation to
  finance.

### Payroll

Payroll is the least forgiving category in the stack: it runs on a date, it is legally
consequential, and errors are visible to every employee.

- Which countries are run on their own engine, which via a partner, and which are
  aggregated third parties. Get this named per country — it changes the support model, the
  compliance ownership and the failure mode.
- Statutory compliance updates: who applies them, how quickly, and what the commitment is.
- Filing and statutory submissions per jurisdiction.
- Pay elements, retro pay, off-cycle runs, corrections and reversals.
- Gross-to-net calculation transparency: can you see why a number is what it is?
- Parallel run support and the reconciliation process.
- Payslip access, formats and historic payslip retention on exit.
- Time and attendance integration where pay depends on it.
- Finance integration: GL posting, cost allocation, journals, accruals.
- Pensions and benefits provider submissions per country.
- Payroll calendar management and cut-off enforcement.
- Approval and segregation of duties — who can approve their own change.
- Year-end processing per jurisdiction.
- What happens when a run fails, and who is accountable when a payment is late.

Payroll requirements need the payroll owner in the room. Do not write them from the HR
side alone, and route all statutory compliance questions to a qualified local adviser.

### Performance and goals

- Cycle configuration: annual, biannual, continuous, and different cycles per population.
- Goal and objective structures, cascading and alignment, and whether goals are optional.
- Review forms: question types, per-population variation, and mid-cycle change handling.
- Rating scales, including running without ratings if that is the design.
- Multi-rater and upward feedback, and anonymity rules.
- Calibration support: grouping, distribution views, in-session rating changes, and an
  audit trail of who changed a rating and why.
- Manager and employee visibility rules — what an employee sees and when.
- Check-in and one-to-one support, and whether notes are private or visible.
- Linkage to compensation and to career levels, if that linkage exists.
- Late and non-completing manager tracking, with escalation to their manager.
- Historic review access when someone changes manager or moves entity.
- Reporting on rating distribution by manager, level and demographic group, held for
  aggregate analysis only.

### Engagement and listening

- Survey types supported: census, pulse, lifecycle (onboarding, exit), always-on.
- Question bank ownership: can you use your own items, and do you retain the results if you
  leave?
- Anonymity and confidentiality model — the minimum reporting threshold, whether it is
  configurable, and how free text is protected. This is the requirement that determines
  whether employees trust the instrument at all.
- Demographic cuts and intersectional filtering, subject to that threshold.
- Free-text analysis: what it does, whether it surfaces individual comments to managers,
  and how sensitive disclosures (harassment, health, safety) are routed.
- Manager dashboards and whether managers can act without HR translating for them.
- Action planning, tracking and follow-through visibility.
- Benchmarking, if offered: ask what the comparison group is, how it is constructed, how
  current it is, and whether you can see the definition. Do not score a benchmark you
  cannot inspect.
- Comparability across time if you change instrument or vendor.
- Integration with HRIS for demographic and hierarchy data, and how often it syncs.
- Response rate mechanics: distribution channels, reminders, and reaching non-desk staff.

### Sourcing and CRM

- Talent pool structure, tagging, and segmentation.
- Campaign and nurture workflows, and consent handling for marketing-style outreach.
- Sequencing and outreach, including sending from a recruiter's own mailbox and
  deliverability implications.
- Contact data enrichment: where the data comes from, on what lawful basis, and what your
  obligations are as a controller. Route to legal — this is a common exposure.
- Deduplication against the ATS and back into it.
- Chrome extension or sourcing capture, and which sites it works on.
- Event and referral capture.
- Reporting on pipeline built versus pipeline converted — the honest measure of a sourcing
  tool.
- Consent, unsubscribe and suppression list handling across jurisdictions.

### Assessment and selection

Higher legal exposure than any other category on this list, because the output influences a
selection decision directly.

- What the instrument measures, and the evidence that it predicts performance in roles like
  yours. Ask for the technical manual, not a brochure.
- Validation evidence: what studies exist, on what populations, in what job families, and
  when.
- Adverse impact evidence by group, and whether they will share it. A refusal is
  informative.
- Accessibility and adjustment support for candidates with disabilities, including time
  extensions and alternative formats, and how a request is handled discreetly.
- Candidate experience: duration, device support, and whether a candidate gets feedback.
- Cheating and proctoring approach, and its privacy implications — proctoring is itself a
  data protection question in several jurisdictions.
- How scores are delivered: pass/fail, banded, ranked, or advisory, and whether hiring
  teams can see the underlying detail.
- Configurable cut scores, who sets them, and what evidence supports them.
- Retest policy and score validity period.
- Integration into the ATS workflow and where the score lands.
- Data retention of assessment results and candidate access rights.

Anything that scores, ranks or filters people needs legal review of both the instrument and
its configuration before go-live. This library gets the questions asked; it does not
validate an instrument.

---

## Part 3 — Requirements that usually should not be must-haves

Not wrong to want. Wrong to let them disqualify a vendor, because they are cheap for
vendors to satisfy, weakly linked to whether the system works in year two, or easily
influenced by a good demo.

- **Interface aesthetics.** Real, but it belongs in a should-have with the daily users
  scoring it, not in the tier that eliminates a vendor.
- **A specific integration with a system you are also about to replace.**
- **A feature you saw in a demo last week that nobody wanted the week before.** Keep it,
  mark its origin, and tier it after the pain-derived requirements.
- **Roadmap items.** Never a must-have. If it is not shippable and demonstrable now, it is
  a risk, not a capability.
- **AI features with no defined job.** "Has AI" is not a requirement. "Reduces the
  coordinator's scheduling time by removing X" is.
- **Vendor size, funding or logo list.** Relevant to viability risk, which belongs in the
  decision paper's risk section, not in the functional scorecard.
- **Anything only one person wants and cannot explain.** Ask what breaks without it. If
  nothing breaks, it is a nice-to-have.
