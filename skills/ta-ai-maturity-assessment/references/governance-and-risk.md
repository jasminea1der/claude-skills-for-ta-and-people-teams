# Governance and risk in AI-assisted hiring

Supporting reference for the governance dimension. Read before running the governance
batch, and again whenever governance scores 1–2.

## Contents

- [How to use this](#how-to-use-this)
- [The organising principle: decision proximity](#the-organising-principle-decision-proximity)
- [Candidate data](#candidate-data)
- [Bias and adverse impact in automated screening](#bias-and-adverse-impact-in-automated-screening)
- [Transparency to candidates](#transparency-to-candidates)
- [Human oversight that means something](#human-oversight-that-means-something)
- [The regulatory picture — verify, do not assert](#the-regulatory-picture--verify-do-not-assert)
- [Vendor due diligence questions](#vendor-due-diligence-questions)
- [Practical governance checklist](#practical-governance-checklist)
- [What to put in the report](#what-to-put-in-the-report)

---

## How to use this

The purpose here is to produce **analysis, structure and the right questions for a
qualified adviser**. Nothing in this file is legal advice, and the assessment must not
conclude that a function is or is not compliant with any instrument. That is a legal
determination that depends on jurisdiction, on the specific configuration of the tools, and
on facts an assessment conversation will not surface.

What the assessment can legitimately do, and should do well:

- Establish which tools sit close to decisions about people, because that is where
  obligation and exposure concentrate.
- Identify where a process could disadvantage a group, and recommend structural fixes.
- Name the questions the function should be putting to counsel and to vendors.
- Point at the current regulatory picture with live sources rather than recollection.

Two things the assessment must not do: compute or state a legal adverse-impact finding, and
recommend any selection approach that uses a protected characteristic. Both cause real
harm, and both are outside what this work is for.

---

## The organising principle: decision proximity

The single most useful move in this dimension is to sort the tool estate by how close each
tool sits to a decision that affects a person. Obligation, exposure and candidate harm all
scale with proximity — not with how much AI the function uses.

**Tier A — acts on the candidate.** Screens, ranks, scores, filters, shortlists, rejects,
assesses. Includes anything producing a score or ordering that a human then follows.
Includes automated video assessment, game-based assessment, CV ranking, knockout logic
driven by a model rather than a rule. This tier carries nearly all the regulatory weight
and nearly all the risk, and it is where the governance conversation should spend its time.

**Tier B — shapes what a human sees.** Search and matching that determines which candidates
surface, interview intelligence that summarises what was said, notes that inform a debrief.
No decision is made, but the information a decision rests on is being selected or
compressed. The risks here are subtler: what gets systematically left out of a summary, and
whether search relevance encodes something it should not.

**Tier C — supports the recruiter's own work.** Drafting adverts, outreach copy, scheduling,
research, meeting notes, internal analysis. Real data-protection duties apply — candidate
personal data is still personal data — but decision-making risk is minimal.

Ask the user to sort their own stack into these three tiers during the governance batch.
The exercise is itself diagnostic: a function that cannot place its tools confidently is
Level 2 at best, however much policy documentation exists. And a function whose entire
estate is Tier C should be told plainly that its governance exposure is low — inflating it
is the fastest way to lose a senior reader.

---

## Candidate data

The practical questions, in rough order of how often they turn up something:

**Where does candidate data actually go?** Every tool that receives a CV, an application, an
interview recording or a transcript is processing personal data, including tools nobody
procured. Shadow usage — a recruiter pasting CVs into a personal consumer AI account — is
common, usually well-intentioned, and is the most frequent unmanaged data path. Ask about it
neutrally; a punitive framing gets a denial and no fix.

**Is there a lawful basis, and does the candidate know?** In GDPR jurisdictions the basis is
usually legitimate interests or contract rather than consent, and the privacy notice has to
reflect what actually happens rather than what happened when it was written. Ask when the
candidate privacy notice was last updated against the current tool estate.

**Are the processing agreements real?** Data processing agreements for each tool that
touches candidate data, and someone who has read the sub-processor list. The questions that
matter commercially: is candidate data used to train the vendor's models, can that be turned
off, where is it stored and processed, and what is the retention period.

**Retention.** AI tooling has quietly extended how long candidate material persists —
transcripts, recordings, embeddings, derived scores. Retention policies written for an ATS
often do not cover derived artefacts, and deletion from the ATS does not necessarily delete
the copy in the note-taker.

**Special-category data.** Health, disability, ethnicity and similar should not be in scope
for hiring tools unless there is a specific, documented reason. Interview recordings and
transcripts capture it incidentally and constantly — a candidate mentioning a health
condition or a caring responsibility. Ask what happens to that material.

**Recordings and transcripts specifically.** They are the fastest-growing category of
candidate personal data in most functions and frequently sit outside the retention policy,
outside the DPA review, and outside the privacy notice. Worth a direct question.

When the user offers data as evidence during the assessment, ask for aggregate counts and
identifiers rather than names, and to leave out special-category fields unless the analysis
genuinely needs them. It reduces their exposure and the assessment does not need it.

---

## Bias and adverse impact in automated screening

### The mechanism, briefly

A model trained on an organisation's historic hiring outcomes learns to reproduce the
patterns in those outcomes — including the ones nobody intended. If a group was
historically less likely to progress for reasons unrelated to capability, a model fitted to
that history will tend to encode it. Removing protected characteristics from the input does
not solve this, because other features correlate with them: postcode, school, career gaps,
language patterns, activity timing, the shape of a CV.

Two further mechanisms worth naming because they are less obvious:

- **Proxy features in matching and search.** Relevance ranking can systematically surface
  one profile shape over another without any explicit criterion. It is not screening, but it
  determines who gets seen, and it usually sits outside whatever review the screening tools
  got.
- **Differential performance in language and speech tooling.** Transcription and language
  analysis do not perform uniformly across accents, dialects and non-native speakers. Where
  transcript quality feeds an assessment or a summary that informs a decision, uneven
  quality becomes uneven treatment.

### What a function should be doing

**Know whether a tool influences selection at all.** Tier A from the section above. If it
does, the rest of this applies; if not, most of it does not.

**Monitor outcomes by stage.** Pass-through rates by stage, compared across groups where
that data is lawfully held and the volumes support it. Aggregate only, monitored over time
rather than as a one-off. The value is in noticing a change, and small-volume comparisons
generate noise that is worse than no signal.

**Run it through counsel where privilege matters.** In several jurisdictions analysis of
this kind is materially better placed as privileged work product directed by legal counsel.
This is a real consideration for a CPO, not a formality, and it is worth stating in the
report because functions often run the analysis first and ask the question afterwards.

**Get validation evidence from the vendor.** What the tool was validated against, on what
population, by whom, and when. A tool that predicts something should be able to say what
that something is and how well it does it.

**Keep a human decision on adverse outcomes.** See below — this is the most robust
structural mitigation available and it is usually the cheapest.

### What this assessment does not do

It does not compute an adverse-impact ratio, apply a legal threshold, or conclude that a
process does or does not have adverse impact. It identifies where the risk sits, whether
monitoring exists, and what to ask. Say this in the report; the precision reads as
competence.

---

## Transparency to candidates

Three separate questions, often conflated:

1. **Are candidates told that automated tools are used?** Increasingly a legal requirement
   in some jurisdictions and a reasonable expectation everywhere.
2. **Are they told what the tools do?** Boilerplate — "we may use automated technology" —
   satisfies nobody and, in some regimes, satisfies nothing. Specificity is the difference.
3. **Is there a route to a human, and to an explanation?** Requesting human review of an
   automated decision, and receiving a meaningful account of the basis for it.

The commercial argument, worth making to a senior reader who might otherwise treat this as a
cost: candidates increasingly assume AI is being used and assume the worst version of it.
A function that can state plainly what it uses, what it does not, and where a person decides
is in a stronger position on candidate experience than one that says nothing — and it is
already doing the work needed to answer the regulator.

The test to apply: **could the function truthfully answer a rejected candidate who asked
how they were assessed?** If the honest answer is no, that is a Level 1–2 finding regardless
of what the privacy notice says.

---

## Human oversight that means something

Human oversight is the most commonly claimed and most commonly hollow control. The
difference between real and nominal:

**Nominal.** A person clicks accept on a ranked list of two hundred candidates. A recruiter
confirms rejections in a batch. The human has the authority to disagree and no practical
capacity or information to exercise it.

**Real.** The person sees the basis for the recommendation, not just the output. They have
the time and standing to disagree, and there are actual cases where they did. Their
disagreement is recorded, and disagreement rates are visible — a rate of zero over months
is evidence the control is nominal.

Practical structural fixes, roughly in order of cost:

- Keep a human decision on every adverse outcome — rejections, not just advancements. This
  is the single highest-value control and is usually cheap.
- Use automated tools to *order* work rather than to *exclude* it, where volume allows. A
  ranking that determines review sequence carries far less risk than one that determines
  who is never reviewed.
- Where model-driven knockouts exist, set the threshold conservatively and audit what fell
  below it — periodically sample rejected candidates and have a human review them blind.
- Record what the tool contributed to each decision, enough to reconstruct a specific case
  later. This is what makes a subject access request or an audit survivable.
- Give the reviewing human the reasoning, not just the score.

---

## The regulatory picture — verify, do not assert

**Search at runtime. Do not state dates, thresholds, obligations or enforcement status from
memory.** This area is moving quarterly: implementation timelines shift, guidance is issued
and revised, new state and national instruments arrive, and enforcement posture changes
independently of the text. Anything asserted from memory will be stale or subtly wrong, and
a wrong regulatory claim in a board paper is exactly the failure mode this collection exists
to avoid.

Ask which jurisdictions the function hires in before doing any of this. The obligations
diverge sharply and a generic answer helps nobody.

### What to search for, by jurisdiction

**European Union.** The EU AI Act's treatment of employment-related AI systems — recruitment,
selection, and decisions affecting the terms of work — as a high-risk category, and what
that entails for organisations deploying such systems as opposed to providing them. Verify
the current phasing of obligations, which of them have taken effect, what deployer duties
(as distinct from provider duties) look like in practice, and any subsequent amendment or
delay to the implementation timeline. Also GDPR Article 22 on automated decision-making,
which applies independently of the AI Act and predates it.

**United Kingdom.** No single AI statute at the time of writing; check the current position,
which has been a sector-regulator-led approach subject to change. UK GDPR and the Data
Protection Act, ICO guidance on AI and data protection and on recruitment tools, Equality
Act 2010 (indirect discrimination is the relevant route), and any current employment or data
reform bill in progress.

**United States — federal.** EEOC position and guidance on algorithmic tools and Title VII,
ADA guidance on assessment tools and reasonable adjustment, and the Uniform Guidelines on
Employee Selection Procedures. Federal guidance in this area has been revised and withdrawn
in recent cycles — verify what currently stands rather than what was published.

**United States — state and city.** NYC Local Law 144 (bias audit and notice requirements
for automated employment decision tools used for candidates in New York City), Illinois AI
Video Interview Act, Maryland facial recognition consent, Colorado's AI legislation, and
California regulations on automated decision systems in employment. Several more states have
introduced or passed instruments; search for the current list rather than relying on this
one, and check effective dates and any amendments or delays, which have been frequent.

**Elsewhere.** Canada (federal and provincial privacy, plus any current AI legislation),
Australia (Privacy Act reform), Brazil (LGPD and AI bill), Singapore and other jurisdictions
with model AI governance frameworks that are advisory rather than binding but are often
what a client audit will reference.

### How to cite it

Prefer primary and official sources — the regulator, the legislature, the enforcement
agency — over vendor blog posts and law-firm summaries, which are useful for orientation and
frequently out of date on specifics. Give each claim its source and the date you retrieved
it. In the report, state which jurisdictions were checked and when, so the reader knows the
shelf life of what they are holding.

Where the position is genuinely unsettled, say so. "This is contested and the guidance has
been revised twice in eighteen months" is more useful to a CPO than false precision, and it
is the honest description of where several of these instruments currently sit.

Every regulatory item in the roadmap carries the same note: **needs local legal review
before implementation.**

---

## Vendor due diligence questions

The questions that separate a vendor with a real position from one with marketing. Give
these to the user; they are useful beyond this assessment, and a function that has asked
them is demonstrably Level 4 on this dimension.

**On the model and its validation**

- What does the system predict or score, stated precisely, and against what outcome was it
  validated?
- On what population was it validated, how large, and how similar to ours?
- When was validation last performed, and does it get redone as the model changes?
- What testing has been done for differential performance across groups? By whom — internal
  or independent? Can we see the methodology, not just the conclusion?
- What is the system's performance for candidates whose first language is not English, or
  who have a disability that affects how they interact with it?

**On our data**

- Is our candidate data used to train or improve your models? Can that be disabled, and is
  it disabled by default?
- Where is data stored and processed? Who are your sub-processors?
- What is the retention period, and what exactly is deleted when we ask?

**On transparency and control**

- What can we tell a candidate about how this system assessed them?
- Can we get the reasoning behind an individual output, or only the output?
- What logs can we retrieve for a specific candidate, and for how long?
- What configuration is under our control — thresholds, weights, which signals are used?

**On compliance posture**

- Which jurisdictions' requirements have you designed for, and what do you provide to
  support a deployer's own obligations?
- Where a bias audit is required for tools of this kind, do you supply one, and what is its
  scope?
- What happens contractually if a regulator determines the tool cannot be used as
  configured?

A vendor claiming their tool is bias-free is itself a finding. No credible provider makes
that claim, because it is not a property a selection tool can have.

---

## Practical governance checklist

Not a compliance certification — a working list for the roadmap. Items are ordered so that
the cheap, high-value ones come first; most functions can complete the first block inside
thirty days without budget or permission.

**Foundations — cheap, fast, no budget**

- [ ] Inventory every tool that touches candidate data, including ones nobody procured.
- [ ] Sort the inventory into Tier A / B / C by decision proximity.
- [ ] Name an owner for AI governance in the function. One person, named.
- [ ] Establish where consumer AI accounts are in use with candidate data, and give the team
      a sanctioned alternative before restricting the unsanctioned one.
- [ ] Confirm no candidate is rejected without a human decision. If any are, that is the
      first thing to change.
- [ ] Check the candidate privacy notice against what the estate actually does today.

**Structure — a quarter, needs decisions and legal input**

- [ ] Confirm which jurisdictions are in scope, and get the obligations for each mapped by
      counsel.
- [ ] Data processing agreements in place and read for every Tier A and Tier B tool.
- [ ] Written human-oversight position: which decisions require a human, at what point,
      seeing what.
- [ ] Candidate-facing disclosure that is specific rather than boilerplate, and a stated
      route to human review.
- [ ] Retention policy extended to transcripts, recordings and derived artefacts.
- [ ] Vendor due diligence questions asked of every Tier A vendor, answers on file.

**Ongoing — two to three quarters, becomes routine**

- [ ] Outcome monitoring by stage established, run through counsel where privilege matters.
- [ ] Records sufficient to reconstruct how a specific candidate was assessed.
- [ ] Pre-purchase governance review as a standing gate for new tooling.
- [ ] Named responsibility for tracking regulatory change, with a review cadence.
- [ ] Periodic blind human review of a sample of automated rejections.

---

## What to put in the report

Keep the governance section factual and proportionate. Overstating risk loses a senior
reader as fast as ignoring it.

- **The tier map.** Which tools sit in Tier A, B, C. This is the finding that carries the
  section, and it is usually the first time anyone has drawn the line.
- **The specific gaps**, in the function's own terms — not a generic compliance list. "No
  human reviews the automated rejections at first stage, and you hire in New York and
  Germany" is a finding. "Ensure compliance with applicable regulations" is not.
- **The jurisdictions in scope**, and what was checked and when, with sources.
- **What needs counsel**, named specifically, so the user can walk into that conversation
  with a list rather than a worry.
- **The honest bottom line.** If the estate is entirely Tier C, say the exposure is low and
  move on. That judgement is what makes the rest of the report credible.

State plainly, once: this is analysis to inform a conversation with a qualified adviser, not
a compliance assessment, and every governance action needs local legal review before it is
implemented.
