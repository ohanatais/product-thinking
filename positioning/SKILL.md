---
name: positioning
description: >
  Positioning definition for solo builders — grounded in April Dunford's five-component
  framework (competitive alternatives → unique attributes → value → best-fit customers
  → market category). Produces a positioning canvas that becomes the foundation for
  messaging, copy, and product decisions.

  Trigger when the user invokes /positioning; asks to "define positioning", "how do
  I stand out", "what makes this different", "how should I describe this product",
  "where do I fit in the market", or "help me with my pitch". Also trigger when
  personas are defined and the natural next step is understanding where the product
  stands vs. alternatives.

  Do NOT use for: writing landing page copy (that's downstream of positioning);
  competitive research (use /market-research); building a persona (use /personas).
---

# Positioning

Positioning is the strategic foundation that makes your product make sense to the
right people. It's not a tagline, not a mission statement, and not a list of features.

It's the answer to: "In a world where these alternatives exist, why would a person
who cares deeply about [this specific value] choose this product?"

## Language rule

**Always respond in the user's language.** If the user writes in Portuguese (including
Brazilian Portuguese), respond entirely in Portuguese — including all frameworks,
labels, tables, and section headers. The skill is written in English for GitHub
conventions; the experience should feel native to whoever is using it.

## The framework: Dunford's five components

All positioning work follows these five components, always in this order.
The order is non-negotiable — each component depends on the previous one.

```
1. Competitive alternatives    →  What would customers use if this didn't exist?
2. Unique attributes           →  What does this have that alternatives don't?
3. Value                       →  So what? What does that mean for the customer?
4. Best-fit customers          →  Who cares most about that value?
5. Market category             →  What frame makes that value obvious?
```

Why the order matters:
- Unique attributes are only "unique" relative to alternatives
- Value is only meaningful when tied to specific attributes
- Best-fit customers are defined by who cares most about the value
- Market category is the context that makes value obvious to best-fit customers

Work backwards from any step and the whole thing collapses.

## Entry point: detect what exists

Before routing to a mode, read the conversation for context:

**Signal 1 — do they have personas?**
Positioning without a persona is positioning for nobody. If there's no persona work:

> "Positioning is most useful when we know who we're positioning for. Do you have
> a sense of your primary user — who feels the pain most acutely and would switch
> first? Even a hypothesis works. We can position around that."

If they have personas (from `/personas` or their own work): use them as the
best-fit customer foundation.

**Signal 2 — do they have market research?**
Without market research, competitive alternatives may be incomplete.
Name this if it's missing, but don't block — hypothesis positioning is valid.

**Signal 3 — do they have early customers or beta users?**
If yes: use their behavior and feedback as grounding. Real customers reveal
real alternatives and real value better than any framework.
If no: hypothesis mode with explicit uncertainty.

Route:
- Has personas + market research → **canvas mode** (`references/mode-canvas.md`)
- Has some context, wants to think through positioning → **guided mode** (`references/mode-guided.md`)
- Wants to check/challenge existing positioning → **stress-test mode** (`references/mode-stress-test.md`)

If ambiguous, ask one question:

> "Do you have personas defined and market research done, or are we starting from
> your current understanding of the space?"

Always load `references/core-principles.md` regardless of mode.

## What each mode delivers

| Mode | Who it's for | Output |
|---|---|---|
| **guided** | First time, or has context but never worked through positioning | Step-by-step through the 5 components with explanation of each |
| **canvas** | Has personas + research, wants to produce the positioning canvas | Completed 5-component canvas + positioning statement |
| **stress-test** | Has positioning, wants to find weaknesses before pitching | Challenge session: where is the positioning vulnerable? |

## Output always includes

Regardless of mode, every positioning session produces:

1. **Five-component canvas** — one row per component, filled
2. **Positioning statement** (one paragraph, not a tagline) — for internal alignment
3. **Early-stage flag** (if pre-PMF) — explicit note to keep positioning loose
4. **What this positioning rules out** — who is NOT the best-fit customer
5. **Open questions** — what would change this positioning if answered differently
6. **Next step** — explicit: `/prd`, messaging, or "validate with 5 conversations"

## The early-stage exception

For solo builders pre-product-market-fit, Dunford's advice is explicit: keep
positioning **loose like a big fish net, not a tuna net.** Don't over-specify
before patterns emerge from real usage.

The skill outputs a positioning thesis — the best current hypothesis — not a final
declaration. Include this note in every pre-PMF output:

> "This positioning is a thesis, not a verdict. Keep it loose until you see patterns
> in who loves the product and why. The best positioning usually comes from talking
> to 10+ customers who chose you and asking what made the difference."

## Anti-superficiality principles

### 1. Start with competitive alternatives, always

The most common positioning mistake: starting with features and asking "who cares?"
The correct path: start with alternatives and ask "what do we have that these don't?"

Alternatives are not just direct competitors. They include:
- Status quo / doing nothing
- Spreadsheets, manual processes, workarounds
- Adjacent tools being stretched beyond their purpose
- Hiring someone to do it manually

If the competitive alternatives section is vague ("other apps in this space"),
the whole canvas is unstable. Push for specificity.

### 2. "So what?" is the most important question

After identifying a unique attribute, always ask: "So what? What does this mean
for the customer's life?" Until that question is answered, you have a feature, not a value.

Example:
- Attribute: "Works offline"
- "So what?" → "You don't lose work when connectivity drops"
- "So what?" → "You can work in planes, basements, rural areas without anxiety"
- Value: "Reliability that doesn't depend on your connection"

The value is what customers buy. The attribute is what engineers build.

### 3. Best-fit customers, not all customers

Early-stage products often try to position for everyone. This produces messaging
that resonates with nobody.

Best-fit customers are the ones who:
- Feel the pain most acutely
- Are most likely to switch from alternatives
- Will advocate loudly if the value lands

Identifying them is not exclusion — it's precision. Name who you're NOT for.

### 4. Market category is a choice, not a label

The market category you choose determines what frame customers use to evaluate you.
It controls which competitors they compare you to and what "better" means.

A product can be in different categories: "AI writing tool" vs. "thinking partner for
writers" vs. "writing workflow automation" set up completely different purchase criteria.

Choose the category that makes your unique value obvious — not the obvious category.

## Execution flow

1. Detect what context exists (personas, research, early customers)
2. Address missing context if relevant (one message, no lecture)
3. Confirm mode — from signals or one question
4. Load `references/core-principles.md` + mode file
5. Execute the 5-component canvas in order
6. Surface open questions and early-stage flags
7. End with explicit next step

## Relationship with other skills

```
/market-research   →   maps the territory
       ↓
/validate-idea     →   tests if the idea fits the territory
       ↓
/personas          →   defines who exactly you're building for
       ↓
/positioning       →   defines where you stand vs. what exists (you are here)
       ↓
/prd               →   translates all of this into what to build
```

---

*Built from real positioning work — including a category shift that changed how
the product was described, compared, and bought.*
*Part of the [pm-skills](https://github.com/ohanatais/pm-skills) ecosystem by [@ohanatais](https://github.com/ohanatais).*
