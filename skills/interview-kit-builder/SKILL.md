---
name: interview-kit-builder
description: Builds a complete structured interview kit for a specific role — 4-6 mapped competencies, a stage-by-stage plan where each stage owns distinct competencies, a coverage grid, behavioural questions with probes and evidence standards, anchored 1-4 rating scales, and a work-sample exercise. Use when someone says they are "building the interview process for a specific role", "designing the loop for one req", "writing a scorecard", "need interview questions for a role", "our interviewers all ask the same three questions", "everyone just assesses culture fit", "we need to structure our interviews", "what should we ask a VP of Engineering", or is opening a new req and wants the assessment designed before the first candidate lands. Also use to fix an existing loop for one role. For diagnosing an entire hiring process across roles use interview-process-audit; for the hiring manager kick-off conversation that feeds this, use hiring-manager-intake.
---

# Interview Kit Builder

Produces a structured interview kit for one role: competencies, stage plan, coverage grid,
question bank with probes, anchored rating scales, and a work sample. The test of the
output is that an interviewer with no training can pick up their section, run it well, and
submit a score that means the same thing as every other interviewer's score.

Structured interviews with defined competencies and anchored scales are the improvement
with the strongest track record in practice. Most in-house loops are still five
unstructured conversations where everyone assesses "culture fit", three people ask about
the same project, and nobody assesses the thing the role will actually fail on.

## What you need to start

Minimum viable input: **the role title, the level, and what the person needs to have
achieved twelve months in.** That is enough to build the whole kit.

If the user has a role brief — from `hiring-manager-intake`, a job description, a scorecard
draft, or a pasted email from the hiring manager — take it and skip the questions.

If they have none of that, do not stall. Ask for those three things in one short message.
If they only give you a title, infer the rest and proceed: draft the first-year outcomes
yourself, label them as inferred, and say "correct anything that is wrong — I'll rebuild
the competencies from your edits." A wrong first draft that the user corrects in ninety
seconds is worth more than a right answer they never reached because they abandoned the
conversation.

Useful but never required: the job advert, the interview stages already committed to, who
is on the panel and what each person is good at assessing, the last two people who failed
in this role and why, the ATS the scorecard has to live in.

Where the environment supports structured multiple-choice questions, use them for the
level, the stage count, and the competency confirmation — those are picks, not essays.

## Process

### 1. Establish the role, level and first-year outcomes

Competencies come from outcomes, not from a title. "Senior Product Manager" tells you
almost nothing; "own the payments roadmap, ship the new checkout, and get three
engineering teams to agree a sequencing" tells you exactly what to assess.

If the outcomes are vague, sharpen them by asking the one question that produces the most
signal: **what would make this hire fail in year one, given they are technically capable?**
The answer is usually stakeholder friction, ambiguity tolerance, or pace — and it is
almost always the competency the existing loop does not assess.

### 2. Select 4-6 competencies. Not more.

Reflect back a proposed set with a one-line rationale for each, and invite edits. Do not
present a menu of twelve and ask the user to choose — propose the set you would run.

Hold the ceiling at six and say why: every competency added either lengthens the loop or
dilutes the time given to the others. Eight competencies across four interviews means each
gets ten minutes, which is enough for a candidate to give one rehearsed anecdote and not
enough for anyone to probe it. Depth on the things that decide the hire beats coverage of
everything.

Build the set from three sources, not one:

- **Role-specific capability** — the craft. What they must be able to do.
- **Evidence of level and scope** — the thing that separates a strong senior from a lead is
  rarely skill, it is the size and ambiguity of the problems they have owned. Assess scope
  explicitly or you will hire one level down and be surprised.
- **The behaviours this team actually needs** — derived from the failure question in step 1,
  not from the company values poster.

Read `references/competency-library.md` for role-agnostic definitions and level
differentiators. Use it as a starting point and rewrite every definition to be specific to
this role — a generic definition of "ownership" produces generic questions.

### 3. Map competencies to stages

Assign each competency to the stage and the interviewer best placed to assess it. Rules
that make the loop work:

- **Each competency is assessed at most twice.** Twice gives you a second read on the things
  that decide the hire. Three times is redundancy you paid for with candidate time.
- **Every competency is assessed at least once.** Obvious, and yet the coverage grid is
  where teams discover that nobody owns "commercial reasoning."
- **No two stages have the same competency set.** If two interviewers have identical
  assignments they will ask the same questions, get the same answers, and mistake the
  agreement for signal.
- **Match assessor to competency.** The hiring manager assesses craft depth and level. A
  cross-functional partner assesses stakeholder influence, because they have actually been
  on the other side of it. Do not have someone assess a competency they cannot judge — that
  is where "seemed fine" scores come from.

Then produce the coverage grid: competencies down, stages across, marks in the cells. It
is a small table and it is the most valuable object in the kit, because gaps and
duplication are invisible in prose and obvious in a grid.

### 4. Write the question bank

For each competency, produce all six of these. The middle four are what make the kit usable
by an untrained interviewer.

1. **Definition** — specific to this role and level, one or two sentences.
2. **Primary behavioural question** — past behaviour, one situation, open. "Tell me about a
   time you…" not "how would you…". Hypotheticals measure articulacy, which correlates with
   presentation skill rather than performance.
3. **2-3 follow-up probes** — the ones that get past a rehearsed answer. Aim at specifics
   the candidate could only know if they were there: what the alternatives were, what they
   got wrong, who disagreed and what happened, what it cost.
4. **Strong evidence** — what a good answer contains. Written so an interviewer can check
   against it while listening.
5. **Weak evidence** — what a thin answer looks like, phrased as observable behaviour rather
   than a feeling.
6. **The common false positive** — the candidate who sounds excellent on this competency and
   has not done the thing. Usually someone adjacent to the work: they were in the room, on
   the team, or reporting to the person who did it. Name the specific pattern for this
   competency and the probe that separates the two.

Read `references/question-design.md` before writing questions. It covers question
construction, probing technique, how to spot rehearsed and secondhand answers, and rating
anchor design.

### 5. Write anchored rating scales

Use a 1-4 scale with a written anchor for each point, specific to that competency.

Two things to explain to the user, because both get argued about:

- **No midpoint.** On a 1-5, a large share of scores land on 3, which carries no
  information and defers the decision to the debrief where the most confident voice wins.
  Four points force each interviewer to commit to a side.
- **Anchors, not adjectives.** "3 = good" is noise; two interviewers will use it to mean
  different things and the average of their scores is meaningless. An anchor describes
  observable evidence: what the candidate said or did that puts them at that point. Write
  the anchors per competency — the same 3 means something different for technical depth
  than for stakeholder influence.

Pair the score with a recommendation that is separate from it — hire / no hire /
lean, with the reason. A candidate can score 3s across the board and still be a no, and
forcing the recommendation to be stated separately makes that visible instead of buried.

### 6. Design the work sample

For most roles a well-designed work sample beats any interview question, because it
observes the work instead of the candidate's account of the work. Include one unless the
role genuinely has no observable output.

Design rules, and the reasoning:

- **Realistic.** Use a real problem the team has faced, sanitised. Puzzles and brainteasers
  measure puzzle skill.
- **Time-boxed and stated.** Give an explicit budget — typically 60-90 minutes — and say
  plainly that you will assess what fits in it. Otherwise the candidate with the most free
  time wins, which selects for unemployment and against caring responsibilities.
- **Never free labour.** Do not use live problems you intend to ship. It is an integrity
  issue and candidates notice.
- **Assessed against the same anchors as everything else.** Two assessors, the same rubric,
  scored independently before they speak.
- **Live over take-home where you can.** A 60-minute working session with one interviewer
  observing gets you the reasoning as well as the output, and it costs the candidate less.
- **Offer an alternative format** where a candidate's circumstances make the default
  unworkable, and assess the alternative against the same competencies.

State which competencies the work sample carries — it usually carries the craft
competency, and that lets you drop it from a conversational stage and use the time better.

### 7. Write the interviewer instructions

The parts untrained interviewers get wrong, in the kit rather than in a training session
that will not happen:

- **Opening.** Two minutes: who you are, what this stage assesses, how long, when they will
  hear back, and that you will leave time for their questions. It costs nothing and it
  improves what candidates give you.
- **Time allocation, written in the stage plan.** For a 45-minute stage: 2 opening, 30 on
  competencies (two competencies, 15 each), 8 for candidate questions, 5 buffer. Without an
  allocation, interviewers spend 25 minutes on the first question and rush the rest.
- **Notes are evidence, not impressions.** Write what the candidate said — specifics,
  numbers, decisions, quotes where you can. "Strong communicator" is not usable in a
  debrief; "walked through the migration decision unprompted, named the two options
  rejected and why" is.
- **Submit the scorecard before the debrief.** Non-negotiable and worth the friction. Once a
  senior person says "I loved them" in the room, everyone's independent read collapses into
  theirs. Independent scores first, discussion second — and the disagreements are the most
  useful part of the debrief, so protect them.
- **Same questions, every candidate.** Comparison requires a common baseline. Probes vary
  with the answer; primary questions do not.

### 8. Produce the kit

Fill `assets/interview-kit-template.md` and write it to disk as a Markdown file named for
the role. Then offer, without building them unprompted: a scorecard export shaped for their
ATS (Greenhouse, Lever, Ashby and most others take structured scorecard attributes — ask
which one and produce the field-by-field version), a one-page interviewer briefing per
stage, or a shareable page for the panel.

If the kit rests on inferred outcomes or an assumed level, carry an assumptions block near
the top listing what was assumed and what would replace it.

The output of `hiring-manager-intake` is the natural input to this skill; the kit this
produces is what `interview-process-audit` assesses when the question moves from one role
to the whole process.

## Output

A Markdown file with these sections, in this order:

1. **Role summary** — title, level, first-year outcomes, assumptions block if any.
2. **Competencies** — 4-6, each with a role-specific definition and why it is on the list.
3. **Stage plan** — each stage: format, duration, interviewer, competencies owned, time
   allocation.
4. **Coverage grid** — competencies × stages, with the assessed-twice-maximum visible.
5. **Question bank** — per competency: definition, primary question, probes, strong
   evidence, weak evidence, false positive.
6. **Rating scale** — the 1-4 anchors, written per competency.
7. **Work sample** — brief, time box, what is assessed, rubric, candidate-facing instructions.
8. **Interviewer instructions** — opening script, note-taking standard, scorecard-before-debrief rule.
9. **Debrief structure** — order of speaking, how to handle a split, who decides.
10. **Scorecard** — the form interviewers fill in.

## Questions that create legal exposure

Interview questions must assess job-relevant capability. That is both the legal standard in
most jurisdictions and the thing that makes the assessment work — a question that does not
predict performance is not worth the risk of asking it.

Include this section in every kit, because the drift is almost always accidental and comes
from an interviewer trying to get at a real concern:

| Concern the interviewer actually has | Where they stray | Ask instead |
|---|---|---|
| Will they be here in two years? | Family plans, marital status, "are you settled?" | "What are you looking for in your next role, and what would make you stay somewhere three years?" |
| Can they do the travel / on-call? | Childcare, dependants, health | "This role is on-call one week in four and involves roughly six trips a year. Does that work for you?" |
| Are they too junior / too senior? | Graduation year, age proxies, "digital native" | Assess scope directly: the size, budget, headcount and ambiguity of what they have owned. |
| Will they fit the team? | Religion, background, social class signals, "culture fit" | Assess the specific behaviours the team needs, as named competencies with anchors. |
| Can they legally work here? | Nationality, birthplace, accent, first language | "Are you authorised to work in [country], now or with sponsorship we would provide?" — asked identically of every candidate. |
| Will they be available Saturdays? | Religious observance | State the schedule, ask whether they can meet it. |
| Are they going to need adjustments? | Health, disability, medical history | Describe the role's requirements, and offer adjustments for the process itself to every candidate. |

Two further points to state in the kit:

- **"Culture fit" is where most bias enters a loop**, because it is unanchored and rewards
  similarity to the interviewer. If the team needs specific behaviours, name them as
  competencies with evidence standards. If it cannot be defined well enough to anchor, it is
  not assessable and should not carry a score.
- This is structural guidance, not legal advice. Employment and equality law varies by
  jurisdiction; ask which jurisdictions the role is hiring in, and have the kit reviewed
  locally before it goes to a panel — particularly where roles are open across several
  countries and one panel runs them all.

Note candidate notes and scorecards are personal data with a retention period. Keep them
evidence-based and job-relevant, which is also what makes them defensible if a decision is
ever challenged.

## Reference files

- **`references/competency-library.md`** — read at step 2. Role-agnostic competency
  definitions with level differentiators showing what good looks like at IC, senior, lead
  and executive level. Use to select and to calibrate the level, then rewrite the
  definitions for this specific role.
- **`references/question-design.md`** — read at step 4 before writing any question. Question
  construction, probing technique, spotting rehearsed and secondhand answers, and how to
  write rating anchors that different interviewers apply the same way.
- **`assets/interview-kit-template.md`** — the output skeleton. Fill it; do not restructure it.

---

*Part of the [Claude Skills for TA and People Teams](REPO_URL) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
