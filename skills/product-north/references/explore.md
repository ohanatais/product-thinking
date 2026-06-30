# explore — Pure discovery

**Goal:** understand the topic deeply enough to make a good decision later. **There is
no solution in this phase.** If you're proposing "do X," you skipped explore.

**Output:** a discovery map (in the chat) — JTBD, tensions, hypotheses, open questions —
and a recommendation of which one to attack first. It's not a decision; it's the ground
before the decision.

## Before you speak: study the real thing

Read the code/data/docs that touch the topic (contract #2). That usually means the
product context (a `CLAUDE.md` or brief), the current focus area, any prior discovery
docs, and the code for the area in question. For a broad sweep, dispatch `Explore`.
**Say what you looked at.**

## The move

1. **Job-to-be-done.** What progress is the user trying to make in their life? (Not
   "use the feature" — the real progress.) Use the JTBD lens from `references/lenses.md`.
   Separate the functional, emotional, and social job. Remember that for many products
   the deepest job is emotional or social, not functional.
2. **Tensions.** Where does the user hesitate, abandon, or build a workaround today?
   Where does the product ask for effort before it returns value? (The classic
   "vitamin, not painkiller" risk.)
3. **Hypotheses, not conclusions.** Write 3–6 falsifiable hypotheses ("we believe X
   because Y; we'd know we were wrong if Z"). Mark which have evidence and which are
   faith.
4. **Open questions.** What do you still not know that would change the decision? Order
   them by "how much does the answer move the direction if it's different from what we
   expect."
5. **Counterpoint (contract #1).** Before closing, question the framing of the topic
   itself: what if the problem they brought isn't the real problem? Name that.

## Cadence

Converse, don't dump. Ask 2–3 questions per round (use `AskUserQuestion` when it helps),
listen, and adapt. One round is the default; open a second only if a material gap
remains.

## End

End by recommending: either move to `frame` (a decision can already be framed) or keep
exploring (something is still unclear). Never tack a solution on here.
