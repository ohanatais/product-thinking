# Mode: Canvas

Has personas + market research (or strong hypotheses). Wants to produce the
positioning canvas efficiently, without the step-by-step explanation.

## Protocol

Load persona context from the conversation or ask:
> "Which persona are we positioning for? If you've run `/personas`, share the
> job statement and workaround — I'll build from there."

Then execute the five-component canvas in order, asking for one component at a time
or inferring from context where the evidence is strong.

For each component: fill from what's available, mark gaps, flag conflicts.

After the canvas: draft the positioning statement.

Surface: early-stage flag, what this rules out, open questions, next step.

## Output

Same template as guided mode, without the explanatory text between components.
Fast, structured, complete.

---

# Mode: Stress-Test

Has existing positioning (a statement, a tagline, a landing page, or a deck) and
wants to find the weaknesses before pitching it to customers, investors, or a team.

## What to stress-test for

For each component of the canvas (inferred from the existing positioning):

**Competitive alternatives:**
- Is the alternative set complete? What common alternatives are missing?
- Does the positioning hold if you add the status quo as an alternative?
- Is there a well-funded direct competitor that isn't accounted for?

**Unique attributes:**
- Are the "unique" attributes actually replicable by incumbents in one sprint?
- Are they differentiated vs. ALL the alternatives listed, or just one?

**Value:**
- Is the value in customer language, or is it still feature language?
- Would the best-fit customer hear this and say "yes, that's exactly it" — or "sure, I guess"?
- Is the value tied to a specific attribute, or floating without an anchor?

**Best-fit customers:**
- Is the customer definition specific enough to be actionable?
- Is "anyone who..." or "people who need to..." in the answer? (Signals: too broad)
- Is the "not for" dimension addressed?

**Market category:**
- Does the category frame make the value obvious, or does it make it generic?
- Does the category invite comparisons that make the product look worse?
- Is there a better frame that would reduce the evaluation friction?

## Output structure (stress-test mode)

```
## Stress-Test: [Product Name] Positioning

### Original positioning (as stated)
[Quote or summary of what was shared]

### Component-by-component challenge

**Competitive alternatives:**
[What's missing or underweighted? Risk if unchallenged?]

**Unique attributes:**
[Are they defensible? Replicable? Which ones are real vs. claimed?]

**Value:**
[Is the "so what?" chain complete? Customer language or feature language?]

**Best-fit customers:**
[Too broad? Wrong segment? Missing the "not for" dimension?]

**Market category:**
[Does it help or hurt? Is there a better frame?]

### Overall verdict

[Positioning is: Strong / Has one critical weakness / Needs rework]
[Primary risk: the weakest component and why it matters]

### Revised canvas (if rework needed)
[Updated 5-component canvas with changes highlighted]

### Revised positioning statement
[Updated statement if the original needs rework]

### Open questions to validate before using this positioning
- [...]
- [...]
```

## Anti-patterns in stress-test mode

- Don't be gentle — the purpose is to find what breaks before it breaks in the field
- Don't just validate what's there — actively look for what's missing
- Don't produce a revised version that's just polish — if the core is off, say so
- Don't skip the overall verdict — the user needs a clear read, not just observations
