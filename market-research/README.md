# market-research

> Market research isn't about confirming your idea is good. It's about understanding the territory before you commit to it — who else is here, whether the space is crowded, and whether the market actually exists.

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

---

## What this skill does

Structured market research for solo builders — from a raw idea to a competitive map, an honest TAM/SAM/SOM, a red/blue ocean read, and a clear strategic implication.

It adapts to how familiar you are with the process. First time mapping a market: it walks you through it. Done it before: it moves fast. Have hypotheses already: it pushes back on them.

---

## Three modes, one interface

| Mode | When to use | Output |
|---|---|---|
| **guided** | First time doing market research | Step-by-step, with explanations of why each step matters |
| **direct** | Knows the territory, wants to move fast | Framework + web research + competitive map + TAM/SAM/SOM, no hand-holding |
| **expert** | Has hypotheses, wants critical pushback | Everything in direct + explicit challenge of assumptions + pre-mortem + strategic positioning read |

The skill detects which mode fits from how you describe the idea and what vocabulary you use. One question if it's ambiguous.

---

## What every output includes

- **Territory map** — who's playing, how they cluster, what they cover
- **Gap analysis** — what's NOT being done, and whether that gap is a feature or a market
- **TAM/SAM/SOM** — sized honestly, sources where available, explicit uncertainty where not
- **Red/blue ocean read** — is this crowded, or is there real white space?
- **Strategic implication** — one paragraph on what this means for what to build next
- **Next step** — explicit: `/validate-idea`, refine positioning, or proceed to PRD

---

## How to install

```bash
cp -r market-research /your-project/.claude/skills/
```

---

## How to trigger

```
/market-research
/pesquisa-mercado

# Natural language:
"research this market"
"who are my competitors?"
"is this a red ocean or a blue ocean?"
"how big is this market?"
"map this space for me"
```

---

## Principles

**Calibrated honesty.** Every claim about market size, competitor traction, or demand carries a confidence marker: [Confirmed], [Estimated], or [Inference]. Numbers are never invented — if a figure isn't findable, the skill says so.

**"I don't know" is valid output.** Better to name an unknown than fill it with a plausible-sounding guess. The goal is an accurate map, not a flattering one.

**Facts vs. inferences, always separated.** Every analytical claim is structured as `Fact: [...]` and `Inference: [...]`, so you always know what's evidence and what's reading.

**Mom Test applied to competitor signals.** Generic praise ("great app", "love it") is discarded. Behavioral evidence ("I pay $X/month because Y", "I stopped using it when Z happened") is what counts.

**No research theater.** The output supports a decision, not a report. Tables over prose, insight over summary, what to do next over what was found.

---

## File structure

```
market-research/
├── SKILL.md                         ← entry point, routing, principles
└── references/
    ├── core-principles.md           ← calibrated honesty, evidence hierarchy, Mom Test
    ├── mode-guided.md               ← first-timer walkthrough
    ├── mode-direct.md               ← fast-path framework + research
    └── mode-expert.md               ← challenge mode — pressure-tests hypotheses
```

---

## How it fits in the sequence

```
/market-research   →   maps the territory (you are here)
       ↓
/validate-idea     →   tests if the idea fits the territory
       ↓
/personas          →   defines who exactly you're building for
       ↓
/positioning       →   defines where you stand vs. what exists
       ↓
/prd               →   translates all of this into what to build
```

This skill feeds `/validate-idea`. If you haven't mapped the territory yet, this is the right place to start.

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohanatais)
