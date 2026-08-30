---
name: engagement-survey-action-plan
description: Turns engagement survey results into a prioritised, owned action plan and the communication that goes back to employees — response-rate and distribution reading, segment cuts with minimum group sizes, anonymised free-text themes, driver identification, three to five owned organisation-level actions, the manager cascade, and the "what we heard, what we're doing, what we're not doing" message. Use when someone says "the survey results are back", "we've got our Culture Amp / Peakon / Glint / Qualtrics results", "engagement is down", "eNPS dropped", "I need to present the survey to the exec team", "what do we actually do with these results", "we need an action plan from the survey", "the response rate fell", "we ran a survey last year and nothing happened", "how do I brief managers on their team scores", or is preparing a results readout, a manager cascade, or an all-hands message about survey findings. Also use for exit-survey and pulse-survey result sets treated the same way. For new-hire feedback use onboarding-plan-audit; for building the performance rating process, use performance-calibration-pack; for arguing for headcount to resource an action, use headcount-business-case.
---

# Engagement survey action plan

Produces what the survey was supposed to produce: a short list of owned, dated, visible
actions, a manager cascade that survives contact with a manager whose scores are bad, and an
employee communication that says what will change, what will not, and why.

The survey is not the intervention. Most organisations run one, build a results deck, present
it to the exec team, and then do nothing employees can see. Employees notice, and the following
year both the response rate and the honesty of the answers fall — the instrument degrades at
the moment it is most needed. The failure is almost never analytical; results decks are usually
fine. It is that results are never converted into a small number of owned, resourced, visible
actions. This skill is about that conversion; the analysis exists to make it honest.

## What you need to start

Ask what they have, in one message, offering the realistic options rather than a specification:
a platform export (CSV or XLSX from Culture Amp, Peakon, Glint, Qualtrics, Workday, Officevibe,
Lattice or anything else — the best case); a PDF results pack; a spreadsheet someone built by
hand; headline scores pasted into the chat; or nothing yet because the survey closes next week.

**Any of these is enough to start.** Where the environment supports structured multiple-choice
questions, use them here and for the minimum-group-size policy — they are picks, not essays.

Three things worth asking alongside the data, because they change the analysis rather than
decorate it:

1. **The response rate this cycle and last**, and the headcount it is a percentage of. A
   falling response rate outranks every score in the file.
2. **What was promised to respondents about confidentiality**, and the organisation's minimum
   group size for reporting. This is a constraint on the output, not a preference.
3. **Which outcome the organisation actually cares about** — usually intent to stay,
   discretionary effort, or eNPS. Drivers are only meaningful against a named outcome.

If they have only headline scores, go to *The degraded case* below and produce the full plan
anyway. A plan built on headline scores that the user sharpens next week beats a perfect
analysis they never got to.

## Process

### 1. Read the response rate before reading a single score

The response rate determines what every other number in the file means, and it is the one
finding meaningful entirely on its own.

- **A falling response rate is the most important finding in the survey**, ahead of any score
  movement. It usually means people concluded that last cycle changed nothing, or that they no
  longer believe the confidentiality commitment — both more serious than a two-point drop on
  wellbeing, and neither fixed by an action plan aimed at the low scores.
- **A skewed response rate changes the interpretation of every segment.** If engineering
  responded at 40% and commercial at 85%, the company score is mostly commercial's opinion.
  Say so rather than reporting a company number as though it were one.
- **Low response with high scores is the trap.** The disengaged are the least likely to
  answer, so low response biases scores upward: a good score on a 45% response is not a good
  result, it is an unknown result with a flattering sample.

`references/analysis-method.md` covers response rate by segment, what counts as a material
change, and how to state confidence limits without overclaiming or dismissing the data.

### 2. Compare to the previous cycle honestly

Score movement is only interpretable if the population is comparable. Establish what changed
between cycles — restructure, acquisition, a large intake of joiners, redundancies, a
return-to-office mandate, a leadership change, a pay freeze — and check two mechanical
effects routinely mistaken for real movement. **Population change:** if half the low-scoring
population left, or the company doubled with new joiners who typically score higher in their
first months, scores rise without anything improving; where the data allows, compare only the
population present in both cycles and say you have. **Instrument change:** a reworded item, a
changed scale, a moved benchmark or a new vendor invalidates the comparison — say it cannot
be made rather than making it with a caveat nobody reads.

External comparison, if they have it: use the group the user actually has, and name it. Never
generate a benchmark, an industry average or a "typical" score — a fabricated comparator
repeated to a board is a career risk for the user and destroys the credibility of the pack.

### 3. Read the distribution, not only the mean

The step most results decks skip, and it changes the response more than any other. A mean of 6
made of 3s and 9s is a different organisation from one made entirely of 6s: the first is
polarised, two populations having different experiences of the same company, and the action is
to find who is in each group and why; the second is uniformly mediocre and the action is
systemic. Same mean, opposite interventions. For every item that matters look at the shape —
the bottom of the scale, whether it is bimodal, whether an improved mean is a shrinking tail or
a growing top. `references/analysis-method.md` gives the specific reads.

### 4. Cut by segment — this is where the actionable findings are

Company-level engagement scores are almost never actionable, because the company is not where
the experience happens. Cut by function and team; by level or grade, and manager versus
individual contributor; by tenure band (under 6 months, 6–24 months, 2–5 years, 5+ years); by
location, and office versus remote versus hybrid; and by any demographic dimension the
organisation lawfully monitors, under the guardrails below. Cut the **manager population as
its own segment** too: managers are both the biggest lever on everyone else's engagement and
frequently the most strained group in the data, and their scores are a leading indicator for
their teams' next cycle.

**The minimum group size is non-negotiable, and here is why.** No segment is reported below
the organisation's stated minimum — commonly in the 5–10 range; ask what theirs is, and apply
5 as a floor if they have no policy. Below that threshold results deanonymise respondents: a
team of four where "one person disagreed" is four people who each know the other three. One
instance of someone being identified — or believing they were — breaks the confidentiality
commitment permanently, and the next survey then measures who is willing to be honest rather
than what people think. Apply it to every cut, including cross-cuts, where it is most often
breached: "women in engineering at director level" can be two people even when each dimension
clears the threshold alone. Suppress the cell, and suppress enough neighbouring cells that it
cannot be derived by subtraction from the total.

### 5. Analyse the free text as themes, never as individual accounts

Read `references/free-text-analysis.md` in full before touching comments — theme extraction,
frequency versus intensity, quote selection, and the escalation protocol. Three rules govern
everything:

- **Report at theme level with frequency and intensity, illustrated by quotes that cannot
  identify anyone.** Paraphrase, or select only quotes containing no role, no event, no team
  detail and no circumstance that would let a colleague identify the writer. A quote reading
  "as the only [role] in [team], I…" is not usable at any level of the organisation, however
  well it makes the point.
- **Comments routinely contain health information, disclosures about personal circumstances,
  and complaints about named individuals.** Report these at theme level only — "several comments
  described workload affecting health" — never at individual level, never with the detail, never
  with a quote, and never naming an individual who is complained about.
- **Anything that appears to disclose harm, harassment, discrimination, bullying, retaliation,
  a safeguarding concern, or a risk to someone's safety goes to the user privately and
  immediately, separately from the analysis, so it can be routed to the proper internal
  channel.** Flag it in the conversation, not in the deck, the action plan or any circulated
  file. Say what channel it likely belongs in — the whistleblowing or speak-up route, employee
  relations, legal, or safeguarding — and stop there. Summarising a disclosure of harm as a
  theme buries it; putting it in a circulating document exposes the person who wrote it.

### 6. Find the drivers, not just the low scores

The lowest-scoring item is not automatically the most important one. Prioritise on what moves
the outcome the organisation cares about — usually intent to stay or discretionary effort —
not on rank order of score. Two filters decide what reaches the plan:

**Impact.** How connected is this item to the stated outcome? If the platform supplies a driver
analysis, use it and say what it is based on. If not, compare how the item scores among people
answering unfavourably on the outcome against those answering favourably — crude, usually
directionally right, and honest about being crude. `references/analysis-method.md` sets out how
to do this with the data most users have.

**Agency.** Can this organisation actually change this in the next two quarters? A low score on
office location for a company on a seven-year lease, on pay in a business that has just frozen
salaries, or on a market-driven equity valuation, is real — but it is not an action-plan item.
It is a communication problem, and belongs in the "what we are not changing and why" section
of the employee message, where it does far more good.

Be honest about this rather than tactful. An unfixable item on the plan produces a workstream
that quietly dies and confirms to employees that the survey changes nothing; naming it as
something the company will not change, with the real reason, is more credible and costs less.

### 7. Convert to three to five organisation-level actions, and no more

A plan with fifteen actions has none. Three to five is roughly what an executive team can hold
attention on for two quarters. Every action carries, without exception:

- **A named owner** — an individual, at a level with the authority to actually do it, not a
  function and not a committee. "People team" is not an owner.
- **A defined outcome** — what will be different, stated so someone can tell in six months
  whether it happened. "Improve communication" is not an outcome. "Every team has a written
  quarterly priority list their manager reviewed with them" is.
- **A date**, with a first visible milestone inside about six weeks. The first milestone matters
  more than the end date, because it is what employees see.
- **How employees will see it happening.** If nobody outside the exec team can tell the action
  is underway, it does not count as an action here — this is the field that most often exposes
  an action as an intention.

Choose the mix deliberately and include at least one of each: an action that fixes something
small and visible quickly does more for trust in the survey than three structural programmes
landing next year.

### 8. Separate organisation-level actions from team-level ones — and weight them correctly

Most of what drives engagement is local: the relationship with the immediate manager, workload
and its predictability, clarity about the job and what good looks like, whether contribution
is recognised. Almost none of that is fixed by a central programme — and central programmes
routinely get built to address it anyway, because the centre is who reads the results.

State the split explicitly: organisation-level actions only where the fix is genuinely
structural — pay architecture, career framework, tooling, a broken process, a policy — and
team-level action owned by managers everywhere else. Then resource the manager side properly,
because it is doing most of the work. Where an action needs headcount or budget to be real, say
so rather than letting it start under-resourced; `headcount-business-case` builds that argument
if the resourcing needs approval.

### 9. Build the manager cascade

The cascade is where most survey follow-through collapses, so specify it rather than assuming
managers work it out. Fill `assets/manager-cascade-template.md`.

**What each manager receives:** their team's results where the group clears the minimum size,
the company results, the comparison, their free-text themes if group size permits, and the
organisation-level actions with owners. Below the threshold they receive the next level up,
with the reason stated in a way they can repeat to their team without sounding like
concealment.

**What they are expected to do, and by when:** share the results, hold a conversation, agree
one or two team-level actions, record them where the People team can see. One or two, not
five — the organisation-level constraint scaled down.

**A structure for the conversation**, because "discuss your results with your team" is where
cascades die. Thank people for responding; share the actual scores including the uncomfortable
ones; say what you notice; ask what is behind it and then stop talking; ask what one change
would make the biggest difference; commit to one or two things you control; say what you will
take upward. The template carries the full version.

**The manager whose own scores are poor.** This is the conversation that decides whether the
cascade works. What to tell that manager:

- Their scores are information about the team's experience, not a verdict on them. A low score
  for a manager who has just delivered a restructure or absorbed two teams is often a measure
  of the situation rather than the person.
- They still hold the conversation. A manager who hides the results confirms everything the
  results said, and the team already knows roughly what they were.
- They do not defend, explain away, or ask who said what. Asking who said what is the single
  most damaging thing a manager can do with survey results, and it should be said to every
  manager in those terms.
- They do not do it alone: their own manager or a People partner helps them prepare and, in the
  worst cases, attends. Support is offered before results land, not after it goes badly.
- Where scores indicate something more serious than a hard year — a pattern across cycles, or
  comments describing behaviour rather than circumstances — that is a performance and possibly
  an employee-relations conversation, held separately by the manager's own manager and never
  conducted through the survey process.

### 10. Write the employee communication

Four parts, in this order. Fill the section in `assets/action-plan-template.md`.

1. **What we heard** — including the bad parts, in recognisable language. Employees have a
   good collective sense of what they said; a summary that softens it tells them the results
   were managed, and everything after that paragraph is discounted.
2. **What we are doing** — the three to five actions, with names and dates. An action with a
   person's name against it is a commitment; one owned by "the People team" is an aspiration.
3. **What we are not doing, and why.** The part organisations cut, and the part that buys the
   credibility. Naming honestly that pay bands will not be reopened this year because of the
   budget position, or that the office is not moving because of the lease, is more trusted
   than a list of warm commitments — it proves the results were read and that the answers are
   not all comfortable. Employees can live with a no; what they cannot live with is silence
   after raising something, which they correctly read as being ignored.
4. **When you will hear more** — a specific date on which something is actually said, even if
   the update is that a workstream slipped. A missed update date does more damage than no
   update commitment.

Keep it short and get it out fast: a plain message within two or three weeks of close beats a
designed deck six weeks later. The gap between close and first communication is itself a
signal employees read.

### 11. Set the follow-through cadence before anything is communicated

Decide and write down: who reviews action progress and how often (monthly is usual, with the
owner reporting, not the People team reporting on their behalf); whether pulse surveys are used
and on what — pulse only what is being acted on, and only if results will be shared, because a
pulse that disappears repeats the original failure at higher frequency; and the point before
the next full cycle where the loop is closed publicly against the original commitments, item by
item, including those not delivered. That closing message determines next year's response rate:
schedule it now, with an owner.

### The degraded case: headline scores only

With only company-level scores — no segment cuts, no free text, no previous cycle — do not stop
and do not hedge the whole output. Produce the prioritisation framework applied to whatever
items exist, saying plainly that impact is estimated rather than measured; the action plan
structure with owners and dates for the user to confirm; and the manager cascade and employee
communication in full, since neither depends much on analytical depth. Carry a labelled block
at the top listing what is missing and what it would change.

Then name what to obtain, in priority order: segment cuts by function, level and tenure first,
because the actionable finding is almost always inside a segment and a company-level plan built
without them will aim at the wrong problem; then the free text, which explains the scores; then
the previous cycle, for direction of travel. Most platforms export all three and it is usually
a twenty-minute request rather than a project — say so, because users assume otherwise.

## Output

Write a Markdown file to disk using `assets/action-plan-template.md` as the skeleton:

1. **Headline** — three or four sentences an exec team can read alone: response rate and what
   it means, the findings that matter, the actions proposed.
2. **Reading the data** — response rate and skew, comparability, population change, confidence.
3. **What the scores say** — including distribution, not only means.
4. **Segment findings** — suppressed cells marked as suppressed, with the reason stated.
5. **Free-text themes** — frequency, intensity, anonymised illustration.
6. **Drivers and priorities** — impact against agency, unfixable items named as communication.
7. **The action plan** — three to five, each with owner, outcome, date, visibility.
8. **Team-level action**, then the **manager cascade** — what managers own and why it is the
   larger half; then the pack and the cascade timetable.
9. **Employee communication** — draft, ready to send.
10. **Follow-through cadence** — reviews, pulses, and the dated close-the-loop message.
11. **Assumptions and gaps** — what was assumed, what is missing, what would change.

Then offer, without building unprompted: a slide version for the exec or board readout, a
one-page manager card, a spreadsheet for action tracking, or a shareable page for the manager
population. Ask who the audience is; the answer usually decides.

## Data, confidentiality and legal

Survey data is personal data even when it carries no names, and free-text comments frequently
contain special-category data — health, disability, religion, sexual orientation, union
membership, race. Handle accordingly.

- **Work from exports without names or employee IDs where the analysis does not require them.**
  It reduces exposure and is no loss: every finding worth acting on is a group finding.
- **The confidentiality commitment made at survey time is binding on this analysis.** If
  respondents were told results would only be reported in groups of five or more, that promise
  governs the output regardless of what an executive asks for afterwards. The answer to a
  request for a smaller cut is the threshold and the reason, not the cut with a caveat.
- **Never attempt to identify an individual respondent, and do not assist an attempt** —
  including triangulating across segments, matching a comment to a known situation, and
  informal "we all know who wrote that". A comment identifiable on its face is handled under
  the escalation protocol, not in the analysis.
- **Report health, disability, family circumstances and protected characteristics at theme
  level only**, never as an inference about a named or inferable person.
- **Anything suggesting discrimination, harassment, bullying, retaliation or risk of harm goes
  to the proper internal channel and usually to legal — not into an analysis document.** Route
  it, note privately that it was routed and to whom, and keep it out of every circulated file.
  Where a pattern rather than an incident appears — a segment reporting materially worse
  treatment — investigate through the right channel and run the analysis at counsel's
  direction, which in several jurisdictions attracts privilege a spreadsheet does not.
- **Ask which jurisdictions are in scope** on a multi-country survey. Works councils and
  employee representative bodies in several European jurisdictions have consultation or
  information rights over surveying and how results are used, rules on profiling and monitoring
  differ, and some countries constrain what demographic data may lawfully be collected at all.
- **Retention.** Say how long the raw comment file is kept and who can access it. Free-text
  exports live on laptops and shared drives for years — a data risk, and once known, the end
  of honest answers.

This is structural guidance, not legal advice. Where results feed decisions about individuals —
a manager's performance, a team's restructure — get that reviewed before it is actioned: survey
results are not a performance instrument, and using them as one is unsound and teaches a
population to answer strategically.

## Reference files

- **`references/analysis-method.md`** — read before interpreting any numbers. Response-rate
  interpretation and skew, distribution reads, segment cuts and minimum group sizes including
  cross-cut and subtraction risks, driver identification with and without a platform driver
  analysis, and honest year-on-year comparison including a changed population.
- **`references/free-text-analysis.md`** — read in full before touching comments. Theme
  extraction, frequency versus intensity, anonymisation and quote-selection rules, and the
  escalation protocol for disclosures of harm, harassment, discrimination or safeguarding.
- **`assets/action-plan-template.md`** — the output skeleton. Fill it; do not restructure it.
- **`assets/manager-cascade-template.md`** — the manager pack, extractable and sendable as is.

---

*Part of the [Claude Skills for TA and People Teams](https://github.com/we-are-move/claude-skills-for-ta-and-people-teams) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
