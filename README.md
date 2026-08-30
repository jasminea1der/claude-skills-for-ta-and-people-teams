# Claude Skills for TA and People Teams

A collection of open-source Claude skills for in-house talent acquisition and people teams.

Eleven skills that do the work a Head of Talent Acquisition or Chief People Officer would
otherwise spend half a day on: the hiring manager intake, the interview kit, the process
audit, the business case, the career framework, the calibration cycle, the survey action
plan, the vendor evaluation, the onboarding plan, the job advert, and an assessment of how
ready your function actually is for AI.

They are built for people who do this job for a living. No explanations of why hiring
matters, no filler, no fabricated benchmarks.

---

## What's in here

### For talent acquisition

| Skill | What it produces |
|---|---|
| [`hiring-manager-intake`](skills/hiring-manager-intake/) | A role brief from the kick-off call — ranked trade-offs, comp reality, calibration plan, open risks. Includes the pushback moves for when a hiring manager asks for a unicorn. |
| [`interview-kit-builder`](skills/interview-kit-builder/) | A structured interview kit for one role — mapped competencies, coverage grid, questions with probes, anchored rating scales, work sample. |
| [`interview-process-audit`](skills/interview-process-audit/) | An audit of your whole loop — where the calendar days actually go, which stages are redundant, drop-off risk, interviewer hours per hire, and a redesigned process. |
| [`job-advert-writer`](skills/job-advert-writer/) | A diagnosis of your job spec and a rewrite that a passive candidate would respond to, with channel variants for careers site, LinkedIn, outreach and referral. |
| [`headcount-business-case`](skills/headcount-business-case/) | The case that gets approved — cost of inaction, options rejected, fully-loaded cost, and the CFO objections pre-empted. |

### For the wider people function

| Skill | What it produces |
|---|---|
| [`career-framework-builder`](skills/career-framework-builder/) | A career framework for one function — levels, real differentiators, evidence-based progression criteria, a dual IC/management track, and the rollout plan including what to do about over-titled people. |
| [`performance-calibration-pack`](skills/performance-calibration-pack/) | A calibration cycle you can run — session design, facilitator run sheet, manager pre-work, in-the-room bias interrupters, consistency checks. |
| [`engagement-survey-action-plan`](skills/engagement-survey-action-plan/) | Survey results turned into three to five owned actions, a manager cascade, and the "what we heard, what we're not doing and why" message. |
| [`onboarding-plan-audit`](skills/onboarding-plan-audit/) | An onboarding audit and outcome-based 30/60/90 plans, plus the manager obligations brief that most programmes forget to write. |
| [`hr-tech-evaluation`](skills/hr-tech-evaluation/) | A vendor selection that survives the demo — ranked requirements, weights set before you look at anything, demo scripts that expose differences, reference call guide, decision paper. |

### Cross-cutting

| Skill | What it produces |
|---|---|
| [`ta-ai-maturity-assessment`](skills/ta-ai-maturity-assessment/) | A six-dimension assessment of your function's AI maturity, the binding constraint holding you back, and a sequenced roadmap. |

---

## How to use them

**In the Claude app or Cowork** — download this repo, then upload a skill folder (or the
whole `skills/` directory) to your Claude account. See [docs/installing.md](docs/installing.md)
for the current routes, which vary by plan.

**In Claude Code** — clone the repo and point Claude at it, or copy the skill folders you
want into `.claude/skills/` in your project or `~/.claude/skills/` for personal use.

**Without installing anything** — every skill is a Markdown file. Open the `SKILL.md`,
paste it into a conversation with any capable model, and it will work. The `references/`
files add depth; attach them when the skill points to them.

Then just describe your situation in your own words. The skills are written to trigger on
the way people actually talk — "my req got knocked back", "the survey results are back",
"our loop has seven stages and nobody knows why".

---

## How these are built

Two rules shape every skill here, and they are worth knowing because they are what makes
these usable rather than impressive.

**They never stall waiting for perfect input.** A skill that opens by demanding a clean
ATS export is a skill nobody runs twice. Every skill here asks for the minimum, proceeds on
clearly labelled assumptions when you do not have the rest, produces the full artefact, and
tells you at the end exactly which two or three numbers would sharpen it. An output built
on stated assumptions and honest about it beats a stalled conversation every time.

**They never invent a statistic.** These outputs get repeated in front of boards. You will
not find a fabricated benchmark, an uncited study, or an invented industry average anywhere
in this repo — and where a skill needs current external facts, such as pay transparency
obligations or AI regulation, it is written to look them up and cite them rather than
assert them from memory. Where typical ranges are genuinely useful they are framed as
starting points to calibrate against your own data.

The full house spec is at [docs/CONVENTIONS.md](docs/CONVENTIONS.md) if you want to write
your own in the same style, or judge whether these meet their own standard.

### Anatomy

```
skills/<skill-name>/
├── SKILL.md      the workflow
├── references/   frameworks, question banks, methodology — loaded when needed
└── assets/       output templates the skill fills in
```

### On the legally sensitive ones

Several of these sit near real exposure — pay and progression criteria, selection and
adverse impact, calibration records, survey free-text containing disclosures. The line
these skills hold is that they produce analysis, structure, and the right questions for a
qualified adviser. They do not produce legal conclusions or compliance sign-off, and they
say so where it matters. Employment law varies by jurisdiction; anything material needs
local review.

---

## Contributing

Issues and pull requests welcome, particularly:

- Findings from actually running these on real work — what stalled, what was generic, what
  a skill asked for that you did not have.
- Additional skills that meet the conventions.
- Jurisdiction-specific gaps, especially outside the UK, EU and US.

If you are adding a skill, read [docs/CONVENTIONS.md](docs/CONVENTIONS.md) first. The two
rules above are not negotiable.

## Licence

MIT. Use them, fork them, adapt them for your team, put your own frameworks in the
`references/` files. Attribution appreciated but not required.

---

Built and maintained by the team at **MOVE**, who run embedded recruitment for in-house
talent teams. We built these for our own delivery and for the people we work with, and
publishing them costs us nothing and saves you a day.
