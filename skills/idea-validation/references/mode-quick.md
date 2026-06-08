# Mode: Quick

Analysis without web search, based on reasoning and prior knowledge. Function: honest,
calibrated initial reaction for the user to decide whether it's worth going deeper.

## Constraints

1. **Zero web searches.** If the urge to search arises, signal it: "I'd need to check this."
2. **No specific numbers** for market size, share, pricing, etc., unless they're
   widely known and stable facts.
3. **Mark confidence on every relevant claim**: `[High]`, `[Medium]`, `[Guess]`.
4. Lean output: 1 page of reading, not 3.

## Before starting: read the context

**Infer who the user is** from the way they write and what they share:

- Casual, short message, no jargon → likely a first-timer or early-stage builder.
  Adjust tone: be direct but don't assume familiarity with product frameworks.
- Uses product vocabulary (ICP, moat, positioning, PMF) → likely experienced.
  Skip explanations, go straight to the analysis.
- Shares a detailed PRD or brief → treat it as evidence. Don't ask them to re-explain
  what's already in the document.
- Mentions a specific audience (client, investor, stakeholder) → note it. If the output
  needs to travel beyond this conversation, suggest `--mode=deliverable` at the end.

**Name the assumption you're making** about their context in the first line of the output:

> "Reading this as a solo builder testing an early idea — let me know if the context
> is different."

This prevents misaligned output without requiring an extra round-trip.

## Protocol

### Step 1: Understand the idea in 1 sentence

Before analyzing, rewrite the idea in 1 sentence using the format:

> For **[persona]** who struggles with **[pain]**, **[product]** is a **[category]**
> that **[benefit]**, unlike **[current alternative]** because **[differentiator]**.

If any slot is empty or vague, that's the first signal. Flag it.

### Step 2: Initial reaction (3–5 sentences)

Honest reaction, no hedging. Adversarial posture: what makes this uncomfortable?
What looks strong? Can be positive or negative — but it must be a reaction, not a summary.

### Step 3: Diagnosis across 4 dimensions

One short section per dimension (2–4 sentences each), applying calibrated confidence:

- **Demand**: is there a real pain? Are people already looking for a solution?
- **Differentiation**: what else is out there? Why this version and not another?
- **Feasibility**: can this be built with the resources available?
- **Monetization**: will someone pay for this? (or N/A for personal projects)

In each dimension, visually separate fact (with confidence marker) from inference.

### Step 4: Score + Verdict + Risk Register

Apply `scoring-rubric.md` in full.

Score with justification per component.

Risk register required even in quick mode. Format:

```
| Risk | Impact | Likelihood | Possible mitigation |
|---|---|---|---|
| ... | High | Med | ... |
```

Minimum 3 rows, maximum 7.

### Step 5: Top 3 critical questions

These questions become the bridge to research mode. They must be:

- **Falsifiable**: can have a yes/no answer or a concrete data point.
- **Specific**: not "does the market want this?" but "how many Notion AI users complain
  about X in 2025–2026 reviews?"
- **Critical**: if the answer is X, the verdict changes.

At the end, offer: "I can run `/validate-idea --mode=research` to answer these with evidence."

## Output structure (template)

```
## Quick Validation: [Idea name]

*Reading this as [inferred context — e.g., "a solo builder testing an early-stage idea"].
Let me know if the context is different.*

**In one sentence:** [structured rewrite]

**Initial reaction:** [3–5 sentences, adversarial posture]

### Diagnosis

**Demand**
- Fact/signal: [claim] [Confidence: High/Medium/Guess]
- Inference: [my reading]

**Differentiation**
- ...

**Feasibility**
- ...

**Monetization** (or N/A)
- ...

### Score
[components + total]

### Risk Register
[table]

### Verdict: [BUILD | VALIDATE FIRST | KILL]
1. ...
2. ...
3. ...

### Top 3 critical questions
1. ...
2. ...
3. ...

### Pivot Paths (if Verdict = KILL or score < 41)
**Pivot 1: [short name]** — improves [component], because [reason], cost: [trade-off].
**Pivot 2: [short name]** — ...

(2–3 pivots. Skip if Verdict = BUILD or VALIDATE FIRST with score ≥ 41.)

To answer these with evidence, run `/validate-idea --mode=research`.
```

## Anti-patterns (don't do this)

- Don't skew positive just to be agreeable.
- Don't invent competitors ("there are probably apps like X, Y, Z" without certainty).
- Don't give specific numbers without an anchor.
- Don't end with "it depends, needs more research" without giving a provisional verdict.
- Don't write 3 pages. Quick is quick.
- Don't skip naming the assumed context — misaligned output wastes more time than one sentence.
