---
name: hr-tech-evaluation
description: Runs a rigorous selection process for HR or TA technology — ATS, HRIS, payroll, performance, engagement, sourcing, assessment, LMS — producing a ranked requirements document, a weighted scorecard set before demos, demo scripts that expose real differences, a reference call guide, and a decision paper naming the recommendation and the runner-up. Use when someone says they are "choosing an ATS", "replacing our HRIS", "looking at performance tools", "doing an RFP", "shortlisting vendors", "our ATS is terrible", "the demos all looked the same", "we need to build a scorecard for this", "which system should we buy", "renewal is coming up and I want to test the market", or is being sold to and wants to evaluate the claim. Also use for building a business case for a system purchase, running vendor references, or pressure-testing a decision already leaning one way. For assessing how mature a function is at using AI rather than choosing a product, use ta-ai-maturity-assessment.
---

# HR & TA Technology Evaluation

Produces the artefacts that make a multi-year system decision defensible: a ranked
requirements document, a weighted scorecard fixed before the first demo, demo scripts
that force vendors off their script, a reference call guide, and a decision paper with a
recommendation and a named runner-up.

The problem this solves is an asymmetry. You buy an ATS every four to six years; the
person selling it sells one every week, has run this exact conversation hundreds of times,
and knows which three screens to show and in what order. A fair fight requires structure
that exists before the first demo, because after the first demo your requirements are
contaminated by what you have seen.

## The reframe: start with the problem, never the category

This is the most valuable thing in this skill, and worth saying to the user in plain terms
early. Almost every failed system purchase started as "we need a new ATS" rather than, e.g.,
"hiring managers do not give feedback, candidates wait [11] days at final stage, and we lose
[1 in 5] offers as a result". The first framing sends you to a demo. The second tells you
what a fix looks like — and sometimes tells you the fix is not a purchase at all, but a
process change, a configuration of what you already own, or a person.

The mechanical consequence matters: **a requirements list assembled after seeing demos is
just a description of the demos.** Every vendor shows you a capability you had not thought
to want, and it feels like insight. Three demos later the list has been quietly rewritten
to match whichever vendor demoed most confidently, and the scorecard that follows is a
rationalisation, not a test.

So the order is fixed: problem, requirements, weights, vendors. Say this to the user, give
the reason, and hold the line if they want to skip ahead.

## What you need to start

Two things: **what is broken**, and **the category they think they need**.

Everything else — user counts, budget, integrations, timeline — sharpens the work but does
not gate it. If the user does not know their budget or which systems must integrate,
proceed on stated assumptions, label them inline, and list them in the assumptions block
of the output. A requirements document built on five labelled assumptions is worth far
more than a stalled conversation.

Ask in small batches, two or three questions at a time, reflecting back what you now
understand after each. Where the environment supports structured multiple-choice questions
(Cowork's `AskUserQuestion` or equivalent), prefer it for scoping questions with a small
answer set — category, replacement or first system, budget band, timeline. Keep free text
for the problem statement, where the texture is the whole point.

## Process

### 1. Get the problem statement before anything else

Ask what is broken, and push past the first answer. "Our ATS is terrible" is not a
problem statement. Get to observable consequence:

- What specifically happens today that should not, or does not happen that should?
- Who feels it — recruiters, hiring managers, candidates, employees, payroll, finance?
- How long has it been like this, and what has already been tried?
- What does "fixed" look like in twelve months? Name something you could measure.
- If you changed nothing, what is the cost of that over the next two years?

Then ask the question that saves the most money: **is this a technology problem?** If
requisition approvals take nine days because four people must approve and two are on
holiday, no ATS fixes that. If the current system is unloved because it was never
configured and nobody was trained, a new system will be unloved in eighteen months for the
same reason. Say so directly when the evidence points there — it is the highest-value
thing you can tell them.

If it is a technology problem, write the problem statement down and get their agreement on
it. It becomes the first section of every artefact and the tiebreak when scoring is close.

### 2. Scope the decision

Cover these, in two or three batches:

- **Category and sub-scope.** If a suite, which modules are genuinely in scope now versus
  aspirationally later — vendors price and demo on the aspiration.
- **Replacement or first system.** A replacement carries data migration, parallel running
  and change management. A first system carries process design work instead.
- **Current stack and integrations.** What it must talk to, in which direction, and how
  critical each link is. HRIS, payroll, SSO/identity, background check, assessment,
  scheduling, comms, finance, BI/warehouse, job boards.
- **Scale.** Employees, system users by type (admin, recruiter, hiring manager, employee
  self-service), hires per year, and expected growth over the contract term. Pricing
  models bite at growth, not at signature.
- **Jurisdictions.** Where employees and candidates are, and where data may or may not
  sit. This drives payroll capability, data residency, works council and consultation
  requirements, statutory reporting and language support harder than any other input. Ask
  it early; retro-fitting it invalidates a shortlist.
- **Budget range and shape.** Annual licence, one-off implementation, internal resource.
  A range is fine; "no idea" is fine too — say what a range would need to come from.
- **Timeline and the forcing event.** Renewal date, funding round, a go-live tied to a
  cycle. Note the notice period on the incumbent contract now — it is routinely missed and
  missing it costs a full extra year.
- **Who decides, and who can veto.** IT, security, legal, procurement, finance, the works
  council. A shortlist that has not been through security review is not a shortlist.

### 3. Build requirements in three tiers, then make them rank

Tiers: **must-have** (its absence disqualifies the vendor), **should-have** (significant
value, but you would live without it), **nice-to-have** (tiebreak only). Two rules do the
work.

**Must-have means disqualifying.** If a vendor failing it would not actually stop you
buying them, it is a should-have. Test each one out loud with that question. Most initial
lists carry twenty-five must-haves and almost none survive; expect to land around six to
ten.

**Rank within tiers, not just between them.** Unranked requirements produce scorecards
where every vendor scores 3.8 out of 5 and nothing differentiates, because the twelve
things that barely matter outnumber and outweigh the three that decide it. Force an
ordering. If the user resists, ask which single requirement they would keep if they could
keep only one, then the next — a forced sequence beats an argument about relative
importance.

Pull from `references/requirements-library.md`, including the categories users routinely
forget and vendors are rarely asked about:

- Data migration from the incumbent — what comes across, at what fidelity, who does it
- Reporting and data export — can you get **your** data out, in what format, at what cost
- Integration with the rest of the stack, and whether the API is real or a roadmap item
- Permissions and access model — role granularity, who can see comp, notes, protected data
- Candidate or employee-facing experience — the part with the largest user population
- Accessibility (state which standard the organisation is held to, and ask for evidence)
- Support model, response times, escalation, and who answers at 6am in your other region
- Implementation resource required from **your** team, in named people and days
- The offboarding and exit path — what leaving looks like, before you enter

Write this out as the requirements document — problem statement, scope, the three tiers in
rank order, each requirement with a named owner and the reason it exists. It is what
vendors get, and the record that these requirements existed before the demos did.

### 4. Set the weights before you see anything

Assign a weight to each requirement or requirement group, summing to 100, with the user, in
the conversation, and write it to the scorecard file. Then state the rule plainly:
**weights are fixed before demos and are not changed afterwards.** The moment a weight
moves after a demo, the scorecard stops testing the preference and starts justifying it —
and it still looks rigorous to everyone who reads it, which is what makes it dangerous. If
a demo genuinely reveals a requirement nobody had considered, add it as a new line with its
own weight, record the date and reason in the change log at the foot of the scorecard, and
re-score every vendor against it including those already seen. Visible and rare is fine.
Silent is not.

Use `assets/scorecard-template.md`, and set the scoring anchors at the same time — a 1–5
scale where each point has a written meaning, because "4 out of 5" means nothing across
three different evaluators.

### 5. Assemble the vendor list

Ask which vendors are already in view and why. If they want to widen the field, use web
search at runtime to identify current products in the category and cite what you find with
dates — do not assert from memory. Capability, pricing and ownership in this market change
quarterly, and stale confidence here is worse than silence.

Do not rank vendors on remembered reputation, and do not tell a user one product is better
than another at anything — the scorecard is the ranking mechanism, which is the point of
building it. Structure the longlist, write the screening questions that cut it to three or
four, and note where a claim needs verifying in a demo.

Screen the longlist on must-haves and hard constraints only — jurisdiction coverage,
integration with a named critical system, scale, budget band. Three or four vendors is the
right shortlist; five is a scheduling problem and produces worse notes.

### 6. Write demo scripts that differentiate

A generic demo is vendor-controlled marketing, and every vendor's generic demo looks
excellent because it has been refined over hundreds of runs to look excellent. A demo
becomes evidence only when you control the scenarios. Full technique in
`references/demo-and-reference-guide.md`; the core of it:

- **Send your scenarios in advance** — three to five, drawn from your real workflows,
  identical for every vendor. Same scenarios, same order, same time budget.
- **Insist on a configured environment** resembling your structure, not the polished demo
  tenant with perfect data and four job titles.
- **Make them show the ugly workflows.** Bulk edits. Correcting a mistake made three weeks
  ago. An untrained hiring manager's first review. Reporting on a question they were not
  given in advance. The unhappy path is where products differ; on the happy path they are
  all the same.
- **Have the daily users in the room**, not only the buyer. The coordinator who will live
  in this eight hours a day notices in ten minutes what an executive buyer misses across
  three demos.
- **Score within an hour of the demo ending**, independently, before discussion. Otherwise
  memory converges on the most confident presenter.

Build one script per shortlisted vendor from the same template, plus the category-specific
probing questions from the reference file.

### 7. Run reference calls properly

The most under-used and highest-signal step, and the one most often cut for time. A
vendor-supplied reference is a happy customer who agreed to take the call — still useful,
if you ask questions a happy customer will answer honestly. Full guide in
`references/demo-and-reference-guide.md`. The questions that work:

- What took longer than you expected?
- What would you do differently if you were implementing it again?
- What does your team complain about?
- Who on your side does the day-to-day admin, and how much of their time does it take?
- What did you have to change about how you work to fit the tool?
- What did you assume it would do that it does not do?
- Would you buy it again, and what would have to be true for you to switch?

Ask for one reference at your scale and in your jurisdictions, one who implemented within
the last twelve months (product and implementation team both change), and one who switched
away from your incumbent — that call is the migration reference. Also try to reach a
customer the vendor did not introduce you to.

### 8. Cover the commercial and contract questions

Structure the questions, get them answered in writing, and hand the answers to legal and
procurement. Contract review is their job, not this skill's — say that plainly, and do not
draft or interpret contract terms. What to get in writing before the shortlist closes:

- **Pricing model and how it scales** — per employee, per user, per hire, per module,
  tiered. Model the cost at today's headcount, at plan, and at plan plus 30%.
- **What triggers an increase** — headcount bands, module additions, renewal uplift, an
  indexation clause, volume overage.
- **Contract length, notice period and renewal mechanics** — including auto-renewal and
  the date by which notice must be given.
- **Implementation and migration cost**, and what is excluded from it.
- **Sandbox or test environment** — whether it exists, whether it costs, whether it
  refreshes from production.
- **Service levels** — uptime, support response by severity, and the remedy when missed.
- **Data ownership and exit** — that your data is yours, the export format available, at
  what cost, over what window after termination, and their retention afterwards.

Exit terms are the most often skipped and most expensive to discover late. Ask before
signature, while you have leverage.

### 9. Interrogate the AI claims specifically

Every vendor in every category now claims AI features. Treat the claim as a requirement
like any other: define what it must do, then test it. For each feature the vendor leads
with, get answers to:

- **What does it actually do**, in one sentence, as a workflow rather than a benefit? Ask
  them to show it running on your scenario, not a recorded example.
- **Does it make or influence an employment decision** — screening, ranking, scoring,
  matching, recommending, rejecting? This is the question that changes the regulatory
  picture, and vendors answer it carelessly. Get the answer in writing.
- **What is it trained on**, and does customer data train the vendor's models? If it does,
  can you opt out, and what does opting out cost you in capability?
- **Bias auditing** — audited by whom, when, against what, and will they share the results
  or only a summary? "Yes, we audit" with nothing shareable behind it is a no.
- **Human oversight design** — where a person is in the loop by design rather than by
  configuration, what that person actually sees, and whether the reasoning is visible
  enough to review or override.
- **What happens when it is wrong**, and how you would find out.

Where regulatory obligations are relevant — for anything touching selection they usually
are — verify the current position by web search at runtime and cite what you find with
dates. The rules for employment-related automated decision-making move quarterly across
jurisdictions; anything from memory will be stale or subtly wrong. Frame the output as
questions for legal, not as a compliance determination.

### 10. Score, then write the decision paper

Score each vendor independently, per evaluator, before any group discussion. Then discuss
the gaps: where two evaluators are two points apart on the same requirement, the
disagreement carries more information than either score. Do not let the total decide on
its own — check three things before writing:

- **Does the winner pass every must-have?** A must-have failure disqualifies regardless of
  total. That is what the tier means.
- **Is the gap real?** Inside a few points across a 100-point weighted scale, the vendors
  are equivalent on the evidence you have. Say so, and decide on something else —
  implementation confidence, references, exit terms, total cost over the term.
- **Where is the score thin?** A requirement scored on a claim rather than a demonstration
  should be marked as such and closed out before signature.

Then fill `assets/decision-paper-template.md`: the recommendation, the runner-up with the
reasons it lost, what would have changed the answer, the risks carried and their
mitigations, and cost over the full term rather than year one. Naming the runner-up
properly is what makes the paper credible to an exec team, and what protects you in
eighteen months when someone asks whether the alternative was considered.

Write every artefact to disk as a Markdown file, then offer one upgrade path suited to the
audience: a slide deck for an exec or board decision, a spreadsheet for the scorecard and
cost model, a Word document for procurement or legal. Offer; do not build all three.

**Handoff.** Where the spend needs a full financial argument, that is
`headcount-business-case` — the same structure works for a system purchase. Where the
evaluation was triggered by a process problem, that is `interview-process-audit`.

## When the user already has a shortlist

Common, and not a failure — take it as the starting position and skip to building the
scorecard and demo scripts around their existing candidates. Do one thing first, in two
sentences and without lecturing: name the risk that requirements defined after seeing
demos are shaped by those demos, and ask one question — *what did you want this to fix
before you saw any of these products?* A clean answer becomes the problem statement. No
clean answer is itself the finding, and worth ten minutes of reconstruction: build
requirements from the workflow and the pain, then mark which ones arrived from a demo.
Those are not automatically wrong — they are unverified as things this organisation needs.

Then set weights before the next demo, and treat any vendor already seen as scored on
partial evidence until the same scenarios have been run against them.

## Legal, data and security guardrails

**Contract review belongs to legal and procurement.** This skill structures the commercial
questions and gets them answered; it does not interpret terms, assess liability caps or
tell anyone a contract is acceptable.

**Data residency and cross-border transfer are jurisdiction-specific obligations.** Ask
where employee and candidate data may be processed and stored, capture it as a
requirement, and route the answer to legal. Do not specify what a jurisdiction permits.

**Data processing agreements, sub-processors and security review are gates, not
paperwork.** Get the vendor's DPA, sub-processor list, security certifications and pen test
summary into security and legal review before the shortlist closes — a vendor failing
security review after the decision is announced is the most expensive way to learn this.

**Employee consultation and automated decision-making.** In some jurisdictions a system
that monitors or evaluates employees triggers works council or union consultation, and a
feature that screens, ranks, scores or rejects people carries obligations that vary by
jurisdiction. Ask, verify by search, and present both as questions for legal — never as
compliance sign-off.

**Personal data in the evaluation itself.** For a trial or sandbox, use anonymised or
synthetic records rather than live candidate or employee data. Easiest exposure to avoid,
and the evaluation does not need real names to work.

## Facts you must not invent

No vendor capability claims, no pricing figures, no market share, no implementation
timelines attributed to a product, no "most companies find". Do not say a named vendor is
better or worse than another at anything — the scorecard is the ranking mechanism, and a
remembered opinion contaminates it. Where a fact about the current market matters, search
at runtime and cite it with a date. Where a number is needed for the cost model, make it
an input the user supplies or the vendor confirms in writing, not a constant you supplied.

## Reference files

- **`references/requirements-library.md`** — checklists by category (ATS, HRIS, payroll,
  performance, engagement, sourcing, assessment) plus the cross-category requirements
  users forget. Read once scope is known, before drafting requirements.
- **`references/demo-and-reference-guide.md`** — how to run demos that differentiate, the
  probing question bank by category, and the reference call guide. Read before writing
  demo scripts, and again before reference calls.
- **`assets/scorecard-template.md`** — weighted scorecard, scoring anchors, change log.
  Fill it before the first demo.
- **`assets/decision-paper-template.md`** — the decision paper skeleton, filled after
  scoring.

---

*Part of the [People Leader Skills](REPO_URL) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
