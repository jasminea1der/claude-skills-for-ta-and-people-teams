# House conventions for skills in this repo

Every skill in `skills/` is written against this document. It exists so that eleven
skills written by different hands feel like one coherent toolkit to the person using them.

Read it before writing or editing any skill.

---

## Who these skills are for

Two personas, both in-house (never agency-side):

- **Head of Talent Acquisition** — owns hiring delivery, recruiter team, hiring manager
  relationships, and the hiring number. Time-poor, judged on speed and quality of hire,
  constantly asked to justify headcount and spend.
- **Chief People Officer / VP People** — owns the people function end to end. Reports to
  the CEO and the board. Judged on retention, engagement, comp spend, org effectiveness
  and risk.

Both are senior, commercially literate, and sceptical of HR fluff. They do not need
concepts explained to them. They need a competent second pair of hands that produces the
artefact they would have produced themselves given four uninterrupted hours.

Write for that reader. No "as a Head of Talent, you know that hiring is important"
throat-clearing. Get to the work.

---

## The two rules that matter most

### 1. Never stall for input

The single biggest reason a skill gets abandoned is that it opens by demanding a perfect
data export or a fifteen-question form before it does anything.

Every skill must be able to produce a real, useful output from whatever the user has
given so far. If a skill needs something it does not have, it should:

1. Ask for the **minimum viable input** — usually one or two things, not a form.
2. If the user does not have it, proceed anyway on clearly-labelled assumptions.
3. Produce the full artefact.
4. Close with a short, specific note on what would sharpen it — naming the exact data,
   not "more information".

State this explicitly in the SKILL.md body so the model using the skill knows it is
allowed, and expected, to proceed. Phrase it as permission, e.g.:

> If the user cannot supply the pipeline data, do not stop. Build the model on stated
> assumptions, label every assumption inline, and flag at the end which two numbers would
> most change the answer.

An output built on assumptions and honest about it is worth far more to these users than
a stalled conversation.

### 2. Never invent a statistic

These skills go to senior people who will repeat what they read in front of a board.
A fabricated benchmark is a career risk for them and a credibility risk for the repo.

Rules:

- **Do not write a specific figure with an implied source.** No "industry average time to
  hire is 41 days" unless the skill instructs the model to look it up and cite it live.
- **Typical ranges are fine when framed as ranges and clearly caveated**, e.g. "recruiter
  req loads in the 15–25 range are common for volume hiring and 8–12 for senior technical
  hiring — treat these as starting points and calibrate against your own historic data."
- **Never invent a citation, company example, or case study.** If a skill wants
  real-world examples or current market data, instruct the model to use web search at
  runtime and cite what it finds.
- Where a number is genuinely needed to make a model work, make it an **explicit input
  the user supplies or confirms**, not a hardcoded constant.

If you find yourself wanting to write a reference file full of benchmarks, write a
reference file full of *the framework for deriving them from the user's own data* instead.
That is more useful and it is honest.

---

## Skill anatomy

```
skills/<skill-name>/
├── SKILL.md          (required)
├── references/       (frameworks, question banks, methodology — loaded on demand)
└── assets/           (output templates the skill fills in)
```

### SKILL.md frontmatter

```yaml
---
name: skill-name-in-kebab-case
description: What it does, then when to use it. Written to trigger reliably.
---
```

The `description` is the only thing the model sees before deciding whether to use the
skill, so it carries the whole triggering burden. Write it as: what the skill produces,
followed by the situations and phrasings that should invoke it. Be a little pushy —
skills tend to under-trigger. Include the phrasings a real person uses, not just the
formal name of the task ("kick-off call with a hiring manager", "the hiring manager wants
a unicorn", "prepping for comp review").

Keep descriptions **mutually exclusive across this repo**. Several skills touch
interviewing; make it unambiguous which one owns which job. Check the other skills'
descriptions before finalising yours.

### SKILL.md body

Target 150–350 lines. Under 500 always. Structure:

```markdown
# Skill Name

One or two sentences on what this produces and why it matters to the reader.

## What you need to start
The minimum viable input, and what to do when it is missing.

## Process
The actual workflow, in imperative steps.

## Output
The structure of the artefact, given explicitly.

## Reference files
What is in references/ and when to read it.
```

Adapt the headings where the skill calls for it. This is a shape, not a straitjacket.

### Writing style inside the skill

- **Imperative voice.** "Ask the hiring manager what would make them reject a candidate
  with a perfect CV." Not "you might want to consider asking".
- **Explain the why.** A model that understands the reasoning generalises to cases you
  did not anticipate. A model given a bare rule follows it off a cliff. When you write an
  instruction, give the one-line reason it exists.
- **Avoid shouted MUSTs and NEVERs.** If something really is non-negotiable (usually the
  legal guardrails below), state it once, plainly, with the reason.
- **Give the model judgement, not a script.** These are conversations with senior people;
  a rigid interrogation reads as junior. Provide the questions that matter and the signals
  to listen for, and let the model adapt the order.

---

## Interaction pattern

Most of these skills involve a conversation. Two failure modes to design against:

**Death by questionnaire.** Asking twelve questions in one message gets one-line answers
to three of them. Ask in small batches — two or three at a time, grouped by theme, with
the reason they matter. Where the tool environment supports structured multiple-choice
questions (Cowork's `AskUserQuestion`, or similar), the skill should say to prefer that
for choices with a small set of sensible answers, since it is far faster to answer than
free text.

**The interrogation with no payoff.** Show progress as you go. After a batch of answers,
reflect back what you now understand before asking the next batch. It makes the user
confident the effort is landing somewhere.

Where a skill runs on a live call (the intake and the AI maturity assessment especially),
say so, and pace it for someone typing notes while talking.

---

## Output conventions

- **Default output is a Markdown file**, written to disk and delivered to the user. These
  users forward things to hiring managers and executives; they need a file, not a wall of
  chat.
- **Offer an upgrade path, do not assume it.** After producing the artefact, offer the
  format that suits the audience: a Word document for anything going to legal or HR ops,
  a slide deck for anything going to a board or exec team, a spreadsheet for anything with
  a model in it, a shareable page for anything a team will refer back to. Offer; do not
  build all four unprompted.
- **Structure outputs for skim-reading.** Headline finding first, evidence under it. A
  CPO reads the first paragraph and the headings; write so that alone is enough.
- **Every output that rests on assumptions carries an assumptions block** — visible, near
  the top or clearly at the end, listing what was assumed and what it would take to
  replace each assumption with fact.

---

## Legal and ethical guardrails

Several of these skills sit near real legal exposure. The line to hold: these skills
produce **analysis, structure and questions for a qualified adviser**. They do not produce
legal conclusions or compliance sign-off.

Apply where relevant:

- **Pay and pay equity.** A skill may structure a pay analysis, surface where gaps appear,
  and frame the questions. It does not conclude that pay is or is not equitable — that is
  a legal determination, and in several jurisdictions the analysis itself is privileged
  work product when run through counsel. Say so.
- **Selection and adverse impact.** A skill may highlight where a process could
  disadvantage a group and recommend structural fixes. It does not compute a legal
  adverse-impact finding, and it never recommends selection decisions that use a protected
  characteristic.
- **Employment law varies by jurisdiction.** Where a skill touches policy, dismissal,
  redundancy, contracts or statutory reporting, it asks which jurisdictions are in scope
  and states plainly that the output needs local legal review.
- **Personal data.** Any skill that ingests employee or candidate data instructs the user
  to supply identifiers rather than names, and to exclude special-category data unless it
  is genuinely required for the analysis. Say why: it reduces their exposure, and the
  analysis does not need it.
- **Health, disability and personal circumstances.** These may surface in engagement
  free-text, exit interviews or intake conversations. Skills should instruct the model to
  report themes at an aggregate level and not to attribute individual-level inferences
  about anyone's health, family situation or protected characteristics.

Write these as a short section near the end of the SKILL.md, titled plainly. One or two
sentences each, with the reason. They read as competence, not as a disclaimer, when
written well.

---

## Attribution

Each SKILL.md ends with exactly this, and nothing more elaborate:

```markdown
---

*Part of the [People Leader Skills](https://github.com/) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
```

No CTAs, no offers, no funnel language inside the skills themselves. The repo README
carries the introduction to who made this and why. Skills earn attention by being good.

---

## Cross-referencing

Where one skill naturally feeds another, say so in a single line at the end of the
process section — e.g. the intake skill notes that its output is the input to the
interview kit builder. This is what makes the collection feel like a system rather than
eleven loose files. Keep it to genuine handoffs; do not cross-link for the sake of it.

## Reference files

Use `references/` for material that is long, occasionally needed, or reused: question
banks, competency libraries, framework explanations, methodology. Point to them from
SKILL.md with a line on when to read each one — the model should not have to guess.

Reference files over ~300 lines get a table of contents at the top.

`assets/` holds output templates the skill fills in — a Markdown skeleton for the report,
a CSV header for a model. Keep them clean and free of placeholder lorem ipsum.
