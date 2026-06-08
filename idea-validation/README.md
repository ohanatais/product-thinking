# idea-validation

> The goal isn't to prove your idea is good. It's to find the single most dangerous assumption underneath it — and test that first, cheaply, before you write a line of code.

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

---

## What this skill does

Brutally honest, evidence-grounded validation of product and business ideas. Every session ends with a score, a verdict, a risk register, and the critical questions still open — never just an opinion.

Three modes of depth, chosen by how much rigor the moment calls for — not by how much time you feel like spending.

---

## Three modes, one interface

| Mode | When to use | Output |
|---|---|---|
| **quick** | Initial reaction, brainstorming, "is this worth researching further?" | No web search — reasoning + prior knowledge, with calibrated confidence per claim |
| **research** | Deciding whether to build, or quick mode revealed it's worth digging in | 6–10 sourced web searches, every market claim backed, facts separated from inferences |
| **deliverable** | Needs to share the analysis with a client, stakeholder, or investor | Everything in research mode, formatted for an external audience |

The skill infers the mode from how you ask. One question only if it's ambiguous.

---

## What every output includes

- **Score 0–100** across four components — Demand, Differentiation, Feasibility, Monetization
- **Verdict** — `BUILD` / `VALIDATE FIRST` / `KILL`, with three reasons behind it
- **Risk register** — Impact × Likelihood, 3–7 rows, always present
- **Top 3 critical questions** that need answers before moving forward
- **Pivot paths** — when the verdict is weak: 2–3 concrete reformulations, each naming what improves, why it fits the market, and what's lost

---

## How to install

```bash
cp -r idea-validation /your-project/.claude/skills/
```

---

## How to trigger

```
/validate-idea
/validar-ideia

# Natural language:
"validate this idea"
"is this worth building?"
"give me honest feedback on this"
"kill or build?"
"react to this PRD"
```

---

## Principles

**Calibrated honesty.** Every claim about market, competition, demand, viability, or monetization carries a confidence marker — [High], [Medium], [Guess] in quick mode; a real source or [Inference] in research and deliverable modes.

**"I don't know" is valid output.** No invented numbers — not for TAM, market share, willingness to pay, churn, or pricing. If there's no basis for a claim, the skill says so and names what research would be needed.

**Facts vs. inferences, always separated.** `Fact: [claim with source or confidence marker]` next to `Inference: [what this suggests — marked as my reading]`.

**Mom Test on every signal.** Generic praise is discarded. Specific behavior and pain — what people actually pay for, actually stopped using, actually built a workaround for — is what counts. Opinions are weak; behavior is strong.

**Adversarial by default.** This skill is a critical layer, not a cheerleader. Strong ideas get told they're strong, with evidence. Weak ideas get told they're weak, with evidence — and a constructive way forward.

---

## File structure

```
idea-validation/
├── SKILL.md                         ← entry point, mode routing, principles
└── references/
    ├── scoring-rubric.md            ← score components + verdict thresholds
    ├── mode-quick.md                ← fast reaction, no web search
    ├── mode-research.md             ← sourced analysis with web research
    └── mode-deliverable.md          ← formatted output for external audiences
```

---

## How it fits in the sequence

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

This skill checks for prior market research before it starts — and uses it as evidence instead of re-researching what you already know.

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohanatais)
