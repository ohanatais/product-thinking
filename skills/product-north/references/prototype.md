# prototype — Navigable visual prototype

**Goal:** solve a real pain — "nobody prototypes visually for me, it's just wireframes
described in chat." Here the prototype is the **center of the conversation**: something
the builder SEES and INTERACTS with, to react to and compare alternatives BEFORE
committing to code.

**This is NOT production design.** Production design produces real UI in the repo. Here
it's **disposable, low-fidelity, fast** — enough to decide the direction, not to ship.
Once the direction is chosen, hand off to your production design/build process.

## When to prototype (not always)

Prototype **only for larger/heavier scenarios, when the builder explicitly asks, or when
you sense they clearly aren't sure of the path.** If the decision is simple or already
clear, don't prototype — recommend and move on. Prototyping for its own sake is waste.

## The move

1. **Confirm the alternatives to compare.** 2–3 distinct directions (not spacing
   variations — concept directions: different flows, different hierarchies, different
   interaction models). Each must answer the JTBD in a different way.
2. **Render it visual and navigable.** Use an inline interactive widget/artifact if your
   environment supports one (e.g. a canvas or visualization tool); otherwise a single
   self-contained HTML file. Clickable screens, states, an end-to-end flow in low-fi.
   Wire the buttons so the builder can give feedback directly from the prototype. Keep
   it deliberately rough (don't polish color/typography — that's production design's job
   and would polish the wrong thing).
   - For a multi-screen flow, a widget with navigation between screens beats a
     description.
   - Use real design tokens (if the project has them) only enough to not look alien;
     don't chase brand fidelity here.
3. **Name each direction's trade-off** next to the visual: what each one wins and risks
   in terms of adoption, user effort, and clarity of value.
4. **Push back (contract #1).** Say which direction you'd choose and why — and the
   steelman of the one you're discarding.

## End

Ask which direction resonated and what they'd change. When they choose, suggest:
`decide` (record the chosen direction) and then handing off to your production
design/build process (which turns the concept into real UI).
