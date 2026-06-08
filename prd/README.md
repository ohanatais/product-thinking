# prd

> The PRD answers one question: what exactly am I building, for whom, and why does this version make sense to build first?

Part of the [pm-skills](https://github.com/ohanatais/pm-skills) ecosystem.

---

## What this skill does

Lean Product Requirements Document for solo builders. Translates everything from market research, validation, personas, and positioning into a clear, buildable spec — in four sections, nothing more.

It's the document you write once before building starts, and hand to Claude Code at the beginning of every session. It's not an enterprise PRD. It's not a backlog. It's not a pitch deck. It's a scope container.

---

## Four sections. Always all four.

```
1. Problem      →  Who has it, what triggers it, what they do today
2. Solution     →  What this product does, for whom, why this version
3. MVP scope    →  Exactly what's in — user-observable, no technical detail
4. Out of scope →  Exactly what's not in this version, with a reason
```

Section 4 is mandatory. A PRD without an explicit out-of-scope is an invitation to build everything. For solo builders: scope discipline is survival.

---

## What makes this different from enterprise PRDs

| Enterprise PRD | Solo builder PRD |
|---|---|
| 9+ sections, personas, journeys, epics | 4 sections, tightly scoped |
| Publishes to Confluence for team alignment | Saves as .md, lives in the repo |
| Covers all personas and journeys | Covers the primary persona and primary job |
| Includes north star metric, product pillars | Includes one success condition |
| Designed for engineers reading alongside PM | Designed for builder + Claude Code reading together |

---

## What every output includes

- **Problem section** with trigger (not just pain), workaround, and cost of status quo
- **Solution section** with one success condition — behavioral, not a dashboard metric
- **MVP scope** — 4–8 user-observable capabilities, zero technical content
- **Out of scope** — minimum 5 items with explicit reasons for deferral
- **Assumptions to validate** — what, if wrong, would change scope or direction

---

## How to install

```bash
cp -r prd /your-project/.claude/skills/
```

---

## How to trigger

```
/prd

# Natural language:
"write a PRD"
"define what to build"
"create a spec"
"what exactly should I build?"
"help me document the product"
```

Also triggers when personas + positioning are defined and the natural next step is translating them into a build spec.

---

## Principles

**Problem section must name the trigger, not just the pain.** "Users struggle with organization" is not a problem statement. "When a freelancer invoices a client for the third time and can't find the original brief, they lose 30 minutes and send the invoice late" is.

**Solution section is product-level, never technical.** What the product does for the user — in user terms. Not how it does it. No API routes, no database names, no library choices.

**One success condition, not five metrics.** The primary signal should be behavioral: something a user does, not something a dashboard shows.

**Out of scope with reasons.** Fewer than 5 items in Section 4 suggests the scope thinking hasn't happened yet. Each item needs a one-line reason: "validated demand not yet", "different persona", "increases complexity 10x".

---

## The PRD as Claude Code context

At the start of every build session:

> "Here's the PRD for this project: [paste PRD]. Today we're building [capability X from Section 3]. [Section 4 item Y] is explicitly out of scope."

This prevents Claude Code from adding unrequested features, making architectural guesses, or building a version that doesn't match the validated scope.

---

## File structure

```
prd/
├── SKILL.md                    ← entry point, four sections, principles
└── references/
    └── scope-discipline.md     ← common PRD failure modes + updating rules
```

---

## How it fits in the sequence

```
/market-research   →   maps the territory
       ↓
/validate-idea     →   tests if the idea fits the territory
       ↓
/personas          →   defines who exactly you're building for
       ↓
/positioning       →   defines where you stand vs. what exists
       ↓
/prd               →   translates all of this into what to build (you are here)
```

This is the last step before building. After the PRD: use it as context in every Claude Code session.

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohanatais)
