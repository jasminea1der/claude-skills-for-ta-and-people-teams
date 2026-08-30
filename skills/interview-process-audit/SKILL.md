---
name: interview-process-audit
description: Audits an existing end-to-end interview process and produces a findings report with a redesigned loop — elapsed-time breakdown, competency coverage grid showing which stages are redundant, assessment validity review, drop-off risk, candidate experience, bias exposure, and total interviewer hours per hire. Use when someone says "our process takes too long", "we keep losing candidates to faster competitors", "we have too many interview stages", "candidates are dropping out", "the team is drowning in interviews", "do we still need the take-home?", "our loop has seven stages and nobody knows why", "time to hire is up", "the founder wants to meet every candidate", "we added a stage after that bad hire", or asks whether a stage can be cut, how long a loop should be, or why offers keep getting declined. Also use for a hiring process health check, an interview process review, or before a TA operating-model change. For designing the questions, scorecards and competencies for one specific role, use interview-kit-builder; for the hiring manager kick-off conversation, use hiring-manager-intake.
---

# Interview Process Audit

Takes a hiring process as it actually runs and produces a findings report with a redesigned
loop: where the calendar time goes, which stages assess the same thing twice, which stages
assess nothing that predicts performance, where candidates leave, what it costs the
interviewing team, and what the process should look like instead.

Interview loops accrete. A stage gets added after one bad hire and never removed. The
result is a process nobody designed, that takes weeks, exhausts the interviewing team,
loses the best candidates to whoever moved faster, and still does not assess the things the
role will fail on. Nobody audits the whole thing because no single person owns the whole
thing.

The output has to survive a conversation where a senior leader defends the stage you want
to delete. Write it accordingly: every recommendation carries the reasoning and the
evidence, not just the verdict.

## What you need to start

Minimum viable input: **the stages in order.** Anything else you can ask for as you go.

Take the process in whatever form the user has it — a process document, a list typed into
a message, a screenshot of an ATS pipeline, a Greenhouse or Ashby stage export, a scorecard
set, or a verbal description that starts "so there's a screen, then the hiring manager, then
some kind of panel thing". All of these are workable. Read what they gave you, reconstruct
the process from it, and ask only for what is genuinely missing.

Ask which roles are in scope early, because it changes everything downstream. A single
process for one job family is a tight audit; "our hiring process" across engineering, sales
and ops is three audits and should be scoped to one first — usually the highest-volume or
most-contested family.

Never stall. If the user has no elapsed times and no drop-off data, that is the normal case,
not a blocker: audit on structure alone, produce the full report, and name the two or three
numbers that would sharpen it. See **The degraded case** below.

Where the environment supports structured multiple-choice questions (Cowork's
`AskUserQuestion` or equivalent), use them for the picks — which roles are in scope, who
owns each stage, whether feedback deadlines exist — and keep free text for the texture:
what the stage was added to fix, and who defends it.

## Process

### 1. Reconstruct the process as it actually runs

Not as the process document says. The gap between the two is itself a finding, and where
the documented process and the real one diverge, the real one is what candidates
experience.

For each stage, establish five things:

| | Why it matters |
|---|---|
| **What it is called** | Use their language in the report. It gets forwarded. |
| **Who runs it** | Load, consistency, and whether the assessor can judge what they are assessing. |
| **What it is supposed to assess** | Half the value of the audit is discovering nobody can answer this. |
| **How long it takes** | Candidate cost and interviewer cost. |
| **How long candidates wait before it** | The single most important number, and almost always unmeasured. |

That last one is the one to push on. Stage count is what everyone argues about; elapsed
time is what loses candidates, and most of a six-week process is spent waiting, not
interviewing. Ask it plainly: *from a candidate passing stage two, how many days until they
are sitting in stage three?* If the answer is "depends", ask for the worst recent case —
people remember the bad ones, and the worst case is what your competitor's candidates
compare against.

Two questions that surface more than anything else in the intake:

- **Which stage was added most recently, and what happened that caused it?** Almost every
  bloated loop has a stage that exists because of one specific bad hire. Naming the incident
  is the beginning of the case for removing the stage — the question becomes whether the
  stage would actually have caught that person.
- **When did anyone last remove a stage?** Usually never. Say so in the report. A process
  that only ever gains stages is not a designed process.

Reflect the reconstruction back before you audit it. A short table of stages, owners,
durations and gaps, with a line asking what you got wrong. It takes the user ninety seconds
to correct and it stops every downstream finding inheriting an error.

### 2. Build the timeline

Lay out the calendar from application to offer, splitting time into two columns: **time in
stage** (interviewing, exercises, scheduling that had to happen) and **time between
stages** (waiting). Total both.

The ratio is the headline. When waiting time dominates — and it usually does — the fix is
not fewer stages, it is the operating discipline around the stages: pre-booked slots,
feedback deadlines, a decision that does not wait for a weekly meeting. That is a much
easier sell than deleting a stage, and it often recovers more days.

Break the waiting time into where it actually goes, because each source has a different
fix: application sitting unreviewed, scheduling back-and-forth, feedback not submitted,
waiting for one interviewer's calendar, decisions batched to a weekly meeting, offer
approval. `references/audit-lenses.md` carries the fixes and their trade-offs.

### 3. Build the coverage grid

Competencies down the side, stages across the top, marks in the cells. This is the single
most powerful object the audit produces, and it is usually the easiest recommendation to
sell, because redundancy is invisible in prose and obvious in a grid.

If the user has defined competencies, use theirs. If they do not — common — derive four to
six from what the stages are trying to assess plus what the role fails on, label them as
inferred, and invite correction. Do not stall on the absence of a competency framework;
the grid works on inferred competencies and the inference itself is a finding.

Then read the grid for four things:

- **Duplication.** Two stages assessing the same competency with no deliberate second-read
  rationale. That is a stage you can delete or repurpose.
- **Gaps.** A competency the role fails on that no stage assesses. Usually the reason the
  loop is not producing better hires despite its length.
- **Unassigned stages.** A stage with nothing in its column. It is not assessing; it is
  either selling, or it is an unrecorded veto. Both need to be named as what they are.
- **Overloaded stages.** One stage carrying four competencies in 45 minutes is assessing
  none of them properly.

A competency assessed twice is fine when the second read is deliberate — the things that
decide the hire deserve two independent looks. Three times is redundancy the candidate paid
for with their time.

### 4. Run the audit lenses

Seven lenses. Read `references/audit-lenses.md` before running them; it carries the
diagnostic questions, the common findings, and the recommended fixes with their trade-offs
for each.

1. **Elapsed time** — total calendar days and where they go.
2. **Redundancy** — the coverage grid, read for duplication.
3. **Assessment validity** — are stages assessing what predicts performance, or what is
   easy to assess?
4. **Drop-off risk** — where candidates leave, and why.
5. **Candidate experience** — what they are told, when, by whom, and what they get out of
   it either way.
6. **Bias and consistency exposure** — unstructured stages, inconsistent sequences,
   unrecorded criteria, unaccommodated processes.
7. **Interviewer load** — total interviewer hours per hire.

Two lenses do most of the persuasive work and deserve extra care:

**Assessment validity** is where you say the difficult thing. Name the classic low-validity
stages plainly when you find them: the unstructured culture-fit chat that rewards
similarity to the interviewer, the CV walkthrough that repeats the recruiter screen, the
panel where nobody has assigned competencies so everyone assesses general impressiveness,
the final chat with a founder that functions as a veto with no criteria. Each is defended
by someone, so give each finding a reason and a replacement rather than just a verdict.
`references/stage-patterns.md` has the per-stage argument.

**Interviewer load** is the number that unlocks change with an engineering or sales leader
who is defending the loop on quality grounds. Compute it from their own inputs: interviewer
hours per candidate at each stage (include preparation and scorecard-writing, not just the
scheduled hour), multiplied by candidates reaching that stage, summed, divided by hires.
Present it as hours per hire and, where they can give you a hiring plan, as total hours
across the year. A leader who will not lose a stage to candidate experience will often lose
it to getting three engineering weeks back.

### 5. Design the replacement loop

Produce a stage-by-stage redesign with a before/after comparison, a new coverage grid, and
a new elapsed-time estimate.

The rules that make a redesign hold up:

- **Justify each surviving stage by what it uniquely assesses.** If you cannot write that
  sentence for a stage, it does not survive.
- **For every removed stage, state explicitly what it was assessing and where that is now
  assessed instead.** This is the whole political game. "We are cutting the panel" invites a
  fight; "the panel's two real competencies move to the hiring manager stage and the work
  sample, both of which assess them with a written rubric rather than a group impression"
  is a design decision. Never remove a stage without rehousing its competency or stating
  plainly that it was assessing nothing.
- **Keep the vetoes but give them criteria.** Where a founder or exec insists on meeting
  every hire, do not fight it — that is rarely winnable and sometimes right. Convert it:
  move it earlier so it does not sit at the end of a six-week process, give it one or two
  named competencies, and get the criteria recorded. An unrecorded final veto is the
  highest-risk stage in most loops.
- **Move the cheap filters earlier and the expensive assessment later.** Obvious, and
  frequently violated by loops that put a three-hour take-home before anyone has told the
  candidate what the job pays.
- **Give the candidate something real early.** A candidate cannot decide about a job they
  have not heard described. A loop where the first three stages extract information and
  give none back drops good people at stage two.
- **State the target elapsed time and the service levels that deliver it**, not just the
  stage count. A five-stage loop run with two-day feedback beats a four-stage loop run with
  a week of silence between each.

Where the redesigned loop needs competencies, questions, scorecards and anchored rating
scales built out properly for a specific role, that is `interview-kit-builder`. Say so and
hand off; do not build a half-kit inside the audit.

### 6. Write the change-management section

An audit that cannot be implemented is worth nothing, and this is where most process
reviews die. Cover four things:

- **Who has to agree.** Name the actual people or roles, per change. Deleting a stage owned
  by a VP is a conversation with that VP, not a process announcement. Sequence the
  conversations so the easiest yes comes first.
- **What to pilot, on what.** Pick two or three live roles rather than changing everything
  at once — ideally one high-volume role where you will get data quickly and one senior
  role where the loop hurts most. A pilot converts "you are lowering the bar" into an
  empirical question, which is a much better argument to be having.
- **What to measure, before and after.** Baseline before you change anything, or the pilot
  proves nothing. The short list: time from application to first contact, time from final
  interview to offer decision, total elapsed days, drop-off rate by stage, offer acceptance
  rate, interviewer hours per hire. Add quality-of-hire proxies if they have any — early
  attrition, probation pass rate, first performance review — while being honest that these
  lag by months and will not settle the pilot.
- **What could go wrong and the answer to it.** The objection is almost always "we will
  lower the bar". The answer is that removing a duplicate assessment does not remove the
  assessment, and that the redesign adds structure where there was none. Pre-write that
  answer for the user.

### 7. Produce the report

Fill `assets/audit-report-template.md` and write it to disk as a Markdown file. Do not
deliver an audit as a wall of chat — this document gets forwarded to the people who own the
stages, and it needs to read well without you in the room.

Lead with the findings, not the methodology. A CPO reads the executive summary and the
headings; write so that alone carries the argument.

Then offer one upgrade path, chosen for the audience: a slide deck if it is going to an
exec team or a hiring-manager forum, a Word document if it goes to HR ops or legal, a
shareable page if the TA team will work from it. Offer; do not build all three.

## The degraded case

Most users cannot supply elapsed times or drop-off data on request. Proceed anyway — the
structural findings are the majority of the value and they need no data at all. Redundancy,
validity, unrecorded criteria, missing competency coverage and interviewer load are all
visible from the stage list alone.

When running without data:

- Say so at the top of the report, in one line. Credibility comes from being explicit.
- Audit structure fully. Do not soften the findings because the data is missing.
- Where a finding depends on a number, state it as a hypothesis with the test attached:
  "if drop-off between the take-home and the panel is above your average, the take-home is
  the cause and this is where to look."
- Close by naming the specific numbers that would sharpen it — three, not a list of twelve,
  and with where to pull each from.

The three that matter most, in order:

1. **Time from application to first human contact.** Usually the biggest single block of
   dead calendar time and the one nobody looks at. Most ATSs report it as time-in-stage for
   the first stage, or you derive it from application date to first activity date.
2. **Time from final interview to offer decision.** Where good candidates are lost to a
   competitor who moved. Time-in-stage for the final stage, plus any approval step that
   lives outside the ATS and therefore will not appear in the report — ask about that
   explicitly.
3. **Drop-off rate by stage, split by candidate-withdrawn versus company-rejected.** The
   pipeline or funnel report in any modern ATS. The split is the whole point: rejections
   are the process working, withdrawals are the process failing, and a single conversion
   number hides the difference.

Add offer acceptance rate and reasons for declines if they have them, and interviewer hours
if they can be reconstructed from calendar data.

## Output

A Markdown file with these sections, in this order:

1. **Executive summary** — the findings and the headline numbers, in a paragraph a CEO could
   read alone.
2. **The process as it runs today** — reconstructed stage table with owners, durations and
   gaps. Plus the documented-versus-actual gap if there is one.
3. **Elapsed time analysis** — total days, time in stage versus time waiting, where the
   waiting goes.
4. **Coverage grid** — competencies × stages, with duplication and gaps marked.
5. **Findings by lens** — the seven lenses, each with the finding, the evidence, and the
   recommendation.
6. **The redesigned loop** — stage by stage with justification, the new coverage grid, and
   the before/after comparison.
7. **What was removed and where it now lives** — the table that wins the argument.
8. **Implementation** — who agrees, what to pilot, what to measure.
9. **Assumptions and what would sharpen this** — inferred competencies, missing data, and
   the two or three numbers to pull.

## Legal and consistency guardrails

These are structural recommendations, not legal advice. Ask which jurisdictions the roles
sit in, and state in the report that anything material — particularly assessment design,
adjustments and record retention — goes to local employment counsel before it is
implemented. Employment and equality law diverges sharply between jurisdictions and a
process running across several countries usually needs the strictest one as its baseline.

Three things to hold in every audit, because each is both a legal exposure and a quality
problem:

- **Consistency between candidates for the same role.** Candidates who go through different
  stages, different interviewers or different questions cannot be compared, and a
  divergent process is difficult to defend if a decision is challenged. Where the audit
  finds sequences varying by candidate — a referral skipping the screen, a senior candidate
  getting a shorter loop — flag it plainly and recommend a documented, consistently applied
  sequence with any exceptions defined in advance.
- **Reasonable adjustments for disabled candidates.** The process should offer adjustments
  proactively to every candidate rather than waiting to be asked, and there should be a
  route to an alternative format for any timed or take-home assessment. Check whether the
  offer exists, who handles the request, and whether the alternative is assessed against
  the same criteria.
- **Recorded criteria for decisions.** Every stage that can reject should have written
  criteria and a recorded reason for the outcome. An unrecorded veto — the final founder
  chat with no scorecard is the usual one — is the single largest risk in most loops, and
  it is also where bias travels undetected.

Where the audit surfaces a pattern that could disadvantage a group — an unpaid multi-day
exercise, an unstructured stage carrying decisive weight, a process with no adjustment
route — flag it as a structural risk and recommend the fix. Do not compute an adverse
impact finding; that is a legal determination. If the user wants to test outcomes by stage
across demographic groups, that analysis is worth doing and is normally run through counsel.

If they share candidate-level data, ask for identifiers rather than names and for
aggregate counts wherever possible. It reduces their exposure and the audit does not need
the detail.

## Reference files

- **`references/audit-lenses.md`** — read before step 4, and again when writing the findings.
  Each lens in depth: what to look for, the diagnostic questions to ask, the findings that
  recur, and the fixes with their trade-offs. Also carries the interviewer-load calculation.
- **`references/stage-patterns.md`** — read at step 4 and step 5. A catalogue of common
  stages: what each genuinely assesses well, what it is bad at, when to keep it, when to cut
  it, and how to fix it if it stays. Use it to argue a specific stage in or out.
- **`assets/audit-report-template.md`** — the output skeleton, including the coverage grid
  and the before/after loop comparison. Fill it; keep its section order.

---

*Part of the [People Leader Skills](https://github.com/) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
