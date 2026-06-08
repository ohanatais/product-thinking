# Core Principles

Loaded by all modes. These govern how personas are built regardless of depth.

## On evidence hierarchy

**Strongest to weakest signals for persona building:**

1. Recorded behavior: usage logs, purchase data, churn patterns, support tickets
2. Interview transcripts: verbatim quotes from real conversations (Mom Test compliant)
3. Community evidence: Reddit threads, forum posts, Discord complaints — what people
   say unprompted to peers, not to companies
4. Review data: App Store, G2, Product Hunt — filter for behavioral specificity
5. Analogy research: users of adjacent products with documented behavioral patterns
6. Founder hypotheses: valid starting point, but must be labeled as assumption

**Mom Test filter (mandatory when analyzing any signal):**

Discard:
- Generic complaints ("it's too complicated")
- Wish lists ("I'd love it if it could...")
- Praise ("amazing tool, love it")
- Hypothetical usage ("I would use this for...")

Prioritize:
- Specific past behavior ("I switched from X because Y happened")
- Quantified frustration ("I spend 2 hours a week doing this manually")
- Revealed willingness to pay (already paying for a workaround)
- The moment that triggered the search ("I started looking when...")

Reference: Rob Fitzpatrick, "The Mom Test".

## On the JTBD framework

**The job is not the feature. The job is the progress the person is trying to make.**

Job statement format: "When [situation], I want to [motivation], so I can [outcome]."

- **Situation**: the context that creates the need — not a demographic trait, a moment
- **Motivation**: the functional or emotional goal — not the feature, the outcome
- **Outcome**: what "done" looks like to them — the measure of success

Each persona should have 1–2 job statements, not a list. More than 2 suggests
either different personas or unclear segmentation.

**The four forces (why people switch):**

1. **Push**: frustration with the current solution (strong enough to create action)
2. **Pull**: attraction of the new solution (clear, believable promise)
3. **Anxiety**: fear of switching (cost, learning curve, data migration)
4. **Habit**: inertia of existing behavior ("this is good enough")

Strong personas identify all four. Weak personas only name the pull.
If push + pull are both present and anxiety + habit are low: this is a high-intent persona.
If push is weak or absent: question whether this persona will actually switch.

## On the workaround

The workaround is the most important behavioral signal.

What the person does *today*, without your product, reveals:
- The real cost of the problem (how hard they work around it)
- The switching cost (the more elaborate the workaround, the harder to change)
- The "good enough" benchmark (what they'd compare you to)

Types of workarounds:
- **Tool stretching**: using a tool beyond its intended purpose (Notion as CRM, WhatsApp as task manager)
- **Manual process**: spreadsheets, physical notebooks, memory
- **Delegation**: hiring someone, outsourcing, asking a colleague
- **Not solving it**: accepting the pain because the cost of switching is too high

The workaround is your real competition — not the category leader.

## On persona count

**1–3 personas for MVP stage. No exceptions.**

More than 3 personas at solo builder stage almost always means:
- The problem isn't specific enough
- The audience segmentation hasn't happened
- The builder is trying to serve everyone

When research reveals many user types: help the user identify the primary persona —
the one most likely to (a) feel the pain acutely, (b) be reachable, and (c) pay.

Mark secondary personas as "future consideration" with a note on what would need
to be true to serve them next.

## On assumptions vs. evidence

Every persona element must be tagged:

- **[Evidence]**: grounded in a quote, behavior, or source
- **[Inference]**: logical reading of evidence — marked as interpretation
- **[Assumption]**: no evidence, needs validation — must be called out

A persona full of [Evidence] tags is rare and valuable.
A persona full of [Assumption] tags is still useful — it makes the bets explicit.
A persona with no tags at all is decoration.

## On output economy

- Persona card format, not prose narrative
- Tables over lists for comparisons
- Quote real language when available (from reviews, interviews, forums)
- Every assumption ends with a note on how to validate it
- No "fictional" names and stock photo descriptions — optional if it helps,
  never required, never the point
