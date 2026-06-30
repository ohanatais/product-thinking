# frame — Frame the problem and recommend

**Goal:** turn a fuzzy problem into a structured decision — real options, with honest
trade-offs, and a recommendation made with conviction. Not "here are 3 paths, you
choose." It's "here are the paths, this is the one I'd take and why — now push back
on me."

**Output:** a framing (in the chat) ready to become `decide` (a decision record) or
`stress` (if the recommendation deserves to be pressured before closing).

## Before you speak: study the real thing (contract #2)

Read the code/data/docs for the area. A recommendation without evidence of the current
state is a guess.

## The move

1. **State the problem in one sentence.** Problem, not solution. If the sentence already
   contains the solution ("we need a button for X"), rewrite it as the underlying
   problem ("the user doesn't realize they can do Y"). Confirm with the builder that
   this is the problem.
2. **Anchor to the current core goal.** Why does this matter for the live objective
   (adoption/retention/value/revenue)? If it doesn't connect, say so — maybe now isn't
   the time.
3. **Open 2–4 real options.** Always include the "do nothing / do the minimum" option.
   For each: what it is, the cost (effort + complexity, in PM language), what it wins,
   what it risks. Use the right prioritization lens (RICE/ICE, Kano — see
   `references/lenses.md`) and **name which one you used**.
4. **Second-order effects.** For the option you'll recommend: if we do this, what
   changes elsewhere in the product, in user behavior, or on the roadmap?
5. **Recommend with conviction + counterpoint (contract #1).** Say what you'd do, why,
   and **the steelman of the path you're discarding** — the strongest version of "they
   might be right to disagree with me."
6. **The biggest risk.** What's the single thing that, if it goes wrong, invalidates
   the recommendation?

## End

Ask whether they want: `stress` (pressure the recommendation before closing),
`prototype` (see it visually before deciding), or `decide` (it's mature — record it).
