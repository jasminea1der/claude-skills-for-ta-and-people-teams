# The six-dimension AI maturity model

The full model behind `ta-ai-maturity-assessment`. Read before running the assessment and
again before scoring.

## Contents

- [How to use this model](#how-to-use-this-model)
- [The level scale](#the-level-scale)
- [The two structural relationships](#the-two-structural-relationships)
- [Dimension 1 — Operational maturity](#dimension-1--operational-maturity)
- [Dimension 2 — Team capability](#dimension-2--team-capability)
- [Dimension 3 — Tooling and technology](#dimension-3--tooling-and-technology)
- [Dimension 4 — Workflow redesign](#dimension-4--workflow-redesign)
- [Dimension 5 — Governance and risk](#dimension-5--governance-and-risk)
- [Dimension 6 — Measurement](#dimension-6--measurement)
- [Scoring at the boundary](#scoring-at-the-boundary)
- [Reading the pattern across dimensions](#reading-the-pattern-across-dimensions)
- [Common false positives](#common-false-positives)

---

## How to use this model

Each dimension below carries:

- **What it is** — and why it is a separate dimension rather than part of another.
- **The five levels**, described as observable behaviour. Score against what the user
  described happening, not what they intend or aspire to.
- **Diagnostic questions** — grouped, three or four to ask, the rest as follow-ups.
- **Evidence to ask for** — what would move a score from self-reported to verified.
- **Fastest single question** — for the rapid pass when there is no time for the full
  batch.
- **The tell** — the specific answer that reliably discriminates between adjacent levels.

Do not read the levels aloud to the user. Ask the diagnostic questions, listen, and score.

---

## The level scale

The same five levels apply across all six dimensions. The names are deliberately
behavioural rather than evaluative — "Experimenting" is a legitimate place to be, and a
function that is genuinely at Level 2 and knows it is in better shape than one that
believes it is at Level 4.

| Level | Name | Shape |
|-------|------|-------|
| 1 | **Ad hoc** | Nothing deliberate. What exists is accidental or individual. |
| 2 | **Experimenting** | Real activity, unowned and unrepeatable. Pilots, enthusiasts, pockets. |
| 3 | **Operating** | Deliberate, documented, used by most of the team most of the time. |
| 4 | **Integrated** | Built into how the function runs. Survives people leaving. Measured. |
| 5 | **Compounding** | The function improves itself. Learning from one hire changes the next. |

Level 5 is rare and should be scored rarely. It is not "very good at Level 4" — it
requires a feedback loop that makes the system better without someone driving it. If the
user cannot describe the loop, it is a 4.

---

## The two structural relationships

**Operational maturity gates realised value.** Where operational maturity is 1 or 2, cap
the *effective* score of Tooling and Workflow Redesign at operational + 1. Report both:
"Tooling: 4 (effective 3)". The reason is mechanical rather than moralistic — AI systems
in hiring consume the function's own data and structure as their input. Screening quality
depends on a defined bar. Interview intelligence depends on structured interviews. Sourcing
recommendations depend on clean historic outcome data. When those inputs are absent, the
tool produces confident output with nothing behind it, which is worse than no output
because it is harder to argue with.

**Governance is a gate, not an average.** Never let a strong tooling or redesign score
compensate for governance ≤ 2. A function automating selection decisions with no bias
monitoring, no transparency to candidates and no record of how decisions are made is
carrying an unpriced liability, and the correct description of that is not "mid-maturity".
Report governance separately and prominently.

---

## Dimension 1 — Operational maturity

### What it is

Whether the underlying hiring process is clean enough to be worth automating: data hygiene
in the ATS, defined and consistently used stages, scorecards that exist and get completed,
documented workflows, a single source of truth for who is where.

This is a separate dimension from tooling because it is almost entirely independent of it.
A function can run a modern ATS badly and a spreadsheet well. It gates the others because
AI applied to a broken process produces faster broken output at higher volume, and adds
the appearance of rigour to a decision that has none.

### The five levels

**Level 1 — Ad hoc.** Process differs by recruiter and by hiring manager. Candidate status
lives partly in the ATS, partly in inboxes, partly in one person's head. Stages exist as
labels but mean different things to different people, or get skipped. No scorecards, or
scorecards that nobody fills in. Nobody could reconstruct why a specific candidate was
rejected six months ago. Reporting requires someone to rebuild the data by hand each time,
and two people asked for the same number produce different answers.

**Level 2 — Experimenting.** A defined process exists on paper — a stage map, a template
somewhere — but adherence is patchy and unenforced. Some teams follow it, usually the ones
where a particular recruiter or hiring manager cares. Scorecards exist for some functions,
typically engineering, and not others. Rejection reasons are captured as free text or a
generic dropdown that everyone picks the first option from. ATS data is broadly right on
the current pipeline and unreliable historically. Reporting is possible but each number
needs a caveat.

**Level 3 — Operating.** Stages are defined, mean the same thing across the function, and
are used consistently enough that a pipeline report is believable. Scorecards exist for
most roles and get completed for most interviews, usually before the debrief. Rejection
reasons use a controlled vocabulary that maps to something. Source of hire is captured and
mostly accurate. The process is documented and a new recruiter is onboarded onto it rather
than absorbing it. There are known gaps — a function that does its own thing, a stage where
data quality drops — and the team can name them.

**Level 4 — Integrated.** Data hygiene is maintained by design rather than discipline:
required fields, validation, stage gates that will not advance without the artefact.
Scorecard completion is near-universal and completion is visible to the people whose
behaviour it depends on. Historic data is trustworthy far enough back to analyse — a year
or more. Workflow is documented, versioned, and owned by a named person or an ops function.
Exceptions are handled explicitly rather than by working around the system. Someone would
notice within days if data quality dropped.

**Level 5 — Compounding.** The operational layer generates usable signal, not just clean
records. Outcome data flows back into the process: which interview signals predicted the
hires who worked out, where the drop-off is, which sources produce candidates who pass
onsite. Definitions are stable enough to compare periods. Data quality is monitored as a
metric with an owner, and process changes are made on the basis of what the data showed
rather than what the last painful hire felt like.

### Diagnostic questions

**Ask these three:**

1. If I asked you for a list of everyone rejected at final stage last quarter and why,
   how long would that take and how much would you trust the answer?
2. Walk me through your stages. Do they mean the same thing to your engineering team and
   your commercial team?
3. What proportion of interviews end up with a completed scorecard, honestly — and is it
   filled in before or after the debrief conversation?

**Follow up on:**

- Where does candidate status actually live for a role in flight?
- What happens in your ATS when someone tries to advance a candidate without the
  interview feedback in? Anything?
- Is there a written version of the process, and when was it last true?
- How far back does your data go before you stop trusting it?
- Which team or function does its own thing, and why has that not been fixed?
- How do you capture rejection reasons — free text, or a list someone designed?

### Evidence to ask for

- A stage-by-stage pipeline report for one quarter — look at whether stage names are
  consistent and whether the funnel is plausible.
- Scorecard completion rate by function, if the ATS will produce it.
- The process documentation, and its last-modified date.
- The rejection-reason picklist. A picklist with four options, one of which is "other" and
  carries 60% of the volume, is diagnostic on its own.

### The tell

Ask what happens when a recruiter tries to move a candidate forward without the required
artefact. **Level 1–2: nothing happens.** **Level 3: someone chases.** **Level 4: the
system does not let them.** This single answer discriminates the middle of the scale more
reliably than any self-assessment.

### Fastest single question

> If you pulled a report on last quarter's hires right now, what would you have to
> apologise for before you sent it?

---

## Dimension 2 — Team capability

### What it is

Whether the people can actually use these tools — and specifically, whether they can do
anything beyond prompting a chat assistant to rewrite text they would otherwise have
written themselves.

Separate from tooling because the two diverge constantly and in both directions: teams
with excellent stacks and no capability (shelfware), and capable individuals with nothing
but a consumer chat tool who have genuinely changed how they work.

The distinction that carries this dimension: **tool familiarity is not capability.** The
common failure is a team who use a chat assistant to rewrite job adverts and believe they
have adopted AI. Rewriting an advert is a text task done faster. It changes no decision, no
sequence, and no outcome. Score it as Level 2 and be specific about why.

### The five levels

**Level 1 — Ad hoc.** No deliberate capability. One or two individuals use consumer AI
tools privately, possibly against policy, and do not talk about it. Most of the team have
not tried. No training, no examples circulating, no shared understanding of what these
tools are good and bad at. If asked, people would describe AI in terms of what they have
read rather than what they have done.

**Level 2 — Experimenting.** Visible enthusiasm and real usage, concentrated in text
generation: adverts, outreach messages, interview questions, summarising a CV. A few
enthusiasts do more and are treated as the AI people. There may have been a training
session; it was a demo, and nothing changed afterwards. Nobody can point to a task that is
done *differently* rather than faster. Prompting is one-shot — ask, accept or discard, move
on. Output goes out with light editing or none, and quality varies by who sent it.

**Level 3 — Operating.** Most of the team use AI in defined parts of their work with
reasonable competence. There are shared prompts, saved templates, or an internal guide that
people actually use, and someone maintains it. People can articulate where the tool is
unreliable and check its output accordingly. Iteration is normal — refine, provide context,
push back on the first answer. A new joiner is shown how the team uses these tools as part
of onboarding rather than discovering it. Usage extends beyond text generation into at
least one analytical or research task.

**Level 4 — Integrated.** Capability is a property of the team, not of individuals. There
is a named owner for AI practice within the function. People bring context to the tools —
their own data, their own criteria, their own historic examples — rather than asking
generic questions. The team can evaluate a tool's output critically, including recognising
when it is confidently wrong, and there are worked examples of them rejecting AI output for
good reasons. Capability development is deliberate and continuous, not a launch event.
Recruiters can redesign a small piece of their own workflow without asking permission.

**Level 5 — Compounding.** The team improves its own practice systematically. What one
recruiter learns propagates — shared patterns, a living internal library, regular sessions
where people show what changed. The function can absorb a new capability quickly because it
has done it before and has a route for doing it. People are fluent enough to identify
opportunities the leadership had not thought of, and there is a mechanism for those to get
tried. Capability is a hiring criterion for new recruiters.

### Diagnostic questions

**Ask these three:**

1. Walk me through the last time someone on your team changed *how* they did a task
   because of a tool — not did the same task faster, did it differently.
2. If I sat with your median recruiter — not your best one — what would I see them using
   AI for in a normal week?
3. What has your team tried with AI that did not work, and what did they conclude?

**Follow up on:**

- Who is the person everyone asks when they are stuck with a tool? What is their actual
  job?
- Is there a shared set of prompts or a guide? Who maintains it, and when did it last
  change?
- Has anyone been trained? What did the training consist of — a demo, or supervised
  practice on their own work?
- Does anyone give the tools your own context — your scorecards, your historic pipeline,
  your competency framework — or is it all generic prompting?
- When the output is wrong, does anyone notice?

### Evidence to ask for

- The shared prompt library or internal guide, if one exists.
- Seat-level usage data from whichever tools report it — licences assigned versus weekly
  active users is the single most informative number in this dimension.
- A recent example of AI-assisted output that went to a candidate or hiring manager.

### The tell

The answer to question 3 — *what did not work*. A team genuinely at Level 3+ has a list:
tried it for X, output was unreliable, stopped. A team at Level 2 has no failures because
they have not pushed anything far enough to hit its limits. **No failures means no depth.**

### Fastest single question

> Other than writing text — adverts, outreach, summaries — what does your team use AI for?

Silence or a strained answer is Level 2. Two concrete examples is Level 3.

---

## Dimension 3 — Tooling and technology

### What it is

What is actually in the stack, how it fits together, and whether it is embedded in the
workflow or bolted alongside it. Includes what is being paid for and not used — which is
information, not an embarrassment, and should be collected without judgement so it gets
answered honestly.

This dimension is about the estate, not about the value extracted from it. Value is
Dimensions 2 and 4. Keep them separate or the shelfware pattern becomes invisible, and the
shelfware pattern is one of the most common and most fixable findings in this whole
assessment.

### The five levels

**Level 1 — Ad hoc.** An ATS, possibly an old one, used as a record store. No AI capability
in the stack beyond whatever the ATS vendor has switched on by default and nobody has
looked at. Any AI usage is individuals on consumer tools with personal accounts, outside
any procurement or security review.

**Level 2 — Experimenting.** Point solutions acquired opportunistically — a sourcing tool,
a note-taker, an outreach sequencer, a scheduling assistant. Each bought to solve one
problem, each with its own login, none integrated with the ATS beyond an export or a Zapier
connection someone built. Nobody has a full list of what is licensed. At least one tool is
paid for and effectively unused, and the renewal date is not tracked. Recruiters context-
switch between systems and re-key data.

**Level 3 — Operating.** A deliberate stack rather than an accumulated one. The core
systems are known, owned, and mostly integrated — candidate data flows between the ATS and
the main adjacent tools without manual export. Licences are tracked against actual usage.
There is a named owner for the stack. New tools go through some form of evaluation before
purchase, even if it is lightweight. Some AI capability is genuinely embedded where the
work happens rather than requiring a detour to another tab.

**Level 4 — Integrated.** The stack is designed around the workflow. AI capability appears
at the point of the task, inside the system the recruiter is already in, not as a separate
destination. Data flows are documented and monitored. There is a deliberate build/buy/use-
native position rather than a default to buying. Vendor performance is reviewed against
what was promised, and tools get removed as well as added — the ability to name something
they switched off is a strong signal here. Security and data-processing review happens
before purchase rather than after an incident.

**Level 5 — Compounding.** The stack is an asset the function controls rather than a set of
vendor relationships it manages. Their own data — historic outcomes, scorecards, pipeline
history — is available to the tools that need it, safely and deliberately, so the tooling
gets better as the function accumulates history. Architecture decisions anticipate
replacing components without rebuilding everything. The function can adopt a new capability
in weeks because the integration surface exists.

### Diagnostic questions

**Ask these three:**

1. List everything in the stack that touches hiring, including things you suspect nobody
   uses. What is the annual spend, roughly?
2. When a candidate applies, how many systems does their data end up in, and does anyone
   re-key it?
3. What is the last thing you switched off or did not renew?

**Follow up on:**

- Which of these has AI capability you are actually using, versus AI capability you were
  sold?
- Which tools are integrated with the ATS properly, versus connected by an export or a
  spreadsheet?
- Who owns the stack? Is that their job or a thing they picked up?
- Are any recruiters using tools you did not buy? (Ask neutrally. Shadow tooling is a
  capability signal and a governance signal at the same time.)
- When does your ATS contract renew, and does anyone have a view on it?

### Evidence to ask for

- The tool inventory or the relevant lines of the vendor spend list.
- Licence counts versus active users, per tool.
- Renewal dates.
- Any integration diagram, however rough.

### The tell

Question 3 — *what have you switched off*. Functions at Level 2 only ever add; the stack is
a sediment of past problems. The ability to name a tool that was removed, and why,
indicates someone is actually managing the estate. Similarly diagnostic: **can they produce
the list at all, or do they have to go and ask finance?**

### Fastest single question

> What are you paying for that nobody uses?

An immediate, specific answer indicates Level 3+ (they know their estate). "I'd have to
check" is Level 2. A confident "nothing" is usually Level 2 with less visibility.

---

## Dimension 4 — Workflow redesign

### What it is

The difference between using AI to do the existing steps faster and redesigning the process
around what is now possible. This is where the value actually sits, and it is where almost
nobody is — including functions that are strong on every other dimension.

The distinction is not subtle once you have the right question. Automation makes step 4
take twenty minutes instead of an hour. Redesign asks whether step 4 should exist, whether
steps 3 and 4 should be one step, whether the decision it feeds could be made earlier with
information that is now cheap to get.

Score this dimension strictly. Almost every function will describe automation as redesign,
and marking that generously removes the single most valuable finding in the report.

### The five levels

**Level 1 — Ad hoc.** The process is what it has always been. AI, where used, is invisible
to the process — an individual drafting faster inside an unchanged step.

**Level 2 — Experimenting.** Tasks within existing steps are accelerated. CV screening
assisted, adverts drafted, notes summarised, outreach generated. Every stage that existed
last year still exists, in the same order, with the same owner and the same handoffs. Time
is saved and typically absorbed by more volume rather than reallocated deliberately. If
asked what has changed structurally, the honest answer is nothing.

**Level 3 — Operating.** At least one real structural change has been made and stuck. A
stage has been merged, removed, resequenced, or moved to a different owner because AI
changed what was possible at that point. Examples: a screening call removed because
structured async assessment now carries that signal; two interviews merged because the
overlap was visible; a sourcing step moved from recruiter to automated with human review at
a different threshold. The change was deliberate, and someone can explain the reasoning and
what it cost.

**Level 4 — Integrated.** Redesign is a habit rather than an event. The function regularly
asks where the constraint now is and reshapes around it. Recruiter time freed has been
deliberately reallocated to work that requires a human — hiring manager calibration,
closing, market intelligence — rather than absorbed into more of the same activity. The
process looks materially different from the industry-standard funnel and the differences
are explicable. Human effort is concentrated where judgement genuinely changes the outcome.

**Level 5 — Compounding.** The process is treated as a designed system that is expected to
keep changing. New capability triggers a review of process shape as a matter of course, not
a bolt-on. The function has removed steps that other organisations still consider mandatory
and can defend each removal with outcome data. What the recruiter role consists of has
changed, and hiring for the role reflects that.

### Diagnostic questions

**Ask these three:**

1. What step have you deleted?
2. Take one role you hire regularly. Walk me through the stages today, and tell me which
   ones existed eighteen months ago.
3. Where AI has saved your recruiters time — where did that time go?

**Follow up on:**

- What is the constraint in your process right now — the thing that actually sets how long
  a hire takes? Has that changed?
- Is there a stage that exists because it always has, that nobody could defend?
- Has the shape of any recruiter's week changed, or just the speed of it?
- Has anything moved earlier or later in the process because information got cheaper?
- Has the recruiter role itself changed — what you would hire for now versus two years ago?

### Evidence to ask for

- Stage maps for one role, current and prior, if any version history exists.
- Any before/after time or volume comparison the function has.
- A description of the recruiter week, ideally from a recruiter rather than the leader.

### The tell

Question 1: **what have you deleted?** Deletion is the discriminator because it is the one
thing automation cannot produce on its own. Anyone can add a tool to a step. Removing a
step requires someone to have decided the signal it produced is now available elsewhere,
and to have taken the risk of being wrong.

Question 3 is the second tell. "It went into more roles per recruiter" is efficiency
extraction, which is legitimate but is Level 2. "It went into hiring manager calibration
and closing" is a deliberate reallocation and supports Level 4.

### Fastest single question

> What does your process no longer include that it did two years ago?

---

## Dimension 5 — Governance and risk

### What it is

Candidate data handling, bias and adverse impact in automated screening, transparency to
candidates, human oversight of decisions, vendor due diligence, and the regulatory picture.

Read `references/governance-and-risk.md` before running this batch. It covers the substance;
this section covers the levels and the questions.

Two framing points that make this dimension land with a senior audience rather than reading
as compliance theatre. First, the exposure is concentrated: it scales with how close the
automation sits to a *decision that affects a person*, not with how much AI is in use.
A function using AI heavily for research, drafting and scheduling carries very little of
this risk. A function letting a tool rank or reject candidates carries a lot, even at low
volume. Second, the obligations are moving quarterly — search and cite at runtime rather
than asserting anything from memory.

### The five levels

**Level 1 — Ad hoc.** No position. Nobody has asked what candidate data goes into which
tool. Recruiters may be pasting CVs into consumer AI accounts. No view on whether any tool
in use makes or influences selection decisions. No candidate-facing disclosure. If a
candidate asked how their application was assessed, nobody could answer accurately.

**Level 2 — Experimenting.** Awareness without structure. Someone — often the CPO, often
after reading something — has raised the question. There may be a policy document, usually
generic and not derived from what the function actually does. Legal or privacy have been
consulted once. Nobody has systematically mapped which tools touch candidate data or which
influence decisions. Vendor claims about bias and compliance are accepted at face value
because there is no basis to challenge them.

**Level 3 — Operating.** The basics hold. There is an inventory of which tools process
candidate data and what each does with it. Data processing agreements are in place and
someone has read them. There is a stated position on human oversight — a named point where
a person makes or confirms any adverse decision — and it is followed. Candidates are told
something truthful about the use of automated tools. Someone owns this, and legal has
reviewed the position rather than just been informed of it.

**Level 4 — Integrated.** Governance is operational rather than documentary. Outcomes are
monitored by stage for adverse impact patterns, with an agreed process for what happens when
a pattern appears — and the monitoring is run through counsel where privilege matters.
Vendors are asked specific questions about training data, validation and bias testing before
purchase, and answers are on file. Records are kept of how automated tools contribute to
decisions, sufficient to reconstruct a specific case. Candidate-facing disclosure is
specific rather than boilerplate. Jurisdictional obligations are mapped against where they
actually hire. Someone tracks regulatory change as part of their job.

**Level 5 — Compounding.** Governance is a design input rather than a review gate. New
tooling is assessed for decision-impact before pilot, not before rollout. Bias monitoring
is routine, trended, and acted on. The function could evidence its process to a regulator,
a client's audit, or a claimant with a subject access request without a scramble.
Transparency is treated as a candidate-experience asset — they tell candidates plainly
because it is defensible.

### Diagnostic questions

**Ask these three:**

1. Which of your tools makes, ranks, scores, or filters a decision about a candidate —
   as opposed to helping a human do their own work?
2. Where do you hire? Which jurisdictions are actually in scope?
3. If a rejected candidate asked whether AI was used to assess them, what would you tell
   them, and would it be true?

**Follow up on:**

- Is any candidate rejected without a human looking at the decision? At which stage?
- What candidate data goes into which tool — and does anyone paste CVs into a consumer
  account?
- Have you asked any vendor how their model was trained or validated, and what did they
  say?
- Has anyone looked at outcomes by stage for patterns across demographic groups? Who ran
  it, and through whom?
- Who owns this? Has legal reviewed the actual position, or just been told about it?
- If a candidate made a subject access request tomorrow, what would you be able to
  produce?

### Evidence to ask for

- The tool inventory annotated with what each does to candidate data.
- Any candidate-facing privacy notice or AI disclosure text.
- Data processing agreements for the tools that touch candidate data.
- Any bias audit, validation study, or vendor documentation of testing.
- The stated human-oversight position, if written down.

### The tell

Question 1 discriminates the whole dimension. The distinction between *tools that help a
human work* and *tools that act on a candidate* is the one that determines exposure, and a
function that cannot draw that line clearly for its own stack is Level 2 at best regardless
of how much policy documentation exists.

A second tell: ask whether they have ever pushed back on a vendor claim. Level 2 functions
have not, because they lack the basis to.

### Fastest single question

> Is any candidate ever rejected, ranked or filtered without a human making that call —
> and where do you hire?

---

## Dimension 6 — Measurement

### What it is

Whether they can tell if any of this worked. Baselines, before/after comparison,
attribution, and the honesty to distinguish a real effect from a coincidence of timing.

Separate dimension because it is uncorrelated with everything else and it is the one that
determines whether the programme survives its second budget cycle. A function that cannot
evidence value will lose the spend to whoever can, regardless of whether the value was real.

The hardest part is attribution, and the model should be honest about it rather than
pretending a clean answer exists. Hiring metrics move for many reasons at once — market
conditions, headcount plan changes, a new hiring manager, seasonality, one difficult req
distorting the average. A time-to-hire drop in the quarter after a tool launched is not
evidence the tool caused it. Level 4 is where the function knows this and designs around
it; Level 3 is where they measure honestly but cannot isolate cause.

### The five levels

**Level 1 — Ad hoc.** No baseline and no measurement. Value is asserted from anecdote and
vendor material. If asked whether a tool is working, the answer is a feeling. Nobody
recorded what things looked like before.

**Level 2 — Experimenting.** Core hiring metrics exist — time to hire, offer acceptance,
source mix — reported periodically, mostly to satisfy a request rather than to make a
decision. No baseline was captured before any tool was introduced. Any claim about AI
impact rests on a before/after comparison assembled retrospectively, or on vendor-reported
usage numbers presented as outcomes. Nobody distinguishes activity metrics (messages sent,
CVs screened) from outcome metrics.

**Level 3 — Operating.** Metrics are defined consistently and trusted. A baseline was
captured before at least one significant change and the comparison was made deliberately.
Activity and outcome metrics are distinguished. Quality signals exist beyond speed —
offer acceptance, early attrition, hiring manager satisfaction, or pass-through rates by
stage. The function can describe what changed after a tool was introduced and is honest
that they cannot fully separate the tool's effect from everything else that moved.

**Level 4 — Integrated.** Measurement is designed into changes before they are made.
Someone decides in advance what would count as success and what would count as failure, and
what the comparison group or comparison period is. Confounds are named rather than ignored.
Quality of hire is measured with something — post-hire performance, manager assessment at
six months, retention — imperfect but consistent. Cost is tracked against outcomes, so tool
spend can be argued in the same terms as headcount spend. Negative results are reported
rather than buried, and at least one tool has been dropped on the evidence.

**Level 5 — Compounding.** Measurement changes behaviour. The function runs deliberate
comparisons — staged rollouts, held-back teams, A/B on process variants where volume allows
— to establish what actually works rather than what appears to. Findings feed back into
process design. Leading indicators are identified and monitored rather than waiting for
lagging outcomes. The function can hold a credible conversation with a CFO about the return
on its tooling, using its own numbers.

### Diagnostic questions

**Ask these three:**

1. Before you introduced your most significant AI tool, what did you write down about
   how things looked at the time?
2. What is your definition of quality of hire, and what do you actually measure for it?
3. If your CFO asked you next week to justify your tooling spend, what would you show
   them, and how comfortable would you be?

**Follow up on:**

- Which metrics do you report, to whom, and how often? Does anyone make a decision on
  them?
- Do you distinguish activity from outcome? Would "CVs screened" ever appear as a result?
- Has any tool ever been dropped because the numbers did not support it?
- What else changed at the same time as your last significant tool launch?
- Do you have anything post-hire — performance, retention, manager satisfaction — that
  links back to how the person was hired?

### Evidence to ask for

- The recurring hiring metrics pack.
- Any before/after analysis done for a tool.
- The definition list for the core metrics — if time to hire is defined differently in two
  places, that is a Dimension 1 finding as well.

### The tell

Question 1: **was a baseline captured before, or reconstructed after?** Reconstructed
baselines are a Level 2 signal, because the reconstruction is always shaped, usually
unconsciously, by the conclusion. Deliberate baselines are Level 3+.

Question 3 is the tell for how the programme will fare politically. Discomfort here, in a
function otherwise scoring 3 and 4, means measurement is the binding constraint.

### Fastest single question

> How would you know if you turned all of it off?

---

## Scoring at the boundary

- **Score down at genuine ambiguity.** If the evidence supports 3 or 4, score 3 and state
  what would move it to 4. A generous score removes the reason to act, and these reports are
  read by people who will act only on a gap they believe in.
- **Weight load-bearing sub-elements.** Dimensions are not checklists to average. Strong
  ATS hygiene with no defined stages is not Level 4 operational, because stages are what
  hygiene is *for*.
- **Score the median, not the best.** The question is what the typical recruiter does, not
  what the strongest one is capable of. Ask explicitly about the median.
- **Self-reported scores stay self-reported.** Where no evidence was seen, say so in the
  report's scope note. It costs nothing and it is why the report will be believed.
- **Not assessed is a legitimate result.** Never guess a dimension the user did not answer
  and never substitute a zero. Mark it Not assessed and note what it would take to close it.

---

## Reading the pattern across dimensions

The shape across dimensions is more informative than any single score. Common patterns:

**Flat 2s across the board.** The most common result. Not a failure — most functions are
here, and the industry conversation runs well ahead of most organisations' reality. The
right response is a small number of deliberate moves, not a transformation programme. Say
this plainly; it is usually a relief and it makes the roadmap credible.

**Tooling 4, capability 2.** Shelfware. They bought capability they cannot use. More tools
makes it strictly worse. The constraint is capability and possibly the absence of an owner.

**Capability 4, operational 2.** Talented people fighting the process. High frustration,
high flight risk among the strongest recruiters, and the AI work will not compound because
there is no clean substrate for it. Fix operations; the capability is already there to
exploit it.

**Everything 3, redesign 2.** The good problem. Foundations hold and the value is
unclaimed. The constraint is that nobody has been given the mandate or the time to redesign
anything, which is usually a leadership decision rather than a capability gap.

**Anything 4, governance 1.** The report leads with this. Not a maturity finding — a risk
finding. Frame in terms of what happens when a candidate, a client audit, or a regulator
asks, and keep the language factual rather than alarmist.

**Everything 3-4, measurement 1-2.** The programme is real but undefendable. It will lose
its budget to a function that can show numbers. This is the argument that moves a CPO, and
it should be made in those terms.

---

## Common false positives

Things that look like maturity and are not. Check each before finalising a score above 2:

- **"We have an AI policy."** A policy nobody has mapped to the actual tool estate is a
  document, not governance. Ask which tools it covers by name.
- **"Our ATS has AI built in."** Vendor capability shipped in a release is not adoption.
  Ask whether it is switched on, who uses it, and what it changed.
- **"We ran a training session."** A demo is not capability development. Ask what people do
  differently in the week after.
- **"We've automated screening."** Usually the same screen, done by a machine, at the same
  point in the process. Automation, not redesign — and a governance question, immediately.
- **"Time to hire came down."** Coincident, not causal, unless something was designed to
  isolate it. Ask what else changed in the same period.
- **"Everyone has a licence."** Licences assigned is not usage. Ask for weekly active
  users; the gap is frequently large and it is the finding.
- **"Our vendor says it's bias-free."** No credible vendor says this. If they did, that is
  itself the finding — ask what testing was done, by whom, on what population.
