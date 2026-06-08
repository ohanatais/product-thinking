# Mode: Behavioral

You have evidence: interview notes, review data, community threads, support tickets,
or any real signal from real users. This mode extracts behavioral patterns from
that evidence and converts them into grounded persona cards.

## Before starting: inventory the evidence

List what's available and rate its quality:

| Evidence type | Quality | Why |
|---|---|---|
| Recorded interview transcripts | High | Verbatim, contextual |
| Your own interview notes | Medium-High | Filter for recall bias |
| Community posts (Reddit, Discord) | Medium | Real language, unprompted |
| App store / G2 / PH reviews | Medium | Filter for specificity |
| "People told me that..." | Low | Memory-filtered, ask what they said |
| Your own assumptions | Baseline | Valid starting point, label clearly |

Before analysis: note which evidence types are present and name the gaps.

## Protocol

### Step 1: Extract raw signals

Read through all evidence and extract raw behavioral signals. Don't interpret yet.
Organize as a flat list:

- [Quote or behavior] — [Source type] — [Confidence: High/Med/Low]

Apply Mom Test filter: discard generic praise, wish lists, hypotheticals.
Keep specific behavior, quantified frustration, revealed WTP, trigger language.

### Step 2: Cluster by pattern

Group signals by behavioral pattern — not by demographic similarity.

Common clusters to look for:
- People who share the same trigger moment
- People who use the same workaround
- People who express the same fear about switching
- People who define "good" the same way

Name each cluster by the behavior, not the demographic:
"The spreadsheet-stretched-to-breaking person" not "35-year-old professional."

### Step 3: Build persona cards from the top 2–3 clusters

For each cluster, build a persona card using the standard template. Tag every element:

- **[Evidence]**: direct from a quote or observed behavior
- **[Inference]**: your reading of the pattern
- **[Assumption]**: not in the data — needs validation

### Step 4: Surface contradictions

If the evidence shows conflicting patterns (some users want X, others want the
opposite), don't average them out. Name the contradiction and decide:
- Is this two different personas? (Probably yes)
- Is this ambivalence within one persona about a specific trade-off? (Possible)

Surface it as an open question.

## Output structure (behavioral mode)

```
## Evidence inventory
[What was analyzed, quality rating, notable gaps]

## Behavioral patterns identified
[Cluster names + brief description of each]

---

## Persona 1: [Functional label]

**Job statement:**
"When [situation], I want to [motivation], so I can [outcome]."
— [Evidence: quote or behavior that grounds this]

**Trigger moment:**
[Evidence-grounded description]
— [Evidence]

**Current workaround:**
[What they actually do] — [Evidence]

**Pains:**
- [Specific] — [Evidence/Inference]
- [...]

**Gains sought:**
[What hired looks like] — [Evidence/Inference]

**Their words** (if available):
> "[Direct quote from interview, review, or community post]"

**Assumptions still open:**
- [Element not confirmed by evidence — how to validate]

---

## Persona 2: [Functional label]
[Same structure]

---

## What the evidence doesn't tell us
[Named gaps — important questions the data doesn't answer]

## Suggested next step
[/positioning, /validate-idea, or "run 3 more interviews focused on X"]
```

## Anti-patterns

- Don't build 4+ personas from one evidence base — you're probably under-clustering
- Don't smooth over contradictions — name them
- Don't present inferences without labeling them
- Don't quote generic praise as evidence
- Don't skip the "evidence doesn't tell us" section — it's often the most useful part
