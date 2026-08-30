# Installing these skills

Skills are folders containing a `SKILL.md` and optional `references/` and `assets/`
subfolders. Nothing here needs to be built, compiled or configured.

Product surfaces change; if a route below no longer matches what you see, the
"no installation" option at the bottom always works.

---

## Claude app and Cowork

Skills can be added to your Claude account and are then available in any conversation.
Availability varies by plan — skill creation is generally available on paid plans, and on
Team and Enterprise plans an administrator may control it.

1. Download this repository — the green **Code** button, then **Download ZIP** — and
   unzip it.
2. In Claude, go to **Settings → Capabilities → Skills**.
3. Choose to add a skill and upload the folder for the skill you want, for example
   `skills/hiring-manager-intake/`. Upload the whole folder, not just the `SKILL.md`, so
   the reference files and templates come with it.
4. Repeat for each skill you want. Start with two or three rather than all eleven — you
   will find out quickly which ones fit how you work.

Once added, you do not invoke a skill by name. Just describe what you are doing and Claude
picks the right one.

## Claude Code

Copy the skill folders into either location:

```bash
# available in one project
cp -r skills/hiring-manager-intake .claude/skills/

# available everywhere
cp -r skills/* ~/.claude/skills/
```

Or clone the repo somewhere and point Claude Code at it when you want a skill.

## Claude Desktop with a connected folder

If you use Claude with a folder on your computer connected, clone or unzip this repo into
that folder. Claude can then read a skill directly when you ask it to.

---

## No installation at all

Every skill is plain Markdown, and this works with any capable model.

1. Open the skill's `SKILL.md` on GitHub and copy it.
2. Paste it into a new conversation with a line like: *"Follow these instructions for the
   task I'm about to give you."*
3. Describe your situation.

If the skill points to a file in `references/`, attach or paste that file when it does. The
reference files carry the depth — the question banks, the competency library, the
facilitator scripts — so a skill run without them is thinner but still works.

This is the fastest way to try one before deciding whether to install anything.

---

## A note on the data these skills touch

Several skills work with employee or candidate information. Before you paste anything:

- Use identifiers rather than names wherever the analysis does not need names. It almost
  never does.
- Exclude special-category data — health, disability, ethnicity, religion, union
  membership — unless it is genuinely required, and if it is, check your own policy on
  processing it first.
- Survey free-text is the highest-risk input in this collection because respondents were
  promised confidentiality and comments frequently contain disclosures. The
  `engagement-survey-action-plan` skill has specific handling for this; read that section
  before you run it.
- Check your organisation's own policy on what may be shared with AI tools. That policy
  governs, not this document.
