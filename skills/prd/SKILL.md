---
name: prd
description: >
  Lean Product Requirements Document for solo builders — translates product thinking
  (market research, validation, personas, positioning) into a clear, buildable spec.
  Four sections: problem, solution, what to build (MVP scope), and what not to build.
  No technical implementation, no team workflow, no Confluence publishing.

  Trigger when the user invokes /prd; asks to "write a PRD", "define what to build",
  "create a spec", "document the product", or "what exactly should I build?". Also
  trigger when personas + positioning are defined and the natural next step is
  translating them into a build spec.

  This is the solo-builder version — lean, product-only, designed to be readable
  by a non-technical builder working with Claude Code. Not the enterprise version.

  Do NOT use for: feature-level specs (this is product level); technical architecture
  decisions; writing user stories in Jira format; Confluence-published team PRDs.
---

# PRD — Solo Builder Edition

The PRD is the document that answers: "What exactly am I building, for whom, and why
does this version (and not some other version) make sense to build first?"

It's written once per product or major phase, then used as context for every build
session. It's the document you hand Claude Code before starting a new feature.

## Language rule

**Always respond in the user's language.** If the user writes in Portuguese (including
Brazilian Portuguese), respond entirely in Portuguese — including all frameworks,
labels, tables, and section headers. The skill is written in English for GitHub
conventions; the experience should feel native to whoever is using it.

## The four sections (always, always all four)

```
1. Problem         →  Who has it, what triggers it, what they do today
2. Solution        →  What this product does, for whom, and why this version
3. MVP scope       →  Exactly what's in. User-observable, no technical detail.
4. Out of scope    →  Exactly what's not in this version, with a reason
```

Section 4 is mandatory. A PRD without an explicit out-of-scope is an invitation
to build everything. For solo builders: scope discipline is survival.

## Entry point: detect what upstream work exists

Before writing the PRD, read the conversation for what's been done:

**Ideal input (write a full PRD):**
- Personas: who, job statement, trigger, workaround
- Positioning: competitive alternatives, unique value, best-fit customers, category
- Validation: some evidence the problem is real

**Partial input (write with explicit gaps):**
- Has an idea + some research, but no formal personas or positioning
- Has done validation but not formal positioning work
- Has personas but is skipping positioning for now

**Minimal input (write a hypothesis PRD):**
- Has a product idea and wants to use the PRD to structure their thinking
- No prior skill work, but a strong mental model of the product

In all cases: write the PRD. Never block. Label missing context explicitly.

If context is thin, ask one question only before starting:

> "Before I draft this, tell me in 2–3 sentences: who is this for, what's the
> problem they have, and what does the MVP do? I'll build from there."

## What makes this PRD different from enterprise PRDs

| Enterprise PRD | Solo builder PRD |
|---|---|
| 9+ sections, personas, journeys, epics, glossary | 4 sections, tightly scoped |
| Publishes to Confluence for team alignment | Saves as .md, lives in the repo |
| Written at start of project, maintained over months | Written before build, updated per phase |
| Covers all personas and journeys | Covers the primary persona and primary job |
| Includes north star metric, product pillars | Includes one success condition |
| Designed for engineers reading alongside PM | Designed for builder + Claude Code reading together |

## What a solo builder PRD is NOT

- A technical spec (no API routes, no database schema, no component names)
- A feature backlog (no Jira tickets, no user stories in "As a... I want...")
- A business plan (no revenue projections, no market size)
- A pitch deck (no investor framing, no growth narrative)

The PRD is for building. It answers: "What exactly should I build first, and why?"

## Anti-superficiality principles

### 1. Problem section must name the trigger, not just the pain

"People struggle to organize their files" is not a problem statement.
"When a freelancer is invoicing a client for the third time and can't find the
original project brief, they lose 30 minutes and send the invoice late" is.

A trigger-grounded problem statement tells you:
- When the problem happens (context)
- How severe it is (loss, frustration, cost)
- What the behavioral signal is (late invoice = real consequence)

### 2. Solution section is product-level, never technical

What the product does for the user — in user terms.
Not how it does it.

Allowed: "The user can create a project folder and attach all related files to it"
Not allowed: "We'll use a Supabase storage bucket with folder-level RLS policies"

The PRD belongs to the product layer. Technical decisions live elsewhere.

### 3. MVP scope is about inclusion AND exclusion

The scope section has two parts: what's in, what's not.

What's in: a short list of user-observable capabilities. If the user can't see it
or do it, it's not in the PRD — it's an implementation detail.

What's not in (Section 4): at least 5 items with a one-line reason each.
Fewer than 5 suggests the scope thinking hasn't happened yet.

### 4. One success condition, not five metrics

How do you know the MVP worked? Name one primary signal.

Not: "We'll track DAU, retention, NPS, activation rate, and conversion."
Yes: "10 users complete the primary job at least twice in their first week."

The primary signal should be behavioral — something a user does, not something
a dashboard shows.

### 5. No technical content anywhere

Prohibited in all four sections:
- URL routes, API endpoints, REST verbs
- File, folder, function, component, class, hook names
- SQL, schema fields, query structures
- Library or framework names
- Architecture decisions, caching strategies, performance targets in technical units
- Code or pseudo-code

If you find yourself writing any of the above: stop and rewrite in user-observable terms.

## Execution flow

1. Read context — detect what upstream work exists
2. Address missing context if relevant (one question max, no lecture)
3. Draft all four sections
4. Validate: no technical content, out-of-scope has ≥5 items, problem has a trigger
5. Present the PRD with explicit labels for assumptions vs. evidence
6. End with next step

## Output structure

```
# PRD: [Product Name] — [Phase / MVP]

**Version:** 1.0
**Date:** [date]
**Stage:** [MVP / Phase 1 / Phase 2]

---

## 1. Problem

**Who:** [Primary persona — job statement if available]

**Trigger:** [The specific situation that makes the problem acute — not a feeling, an event]

**Today's workaround:** [What they do without this product]

**Cost of the workaround:** [Why the status quo is actually painful — time, money, anxiety, consequence]

---

## 2. Solution

**What it is:** [One paragraph — what the product does, for whom, in user terms]

**Why this version:** [Why this specific scope makes sense as the starting point]

**Primary persona:** [Who this version is built for]

**Not built for (yet):** [Who is explicitly out of scope for this version]

**One success condition:** [The behavioral signal that tells you the MVP worked]

---

## 3. MVP Scope

What a user can do in this version:

- [Capability 1 — user-observable, no technical detail]
- [Capability 2]
- [Capability 3]
- [...] (typically 4–8 items for an MVP)

---

## 4. Out of Scope (this version)

| Feature / capability | Why not now |
|---|---|
| [Item 1] | [Reason — "validated demand not yet", "increases complexity 10x", "different persona", etc.] |
| [Item 2] | [...] |
| [Item 3] | [...] |
| [Item 4] | [...] |
| [Item 5] | [...] |

---

## Assumptions to validate

- [Something assumed in this PRD that, if wrong, would change scope or direction]
- [...]

```

## Relationship with other skills

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

This is the last step in the product discovery sequence before building.
After the PRD: use it as context in every Claude Code session.

---

*Built from real solo product work — including a PRD that kept scope contained
through 4 months of building and prevented feature creep that would have killed the timeline.*
*Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem by [@ohanatais](https://github.com/ohanatais).*
