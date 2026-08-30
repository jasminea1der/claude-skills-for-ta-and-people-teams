---
name: ta-ai-maturity-assessment
description: Runs a structured six-dimension assessment of how mature a talent acquisition or people function is in its adoption of AI, and produces a written report with a score per dimension, the binding constraint, and a sequenced 30-day / next-quarter / 2-3 quarter roadmap. Use when someone asks "how good are we at AI", "where are we on AI adoption", "the CEO wants an AI plan for hiring", "we bought a bunch of AI tools and I can't tell if they're working", "the board is asking what we're doing with AI in recruitment", "AI readiness", "AI maturity", "benchmark our TA team on AI", or wants to know what to do next with AI in talent, recruiting, or the wider people function. Also use when preparing an AI position for a board paper, a budget conversation, or a leadership offsite. Not for choosing between named vendors — that is hr-tech-evaluation.
---

# TA & People Function AI Maturity Assessment

Produces a written maturity assessment across six independent dimensions, names the one or
two constraints that are actually holding the function back, and sequences the fix into
horizons. The point is not a score. The point is a defensible answer to "what do we do
next, and why that first" that survives contact with a CEO who has just read something
about AI on a plane.

Most AI maturity work fails in one of two ways: it produces a single number that means
nothing, or it produces a list of twenty improvements with no ordering. This skill exists
to avoid both.

## The core idea: these dimensions move independently

A team can have an excellent stack and no capability to use it. A team can have highly
capable individuals sitting inside a process that prevents them adding value. Averaging
those into "Level 2.6" destroys the only information that mattered.

Six dimensions, scored separately, never averaged into a headline number:

| # | Dimension | The question it answers |
|---|-----------|------------------------|
| 1 | **Operational maturity** | Is the underlying process clean enough for AI to help? |
| 2 | **Team capability** | Can the people actually use these tools? |
| 3 | **Tooling and technology** | What is in the stack, and is it integrated or bolted on? |
| 4 | **Workflow redesign** | Are they doing old steps faster, or doing different steps? |
| 5 | **Governance and risk** | Would this survive a candidate complaint, an audit, or a regulator? |
| 6 | **Measurement** | Can they tell whether any of it worked? |

Two structural relationships matter more than any individual score, and the report must
make them explicit:

- **Operational maturity gates everything.** AI applied to a broken process produces
  faster broken output — more candidates screened against an unclear bar, more interview
  notes summarising unstructured interviews. Where operational maturity is Level 1–2, cap
  the *realised* value of tooling and workflow redesign at operational + 1, and say so.
  The raw score can still be high; the effective score is not.
- **Governance is a gate, not an average.** A function at Level 4 on tooling and Level 1
  on governance is not "mid-maturity". It is carrying a risk position it has not priced.
  Never let a strong tooling score wash out a weak governance score.

Read `references/maturity-model.md` before scoring. It carries the full five-level anchors
for each dimension, the diagnostic questions, and the evidence to ask for.

## What you need to start

One thing: a conversation with someone who knows how the function actually works. Ideally
the Head of TA, CPO, or a TA Ops lead.

Nothing else is required. If the user offers artefacts — an ATS stage report, a tool
inventory, a vendor invoice list, a recruiter headcount, last quarter's hiring metrics —
take them, they sharpen the scoring considerably. If they have none, run entirely on the
conversation and say in the report that scores are self-reported and unverified.

Never stall waiting for data. If the user goes quiet on a dimension, has to drop off the
call, or answers three of six themes, score what is covered, mark the rest **Not
assessed** rather than guessing, and produce the full report anyway. A report covering
four dimensions honestly is worth more than a stalled conversation. Say at the end which
two unanswered questions would most change the picture.

## Process

### 1. Frame it, in two sentences

Open by saying what this will produce and how long it takes: six themed batches of
questions, roughly 20–30 minutes conversationally, ending in a written report with a
roadmap. Ask one calibrating question before starting:

> Is this for your own planning, or does it need to go to someone — a CEO, a board, a
> budget conversation?

The answer changes the register of the report, not the assessment. A board-bound report
leads harder on risk and spend; a planning report leads on sequencing.

### 2. Run the assessment in six themed batches

One batch per dimension. Two to four questions per batch, never more. Twelve questions in
one message gets one-line answers to three of them.

Where the environment supports structured multiple-choice questions (Cowork's
`AskUserQuestion` or equivalent), prefer it for anything with a small set of sensible
answers — "which of these describes your scorecard situation" is far faster to answer than
free text, and it produces cleaner scoring. Keep free text for the questions where the
texture is the point: what broke, what got abandoned, what the team actually does.

Order the batches: **Operational → Team capability → Tooling → Workflow redesign →
Governance → Measurement.** Operational first because it sets the ceiling for the rest and
because it is the least threatening place to start. Governance late, because by then you
know what they are automating and can ask about the right risks rather than reciting a
compliance list.

Adapt the order if the user leads somewhere. Someone who opens with "we bought three tools
and nobody uses them" has just handed you the tooling and capability batches — take them
in that order and backfill operational afterwards.

After each batch, reflect back in one or two lines what you now believe, and where you are
provisionally scoring them. This is what stops an assessment feeling like an
interrogation, and it lets the user correct you before the error compounds.

> So: stages are defined and everyone uses them, but scorecards exist for engineering and
> nowhere else, and half of them get filled in after the debrief. That is a Level 3 on
> operational maturity with a real soft spot in evidence capture. Fair?

### 3. Push past the first answer on two specific questions

Two places where the first answer is almost always wrong, and where pushing is the whole
value of doing this with a human rather than a form:

**Capability.** "The team is using AI" almost always means some recruiters paste job
adverts into a chat assistant and rewrite them. That is Level 2 tool familiarity, not
adoption. Ask for a specific example: *walk me through the last time someone on your team
changed how they did a task because of a tool — not did it faster, did it differently.*
If nobody can name one, capability is Level 2 regardless of how many licences exist.

**Workflow redesign.** "We've automated screening" usually means the same screen, done by
a machine, at the same point in the process. Redesign means the process shape changed:
stages collapsed, a step removed because it no longer earns its place, work moved earlier
or later because the constraint moved. Ask: *what step have you deleted?* Deletion is the
tell. Almost nobody has an answer, and that is fine — say so plainly, because it is the
honest finding and it is where the value is.

### 4. Score each dimension

Score 1–5 against the anchors in `references/maturity-model.md`. The anchors describe
observable behaviour; score against what the user described, not what they aspire to.

Rules that keep scores meaningful:

- **Score conservatively at the boundary.** If the evidence supports 3 or 4, score 3 and
  say what would move it to 4. A generous score removes the reason to act.
- **A dimension is only as strong as its weakest sub-element if that element is
  load-bearing.** Great data hygiene with no defined stages is not Level 4 operational.
- **Distinguish raw from effective where the gate applies.** Present both: "Tooling: 4
  (effective 3 — see operational constraint)".
- **Mark unassessed dimensions as "Not assessed", never as a guess or a zero.** A guessed
  score is the one thing that will get the whole report dismissed.

### 5. Identify the binding constraint

This is the part that makes the report worth reading. "Improve everything" is useless
advice. Name the one or two things that, if fixed, unblock the most, and show the
reasoning.

Diagnostic patterns, in priority order:

1. **Operational floor.** Operational ≤ 2 while any other dimension ≥ 3 → operations is
   binding. They are building on sand and further tooling spend compounds the mess.
2. **Governance exposure.** Governance ≤ 2 while anything automated touches a selection
   decision (screening, ranking, scoring, rejection) → governance is binding regardless of
   every other score. This is the one case where the constraint is about downside, not
   upside, and it should be stated in those terms.
3. **Shelfware gap.** Tooling exceeds capability by two or more levels → capability is
   binding. They are paying for capacity they cannot use; more tools makes it worse.
   Ask what is being paid for and unused, by name, and put it in the report.
4. **Measurement blindness.** Measurement ≤ 2 while everything else ≥ 3 → measurement is
   binding. Not because measurement creates value, but because without it the programme
   cannot be defended and will lose its budget in the next cycle. Say that explicitly to a
   CPO; it is the argument that lands.
5. **Redesign ceiling.** Everything ≥ 3 and workflow redesign ≤ 2 → redesign is binding.
   This is the good problem: the foundations hold and the value is unclaimed.

Where two constraints tie, prefer the one that is cheaper to fix — early momentum buys
permission for the expensive one.

State the constraint as a claim with reasoning attached, not a label. The figures in the
example below are placeholders — use the ones the function gave you:

> **The binding constraint is scorecard discipline, not tooling.** You have interview
> intelligence running on [60]% of interviews, but it summarises unstructured conversations
> against no agreed bar, so the output is a transcript with better formatting. Fixing
> scorecards costs you a design session and two months of enforcement, and it converts a
> tool you already pay for from decorative to decisive.

### 6. Build the sequenced roadmap

Three horizons. Every item tagged with its dimension, effort, and impact.

- **Next 30 days** — things that need no budget, no procurement, and no one else's
  permission. Usually operational hygiene, a governance stocktake, a baseline measurement,
  killing an unused licence. Three to five items, maximum.
- **Next quarter** — things needing a decision, a small spend, or a change to how the team
  works. Four to six items.
- **Next two to three quarters** — structural: redesign, integration, a role, a policy
  that needs legal sign-off. Three to five items.

Effort as Low / Medium / High with a one-line reason (people, money, or political
capital). Impact tied to the constraint: an item that does not relieve the binding
constraint or a real risk should be justified or cut. Sequence so that dependencies are
visible — if the quarter-two item requires the 30-day item to have landed, say so.

Be ruthless about volume. Fifteen well-argued items get done; forty get filed.

### 7. Write the section on where AI does not help

Include it. A report claiming everything can be AI-enabled reads as vendor material to a
senior audience and costs you the credibility of everything else in the document.

Name the parts of hiring that remain stubbornly human, with the reason each resists:

- **Closing a senior candidate.** The decision turns on trust, judgement about the people
  they would work with, and a read on whether the story is real. It is a relationship
  transaction; a well-written email does not move it.
- **Calibrating a hiring manager's expectations.** The work is changing someone's mind
  about what they can get for the money in this market. That requires a person willing to
  disagree with them, with the standing to do it. Evidence helps; it does not substitute.
- **Judgement on borderline candidates.** The genuinely ambiguous case is exactly where
  models are least reliable and where the cost of a confident wrong answer is highest.
  Structure the decision, do not automate it.
- **Reading the room in a hiring debrief.** Where the real disagreement is, who has gone
  quiet, whose objection is actually about something else.
- **Anything the organisation must be able to explain and stand behind.** A rejection a
  candidate challenges. A decision a regulator asks about. Accountability does not
  delegate.

Adapt to what the user described rather than pasting the list. If they told you their
recruiters spend most of their week on scheduling, the point about closing is worth less
to them than a point about where scheduling automation stops.

### 8. Produce the report

Fill `assets/report-template.md` and write it to disk as a Markdown file. Do not deliver
the assessment as a wall of chat — this gets forwarded.

Then offer one upgrade path, chosen for the audience they named in step 1: a slide deck if
it is going to a board or exec team, a Word document if it is going to HR ops or legal, a
shareable page if the team will refer back to it. Offer; do not build all three.

**Handoffs.** Where the roadmap says "evaluate or buy something", that is `hr-tech-evaluation`.
Where operational maturity came back low specifically on interview structure, scorecards
or debriefs, that is `interview-process-audit`. Where the gap is that hiring managers
never define the bar in the first place, that is `hiring-manager-intake`.

## The rapid version

If the user is between meetings or on a live call with limited time, offer a six-question
pass — one diagnostic question per dimension, taken from the "fastest single question"
line in each dimension of `references/maturity-model.md`. It produces a directional score
with lower confidence. Label it clearly as a rapid assessment in the report and say what a
full pass would change. This is better than deferring, because the deferred version does
not happen.

## Scoring honestly

Two failure modes to design against, both of which destroy the report's usefulness:

**Inflation to be pleasant.** The user is describing their own function and will be
invested in it sounding capable. Score what was described. Where you score lower than they
expect, show the anchor text and let the model do the arguing.

**Deflation to justify a programme.** Equally corrosive. If the function is genuinely at
Level 4 on tooling, say so, and put the effort somewhere it is needed.

If the honest answer is "you are at Level 2 across the board and the industry conversation
is ahead of almost everyone's reality", say that. It is usually true, it is a relief to
hear, and it makes the roadmap credible.

## Facts you must not invent

No adoption percentages, no benchmark scores, no "most TA teams are at Level 2", no vendor
capability claims, no named case studies. This report goes in front of boards.

Where current external facts matter — regulation above all — search at runtime and cite
what you find with its date, rather than asserting from memory. The regulatory picture for
employment-related AI is moving quarterly and anything stated from memory will be stale or
subtly wrong. `references/governance-and-risk.md` lists specifically what to verify.

Where a number would help the argument, make it the user's own: ask for their time to
hire, their recruiter req load, their tool spend. Their own baseline is more persuasive to
their board than any external benchmark, and it is defensible.

## Legal and ethical guardrails

**This is analysis, not compliance sign-off.** The assessment surfaces where the function
carries risk and frames the questions for a qualified adviser. It does not certify
compliance with the EU AI Act, NYC Local Law 144, or any other instrument, and the report
says so.

**Adverse impact.** The skill may flag where automated screening, ranking or scoring could
disadvantage a group, and recommend structural fixes — validating the tool, monitoring
outcomes by stage, keeping a human decision-maker on rejections. It does not compute a
legal adverse-impact finding, and it never recommends a selection approach that uses a
protected characteristic.

**Jurisdiction.** Ask early which jurisdictions they hire in — the governance dimension is
close to meaningless without it, and the obligations diverge sharply. State plainly that
any governance action in the roadmap needs local legal review before it is implemented.

**Personal data.** If the user offers candidate or employee records as evidence, ask for
aggregate counts and identifiers rather than names, and to leave out special-category data
unless the analysis genuinely needs it. It reduces their exposure and the assessment does
not need it.

## Reference files

- **`references/maturity-model.md`** — the full six-dimension model: five described levels
  per dimension, diagnostic questions, evidence to ask for, and the fastest single
  question per dimension. Read this before running the assessment, and again before
  scoring.
- **`references/governance-and-risk.md`** — candidate data handling, bias in automated
  screening, transparency, what to verify in the regulatory picture and where, and a
  practical governance checklist. Read before running the governance batch, and whenever
  governance scores 1–2.
- **`assets/report-template.md`** — the report skeleton. Fill it; keep its section order.

---

*Part of the [People Leader Skills](REPO_URL) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
