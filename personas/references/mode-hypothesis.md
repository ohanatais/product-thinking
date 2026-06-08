# Mode: Hypothesis

You have a product idea and a mental model of who the user is — but no interviews,
no reviews, no real user signal yet. This mode makes your assumptions explicit,
structures them into a testable persona, and tells you exactly what to validate first.

The output is not a "real" persona. It's a **bet** — stated clearly enough to be tested.

## The right posture

A hypothesis persona is useful precisely because it names what you don't know.
The goal is not to build a convincing portrait. The goal is to surface the 2–3
assumptions that, if wrong, would make the entire persona (and your product direction)
collapse — and then prioritize those for validation.

## Protocol

### Step 1: Extract the founder's mental model

Ask a series of questions (combine into one message where possible):

1. "Who do you picture when you imagine your first 10 users? Describe them in terms
   of behavior and situation — not age and job title."
2. "What's the moment where this person feels the problem most acutely? Walk me through
   a specific situation."
3. "What do they do today to deal with it? What's the clunky workaround?"
4. "Why haven't they switched yet? What's kept them with the workaround?"

If they can answer all four fluently: one persona is already forming. Build it.
If they struggle with question 2 or 3: those are the critical gaps.

### Step 2: Build the hypothesis persona card

Fill every element with what the founder believes. Tag everything as [Assumption].
Do not present it as fact.

### Step 3: Risk-rank the assumptions

Not all assumptions are equal. Rank by: "If this assumption is wrong, how much does
the persona (and product direction) change?"

**Critical assumptions** (wrong = different product):
- The trigger moment
- The current workaround
- Whether the pain is frequent enough to act on

**Important assumptions** (wrong = different feature set):
- What "hired" looks like to them
- Their switching anxiety

**Nice-to-know** (wrong = minor calibration):
- Channel, vocabulary, demographic context

### Step 4: Build a validation plan

For the top 2–3 critical assumptions, provide the fastest way to test each:

| Assumption | How to test | Time needed | What "confirmed" looks like |
|---|---|---|---|
| [Trigger moment X] | 5 conversations with [profile], ask about last time this happened | 1–2 weeks | 3+ people describe similar moment unprompted |
| [Workaround Y] | Reddit/community search for "how do you manage [X]" | 1–2 hours | Multiple people describe this workaround |
| [...] | [...] | [...] | [...] |

## Output structure (hypothesis mode)

```
## Hypothesis Persona: [Functional label]

> This is a hypothesis, not a grounded persona. Every element is an assumption
> that needs validation before making major product decisions based on it.

**Job statement (assumed):**
"When [situation], I want to [motivation], so I can [outcome]."
— [Assumption]

**Trigger moment (assumed):**
[Description] — [Assumption]

**Current workaround (assumed):**
[Description] — [Assumption]

**Pains (assumed):**
- [...] — [Assumption]

**Gains sought (assumed):**
[Description] — [Assumption]

---

## Assumption risk ranking

| Assumption | If wrong → | Priority |
|---|---|---|
| [Most critical] | Different product direction | Validate first |
| [...] | Different feature set | Validate second |
| [...] | Minor calibration | Validate eventually |

## Fastest validation path

| Assumption to test | Method | Time | Confirmation signal |
|---|---|---|---|
| [...] | [...] | [...] | [...] |

## Suggested next step

Before building: run [N] conversations targeting [profile].
If validation confirms the trigger and workaround: return to `/personas --mode=behavioral`
with the evidence and rebuild from there.

Or, if you want to proceed with this hypothesis while validating in parallel:
`/positioning` can work with a hypothesis persona — just keep the uncertainty explicit.
```

## Anti-patterns

- Don't present hypothesis elements as facts — the [Assumption] tag is mandatory
- Don't skip the risk ranking — not all assumptions matter equally
- Don't give a validation plan that requires months — fastest path is the goal
- Don't discourage moving forward — hypothesis + parallel validation is a valid path
- Don't produce 3+ personas from zero evidence — one hypothesis persona, stated clearly
