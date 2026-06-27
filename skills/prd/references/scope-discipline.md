# PRD References — Solo Builder Edition

## On scope discipline (the hardest part)

For solo builders, the PRD's most important function is not documentation —
it's scope containment. Every feature you add to the MVP is a week of building
you won't get back. Every feature you defer is a week of learning you might get instead.

**The rule:** if it's not in Section 3, it doesn't get built in this phase.
Not "we'll do it quickly." Not "it'll only take an afternoon." Not in scope.

**The test for Section 3:** can a user *see* or *do* this? If yes, it belongs in scope.
If it's an implementation detail (authentication method, database choice, API design)
it belongs in a technical spec, not the PRD.

**The test for Section 4:** is this something you *could* build but *chose not to*?
If yes, it belongs in out-of-scope. The out-of-scope section is a decision record —
it shows that these things were thought about and deferred deliberately.

## Common PRD failure modes for solo builders

**1. The aspiration PRD**
Describes what the product will eventually be, not what the MVP actually is.
Result: no clear build target, every session starts with "what are we building today?"

Fix: Section 3 should be readable in 2 minutes and leave no ambiguity about what's in.

**2. The feature list PRD**
Section 3 is a list of 25 items that would take 6 months to build.
Result: the builder either ignores the PRD or never finishes the "MVP."

Fix: Ask "what's the smallest version of this that would let a user complete the primary job?"
That's your MVP. Everything else goes to Section 4.

**3. The technical PRD**
Full of implementation details, API designs, component names.
Result: Claude Code uses the PRD as a tech spec, not a product foundation.
The build follows the spec instead of the user need.

Fix: If Claude Code would use a sentence to write code instead of to understand the user,
it doesn't belong in the PRD.

**4. The empty out-of-scope**
Section 4 has 2 items or is missing entirely.
Result: scope expands during the build because nothing was formally deferred.

Fix: Before finalizing, read the list of everything you *didn't* put in Section 3.
The most important deferrals should be explicitly named with a reason.

**5. The vague problem statement**
"Users need a better way to manage their tasks."
Result: Section 3 can justify almost any feature, because the problem is broad enough
to support anything.

Fix: The problem statement must include a trigger (when), a consequence (what happens),
and a workaround (what they do today). Without all three, it's a category, not a problem.

## The PRD as Claude Code context

When building with Claude Code, the PRD becomes the persistent context document.
At the start of each session:

> "Here's the PRD for this project: [paste PRD]. Today we're building [capability X
> from Section 3]. The constraint is [Section 4 item Y is explicitly out of scope]."

This prevents Claude Code from:
- "Helpfully" adding features that weren't requested
- Making architectural decisions based on guesses about product direction
- Building a version of the product that doesn't match the validated scope

The PRD is not a constraint on creativity — it's a shared understanding of what success looks like.

## On updating the PRD

The PRD is a living document, but not one that changes daily.

**Update when:**
- A user behavior reveals that a scoped capability isn't actually useful
- Validation changes what the primary persona is
- A Section 4 item moves to Section 3 (new phase starts)

**Don't update when:**
- You think of a cool feature (add it to Section 4 instead)
- A build session revealed a technical constraint (solve in the build, not the PRD)
- The implementation turned out different from what you imagined

Version bump for Section 3 changes. No version bump for Section 4 additions.
