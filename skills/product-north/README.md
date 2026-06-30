# product-north

> The product-director brain that lives before the code — it pushes back by default, studies the real thing, and ends on a decision you can act on.

Part of the [product-discovery](https://github.com/ohanatais/product-discovery) skill set, within the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

---

## What this skill does

Most planning tools accept more than they question. `product-north` is the opposite: a Senior PM / Product Director who **pushes back by default**, studies your real code, data, and docs before giving an opinion, and speaks the language of product and business — not architecture.

It's the messy, strategic thinking that happens *before* the spec and the code: is this the right problem? Is it worth building? What does it break? How do I launch it? It produces the thinking that makes the spec and the code good — and it ends where the build spec begins.

This is the orchestrator of the discovery set. It can route into the other skills here (`/positioning`, `/personas`, `/prd`) and out to your build and go-to-market process — but on its own it does one thing: think a product decision all the way through, with a contrarian on the other side of the table.

---

## Six modes

```
explore    →  pure discovery: JTBD, tensions, hypotheses. No solution yet.
frame      →  real options, honest trade-offs, a recommendation with conviction
stress     →  devil's advocate: pre-mortem, second-order effects, retention risk
prototype  →  a navigable, low-fi visual prototype to compare directions
gtm        →  positioning, narrative, channel, build-in-public launch, success metric
decide     →  a durable decision record + a handoff to what comes next
```

You can start anywhere. The usual entry is `explore` (a new topic) or `frame` (a problem already named).

---

## The operating contract (every mode)

1. **Push back by default** — name the assumption, the second-order risk, and the steelman of the opposite path *before* recommending. If you can't steelman the opposite, you don't understand the problem yet.
2. **Evidence before opinion** — read the code, data, and docs before opining. Opinion without evidence is hallucination with confidence.
3. **Product language, not engineering** — lead with adoption, activation, retention, value, revenue. Not libraries and schema.
4. **Name the lens** — when you use a framework (JTBD, Kano, RICE, Hooked, PMF...), name which one and why, so you learn the reasoning, not just the conclusion.
5. **Anchor to the current core goal** — every recommendation ties to the one objective that matters right now.
6. **End actionable** — a clear recommendation or a decision record. Never just "it depends."

---

## How it fits in the flow

```
  product-north          ← the strategic thinking (you are here)
  explore → frame → stress → prototype → gtm → decide
       │
       ▼  (decision record in docs/decisions/)
  /prd  →  build spec     ← what to build, for whom, why this version
       │
       ▼
  design / build / launch ← production UI, code, and go-to-market
```

It **ends where the build spec begins.** When the thinking is mature, it hands off explicitly — usually to `/prd`, sometimes to `/positioning` (for the full canvas) or your go-to-market step.

---

## How to install

```bash
cp -r product-north /your-project/.claude/skills/
```

Or install the whole set as a plugin marketplace:

```
/plugin marketplace add ohanatais/product-discovery
/plugin install product-discovery@product-discovery
```

---

## How to trigger

```
/product-north

# Natural language:
"is X worth building?"
"what's the best path to Y?"
"how do I increase retention?"
"does this solve the right problem?"
"help me decide between A and B"
"I need a devil's advocate on this idea"
"how do I launch / position this?"
```

---

## File structure

```
product-north/
├── SKILL.md                  ← entry point, operating contract, mode routing
└── references/
    ├── explore.md            ← pure discovery (JTBD, tensions, hypotheses)
    ├── frame.md              ← options + trade-offs + recommendation
    ├── stress.md             ← devil's advocate (pre-mortem, steelman)
    ├── prototype.md          ← navigable low-fi visual prototype
    ├── gtm.md                ← positioning, narrative, launch, metric
    ├── decide.md             ← durable decision record + handoff
    └── lenses.md             ← the framework library (load on demand)
```

---

## Language

Written in English for GitHub conventions; **responds in your language.** Write to it in Portuguese and the whole experience — frameworks, tables, headers — comes back in Portuguese.

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohanatais)
