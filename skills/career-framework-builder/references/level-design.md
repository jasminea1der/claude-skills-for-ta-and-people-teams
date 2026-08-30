# Level design

The design half of the framework: how many levels, what separates them, how to write a
descriptor that survives contact with two managers who disagree, and how to build a dual
track that is not a consolation prize.

Read this before writing any level descriptor.

## Contents

- [How many levels](#how-many-levels)
- [The five differentiators](#the-five-differentiators)
- [The two differentiators to keep out](#the-two-differentiators-to-keep-out)
- [Writing a level descriptor](#writing-a-level-descriptor)
- [Worked example: a descriptor written badly and written well](#worked-example-a-descriptor-written-badly-and-written-well)
- [The dual track](#the-dual-track)
- [Levels, titles and the difference between them](#levels-titles-and-the-difference-between-them)
- [Testing the framework before you ship it](#testing-the-framework-before-you-ship-it)

---

## How many levels

### The two failure modes

**Too few.** A three-level framework in a function of eighty people means most people
spend years at the same label. The damage is not motivational fluff — it is concrete.
Strong mid-level people leave, because every external role looks like a step up when your
internal ladder has no next rung. Managers invent informal distinctions ("senior-senior",
"acting lead") to recognise growth, and those informal distinctions become the real
system, unwritten and inconsistent.

**Too many.** An eight-level framework in a function of twenty-five means each step
represents a change too small to describe. Once a promotion does not require a visible
change in scope, it becomes an annual expectation, granted for retention rather than
recognition. The framework then loses authority the first time someone is visibly promoted
without changing what they do — after which nobody uses the descriptors for anything.

Too many levels is the more common error in companies building their first framework,
because level count feels generous and generosity feels safe. It is not: it devalues every
promotion including the deserved ones.

### The two anchors

**Expected tenure.** Take median tenure in the function and ask how many promotions a
strong performer could plausibly earn in that time. If median tenure is three years and
promotion realistically takes two to three years at mid-levels, most people will see one
promotion, possibly two. A framework with eight levels is describing a career almost
nobody in the company will have.

**Headcount available to fill the levels.** Ask the user to sketch how many people they
expect at each level in eighteen months. If several levels come out at zero or one, those
levels are aspirational. That is not automatically wrong — you want the top of the ladder
visible before anyone reaches it, so people can see where it goes — but it should be a
deliberate choice, described as such, and limited to the top one or two levels. Empty
levels in the middle are a design error: they create a gap people are expected to jump.

### Starting points by size

Calibrate against the user's own tenure and headcount data. These are starting points for
a conversation, not benchmarks.

| Function headcount | IC levels | Notes |
|---|---|---|
| Under 15 | 3–4 | Junior / core / senior, plus a lead level if any exist. Resist more. |
| 15–50 | 4–5 | The first level where a dual track becomes worth formalising. |
| 50–150 | 5–6 | Management track separates properly here. |
| 150+ | 6–7 | Top one or two levels rare and gated hard, often company-wide approval. |

Stage matters as much as size:

- **Early stage, fast growth.** Fewer levels, wider bands within each level. Roles change
  faster than any framework can track, and people's scope can double in a year without a
  title change. Wide bands absorb that; extra levels do not.
- **Scaling, headcount doubling.** This is when a framework earns its cost, because
  managers are hiring at levels they have never hired at and need a shared bar. Build for
  the size you will be in a year, not the size you are.
- **Mature, low growth.** More levels are sustainable because tenure is longer, but the
  promotion rate falls and the framework has to be honest about that. Better to have five
  levels people trust than seven where three are unreachable.

### The pushback to give

When a user wants more levels than the function can fill, the useful question is: *how
many people do you expect at each level in eighteen months, and who are they?* Naming
people makes empty levels obvious in a way that abstract discussion does not. If two
levels have the same people in mind, they are one level.

---

## The five differentiators

Pick the dimensions before writing any descriptor, then write every level against the same
set. This is what makes a framework read as one ladder instead of five job descriptions
stapled together — and it is what lets a manager compare two people at different levels on
the same axis.

### 1. Scope of impact

*What breaks if this person is wrong, and for how long.*

The cleanest progression in the whole framework, and the one to lead with. A useful
ladder: own work → own team's output → the function's outcomes → the company's direction.

Write it as consequence, not as area of responsibility. "Owns the billing service" tells
you nothing about level — a graduate and a principal engineer can both be said to own it.
"A mistake in their work is caught in review" versus "a mistake in their judgement costs
the function a quarter" separates levels immediately.

### 2. Autonomy and problem type

*Are they given the problem and the approach, given the problem, or finding the problem?*

Usually the single sharpest differentiator, because it is observable weekly and it maps
onto how much of a manager's attention the person consumes.

The progression:

- Given a well-defined task and told how to approach it.
- Given a well-defined task; chooses the approach.
- Given a problem; defines the work.
- Given an area; identifies which problems are worth solving.
- Identifies problems the organisation has not recognised, and convinces it they matter.

That last step is the real senior/staff boundary in most functions, and it is worth
stating explicitly because it is where promotion arguments concentrate.

### 3. Ambiguity tolerated

*How undefined the situation can be before they need someone else to define it.*

Related to autonomy but distinct: autonomy is about who decides the approach, ambiguity is
about how much is unknown when work starts. Someone can be highly autonomous on
well-specified work and stall completely when the goal itself is contested.

Write it in terms of what the person does when the situation is unclear: escalates,
proposes options, makes a call and communicates it, or reframes the question entirely.

### 4. Influence, and over whom

*Who changes their behaviour because of this person, and through what.*

The progression runs: their own work → their immediate team → peers in other functions →
leaders more senior than them → people outside the company.

Two things to get right. First, name *who* — "influences stakeholders" is unusable,
"changes the plans of teams they have no authority over" is assessable. Second, distinguish
influence from authority. A manager's team does what they say because of the reporting
line; that is not evidence of influence and should not be scored as such. Influence is what
happens without positional power, which is exactly why it works as an IC differentiator.

### 5. Functional depth

*The craft dimension. The only one written entirely in the function's own language.*

This is what stops the framework being generic corporate wallpaper. For engineering it is
about system design, technical judgement and the ability to make good decisions under
incomplete information. For sales it might be deal complexity, sales cycle length, and
who they can hold a conversation with on the customer side. For design, the ambiguity of
the problem and whether they are shaping the product question or executing on it.

Write this section with someone who actually does the work. Getting it wrong is how a
framework loses the function's respect in the first week — practitioners can tell within
one paragraph whether the author understands the job.

---

## The two differentiators to keep out

Users will push for both. Have the reasons ready, because "we don't do that" is not an
argument that survives a founder who wants it.

### Years of experience

Superficially attractive: it is objective, easy to verify and easy to apply. It is also
wrong on three counts.

- **It rewards tenure rather than contribution.** The framework's entire purpose is to
  describe what someone does. Time served is an input to capability, not a measure of it.
- **It becomes indefensible on contact with reality.** The moment a fast third-year is
  visibly operating above a static eighth-year, the framework either promotes the wrong
  person or is ignored. Both outcomes destroy it.
- **It carries real risk.** Years of experience correlates strongly with age, and a
  progression criterion that correlates with a protected characteristic is a problem in a
  promotion process and a bigger one under pay transparency scrutiny. This is a point to
  put to counsel rather than to assert, but it is enough reason on its own to leave it out.

The honest framing to give the user: experience *predicts* level, and it is a perfectly
reasonable thing to notice when hiring. It does not *define* level, and it must not appear
in a written criterion.

### Headcount managed

The more damaging of the two, because it looks like a real measure of scope.

- **It makes management the only route up.** Your best practitioners take teams to get
  promoted, stop doing the work you needed from them, and often turn out to be mediocre
  managers. You lose twice.
- **It moves levels for reasons that have nothing to do with the person.** A reorg that
  splits a team demotes someone by this measure. A hiring freeze caps their growth. Level
  should change when a person's contribution changes, not when the org chart does.
- **It rewards empire-building.** If headcount is the ladder, managers argue for headcount
  they do not need, and resist the efficient answer that requires fewer people.

Scope of impact captures everything headcount was proxying for — a manager of thirty
usually does have larger scope than a manager of three — without the distortion, and
without breaking the IC track.

If the user insists on some size signal, the defensible version is *scope of the
organisation the role sits over* as context for a management-track descriptor, not as a
criterion that produces a level.

---

## Writing a level descriptor

### Structure

Per level, in this order:

1. **One-line purpose.** What this level exists for. "The level at which someone owns a
   problem area without supervision" is worth more than three paragraphs.
2. **The five differentiators**, two to four sentences each.
3. **Functional depth**, written in the function's language.
4. **What this level is not** — the boundary against the level above. Optional, but it is
   often the most-read paragraph in the whole document, because it answers the question
   people actually have.

### Rules that make descriptors usable

**Write for a decision, not for a brochure.** The test for every sentence: could two
managers, reading this about the same person, reach different conclusions? If yes, rewrite
it. That single test removes most of the adjectives.

**Describe behaviour, not traits.** "Is strategic" is unassessable. "Chooses which of
three plausible directions the team takes, and can explain why the other two were
rejected" is observable.

**Keep it short.** A page per level, less at junior levels. Descriptors are not read
carefully by anyone except during a promotion case; every extra paragraph reduces the
chance the document is used at all.

**Make each level a genuine step.** For every adjacent pair, ask: *can I describe a real
person who is clearly at one and clearly not the other?* If not, they are one level.

**Do not write it as a checklist of tasks.** Task lists date immediately and get gamed —
people do the listed thing rather than the thing that mattered. Describe the nature of the
work, and let evidence attach to it in the progression criteria.

**Cumulative, not replacement.** Each level includes everything below it. Say this once at
the top of the matrix so descriptors do not have to repeat expectations.

---

## Worked example: a descriptor written badly and written well

Function: engineering. Level: the first senior IC level.

### Badly written

> **Senior Engineer**
>
> Senior Engineers are experienced engineers with typically 5+ years of experience. They
> demonstrate technical leadership and strong ownership. They are self-starters who
> deliver high-quality code and mentor junior members of the team. Senior Engineers
> communicate effectively with stakeholders and are strategic thinkers who drive impact
> across the business. They act as role models for our values.

What is wrong with it:

- **"5+ years"** — tenure as a criterion, with all the problems above.
- **"Demonstrates technical leadership", "strong ownership", "self-starter", "strategic
  thinker", "drives impact"** — every one is an adjective the reader supplies their own
  meaning for. Two managers will not agree.
- **"High-quality code"** — expected at every level. A differentiator that does not
  differentiate.
- **"Communicates effectively with stakeholders"** — no scope, no named audience, no
  observable behaviour.
- **"Role model for our values"** — values belong in performance expectations, not in
  levelling. Putting them here makes level a judgement about character, which is where
  promotion processes acquire bias and become hard to defend.
- Nothing anywhere says what changes between this level and the one below it.

### Well written

> **Senior Engineer**
>
> *The level at which someone owns a problem, not a task. The first level where a manager
> can hand over an outcome and stop tracking the path to it.*
>
> **Scope of impact.** Owns delivery of a substantial component or service that other
> teams depend on. Their judgement calls shape how that component behaves for the next
> year; a poor call costs the team weeks, and is not usually caught in code review.
>
> **Autonomy and problem type.** Given a problem, not a solution. Breaks it down, sequences
> it, identifies what has to be true for it to work, and surfaces the risks early enough to
> act on. Sets their own approach and is right often enough that the approach is not
> reviewed by default.
>
> **Ambiguity.** Starts work when requirements are incomplete. Makes and documents
> reasonable assumptions rather than waiting for certainty, and revisits them as facts
> arrive. Escalates when a decision needs authority they do not have, with a recommendation
> attached.
>
> **Influence.** Their technical opinion changes what other engineers on the team build.
> Reviews others' designs and improves them. Can hold a technical conversation with a
> product manager that changes the product plan, not only the implementation.
>
> **Functional depth.** Designs systems that survive requirements changing under them.
> Chooses deliberately between speed and durability, and can articulate the trade-off to a
> non-engineer. Debugs across service boundaries. Knows when the technically superior
> option is the wrong business call.
>
> **What this level is not.** Scope stays within their team's remit. A Staff Engineer's
> work spans teams that do not report to the same manager, and involves problems nobody has
> yet framed as problems.

Why it works: every paragraph describes something a promotion case could produce evidence
for; no adjective carries the argument; the boundary with the level above is explicit; and
a practitioner reading it recognises the job.

---

## The dual track

### What a real dual track requires

Build it properly or do not claim to have one — a fake dual track is worse than none,
because it advertises a path that visibly does not exist.

Four conditions, all of them structural:

1. **Genuine scope equivalence.** The senior IC level and its management counterpart cover
   comparable scope on the differentiators. Different work, same weight.
2. **The same pay band.** Not "overlapping". The same band, with the same top. This is the
   condition people check first, and the one that most often reveals the track is
   decorative.
3. **The same ceiling.** If the management track goes one level higher, the IC track is a
   holding pattern and will be read as one.
4. **The same promotion bar.** Reaching the senior IC level is as hard as reaching the
   equivalent management level. If IC promotion is easier, the level is a retention prize
   and the management track knows it.

### How dual tracks fail

**Decorative equivalence.** The chart shows the levels side by side; the pay band, the
approval process, or who gets invited to leadership meetings shows they are not. People
read the behaviour, not the chart.

**The IC ceiling.** IC track ends at the level below where the management track keeps
going. Every ambitious IC eventually switches, which is what the track was built to
prevent.

**Promotion committees that only speak management.** The committee is made of managers, so
management evidence — headcount, budget, reorgs delivered — is legible and IC evidence is
not. Fix it structurally: senior ICs sit on the committee for IC promotions, and the
evidence template for the IC track is written separately rather than adapted from the
management one.

**No mechanism to actually influence.** The framework says a Principal Engineer influences
the function's technical direction. Then there is no forum where technical direction is
set, or they are not in it. The level becomes a title with no lever attached. Whenever the
descriptor asserts influence at a scope, name the mechanism that makes it possible — the
architecture forum, the planning cycle, the design review, the strategy meeting they
attend.

**Treating the switch as one-directional.** Good managers sometimes want to return to
craft work. If moving back reads as a demotion, people stay in management jobs they are
bad at. Say explicitly that movement between tracks at the same level is lateral, and
handle it as such in pay.

### Where the tracks diverge

Below the senior IC level there is usually one track. The split happens where the
management job becomes a job rather than an addition — typically the first level where
someone has direct reports as their primary responsibility.

Above the split, write both descriptors against the same five differentiators, and add
management-specific functional depth for the management track: hiring and developing
people, performance management, planning and resourcing, and organisational design as
scope grows. Do not add a sixth differentiator for the management track that the IC track
cannot be assessed on — that is how the two tracks stop being comparable.

---

## Levels, titles and the difference between them

**Level is internal architecture; title is external signalling.** They are related but
serve different masters — level drives pay band and promotion, title has to make sense to
customers and to the hiring market.

Design them separately, then map:

- Levels can be numbers or names, but keep them internal and stable.
- Multiple titles can map to one level. Sales might need different titles for different
  segments at the same level; engineering usually does not.
- Titles have to survive the market. If everyone in the segment calls the role "Staff
  Engineer" and you call it "Engineer IV", candidates will read your level as junior.

**On title inflation.** Where titles have already inflated, the level framework is the
correction mechanism — but the correction is done by levelling people accurately, not by
demoting titles. Someone can be an "Senior Manager" by title and mapped at a level whose
band and expectations match their actual scope. `references/rollout.md` handles that case
in detail; it is the hardest part of the project.

---

## Testing the framework before you ship it

Four tests, in ascending order of usefulness. Run at least the third.

1. **The adjacent-pair test.** For every pair of neighbouring levels, describe a real
   person clearly at one and not the other. Any pair that fails is one level.

2. **The adjective sweep.** Search the descriptors for "strong", "excellent",
   "effective", "demonstrates", "strategic", "world-class", "senior". Each hit is a
   sentence that has not said anything yet. Rewrite or delete.

3. **The blind levelling test.** The single best test. Take six to eight real people
   across the function, have two managers who both know them level them independently
   against the draft, and compare. Disagreements point at exactly the descriptors that are
   ambiguous — and one round of this improves a framework more than a week of editing.
   Use identifiers rather than names if the results are being shared.

4. **The promotion-case test.** Take a recent promotion — ideally one that was contested —
   and write the case against the new criteria. If the criteria would have made the
   decision clearer, they work. If the case still comes out as a matter of opinion, the
   evidence requirements are not specific enough.
