# positioning

> Positioning is not a tagline. It's the answer to: in a world where these alternatives exist, why would someone who cares deeply about this specific value choose this product?

Part of the [product-thinking](https://github.com/ohanatais/product-thinking) skill set, within the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

---

## What this skill does

Positioning definition for solo builders — grounded in April Dunford's five-component framework. Produces a positioning canvas that becomes the strategic foundation for messaging, copy, and product decisions.

Works in three modes: guided (working through it for the first time), canvas (has personas and research, wants the full canvas), and stress-test (has positioning, wants to find weaknesses before using it).

---

## The framework: five components, always in order

```
1. Competitive alternatives    →  What customers use if this doesn't exist
2. Unique attributes           →  What this product has that alternatives don't
3. Value                       →  What those attributes mean for customers
4. Best-fit customers          →  Who cares most about that value
5. Market category             →  The frame that makes that value obvious
```

The order is non-negotiable. Each component depends on the previous one. Work backwards from any step and the whole thing collapses.

---

## Three modes, one interface

| Mode | When to use | Output |
|---|---|---|
| **guided** | First time, or has context but never worked through positioning | Step-by-step with explanation of each component |
| **canvas** | Has personas + research, wants the canvas efficiently | Completed 5-component canvas + positioning statement |
| **stress-test** | Has positioning, wants to find weaknesses | Component-by-component challenge + verdict + revised canvas |

---

## What every output includes

- **Five-component canvas** — one row per component, filled
- **Positioning statement** — one paragraph, for internal alignment
- **Early-stage flag** — explicit note to keep positioning loose pre-PMF
- **What this positioning rules out** — who is NOT the best-fit customer
- **Open questions** — what would change this positioning if answered differently
- **Next step** — explicit: `/prd`, messaging, or "validate with 5 conversations"

---

## How to install

```bash
cp -r positioning /your-project/.claude/skills/
```

---

## How to trigger

```
/positioning

# Natural language:
"define my positioning"
"how do I stand out?"
"what makes this different?"
"how should I describe this product?"
"where do I fit in the market?"
```

---

## Principles

**Start with competitive alternatives, always.** The most common positioning mistake: starting with features and asking "who cares?" The correct path: start with alternatives and ask "what do we have that these don't?"

**"So what?" is the most important question.** After every unique attribute: "So what? What does this mean for the customer's life?" Until that's answered, you have a feature, not a value.

**Pre-PMF: big fish net, not tuna net.** Dunford's own advice: keep positioning loose until you see patterns in who loves the product and why. This skill outputs a thesis, not a verdict.

**Best-fit customers, not all customers.** Positioning for "anyone who could use this" produces messaging that resonates with nobody. Precision is not exclusion.

---

## File structure

```
positioning/
├── SKILL.md                              ← entry point, framework, principles
└── references/
    ├── core-principles.md                ← Dunford's five components in depth
    ├── mode-guided.md                    ← step-by-step walkthrough
    └── mode-canvas-and-stress-test.md    ← canvas (fast) + stress-test (challenging)
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
/positioning       →   defines where you stand vs. what exists (you are here)
       ↓
/prd               →   translates all of this into what to build
```

---

Part of the [build-from-zero](https://github.com/ohanatais/build-from-zero) ecosystem.

Made by [Ohana Taís](https://github.com/ohanatais) · [![LinkedIn](https://img.shields.io/badge/LinkedIn-ohanatais-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ohanatais)
