# Audit lenses

The seven lenses in depth. For each: what to look for, the diagnostic questions that
surface it, the findings that recur, and the fixes with their trade-offs.

Run all seven. They interact — a long loop is also an expensive loop and a leaky one — but
they produce different recommendations and different arguments, and different people in the
organisation care about different ones. The CFO cares about interviewer load. The hiring
manager cares about quality. The candidate-facing recruiter cares about drop-off. Give each
of them their lens.

## Contents

- [1. Elapsed time](#1-elapsed-time)
- [2. Redundancy](#2-redundancy)
- [3. Assessment validity](#3-assessment-validity)
- [4. Drop-off risk](#4-drop-off-risk)
- [5. Candidate experience](#5-candidate-experience)
- [6. Bias and consistency exposure](#6-bias-and-consistency-exposure)
- [7. Interviewer load](#7-interviewer-load)
- [Reading the lenses together](#reading-the-lenses-together)

---

## 1. Elapsed time

### What to look for

Split the calendar into **time in stage** and **time between stages**, and total both.
Almost every process that feels slow is slow in the gaps, not in the interviews. Five
interviews is five hours of a candidate's life; five weeks of waiting is what makes them
take the other offer.

Map the waiting into its sources, because each has a different fix and a different owner:

| Source of delay | Typical shape | Who owns the fix |
|---|---|---|
| Application sits unreviewed | Days to weeks, invisible to everyone | Recruiter capacity, or automation of the sift |
| Scheduling back-and-forth | Multiple days per stage, compounds across the loop | Recruiter authority and calendar access |
| Feedback not submitted | The most common single blocker | Hiring manager and interviewers |
| Waiting for one person's calendar | Concentrated on a bottleneck interviewer | Panel design, backups |
| Decisions batched to a weekly meeting | Up to a week per occurrence | The decision forum's cadence |
| Offer approval and comp sign-off | Often invisible in the ATS | Finance, HR ops, the exec sponsor |

The offer-approval step deserves a direct question. It frequently lives outside the ATS,
so it does not appear in any report, and it sits at the exact point where a candidate is
most likely to be in another process.

### Diagnostic questions

- Walk me through your last hire for this role, by date. When did they apply, when did they
  first speak to a human, when was each stage, when did they get the offer?
- Between passing a stage and sitting in the next one, how many days? Typical, and worst
  recent case.
- Who has to give feedback before a candidate moves on, and is there a deadline? What
  happens if it is missed?
- Can a recruiter book an interview directly into an interviewer's calendar, or do they
  have to ask?
- Is there a meeting where hiring decisions get made? How often does it run?
- After the final interview, what has to happen before an offer can be verbally extended?

### Common findings

- **The gaps are the majority of the calendar.** Say it as a ratio in the report — hours of
  interviewing across weeks of process is a sentence that changes the conversation.
- **One bottleneck interviewer.** Frequently the hiring manager or a named senior person
  present at every loop. Their calendar sets the pace of all hiring in the team.
- **No feedback deadline exists.** Nobody is late because nothing is due.
- **The weekly decision meeting.** A candidate finishing on a Tuesday waits six days for a
  decision that takes four minutes.
- **Sequential where it could be parallel.** Two independent stages run one after the other
  because that is the pipeline order in the ATS.

### Fixes and trade-offs

**Feedback service levels — a stated deadline, usually 24 or 48 hours, with the candidate
told the same date.** Cheapest and highest-yield fix available. Trade-off: it needs
enforcement, and enforcement means someone senior backing it. Pair it with the interviewer
load number — you are asking for two days of turnaround, not more hours. Telling the
candidate the same date creates useful external pressure.

**Pre-booked interview slots — panel members hold recurring weekly slots for an open req.**
Removes most scheduling latency at once. Trade-off: held time gets wasted when the pipeline
is thin, which interviewers notice and resent. Only apply to actively-hiring reqs and
release slots not used by a stated cut-off.

**Recruiter authority to schedule without asking.** Calendar access plus a standing
agreement that booked time is accepted. Removes a whole round trip per stage. Trade-off:
requires trust and a clear rule about protected time. It is a culture change more than a
process change, and it is usually the highest-leverage thing on this list.

**Batching stages into a single day.** Two or three stages in one block. Compresses days
into hours and candidates generally prefer it. Trade-off: it commits interviewer time
before you know the candidate is worth it, so it works best for later stages and senior
roles; it is harder for candidates who need to take time off, so offer a split alternative.

**Kill the weekly decision meeting as a gate.** Keep the meeting for calibration; let
decisions be made asynchronously against the scorecards as they land. Trade-off: less
group discussion. Mitigate by keeping the forum for split decisions only, which is where
discussion adds value anyway.

**Parallelise independent stages.** Where a stage does not depend on the outcome of
another, run them in the same week. Trade-off: you spend assessment time on candidates who
would have failed the earlier stage. Worth it late in the funnel, wasteful early.

**Pre-clear the offer.** Agree the band and approval route at kick-off, not at offer.
Trade-off: none worth mentioning. This is pure latency removal and it is routinely missed.

---

## 2. Redundancy

### What to look for

Build the coverage grid — competencies down, stages across — and read it for duplication.
This is the most powerful finding the audit produces and usually the easiest to sell,
because nobody has to admit anything was wrong: the stages were added at different times
by different people, and the overlap is a fact rather than an accusation.

Four patterns in the grid:

- **Duplication.** The same competency assessed three or more times, or twice with no
  deliberate second-read rationale.
- **Gaps.** A competency the role fails on that no stage assesses.
- **Empty columns.** A stage assessing nothing nameable. It is selling, or it is a veto.
- **Overloaded columns.** Four competencies in one 45-minute conversation.

The specific duplications that recur:

| Duplication | What is actually happening |
|---|---|
| Recruiter screen and hiring manager screen both do motivation and CV walkthrough | The manager does not trust or does not read the recruiter's notes |
| Two technical stages both assessing core craft | One was added for depth and neither was re-scoped |
| Panel and hiring manager both assessing collaboration | Nobody assigned competencies to the panel |
| Presentation and work sample both assessing the same analytical skill | Two stages of one assessment, at double the candidate cost |
| Every stage assessing motivation | Everyone asks "why us?" because it is an easy opener |

### Diagnostic questions

- For each stage: what does this assess that no other stage assesses?
- Where two stages cover the same ground: has anyone ever passed one and failed the other?
  If not, the second is confirming the first, which is not an assessment.
- Does the hiring manager read the recruiter's screen notes before their own interview?
- Who assigned competencies to the panel? Do panel members know which is theirs?
- What question does every interviewer ask?

### Common findings

- **Motivation assessed four times, level and scope assessed never.** The most common
  finding in the whole audit.
- **The second technical stage confirms the first.** Almost nobody has an example of a
  candidate who passed one and failed the other, which is the tell.
- **The panel duplicates everything and owns nothing**, because it was designed as "meet
  the team" and drifted into an assessment.

### Fixes and trade-offs

**Delete the duplicate stage.** The strongest recommendation available, and the hardest
conversation. Always pair it with where the competency now lives.

**Re-scope rather than delete.** Where the stage has a defender or genuine political
weight, keep it and give it a narrower, exclusive brief. A second technical stage that goes
from "assess engineering ability" to "assess system design at scale, which the first stage
cannot reach" is now earning its place. Trade-off: you keep the elapsed time and the
interviewer cost. Take this route when deletion is unwinnable, not as the default.

**Merge two stages into one longer one.** Two 45-minute conversations become one 60-minute
one with two competencies. Saves a scheduling round trip and candidate context-switching.
Trade-off: you lose the second independent reader, so only merge where the same person
could credibly assess both.

**Keep a deliberate second read on the one or two competencies that decide the hire.** Not
all duplication is waste. State in the report which duplication is intentional so the
recommendation does not read as mechanical.

---

## 3. Assessment validity

### What to look for

Whether stages assess things that predict performance in this role, or things that are easy
to assess. Ease and validity are almost inversely related: general impressiveness, warmth,
confidence and fluency are effortless to judge and mostly measure presentation skill.

The structural test for any stage: **would two different assessors, seeing the same
candidate, reach the same conclusion for the same reasons?** If not, the stage is producing
noise that later gets treated as signal.

The four low-validity stages to name when found:

- **The unstructured culture-fit chat.** Unanchored, so it rewards similarity to the
  interviewer, and it carries decisive weight because "I just didn't feel it" is hard to
  overturn. If the team needs specific behaviours, those are competencies with evidence
  standards. If it cannot be defined well enough to anchor, it is not assessable.
- **The CV walkthrough that repeats the screen.** Chronology is not assessment. The
  candidate narrates a document everyone has read, and the interviewer forms an impression
  from delivery.
- **The panel with no assigned competencies.** Four people assessing general
  impressiveness, then agreeing with each other, and the agreement being mistaken for
  reliability. Independent readers only add signal when they are reading different things
  and scoring before they speak.
- **The final chat with a founder or exec.** Functions as a veto with no criteria and no
  scorecard, at the point of maximum sunk cost for everyone. Often the deciding stage in
  the whole process and the only one with nothing written down.

Then check the positive side: is anything in the loop actually observing the work? A
well-designed work sample beats any conversation because it observes the work rather than
the candidate's account of it. A loop of five conversations and no work observation is
assessing the ability to describe work.

### Diagnostic questions

- What does a candidate have to do to fail this stage? If nobody can answer, it is not a
  filter.
- When did this stage last reject someone who had passed everything before it? What was
  the reason given?
- Is there a scorecard? Is it filled in before the debrief or after?
- Does anyone in this loop see the candidate do work resembling the job?
- Which stage do people trust most when they disagree? Is that the stage with the most
  structure, or the most senior person?
- What was the last bad hire, and which stage should have caught them? Would it have?

### Common findings

- **The most trusted stage is the least structured one**, and it is trusted because a
  senior person runs it.
- **The stage added after a bad hire would not have caught that hire.** Ask directly. It
  is the strongest single argument for removing a stage that exists as a scar.
- **No work sample anywhere**, in a role with an entirely observable output.
- **Scorecards filled in after the debrief**, which means they record the group decision
  rather than independent evidence.

### Fixes and trade-offs

**Structure the stage rather than removing it.** Assigned competencies, a common question
set, anchored scales, scorecards before the debrief. Converts a low-validity stage into a
useful one without a political fight. Trade-off: it needs writing and a small amount of
interviewer training — `interview-kit-builder` does the writing.

**Replace a conversation with a work sample.** The highest-value substitution in most
loops. Trade-off: design cost, assessor time, and the candidate-cost issues covered under
drop-off. Prefer a live 60-minute working session over a take-home where the role allows.

**Convert a veto into an assessed stage.** For the founder or exec final: name one or two
competencies only they can assess (usually strategic judgement, or a genuine read on
mission), give them the same scorecard, and move the stage earlier so it does not sit at
the end. Trade-off: exec time earlier in the funnel, on more candidates. Cap it by making
the stage short.

**Kill the CV walkthrough and give the time to a competency.** Cheap, and no one defends
the walkthrough once it is named.

---

## 4. Drop-off risk

### What to look for

Where candidates leave of their own accord. Split every stage transition into
**company-rejected** and **candidate-withdrawn**. Rejections are the process working;
withdrawals are the process failing. A single conversion rate hides the difference and is
the reason most funnel reports are useless for this purpose.

The structural drop-off causes, in rough order of how often they are the culprit:

- **Silence.** Days of no contact after a stage. The candidate assumes rejection and
  re-engages elsewhere. The cheapest thing on this list to fix and the most commonly
  neglected.
- **An unpaid, long take-home.** Multi-hour exercises with a vague brief filter hardest on
  the candidates with the least free time — those with caring responsibilities, those
  already in demanding jobs — which is close to the opposite of the intended filter.
- **Too many stages before any real information about the job.** Comp, scope, team, the
  actual problems. Candidates withdraw at stage two because they still do not know whether
  they want it.
- **Scheduling burden.** Five separate appointments, each needing time off, each negotiated
  over email.
- **A junior-feeling assessment given to a senior candidate.** A director asked to do a
  timed coding test or a generic case study reads it as a signal about the organisation and
  leaves. This is the single most common source of senior withdrawal.
- **Repetition.** Being asked the same question by the fourth interviewer tells the
  candidate the organisation does not talk to itself.
- **Late-breaking bad news.** Comp discussed at offer, on-site expectations at stage four.

### Diagnostic questions

- Where do people withdraw, and does the ATS distinguish withdrawal from rejection?
- What is the longest unpaid task you ask for, and what is the stated time budget? What
  does it actually take?
- At what point does a candidate learn the salary range? The working pattern? The team?
- Has anyone read the exercise brief recently and timed themselves doing it?
- Do senior candidates get the same loop as everyone else? Have any pushed back on a stage?
- What do declining candidates say when asked why?

### Common findings

- **Withdrawal clusters right after the largest unpaid ask**, and everyone had assumed it
  was a quality filter.
- **Nobody tracks the split**, so the drop-off is invisible.
- **Comp arrives too late.** A process that runs four stages before the range surfaces is
  spending everyone's time on a conversation that may be impossible.
- **Silence between the final interview and the offer** is where the strongest candidates
  are lost, because they are the ones with a competing process.

### Fixes and trade-offs

**Contact within a stated window, always, including rejections.** Trade-off: recruiter
time, largely solved by templates and an ATS trigger.

**Time-box the exercise, state the box, and assess only what fits in it.** Say it in the
brief: "this should take 90 minutes; we assess what you produce in that time; do not spend
longer." Trade-off: less to assess. That is the point — you are removing the free-time
advantage.

**Move to a live working session.** Same signal, lower candidate cost, and you see the
reasoning. Trade-off: assessor time.

**Pay for anything long.** Trade-off: budget and administration, and it does not scale to
high volume. Where budget will not stretch, shorten the exercise instead.

**Front-load the honest information.** Range, working pattern, team shape, and the real
problems of the job, at the first conversation. Trade-off: some candidates leave earlier.
That is a saving, not a loss.

**Scale the loop to the level.** Senior candidates get a shorter loop with more senior
assessors and a discussion-based assessment rather than a test. Trade-off: consistency —
which is fine as long as the loop is consistent *within* a role, defined in advance, and
not varied candidate by candidate. Varying by level is a design decision; varying by
individual is a risk.

---

## 5. Candidate experience

### What to look for

What the candidate is told, when, and by whom — and what they get out of the process even
if they do not get the job. This lens is often dismissed as soft; treat it as a conversion
problem, because that is what it is. Every candidate is also a customer, a referrer, and a
future applicant.

Trace the journey and note every point where the candidate is left to guess:

- **On application.** Confirmation, an honest indication of timeline, and what happens next.
- **Before each stage.** Who they will meet, their role, the format, the duration, what is
  being assessed, and how to prepare. Telling a candidate what a stage assesses improves
  what you learn — you are testing capability, not their ability to guess the format.
- **Adjustments.** Offered proactively to everyone, with a route that does not require
  disclosing a diagnosis.
- **Between stages.** A named next contact date, and contact on that date even if the news
  is "no news yet".
- **On rejection.** Which stage, how fast, and whether anything is said beyond the
  template. Late-stage rejections deserve a call and specific feedback.
- **On offer.** How fast, by whom, and whether the verbal precedes the paperwork.

### Diagnostic questions

- What does a candidate receive before each stage? Ask to see it.
- Are candidates told what each stage assesses?
- Who tells a candidate they have been rejected, and how long after the decision?
- Does anyone at final stage get a call rather than an email?
- Is an adjustment offer made to every candidate, or only when asked?
- If a candidate asked "what happens next and when", could the recruiter answer precisely?

### Common findings

- **Preparation material stops after the first stage.** The screen has a well-crafted
  email; nothing after it does.
- **Rejection at late stages is a template.** Someone gave you six hours and got three
  sentences. This is where employer reputation is actually made.
- **Adjustments only on request**, which means the candidates least comfortable asking do
  not get them.
- **Nobody owns the silence.** The recruiter is waiting on feedback, so the candidate hears
  nothing, and no one thinks of that as a decision.

### Fixes and trade-offs

**A stage-by-stage candidate communication map** — one document defining what goes out
before and after every stage, who sends it, and when. Trade-off: an afternoon to write.
This is the highest-return fix in the lens.

**Tell candidates what each stage assesses.** Free, and it improves signal quality.

**A five-minute call for every final-stage rejection**, with specific, evidence-based
feedback drawn from the scorecards. Trade-off: recruiter time, and a small amount of risk
if feedback is careless — so give evidence about the role's requirements, never
characteristics, and keep it to what is written in the scorecards.

**Proactive adjustment offer at first contact and again before any assessment**, phrased so
no diagnosis is needed. Trade-off: none.

**Give something back.** A named benchmark against the level framework, an introduction, an
honest read on what would make them a yes next time. Trade-off: time, and only worth doing
for late-stage candidates.

---

## 6. Bias and consistency exposure

### What to look for

This lens is where quality and legal exposure are the same problem. An unstructured stage
is both the least predictive and the least defensible.

- **Unstructured stages carrying decisive weight.** No question set, no anchors, no
  scorecard — and yet the stage everyone defers to.
- **Sequences varying between candidates for the same role.** A referral skipping the
  screen, an internal candidate meeting a different panel, a candidate with a strong
  advocate skipping a stage. Different processes cannot be compared, and the variation is
  hard to defend.
- **Interviewer sets varying between candidates.** Different assessors applying different
  private bars.
- **Unrecorded criteria.** Any stage that can reject without written criteria and a recorded
  reason.
- **Unaccommodated processes.** No adjustment route, no alternative format for a timed
  assessment, video-only formats with no alternative.
- **Assessment content that measures exposure rather than capability.** Brainteasers,
  culture-coded questions, hobby and school talk, and "would I have a drink with them"
  framings. Also the proxies that stand in for protected characteristics: graduation year,
  career gaps treated as a red flag, accent, "polish".
- **Debrief order.** The most senior voice speaking first collapses everyone else's
  independent read into theirs.

### Diagnostic questions

- Does every candidate for this role go through the same stages, in the same order, with the
  same interviewer roles? What are the exceptions and who authorises them?
- Which stage can reject a candidate with no written record of why?
- Is there a scorecard for every stage? Submitted before the debrief?
- Who speaks first in a debrief?
- Is an adjustment route offered to everyone, and is there an alternative to the timed
  exercise?
- Have interviewers had any structured-interview training? Who has interviewed most, and
  who has never been trained?
- Does anyone look at pass-through rates by stage across groups?

### Common findings

- **The highest-weight stage has the least structure**, which is the finding to lead with.
- **Referrals get a different process.** Universal, rarely written down, and a clean
  consistency problem.
- **Nobody has ever looked at pass-through by stage across groups**, so if a stage is
  filtering unevenly, no one would know.
- **Scorecards exist for the technical stage only.**

### Fixes and trade-offs

**A defined stage sequence per role, with exceptions defined in advance rather than
improvised.** If referrals genuinely skip the screen, write that down as a rule applying to
all referrals, with a stated reason. A written exception applied consistently is a policy;
an improvised one is a risk.

**Scorecards with written criteria at every stage that can reject.** Trade-off: interviewer
effort, which the feedback service level should absorb.

**Scorecards submitted before the debrief, and the most junior person speaking first.**
Free, and it protects the independence that makes multiple interviewers worth having.

**Proactive adjustments and an alternative format for every assessment**, assessed against
the same criteria.

**Monitor pass-through by stage.** Where numbers are large enough to be meaningful, look at
stage conversion across groups to find where a filter behaves unevenly. Trade-off: it needs
data the ATS may not hold well, and it should normally be run through counsel — in several
jurisdictions the analysis is more protected that way, and the findings are sensitive.
This surfaces where to investigate; it is not a legal adverse-impact determination.

---

## 7. Interviewer load

### What to look for

Total interviewer hours per hire. Nobody counts it, it is a real and large cost, and it is
frequently the argument that unlocks change with an engineering or sales leader who is
defending the loop on quality grounds. Someone who will not lose a stage for candidate
experience will often lose it for three engineering weeks back.

Compute it from the user's own numbers, never from a benchmark:

1. For each stage, **interviewer hours per candidate** = (number of interviewers) ×
   (scheduled duration + preparation + scorecard writing). Use 15–30 minutes of overhead per
   interviewer per stage unless the user has a better figure, and label it as an assumption.
   Debrief time counts too: a 30-minute debrief with four people is two hours.
2. Multiply by **candidates reaching that stage per hire** — from their funnel data, or
   from their own estimate.
3. Sum across stages for **hours per hire**.
4. Multiply by planned hires for the **annual load**, and express it in whatever unit lands
   with the audience: engineer-weeks, a proportion of a team's capacity, or fully-loaded
   cost if the user wants a money figure and can supply an hourly rate. Do not invent a
   rate.

Also look at the distribution, not just the total. Load usually concentrates on a handful
of people — a bottleneck interviewer appearing in every loop is simultaneously the elapsed
time problem, the consistency problem and a burnout risk.

### Diagnostic questions

- How many interviewers are in each stage, and how long is each scheduled for?
- Is there a debrief? Who attends and how long does it run?
- How many candidates reach each stage per hire?
- Who does the most interviews? How many hours a week is that at peak?
- Has anyone declined to interview, or given late feedback because of load?
- How many hires are planned in this family over the next year?

### Common findings

- **The number is much larger than anyone expected**, particularly once panels, debriefs and
  preparation are included.
- **A four-person panel is the largest single line item**, and usually the least structured
  stage.
- **Load is concentrated on two or three people**, who are also the ones giving late
  feedback — which reframes the feedback problem as a capacity problem with a structural
  fix.
- **Nobody has ever seen this number**, which is why the loop kept growing.

### Fixes and trade-offs

**Shrink the panel.** Four interviewers to two, each with assigned competencies and a
scorecard. Halves the cost of the most expensive stage. Trade-off: fewer perspectives —
answered by pointing out that unassigned perspectives were correlated and added little.

**Move expensive stages later.** Have the cheap filters do more work. Trade-off: more weight
on the early stages, so they need to be good.

**Widen the interviewer pool with training.** Reduces concentration and the bottleneck.
Trade-off: real training cost, and consistency risk until the kit is in place.

**Cut candidates reaching expensive stages by tightening earlier ones.** Often the largest
single lever, because load scales with the number of candidates as well as the number of
stages.

**Reuse the numbers in the redesign.** Show hours per hire before and after. It is the most
persuasive line in the report for an operational audience.

---

## Reading the lenses together

Three combinations that recur and change the recommendation:

- **Long elapsed time plus low interviewer load** means the problem is latency, not volume.
  Fix the operating discipline — service levels, scheduling authority, decision cadence —
  and leave the stage count alone. This is the case where the easy recommendation is also
  the right one.
- **High interviewer load plus high redundancy** means stages come out. The coverage grid
  is the argument and the load number is the motivation. Lead with the grid, close with the
  hours.
- **Good structure plus high drop-off** means the problem is not assessment at all: it is
  communication, candidate cost, or the loop being wrong for the level. Do not recommend
  more structure; recommend information, speed and a right-sized loop.

Where lenses conflict, say so rather than smoothing it over. Adding a work sample improves
validity and increases candidate cost; a shorter loop is faster and gives fewer independent
reads. State the trade-off, make a recommendation, and give the reason. A report that
pretends every change is free is one a senior reader stops trusting.
