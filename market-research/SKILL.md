---
name: market-research
description: >
  Structured market research for solo builders — raw idea to competitive map,
  TAM/SAM/SOM, and strategic positioning. Three modes by familiarity: guided
  (first time), direct (knows what they want), expert (has hypotheses, wants
  pushback). Always responds in the user's language.

  Trigger when the user invokes /market-research or /pesquisa-mercado; asks to
  research a market, map competitors, check if a space is red or blue ocean,
  or size a market. Also trigger when a product idea is shared and no prior
  market research exists — even if asking for something else (like validation).

  Do NOT use for: validating idea fit (use idea-validation skill); competitive
  analysis of a live product with known users; pure SEO or keyword research.
---

# Market Research

Structured market research for solo builders — from territory mapping to strategic
positioning. Adapts to your familiarity with the process.

## Language rule

**Always respond in the user's language.** If the user writes in Portuguese (including
Brazilian Portuguese), respond entirely in Portuguese — including all frameworks,
labels, tables, and section headers. The skill is written in English for GitHub
conventions; the experience should feel native to whoever is using it.

## Entry point: detect context before routing

Before loading any mode, read the conversation for signals:

**Signal 1 — did they skip market research?**
If the user is asking for idea validation, PRD feedback, or build decisions without
evidence of prior market research: flag it once, clearly, without lecturing.
Offer two paths:

> "Before we validate the idea, it helps to understand the territory — who else is
> playing here and whether the market exists. Want to run a market research first
> (takes 30–60 min), or proceed directly to validation knowing we'll be working with
> less context?"

If they choose to proceed: load idea-validation skill and note the missing context
in the output. Do not block.

**Signal 2 — what's their familiarity level?**
Read the message for vocabulary, level of detail, and framing:

- Uses terms like TAM, SAM, competitive moat, ICP, positioning → likely **expert**
- Has a clear idea, asks specific questions, knows what they want to find → likely **direct**
- Describes an idea loosely, asks "is this a good idea?" or "who else does this?" → likely **guided**

If the signal is ambiguous, ask **one question only**:

> "Quick question before we start: have you done market research before, or is this
> your first time mapping a space?"

Route based on the answer:
- First time / not sure → **guided** (`references/mode-guided.md`)
- Done it before / knows what they want → **direct** (`references/mode-direct.md`)
- Has hypotheses, wants critical analysis → **expert** (`references/mode-expert.md`)

Always load `references/core-principles.md` regardless of mode.

## What each mode delivers

| Mode | Who it's for | Output |
|---|---|---|
| **guided** | First time doing market research | Step-by-step with explanations of why each step matters. Ends with structured summary + next step suggestion. |
| **direct** | Knows the territory, wants to move fast | Framework + web research + competitive map + TAM/SAM/SOM. No hand-holding. |
| **expert** | Has hypotheses, wants critical thinking | Everything in direct + explicit challenge of assumptions + pre-mortem + strategic positioning recommendation. |

## Output always includes

Regardless of mode, every market research session produces:

1. **Territory map** — who's playing, how they're clustered, what they cover
2. **Gap analysis** — what's NOT being done, and whether that gap is a feature or a market
3. **TAM/SAM/SOM** — sized honestly, with sources where available and explicit uncertainty where not
4. **Red/blue ocean read** — is this crowded or is there real white space?
5. **Strategic implication** — one paragraph on what this means for what to build next
6. **Next step** — explicit suggestion: validate the idea (`/validate-idea`), refine positioning, or proceed to PRD

## Principles (non-negotiable in all modes)

These are inherited from the product thinking philosophy behind this skill:

**Calibrated honesty.** Every claim about market size, competitor traction, or demand
gets a confidence marker: [Confirmed], [Estimated], or [Inference]. Never invent numbers.
If a figure isn't findable, say so.

**"I don't know" is valid output.** Better to name an unknown than to fill it with a
plausible-sounding guess. The goal is to map the territory accurately, not to make the
idea look good.

**Facts vs. inferences, always separated.** Structured as:
```
Fact: [claim with source or confidence marker]
Inference: [what this suggests — marked as my reading]
```

**No research theater.** The output supports a decision, not a report. Tables over prose.
Insights over summaries. What to do next over what was found.

**Mom Test applied to competitor signals.** When reading reviews or community signals:
discard generic praise ("great tool", "love it"). Prioritize behavioral evidence
("I pay $X/month because Y", "I stopped using it when Z happened").

**Web search budget.** Mode guided: up to 6 searches. Mode direct: 6–10. Mode expert:
up to 12. More than that only with explicit user approval. Principle: synthesize well
what you find, don't compensate with volume.

## Relationship with other skills

```
/market-research   →   maps the territory
       ↓
/validate-idea     →   tests if the idea fits the territory
       ↓
/personas          →   defines who exactly you're building for
       ↓
/positioning       →   defines where you stand vs. what exists
       ↓
/prd               →   translates all of this into what to build
```

This skill feeds `/validate-idea`. If you've already done market research, start there.
If you're here without having validated your idea yet, this is the right first step.

## Anti-patterns (non-negotiable across all modes)

- **No cheerleading.** If the space is crowded, say it's crowded. If the gap is real,
  say it's real. Evidence, not encouragement.
- **No invented numbers.** TAM/SAM/SOM without a real anchor is decoration. Name the
  unknown instead.
- **No "interesting findings" summaries.** Lead with the sharpest insight, not a recap.
- **No blocking.** If the user wants to skip a step, let them — but name what's missing.
- **No research theater.** Volume of searches does not equal quality of analysis.

## Execution flow

1. Read context for signals (skipped research? familiarity level?)
2. Address skipped research if detected (one message, two options, no lecture)
3. Confirm mode — either from signals or one question
4. Load `references/core-principles.md` + mode file
5. Execute mode protocol
6. Produce output following mode structure
7. End with explicit next step

---

*Built from a real market research process — including a pivot, TAM/SAM/SOM iteration,
and a competitive map that revealed where the space was actually empty.*
*Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem by [@ohanatais](https://github.com/ohanatais).*
