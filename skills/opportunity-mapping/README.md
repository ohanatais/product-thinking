# opportunity-mapping

> Most ideation tools start from the idea and ask "is this good?". This one starts from **you** and asks "what's good *for you*?". The same idea is brilliant for one founder and doomed for another — the variable isn't the idea, it's the fit.

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

---

## What this skill does

Starts from the **founder**, not the idea. It takes your unfair advantage, the channels you can actually reach, what you want to learn, and your hard constraints — then generates a space of product opportunities, filters them against who you are, and ranks them on a **Founder × Market × Channel** fit rubric.

Every session ends with a ranked shortlist, fit scores, the single riskiest assumption, and a cheap test — never just a list of ideas.

This is the deepest skill in the sequence, and it sits **before** market research. It's the step that was missing: the one that produces the idea instead of assuming you already have it.

---

## Why this is different from idea-validation and market-research

`idea-validation` and `market-research` are excellent when you already have an idea — they map its territory and stress-test it. But both assume the idea exists.

`opportunity-mapping` is for when you *don't* have the idea yet — or when you have a few directions and need to know which one fits **you**. It inverts the starting point: the founder is the input, the idea is the output. And it makes **distribution fit** a first-class part of the score, because the hardest lesson in solo building is that a great product on a channel you can't reach is an invisible product.

| Skill | Starts from | Answers |
|---|---|---|
| **opportunity-mapping** | the founder | "what should I build, given who I am and how I can reach people?" |
| market-research | one idea | "what's the territory around this idea?" |
| idea-validation | one idea | "is this idea worth building?" |

---

## Three modes, one funnel

| Mode | When to use | Output |
|---|---|---|
| **explore** | No idea yet — start from the profile, see the field | No heavy web search — 8–12 opportunities generated, filtered by constraints, ranked by fit with calibrated confidence |
| **focus** | Have a field or 2–3 candidates — narrow with evidence | Web research — competitors, dead products, channel reality per candidate; **signals you when to turn on deep research** |
| **pressure-test** | Nearly decided — stress it before committing | Targeted research — attacks the fit across all three axes, pre-mortem, strongest case against, re-scored verdict |

The modes form a funnel: **explore** opens the field, **focus** narrows it, **pressure-test** stresses it. Run one, or flow through all three. The skill infers which mode fits from where you are; one question only if it's ambiguous.

---

## What every output includes

- **Profile read** — your unfair advantage, reachable channels, learning goal, and constraints, restated so you can correct them
- **Opportunity space** — concrete, specific opportunities tied to *you* (never generic)
- **Fit Score 0–100** across four components — Founder Fit, Channel Fit, Market Pull, Build & Monetize Fit
- **Verdict** — `PURSUE` / `EXPLORE FURTHER` / `PASS`, with a hard override when Channel Fit is too low
- **Ranked shortlist** — the top picks, with why each fits you
- **Riskiest assumption + cheap test** — the one thing to check before building, and how to check it for almost nothing

---

## The fit rubric

Four components, 0–25 each, total 100:

1. **Founder Fit** — real unfair advantage, relevant expertise, and learning upside
2. **Channel Fit** — discoverability given your *actual* reach today (the decisive axis)
3. **Market Pull** — real, frequent, costly pain; demand; unsaturated space
4. **Build & Monetize Fit** — simple to build excellently solo + a compatible revenue path

**The override that defines the skill:** if Channel Fit ≤ 8, the verdict caps at `EXPLORE FURTHER` no matter how high the total — because a great product nobody can discover is a trap, and the rubric is built to surface that trap, not hide it behind a high average.

---

## How to install

```bash
cp -r opportunity-mapping /your-project/.claude/skills/
```

---

## How to trigger

```
/map-opportunities
/mapear-oportunidades

# Natural language:
"I don't know what to build"
"help me find a product idea that fits me"
"what should I build given my background?"
"I have skills but no idea what to make"
"which of these directions fits me best?"
```

---

## Principles

**Start from the founder.** The same opportunity scores differently for different founders. Never evaluate an idea in the abstract — always against the specific profile on the table.

**Channel-fit doctrine.** Distribution is the first thing to check, not the last. "Build it and they'll come" is not a channel. Evaluate every opportunity against the founder's *real* reach, not an aspirational one.

**Advantage ≠ interest.** Wanting to learn X is a reason to choose, not an advantage in X. Real advantage is what *few* people have.

**Calibrated honesty.** Every claim carries a confidence marker — [High]/[Medium]/[Guess] in explore; a real source or [Inference] in focus and pressure-test. No invented numbers, ever.

**Mom Test on every signal.** Behavior over stated preference. Spreadsheets and manual workarounds are strong demand signals.

**"None of these fit" is a valid answer.** This skill has no obligation to crown a winner. If nothing fits well, the honest output is *why* — and what would change it. Pushing a weak-fit opportunity just to deliver something is the worst result.

**Adversarial by default.** A critical layer, not a cheerleader. Killing an idea cheaply, before the code, is a win for the method.

---

## File structure

```
opportunity-mapping/
├── SKILL.md                         ← entry point, founder-profile intake, mode routing
└── references/
    ├── fit-rubric.md                ← Founder × Market × Channel scoring + the Channel-Fit override
    ├── core-principles.md           ← the founder-first inversion, channel-fit doctrine, Mom Test
    ├── mode-explore.md              ← generate the field from the profile (no heavy search)
    ├── mode-focus.md                ← narrow with evidence (signals when to enable deep research)
    └── mode-pressure-test.md        ← stress-test the chosen direction across all three axes
```

---

## How it fits in the sequence

```
/map-opportunities  →  starts from the founder, produces a ranked, fitted shortlist (you are here)
       ↓
/market-research    →  maps the territory of the top pick
       ↓
/validate-idea      →  tests the riskiest assumption of the chosen idea
       ↓
/personas           →  defines exactly who you're building for
       ↓
/positioning        →  defines where you stand vs. what exists
       ↓
/prd                →  translates all of this into what to build
```

If you arrive at `market-research` or `idea-validation` without an idea — or with one that clearly doesn't fit your profile — start here first.

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohana-taís)
