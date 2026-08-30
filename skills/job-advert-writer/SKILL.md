---
name: job-advert-writer
description: Diagnoses a job specification and rewrites it as a candidate-facing job advert that a strong passive candidate would actually respond to — a specific diagnosis of what the original gets wrong, a rewrite ordered around the questions candidates ask, a hard cut of the requirements list into real must-haves, an inclusive-language and readability pass, pay transparency handling, and channel variants for the careers site, LinkedIn, recruiter outreach and internal referral. Use when someone says "write the job ad", "turn this JD into an advert", "this spec is unreadable", "our job postings are terrible", "why is nobody applying to this role", "make this less corporate", "rewrite this for LinkedIn", "we need a shorter version for outreach", "should we put the salary in the ad", "check this posting for biased language", or hands over an inherited job description and asks for something they can actually post. Owns the outward-facing advert copy; for the hiring manager kick-off that produces the underlying brief use hiring-manager-intake, and for scorecards and interview questions use interview-kit-builder.
---

# Job Advert Writer

Turns an internal job specification into an advert that makes a case rather than lists
requirements. Produces a diagnosis of the original, a rewritten advert, and the channel
variants the role actually needs.

The advert is usually the only piece of employer marketing a candidate reads, and it is
almost always the worst-written asset the company owns. It is typically written by the
hiring manager, for the hiring manager, inherited from the last time the role was open,
and optimised for internal sign-off. The result reads as a list of demands issued to
someone who has not yet decided they want the job — and the people it deters most reliably
are exactly the ones worth reaching: employed, in demand, not searching, and reading it on
a phone with about forty seconds of patience.

The job is not to make the advert nicer. It is to make it **persuasive to someone who does
not have to reply.**

## What you need to start

Take whatever the user has: a pasted job description, an uploaded file, a link to a live
posting, or a role brief from `hiring-manager-intake`. If they give you a link, fetch it —
what is actually published is often worse than the internal document they think they are
sending you.

If they have no spec at all, ask four things and nothing more:

1. Role and level
2. What this person will actually do — the first big thing waiting for them
3. Why the role exists, and why now
4. Who they report to and who they work with day to day

Then write the advert. If they answer two of the four, write it anyway, mark the gaps
inline as `[TO CONFIRM]`, and say specifically what each gap costs — an advert with no
answer to "why now" reads as a backfill nobody is excited about, and that is a real
conversion cost, not a formatting nitpick.

Never stall. A draft the user corrects in five minutes beats a questionnaire they abandon.
Almost every input gap here can be filled with a labelled assumption and fixed on review.

Ask early, in one line, where the role is posted — the jurisdiction determines pay
transparency obligations, and it is much cheaper to know before drafting than after.

Where the environment supports structured multiple-choice questions (Cowork's
`AskUserQuestion` or equivalent), prefer it for the small-set choices — jurisdiction, level,
and which channel variants they need — and keep free text for the role detail, where the
specifics are the whole point.

## Process

### 1. Diagnose the original before you rewrite it

Lead with this. It is the part that teaches the user something, and it is what makes them
trust the rewrite that follows rather than treating it as one more opinion about wording.

Keep it to five to eight specific observations, each quoting the actual text and naming the
cost. Generic critique ("it's a bit corporate") is worthless. Diagnose against these:

- **Order.** How far down does the reader get before learning what they would actually do?
  If the first 150 words are about the company's founding, its market position and its
  values, the advert has spent its only real attention budget on the reader's least urgent
  question.
- **Direction of address.** Count sentences about what the company wants versus what the
  candidate gets. Most specs run heavily one way. "The successful candidate will be
  responsible for" is the house style of a document written for an approvals process.
- **The requirements list.** Length, and how many items are genuinely disqualifying. This is
  where the most damage happens — see step 3.
- **Specificity.** Could this advert be for any company hiring this title? If yes, it does
  no work. The details that persuade are the ones only true of this role.
- **Unanswered questions.** Which of the candidate's seven questions (step 2) does it never
  answer? Missing pay, missing manager, missing process is standard.
- **Language that narrows the pool.** Run `references/language-audit.md` over it and report
  what it catches, with the replacement.
- **Readability.** Sentence length, paragraph length, jargon and acronym density, whether
  anything load-bearing is trapped in an image.

Then say plainly what it is costing: fewer applications, a narrower and more homogeneous
applicant set, more screening time spent on people who did not understand the role, and
candidates arriving at interview sold on something the job is not.

### 2. Rewrite around the candidate's questions, in their order

Candidates read in a fixed order, and it is not the order internal specs are written in.
Structure the advert to answer these, in this sequence:

1. **What is this job, actually?** In plain words, in the first two sentences.
2. **Why does it exist, and why now?** New team, funded growth, a problem someone has
   decided to solve. "Why now" is the single most under-used persuasive fact in recruiting
   and almost no advert includes it.
3. **What will I be doing in the first year?** Concrete, sequenced, real. This is the
   section that converts.
4. **Who will I work with, and who do I report to?** Name the manager and their background.
   People join teams and managers.
5. **Why is this a good move for me?** The honest case — scope, ownership, what they will
   be able to do next that they cannot do now. Include the trade-offs; credibility is
   persuasive and the drawbacks surface at interview anyway.
6. **What does it pay?** See step 5.
7. **What is the process, and how long will it take?** Stages, rough timeline, who they
   meet. Removing uncertainty removes a reason not to start.

Requirements come *after* the case is made, not before it. A reader who has decided the job
is interesting reads a requirements list as "can I do this?"; a reader who has not decided
reads it as "am I allowed to apply?" — and drops out.

`references/advert-anatomy.md` has the section-by-section detail, what each section must
achieve, and worked weak-versus-strong examples. Read it before writing the first draft.

### 3. Cut the requirements list, hard

This is the highest-leverage edit in the whole document and it is the one the user will
resist, so make the argument explicitly.

Separate the list into three buckets:

- **Genuine must-haves** — someone has actually failed in this job, or an adjacent one,
  without this. Aim for three to five. If the list runs to ten, it is a wish list.
- **Learnable here** — real for the role but acquirable in the first few months. Move these
  into the first-year section as "you'll pick up X", where they read as growth rather than
  as a gate.
- **Nice-to-haves** — say so, in a short separate list, and say plainly that nobody is
  expected to have all of them.

Then explain the mechanism, because it is the part that changes behaviour: a fifteen-item
list is a description of nobody, and it is read two different ways. A candidate who assesses
themselves conservatively reads the list as a gate and counts themselves out unless they
clear nearly every line. A confident one reads the same list as aspirational and applies on
a partial match. So the long list does not raise the quality bar. It changes *who* applies,
in a direction nobody chose, while cutting volume across the board.

Add one line to the advert that does real work: **"If you meet most of this and the role
excites you, apply."** It is not a platitude; it is an explicit instruction that overrides
the conservative reading.

Test every surviving requirement with the same question: *has someone done this job well
without it?* If yes, it is not a must-have.

### 4. Run the language audit

Read `references/language-audit.md` and apply it. It covers vague signalling language and
superlatives, degree requirements filtering on access rather than capability,
years-of-experience thresholds standing in for capability (and acting as an age proxy),
physical requirements that are not genuinely essential, culture language that proxies for
age or lifestyle, and insider jargon and acronyms. For each pattern it gives the
replacement, not just the flag.

Make the commercial argument alongside the legal one, because the commercial one is what
gets the edit accepted: this language costs applications and narrows the pool it does
reach. The legal exposure is real, and in several jurisdictions specific to advertising,
but "fewer and worse applicants" is the argument that wins the meeting.

### 5. Handle pay

Ask which jurisdictions the role is posted in, then **verify current pay transparency
requirements with a web search rather than asserting them from memory.** This area changes
faster than any model's training data: US states and cities, several EU member states
implementing the EU Pay Transparency Directive, and others have added or amended
requirements recently, and the specifics — whether a range is required, whether it must be
in the posting itself, what counts as a good-faith range, whether benefits must be
described — vary. Cite what you find. Flag that the final wording needs local review; this
skill produces the draft and the questions, not compliance sign-off.

Separately, make the case for publishing a range even where nothing requires it:

- A candidate who does not see a number assumes the worst or assumes nothing, and the
  strongest people — who have options and are not searching — will not spend a screening
  call to find out.
- Screening on pay in the advert removes the most common cause of late-stage offer failure,
  which is expensive precisely because it happens after everyone's time is spent.
- Applications self-select toward the level being paid for. Fewer, better-matched applicants
  is the outcome, and it is a better outcome than more applicants.
- Internally, refusing to publish a range is usually a signal that the band will not survive
  contact with the market — which is worth knowing in week one rather than week nine. That
  belongs in `hiring-manager-intake` or `headcount-business-case`, not in the advert.

If the user will not publish a number, do not stall or moralise. Write the advert without
one, and add a line that does the next best thing: the level being hired at and a
commitment to discuss range on the first call.

### 6. Accessibility and readability pass

The advert is read on phones, by people with limited time, by non-native speakers of the
language it is written in, and by screen readers. Apply:

- **Plain language.** Short common words. Active voice. "You'll own the pricing model", not
  "the successful candidate will be responsible for the ownership of pricing methodology."
- **Sentence length.** Aim around 15-20 words average; break anything over 30. Vary it, or
  it reads as a manual.
- **Paragraph length.** Two to three sentences. Long blocks are skipped on mobile.
- **Structure for screen readers.** Real headings in a logical order, real bullet lists, no
  headings faked with bold text. Descriptive link text — "how we interview", never "click
  here".
- **No load-bearing text in images.** Salary, requirements or process trapped in a graphic
  is invisible to screen readers and to search.
- **Expand every acronym on first use**, or cut it. Internal acronyms in an external advert
  signal that the document was never rewritten for the reader.
- **Say how to request an adjustment**, with a named contact route, and mean it.

### 7. Produce the channel variants

One advert does not work everywhere. Produce all four, and explain what changes and why —
the user needs to be able to maintain them when the role changes.

| Variant | Length | What changes |
|---|---|---|
| **Careers site** | Full | The complete advert. This is the canonical version everything else links to; it can carry the full first-year detail, the team, the process and the pay range. |
| **LinkedIn / job board** | Roughly a third | Front-load ruthlessly — the first two lines are all that show before the fold. Cut company history, compress the first-year section to three bullets, keep the pay range, keep the process line. Boards are browsed, not read. |
| **Recruiter outreach opener** | 2-3 sentences | Not an advert. One specific reason this person, one specific reason this role is interesting, one low-commitment ask. No requirements, no company boilerplate. It is a message from a person, not a broadcast. |
| **Internal referral** | Short, plain text | Written so an employee can paste it into a message to a friend without embarrassment. Names the team and the manager, says what the person will work on and what kind of person would enjoy it. Drops the marketing voice entirely. |

Use `assets/advert-template.md` as the output skeleton; it carries all four variants.

### 8. Offer the interactive version — do not build it unprompted

For some roles, showing beats describing: a commission role with a live earnings model the
candidate can move sliders on, a team structure they can see, a first-90-days timeline, a
day-in-the-life. Offer a single-file interactive HTML version of the advert for these, and
build it only if the user says yes. Most roles do not need it and an unasked-for
microsite is a distraction from the copy, which is what actually converts.

## Output

A Markdown file, written to disk, containing in this order:

1. **Diagnosis of the original** — five to eight specific observations, each quoting the
   text and naming the cost. Skip if there was no original.
2. **The rewritten advert** — full careers-site version.
3. **Channel variants** — LinkedIn, outreach opener, referral version.
4. **What changed and why** — a short table mapping the significant edits to the reason,
   so the user can defend each one to the hiring manager who wrote the original.
5. **Requirements decisions** — what was cut, what was moved to nice-to-have, what was
   moved into the first-year section, and the must-haves that survived.
6. **Pay section** — the range as published, plus what the jurisdiction check found, cited.
7. **Open questions and assumptions** — every `[TO CONFIRM]`, what it costs to leave it
   blank, and who can answer it.

Lead with the diagnosis; a CPO or Head of TA reading only the first section should still
learn something they can use on the next twenty adverts.

Then offer — without building unprompted — a Word version for sign-off, the interactive
HTML version where it fits, or a short one-page rationale for a hiring manager who is
attached to the original wording.

## Legal and ethical guardrails

- **Advertising is regulated differently from the rest of hiring.** Wording that suggests a
  preference on age, sex, race, religion, disability, national origin, family status or
  other protected characteristics creates exposure at the point of publication, before a
  single application arrives. This skill flags language likely to have that effect and
  proposes replacements; it does not certify an advert as compliant. Have the final wording
  reviewed locally, particularly for roles posted in several jurisdictions at once.
- **Pay transparency rules vary and change.** Ask which jurisdictions apply and verify the
  current requirement by web search at drafting time, citing the source. Do not state a
  rule from memory.
- **Requirements must be job-related.** Degree requirements, years-of-experience thresholds
  and physical requirements that are not genuinely essential narrow the pool along lines
  nobody chose and are the requirements most often challenged. Where one is genuinely
  essential — a licence, a legal qualification, a physical capability the work truly
  requires — keep it, and state it precisely rather than broadly.
- **Diversity statements should describe what you do, not what you feel.** A sentence
  claiming commitment is worth nothing next to a described practice: structured interviews,
  published ranges, a named adjustments contact, flexible working stated specifically. Write
  the practice or write nothing; candidates read boilerplate as boilerplate.
- **Do not promise what the process cannot deliver.** A stated timeline and stage count in
  the advert becomes a commitment. If the process actually takes seven weeks, say seven.

## Reference files

- **`references/advert-anatomy.md`** — read before writing the first draft. Section by
  section: what each must achieve, how it fails, and worked before-and-after examples of a
  weak and a strong version of each. This is the reference that carries the skill.
- **`references/language-audit.md`** — read at the diagnosis step and again before final
  output. The pattern, why it costs applications, and the replacement to write instead.
- **`assets/advert-template.md`** — the output skeleton, including all four channel
  variants.

## Handoff

The competencies and outcomes the advert sells should be the same ones the loop assesses.
Pass the first-year section and the surviving must-haves to `interview-kit-builder` so
candidates are measured against what they were sold — an advert promising ownership and
scope, followed by a loop testing only technical trivia, loses the exact people the advert
worked on. Where the underlying role is not defined well enough to write about, that is
`hiring-manager-intake`.

---

*Part of the [Claude Skills for TA and People Teams](https://github.com/we-are-move/claude-skills-for-ta-and-people-teams) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
