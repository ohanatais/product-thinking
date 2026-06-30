# decide — Consolidate the decision (durable + handoff)

**Goal:** close the conversation into an artifact that survives the end of the context
window and is ready to become work. Durable state lives on disk, not in the chat.

**Output:** a **decision record** in `docs/decisions/NNN-short-title.md` + a clear
handoff to the next step (usually writing the build spec — e.g. `/prd`).

## Before you write

1. **Confirm there's a real decision.** If there's still untested faith or an option
   left open, don't force the record — go back to `frame` or `stress`. A decision record
   for a decision that wasn't made is debt, not clarity.
2. **Find the next number.** List `docs/decisions/` (create the folder if it doesn't
   exist). Use the next sequential number, zero-padded (`001`, `002`, ...).

## Decision record format

Save to `docs/decisions/NNN-short-title.md`:

```markdown
# NNN — <Decision title>

- **Date:** <YYYY-MM-DD>
- **Status:** decided
- **Core goal this serves:** <adoption / retention / value / revenue — which and why>

## Context
<The problem in 2–4 sentences. Why decide this now. What was studied (real evidence).>

## Decision
<What was decided, in one clear, actionable sentence.>

## Alternatives considered
<Each real option, with its trade-off. Include "do nothing." Mark the chosen one.>

## Why this one (and the steelman of the opposite)
<The rationale + the strongest version of the discarded path — so the decision can be
revisited later, honestly.>

## Risks and what mitigates them
<The 1–3 risks that survived the stress test, and the plan for each. The faith
assumptions.>

## How we'll know we were right
<The metric/signal that validates or invalidates the decision. When to re-evaluate.>

## Next step
<The handoff: /prd "<sentence>", the design step, a copy/content step, etc.>
```

Keep it lean — a record nobody re-reads is useless. Synthesis, not a transcript of the
conversation.

## End

Confirm the saved file path and give the exact next-step command, ready to copy. If the
next step is the build spec, write the `/prd` (or spec) sentence already drafted from the
decision — the decision record is the best input a spec can receive, and it's what makes
the spec question less and model better.
