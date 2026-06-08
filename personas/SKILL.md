---
name: personas
description: >
  Persona creation grounded in real behavior — JTBD-infused, not demographic.
  For solo builders who need to understand who they're building for before writing
  a line of code. Three modes: guided (first time), behavioral (has interviews or
  reviews to analyze), hypothesis (has an idea, no users yet).

  Trigger when the user invokes /personas or /personas-de-usuario; asks to "create
  personas", "define my target user", "who am I building for", "who is my persona",
  or shares interview notes / review data and wants to extract user patterns.

  Also trigger when a user has completed market research or idea validation and
  the natural next step is defining who exactly they're building for.

  Do NOT use for: audience segmentation for ads; writing user stories (use /prd);
  demographic profiling without behavioral grounding.
---

# Personas

JTBD-infused persona creation for solo builders. The goal is not a profile card
with age, location, and job title. The goal is understanding the job someone is
trying to get done, the moment that triggers the search for a solution, and what
"hired" and "fired" looks like for them.

## Language rule

**Always respond in the user's language.** If the user writes in Portuguese (including
Brazilian Portuguese), respond entirely in Portuguese — including all frameworks,
labels, tables, and section headers. The skill is written in English for GitHub
conventions; the experience should feel native to whoever is using it.

## The core principle before anything else

Traditional personas answer: "Who is this person?"
JTBD-infused personas answer: "What is this person trying to accomplish, and why
are they looking for a new way to do it right now?"

The second question builds products. The first builds marketing slides.

A persona without a trigger moment and a job statement is decoration.

## Entry point: detect what the user has

Before routing to a mode, read the conversation for what evidence exists:

**Level 0 — only an idea, no users yet:**
They have a product hypothesis. No interviews, no reviews, no users. → **hypothesis mode**

**Level 1 — has some signal:**
They have interview notes, community research, review data, or customer conversations,
even informal ones. → **behavioral mode**

**Level 2 — unsure or never done this:**
They ask "what are personas" or "how do I start" or describe their idea loosely.
→ **guided mode**

If the signal is ambiguous, ask **one question only:**

> "Do you have any user research, interview notes, or review data to work from —
> or are we starting from your hypotheses about who the user is?"

Route based on the answer:
- No data → **hypothesis** (`references/mode-hypothesis.md`)
- Has data → **behavioral** (`references/mode-behavioral.md`)
- First time → **guided** (`references/mode-guided.md`)

If the user wants to skip personas entirely and proceed to positioning: do not block.
Note in the positioning output that best-fit customers are based on hypotheses, not grounded personas.

Always load `references/core-principles.md` regardless of mode.

## What each mode delivers

| Mode | Who it's for | Starting point |
|---|---|---|
| **guided** | First time thinking about personas | Education + template walkthrough |
| **behavioral** | Has interviews, reviews, or any real user signal | Extracts patterns from real evidence |
| **hypothesis** | Has an idea, no users yet | Makes assumptions explicit and testable |

## Output always includes

Regardless of mode, every persona session produces:

1. **1–3 personas maximum** — more than 3 is usually noise at solo builder stage
2. **Job statement** for each: "When [situation], I want to [motivation], so I can [outcome]"
3. **Trigger moment** — what happened in their life that made them start looking
4. **Current workaround** — what they use today (the status quo to displace)
5. **Pains** — specific, behavioral (not generic "it takes too long")
6. **Gains sought** — what "hired" looks like to them
7. **Red flags** — assumptions that still need validation
8. **Next step** — explicit suggestion: `/positioning` or `/validate-idea` or "go interview these people"

## Anti-superficiality principles (non-negotiable in all modes)

### 1. Behavior over demographics

Age, location, job title, income bracket — these are decoration unless they explain
a behavioral pattern. "36-year-old product manager in São Paulo" tells you nothing
about what to build. "Someone who has tried three different note apps and still keeps
a physical notebook" tells you everything.

Only include demographics if they explain the behavior, not as filler.

### 2. The trigger moment is mandatory

Every persona needs a trigger: the specific situation that made this person start
looking for a solution. Without it, the persona is a static portrait that doesn't
tell you when and why they'd consider your product.

Good trigger: "Lost a client because they couldn't find a conversation note from
two months ago."
Bad trigger: "They want to be more organized."

### 3. Job statements, not feature requests

JTBD format: "When [situation], I want to [motivation], so I can [outcome]."

"I want a tool to manage my tasks" is not a job statement.
"When I'm juggling five client projects and my weekly review comes, I want to see
all open commitments in one place, so I can start the week without the anxiety of
forgetting something critical" is.

The difference: the first describes a feature. The second explains why someone would
change their behavior to use it.

### 4. The workaround is the real competitor

What your persona does today — spreadsheets, WhatsApp notes, Notion hacks, hiring
an assistant, doing it manually — is your real competition. Not Notion itself.
The workaround shows you the cost of the status quo and what "good enough" looks like.

### 5. "I don't know" is valid output

If a critical element of the persona can't be inferred from the evidence available,
say so explicitly and mark it as an assumption to validate. Invented behavioral
patterns are worse than admitted gaps.

### 6. Maximum 3 personas

Solo builders can't build for everyone. More than 3 personas at this stage usually
means the segmentation hasn't happened yet. If the research points to many distinct
user types, help the user choose the one persona that represents the highest-signal
audience for the MVP.

## Execution flow

1. Read context — detect evidence level
2. Address missing evidence if relevant (one message, no lecture)
3. Confirm mode — from signals or one question
4. Load `references/core-principles.md` + mode file
5. Execute mode protocol
6. Produce output following mode structure
7. End with explicit next step

## Relationship with other skills

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

This skill feeds `/positioning`. Strong personas make positioning decisions obvious.
If you're here without market research or validation, that context will be missing
from the behavioral grounding — name it.

---

*Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem by [@ohanatais](https://github.com/ohanatais).*
