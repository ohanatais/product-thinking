---
name: idea-validation
description: >
  Provides brutally honest, evidence-grounded validation of product or business ideas
  with calibrated confidence and explicit verdicts. Use whenever the user invokes
  /validate-idea, asks to "validate this idea", "analyze if this makes sense", "give
  honest feedback" about an idea, product concept, startup, app, feature, or business
  — even without an explicit command. Also use when the user shares a PRD, master
  prompt, or brief and asks for a reaction, or when deciding whether to invest time
  in building something. Has 3 modes (quick, research, deliverable) and always ends
  with score 0-100 + verdict (Build / Validate first / Kill) + structured risk register.
  Do NOT use for: validating bugs, code, or isolated technical decisions — only for
  product or business ideas.
---

# Idea Validation

Honest, evidence-grounded analysis of product ideas. Three modes of depth.
Output always includes score, verdict, risk register, and open critical questions.

## Language rule

**Always respond in the user's language.** If the user writes in Portuguese (including
Brazilian Portuguese), respond entirely in Portuguese — including all frameworks,
labels, tables, and section headers. The skill is written in English for GitHub
conventions; the experience should feel native to whoever is using it.

## When to use

Explicit triggers: `/validate-idea`, "validate this idea", "analyze if this makes sense",
"honest feedback on this", "is this worth building", "kill or build".

Implicit triggers: user shares a PRD, master prompt, brief, or product description and
asks for a reaction or opinion. User is deciding whether to invest time in something.

**Do not use for:** isolated technical decisions (which stack, which library), code
validation, bugs.

## Entry point: check for market research first

Before routing to a mode, check whether the user has done market research.

**If there's no evidence of prior market research:**
Flag it once, without lecturing. Offer two paths:

> "Before validating the idea, it helps to have the territory mapped — who else is
> playing here, whether the market exists, and where the white space is. Want to run
> `/market-research` first (30–60 min), or proceed directly knowing we'll be working
> with less external context?"

If they choose to proceed: note the missing context explicitly in the output
under the Demand and Differentiation components. Do not block.

**If market research exists** (shared in the conversation or as a document): read it
before starting. Use it as evidence. Do not re-research what's already been covered.

## Mode routing

If the user doesn't specify a mode, **infer from context first**:

- Short, casual message ("kill or build this quick") → **quick**
- Detailed description, PRD, or brief → **research**
- Explicitly mentions a client, stakeholder, or investor audience → **deliverable**
- Ambiguous → ask one question only:

> "How deep do you want to go? Quick reaction (no web search, fast), full research
> (web searches, sourced claims), or a formatted deliverable for an external audience?"

Modes:

1. `--mode=quick`: no web search, based on reasoning and prior knowledge, with
   calibrated confidence per claim. Use when: user wants an initial reaction, is
   brainstorming, or just wants to know if it's worth researching further.

2. `--mode=research`: 6–10 web searches (hard limit: 10), each with a clear question
   it answers. Every market claim sourced. Facts separated from inferences. Use when:
   user wants to decide whether to build, or when quick mode revealed it's worth
   investigating.

3. `--mode=deliverable`: everything from research + formatting for external audience
   (client, stakeholder, investor). Use when: user needs a professional deliverable.

**Load the reference file for the chosen mode before producing output:**
- `references/mode-quick.md`
- `references/mode-research.md`
- `references/mode-deliverable.md`

**Always also load:** `references/scoring-rubric.md` (score and verdict rubric,
consistent across all modes).

## Anti-superficiality principles (mandatory in all modes)

These are non-negotiable. Breaking any of them invalidates the skill output.

### 1. Calibrated honesty

For every relevant claim about market, competition, demand, viability, or monetization:

- In `quick` mode: mark confidence as **[High]**, **[Medium]**, or **[Guess]**.
  Guess = no solid basis, it's plausible reasoning.
- In `research` and `deliverable` modes: every claim about the external world needs
  a web source. Without a source, mark as **[Inference]**.

### 2. "I don't know" is valid output

If there's no evidence or basis for a claim, say "I don't know" or "I'd need to
research this." **Never invent numbers** for TAM, market share, willingness to pay,
competitor churn, pricing benchmarks, or any specific figure without a source.

### 3. Facts vs. inferences — always separated

In any analytical section, visually separate what is fact (from the world) from what
is inference (my reading). Recommended structure:

```
**Fact:** [claim with source or confidence marker]
**Inference:** [what this suggests — marked as my reading]
```

### 4. Mom Test on reviews and validation signals

When analyzing reviews, user comments, or validation signals:

- **Discard generic praise** ("amazing app", "love it", "perfect") — not evidence.
- **Value specific behavior and pain** ("I use this every day for X", "I stopped using
  it because Y", "I paid for Z").
- **Look for contradictions** between what users say they do and what the product delivers.
- **List questions NOT answered** by the available data.

Reference: Rob Fitzpatrick, "The Mom Test". Principle: opinions are weak, behavior is strong.

### 5. Verdict always required

Every output ends with:

1. **Score 0–100** across 4 components (Demand, Differentiation, Feasibility,
   Monetization) + aggregate. Rubric in `references/scoring-rubric.md`.
2. **Verdict**: `BUILD` | `VALIDATE FIRST` | `KILL`, with **3 reasons** supporting
   the decision.
3. **Risk register**: table with Impact × Likelihood (Low/Med/High on each axis),
   3–7 rows, always present.
4. **Top 3 critical questions** that need to be answered before moving forward.
5. **Pivot Paths** (required if Verdict = KILL, or VALIDATE FIRST with score < 55):
   2–3 possible reformulations of the idea that could increase the score, each with:
   (a) which score component improves, (b) why this pivot makes sense against the
   market found, (c) what's lost vs. the original idea. Posture: constructive, not consolatory.

### 6. Token economy

Output should be **sufficient, not exhaustive**:

- Tables over prose for comparable data.
- No repeating context already in the conversation.
- No decorative sections or fillers like "In conclusion, as we saw above...".
- Quick: fits in ~1 screen. Research: ~2–3 screens. Deliverable: limited by audience,
  but main body in 2–4 pages.
- Web searches are expensive: hard budget of 10 in research mode. More only with
  explicit user approval.

### 7. No number theater

Prohibited:
- Invented round numbers ("the X market is $50B")
- Lists like "I analyzed 28 competitors and identified 9 opportunities" without evidence
- TAM/SAM/SOM without a real source (in quick mode, say "I can't estimate this
  confidently without research")
- Vague phrases like "high growth potential" without an anchor

### 8. Adversarial by default

The skill assumes a **critical layer** posture, not a cheerleader. When in doubt,
press against the idea. The user asked for honesty, not emotional validation.

When the idea is strong, say it's strong with evidence. When it's weak, say it's weak
with evidence. When it's inconclusive, say "inconclusive" and list what needs to be known.

## Execution flow

1. Check for prior market research — address if missing (one message, two options).
2. Identify the idea to validate (extract from context, or ask for a description).
3. Infer the mode from context — ask only if ambiguous.
4. Load `references/scoring-rubric.md` + the chosen mode file.
5. Execute the mode protocol.
6. Produce output in order: Diagnosis → Score components → Risk register →
   Verdict → Critical questions.
7. End with explicit next step.

## Notes

- This skill is designed for Product Management but works for any product or business idea.
- The skill **does not replace** real user interviews. It maximizes the signal
  extractable from secondary sources and structured reasoning.
- For personal projects / vibe coding, the threshold for `BUILD` should be more
  permissive than for funded projects. Contextual adjustment is allowed, but always
  made explicit in the output.

## Relationship with other skills

```
/market-research   →   maps the territory (run this first)
       ↓
/validate-idea     →   tests if the idea fits the territory (you are here)
       ↓
/personas          →   defines exactly who you're building for
       ↓
/positioning       →   defines where you stand vs. what exists
       ↓
/prd               →   translates all of this into what to build
```

---

*Built from a real validation process — including a pivot that changed TAM, personas,
and positioning before a line of code was written.*
*Part of the [pm-skills](https://github.com/ohanatais/pm-skills) ecosystem by [@ohanatais](https://github.com/ohanatais).*
