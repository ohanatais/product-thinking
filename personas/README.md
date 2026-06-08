# personas

> A persona is not a profile card. It's the answer to: what job is this person trying to get done, and what would make them switch to do it better?

Part of the [pm-skills](https://github.com/ohanatais/pm-skills) ecosystem.

---

## What this skill does

JTBD-infused persona creation for solo builders. Three modes based on what evidence you have — not based on how much time you want to spend.

The goal is not age, location, and job title. The goal is the trigger moment, the workaround, and the job statement. Those three things build products. Demographics build slides.

---

## Three modes, one interface

| Mode | When to use | Starting point |
|---|---|---|
| **guided** | First time building personas | Education + collaborative template walkthrough |
| **behavioral** | Has interviews, reviews, or community data | Extracts behavioral patterns from real evidence |
| **hypothesis** | Has an idea, no users yet | Makes assumptions explicit and testable |

The skill detects which mode fits from context. One question if ambiguous.

---

## What every output includes

- **1–3 personas maximum** — more than 3 is noise at solo builder stage
- **Job statement**: "When [situation], I want to [motivation], so I can [outcome]"
- **Trigger moment** — the event (not the feeling) that starts the search
- **Current workaround** — the status quo being displaced
- **Behavioral pains** — specific, not generic
- **Gains sought** — what "hired" looks like
- **Red flags** — assumptions still needing validation
- **Next step** — explicit: `/positioning`, `/validate-idea`, or "go talk to these people"

---

## How to install

```bash
cp -r personas /your-project/.claude/skills/
```

---

## How to trigger

```
/personas
/personas-de-usuario

# Natural language:
"define my target user"
"who am I building for?"
"create personas"
"who has this problem?"
```

---

## Principles

**Behavior over demographics.** "36-year-old PM in São Paulo" tells you nothing. "Someone who's tried three note apps and still keeps a physical notebook" tells you everything.

**The trigger moment is mandatory.** Without it, the persona is a static portrait. You don't know when or why they'd consider your product.

**The workaround is the real competitor.** What they do today — spreadsheet, WhatsApp hack, hiring someone — is what you're actually competing against, not the category leader.

**"I don't know" is valid output.** Invented behavioral patterns are worse than admitted gaps. Tag every unconfirmed element as [Assumption] with a validation note.

**Maximum 3 personas.** More than 3 at MVP stage almost always means the segmentation hasn't happened yet.

---

## File structure

```
personas/
├── SKILL.md                         ← entry point, routing, principles
└── references/
    ├── core-principles.md           ← JTBD, Mom Test, evidence hierarchy
    ├── mode-guided.md               ← first-timer walkthrough
    ├── mode-behavioral.md           ← evidence-based extraction
    └── mode-hypothesis.md           ← assumption-first with validation plan
```

---

## How it fits in the sequence

```
/market-research   →   maps the territory
       ↓
/validate-idea     →   tests if the idea fits the territory
       ↓
/personas          →   defines who exactly you're building for (you are here)
       ↓
/positioning       →   defines where you stand vs. what exists
       ↓
/prd               →   translates all of this into what to build
```

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohanatais)
