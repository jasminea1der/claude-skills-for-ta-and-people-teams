---
name: career-framework-builder
description: Builds a career framework for one function — level count, the competencies that actually differentiate levels, evidence-based progression criteria, a dual IC/management track, and the connection to titles and pay bands. Use when someone says they need a career framework, levelling framework, career ladder, competency framework, job architecture, progression framework or growth framework; when promotion decisions are inconsistent or fought over; when people ask "what do I need to do to get promoted" and nobody has a good answer; when titles have inflated or drifted; when engineers, salespeople or designers are leaving because they cannot see a path; when someone wants to fix a framework that exists but is not being used; or when a levelling exercise needs to happen before pay bands can be built. Also use for mapping existing employees onto new levels and for handling over-titled people. Owns the levels and the progression criteria; for running the ratings moderation session those criteria feed, use performance-calibration-pack.
---

# Career Framework Builder

Produces a working career framework for one function: how many levels, what genuinely
separates one level from the next, what evidence a promotion case needs, how the IC and
management tracks relate, and how the whole thing connects to titles and pay.

This is usually a project that has stalled for two years because nobody had a starting
point. The job here is to produce a concrete, arguable draft fast, not a perfect one
slowly. A framework someone can mark up in a meeting beats a blank template every time.

---

## Scope it small, and say why

The commonest way this project fails is trying to level the whole company at once. It
produces a matrix so generic it differentiates nothing, it needs sign-off from every
function head simultaneously, and it dies in month four.

Push for **one function first, built properly, then extend**. Give the user the reasoning
rather than just the rule:

- Levelling is only useful when the descriptors are specific enough that two managers
  reading them reach the same decision about the same person. Specificity comes from
  functional detail, which cannot be written generically.
- One function gives you a real test. You find out whether the levels map cleanly onto
  actual people before you have committed the whole company to a structure.
- The second function takes a fraction of the time, because the level count, the
  differentiator set, the progression-evidence pattern and the pay-band architecture all
  carry over. Only the functional depth is rewritten.

Pick the function with the most pain — usually the largest, the one with the worst
attrition at mid-level, or the one where promotion arguments are most frequent. If the
company genuinely needs company-wide architecture now (a pay transparency obligation, a
merger, a comp system implementation), build the shared spine — level count, level names,
the differentiator set, band structure — and then the functional detail one function at a
time. Say plainly that the spine alone is not usable for promotion decisions.

---

## What you need to start

Minimum viable input is two things: **the function** and **roughly how many people are in
it**. Everything else improves the draft but does not gate it.

Ask for the rest in two small batches, not a form:

**Batch one — shape.**
- Function and headcount, plus rough distribution (how many junior, mid, senior).
- The titles actually in use today, including the awkward ones.
- Whether there is a management layer inside the function and how deep it goes.

**Batch two — constraints.**
- Is there a dual track today, formally or informally? Do senior ICs exist?
- Do pay bands exist, are they being built alongside, or will they follow later?
- Company headcount overall, stage, and growth expectation over the next 18 months.
- What triggered this now — a promotion dispute, attrition, a pay transparency
  obligation, a funding round, a new CPO. The trigger tells you what the framework has to
  survive politically.

Where the environment supports structured choice questions, use them for the closed ones
(dual track yes/no/informal; bands exist/building/later). Faster to answer than free text.

**If the user cannot answer most of this, do not stop.** Build the draft from function,
company size and stage alone, state every assumption inline, and label the whole thing a
starting draft to react to. Then ask which parts are wrong — reacting to a concrete level
matrix surfaces the real constraints far faster than an interview does.

---

## Process

### 1. Set the level count deliberately

The level count is the first real decision and the hardest to change later, because it is
baked into every title and every pay band.

The failure at both ends:

- **Too few levels** and people spend four years at the same label with no recognised
  progress. Strong mid-level people leave, because from the outside every other company
  looks like it offers a step up.
- **Too many levels** and each step means almost nothing. Promotion degrades into an
  annual entitlement, managers grant it to retain people rather than to recognise a real
  change in scope, and the framework loses authority the first time someone is promoted
  who obviously has not changed what they do.

Anchor the count on two things: **expected tenure** and **headcount available to fill the
levels**. If the median tenure in the function is three years and you have eight levels,
most people will never see a promotion. If you have twelve people and six levels, you
have two people per level and the levels are decorative.

Rough starting points, to be calibrated against the user's own tenure and headcount data,
not treated as rules — see `references/level-design.md` for the full reasoning:

| Function headcount | IC levels, typical starting point |
|---|---|
| Under 15 | 3–4 |
| 15–50 | 4–5 |
| 50–150 | 5–6 |
| 150+ | 6–7, with the top levels rare and gated hard |

Push back explicitly when a user wants more levels than they have people to fill. Ask how
many people they expect at each level in 18 months. If the answer is one or zero for
several levels, those levels are aspirational and should be described as such — or cut.

### 2. Choose the differentiators before writing any descriptors

This is the heart of the framework. A level is defined by what changes between it and the
level below. Pick the dimensions first, then write every level against the same set, so
the framework reads as one ladder rather than five unrelated job descriptions.

The five that carry most of the weight:

1. **Scope of impact** — what breaks if this person is wrong. Their own task, their team's
   quarter, the function's year, the company's strategy.
2. **Autonomy and problem type** — are they given the problem and the approach, given the
   problem, or finding the problem? This is usually the single sharpest differentiator.
3. **Ambiguity tolerated** — how well-defined the situation is when they are expected to
   make progress in it.
4. **Influence, and over whom** — persuading their own team, peers in other functions,
   leaders more senior than them, people outside the company.
5. **Functional depth** — the craft dimension. Written specifically for the function, and
   the only one that does not transfer between functions.

Two differentiators to keep out, and the reasons matter because users will push for both:

- **Years of experience.** It rewards tenure rather than contribution, it makes the
  framework indefensible the moment a fast third-year outperforms a static eighth-year,
  and it correlates with age closely enough to create real risk in a promotion process.
  Experience predicts level; it does not define it.
- **Headcount managed.** It makes management the only route upward, so your best
  practitioners take teams they do not want and stop doing the work you needed them for.
  It also means levels move when a reorg happens rather than when a person grows. Scope of
  impact captures what headcount was proxying for, without the distortion.

Read `references/level-design.md` before writing descriptors. It covers each
differentiator in depth, how to phrase them so two managers reach the same answer, and
worked examples of a level descriptor written well and badly.

### 3. Write the level descriptors

Per level: a one-line summary of the level's purpose, then a short paragraph on each
differentiator, then the functional depth section written in the function's own language.

Keep them short. A descriptor nobody reads has no effect on any decision. Aim for
something a manager can hold in their head — roughly a page per level, less at junior
levels.

Test each pair of adjacent levels with the question: *could I describe a real person who
sits clearly at one and not the other?* If not, the two levels are one level.

### 4. Build the dual track, if the function has one

Where the function has senior craft work that should not be done by managers — engineering,
design, data, science, sometimes sales and legal — build the IC track properly or do not
claim to have one.

Properly means: senior IC levels are genuinely equivalent to their management counterparts
in scope, in pay band, in who they influence, and in how hard they are to reach. A "Staff"
level that pays less than the manager level it claims to parallel is not a track, and
everyone in the function works that out within a week.

Dual tracks fail in predictable ways — decorative equivalence, an IC ceiling one level
below the management ceiling, promotion committees that only understand management
evidence, and senior ICs with no organisational mechanism to actually influence anything.
`references/level-design.md` covers each and how to design against it.

### 5. Write progression criteria as evidence, not adjectives

"Demonstrates leadership" is not a criterion. It cannot be argued for or against, so in
practice it means whatever the person deciding wants it to mean — which is exactly the
inconsistency the framework exists to remove.

Use this pattern for every criterion:

> **The behaviour** — observable, specific
> **at what scope** — team, function, company
> **with what evidence** — what a promotion case would actually contain

Worked example:

- Bad: *Demonstrates technical leadership.*
- Better: *Has led the technical design of a project spanning at least two teams,
  including the trade-off decisions and the sequencing, and the design held up through
  delivery.* Evidence: the design document, the delivery outcome, and the view of an
  engineer on the other team.

Make the sustained-performance requirement explicit: promotion recognises that someone is
already operating at the next level, typically for two review cycles or a meaningful
project cycle, not that they are ready to try. This one sentence prevents most promotion
disputes, because it moves the argument from prediction to evidence.

### 6. Connect it to pay, and keep the processes separate

State the architecture explicitly, because this is where frameworks either become load-
bearing or become a document:

- **One band per level**, with the level as the input to the band, not the reverse.
- **Adjacent bands overlap.** Overlap is a feature: it means someone strong late in one
  level can be paid more than someone new to the level above, so pay can recognise
  performance without forcing a premature promotion. No overlap and every pay problem
  becomes a promotion request.
- **Promotion and pay are decided in separate processes** using the same framework.
  Deciding them together means budget silently determines who gets levelled, and the
  levelling stops being a statement about scope. Level people against the descriptors
  first; apply the pay consequence second.

Pay transparency regulation in a growing number of jurisdictions increasingly requires
objective, documented criteria for progression and pay — the EU Pay Transparency
Directive as transposed by member states, and pay transparency and pay-range disclosure
laws in a number of US states and elsewhere. Do not assert what any of them currently
require. Instruct the user to confirm current obligations and timing for their specific
jurisdictions with counsel, and note that a documented, criteria-based framework is
usually the practical foundation for meeting them regardless of the detail.

Do not build actual pay numbers here. Levelling first, benchmarking and band-setting
after, with market data the user supplies.

### 7. Plan the rollout before you finish the framework

Frameworks die at rollout, not at design. Cover, at minimum: mapping every existing person
to a level, deciding what happens to people whose title sits above their actual scope,
whether titles are grandfathered, how it is communicated, and how managers are trained to
use it.

Read `references/rollout.md` for the full sequence. The over-titled-people problem is the
most politically difficult part of the entire project and that file handles it directly —
do not improvise it.

### 8. Produce the artefact

Write the framework to a Markdown file using `assets/framework-template.md`. Then offer
one upgrade path suited to the audience — a slide summary for the exec conversation, a
spreadsheet for the mapping worksheet, a shareable page if the whole function will refer
to it. Offer; do not build all three.

---

## When the user has almost no context

Produce a draft framework anyway. Base it on function, company size and stage, label it
clearly as a starting draft, and make it concrete — real level names, real descriptors,
real criteria, all specific enough to disagree with.

Then close with the two or three inputs that would sharpen it most, named exactly: the
current title list, the headcount distribution across those titles, and median tenure in
the function. Do not ask for "more information".

---

## Output

A single Markdown file containing:

1. **Framework overview** — function, scope, level count and the reasoning for it, track
   structure, and what this framework does and does not decide.
2. **Level matrix** — one table, levels as rows, differentiators as columns. The page
   people will actually use.
3. **Level descriptors** — one section per level, both tracks where relevant.
4. **Progression criteria** — per level transition, in the behaviour/scope/evidence
   pattern, with the sustained-performance bar stated.
5. **Titles and pay bands** — level-to-title mapping, band structure and overlap
   principle, and the separation of promotion and pay decisions.
6. **Mapping worksheet** — the structure for placing existing people, with the over-titled
   handling.
7. **Rollout plan** — sequence, communications, manager training, first cycle.
8. **Assumptions** — every assumption made, and what would replace each with fact.

---

## Reference files

- `references/level-design.md` — read before writing any descriptor. The five
  differentiators in depth, how to write descriptors that two managers read the same way,
  dual track design and its failure modes, level count reasoning by size and stage, and
  worked good/bad examples.
- `references/rollout.md` — read before the rollout section, and always when the user asks
  about mapping people or over-titled employees. Mapping process, over-titled and
  under-levelled people, grandfathering, manager training, communications, first-cycle
  mistakes.
- `assets/framework-template.md` — the output skeleton to fill in.

---

## Legal and ethical guardrails

**This produces structure, not legal conclusions.** A levelling framework has direct pay
and progression consequences, so it sits close to real legal exposure. Route the finished
framework and the mapping outcomes through counsel before rollout, particularly where
levelling changes anyone's pay or title.

**Pay equity is a legal determination, not an output of this skill.** The framework can
make progression criteria objective and documented, which is what defensibility rests on.
It does not conclude that pay is equitable. Where mapping people onto levels reveals
apparent pay differences between comparable people, flag the pattern and recommend a
proper pay equity analysis run through counsel — in several jurisdictions that analysis is
privileged work product when run that way, and doing it informally first forfeits that.

**Keep protected characteristics out of levelling entirely.** Level against scope and
evidence only. Where the mapping exercise produces a distribution that looks skewed — any
group defined by a protected characteristic clustered at lower levels than tenure and scope
would explain — treat that as a signal to examine the criteria and the historic promotion
decisions, not as something to correct by adjusting individuals' levels.

**Jurisdiction and data.** Titles, levels and pay bands interact with local employment law,
collective agreements and works council consultation in ways that differ by country — ask
which jurisdictions are in scope and say plainly that the output needs local legal review,
since in several European jurisdictions changing a levelling structure triggers formal
consultation before it can be implemented. Use employee identifiers rather than names in
any mapping data shared for analysis; the worksheet works fine without names and it limits
exposure if the file travels further than intended.

---

## Related skills

The level descriptors written here are what interviewers should assess against. Hand the
target level's descriptor and its progression criteria to **interview-kit-builder** so
external hiring and internal progression are held to the same bar — otherwise you level
externally hired people generously and internally promoted people harshly, and the
framework loses credibility from both directions.

The framework is also the reference point for **performance-calibration-pack**: calibration
compares people against the expectations of their level, which only works once those
expectations are written down.

---

*Part of the [Claude Skills for TA and People Teams](https://github.com/we-are-move/claude-skills-for-ta-and-people-teams) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
