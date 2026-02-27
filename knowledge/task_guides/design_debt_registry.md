# Design Debt Registry

## Executive Summary

Design debt is the accumulated cost of deferred, inconsistent, or unresolved design decisions across a product. Left unmanaged, it degrades user experience, slows design velocity, and increases engineering rework. A **Design Debt Registry** is a living backlog that names, classifies, prioritizes, and tracks debt items — turning invisible friction into actionable work.

This guide covers the full lifecycle: discovery → classification → registration → prioritization → remediation → prevention.

**When to use this task:**
- Product has grown rapidly and feels visually or behaviorally inconsistent
- Design system adoption is low or component drift is suspected
- Engineering frequently builds around design specs instead of from them
- Accessibility findings keep recurring without resolution
- Team wants to make a business case for "cleaning up" the product

**When NOT to use:**
- For a single, isolated bug fix — use your normal issue tracker
- As a substitute for a proper UX audit (run `ux_audit` first if you lack a baseline)
- When the team has no capacity to act on debt (registering without resolving creates frustration — time the effort with a debt-reduction sprint)

---

## Prerequisites

- Access to current product (live builds or latest designs)
- Reference to design system / component library (if exists)
- Prior audit findings (heuristic evaluation, token audit, accessibility audit) — optional but accelerates discovery
- Agreed classification taxonomy (see below)
- Stakeholder buy-in that debt is worth tracking

---

## Design Debt Taxonomy

### By Type

| Type | Description | Examples |
|------|-------------|---------|
| **Visual inconsistency** | Off-spec spacing, color, typography, elevation | Buttons using 4 different border radii across product |
| **Interaction pattern drift** | Multiple ways to do the same action | 3 different delete confirmation patterns |
| **Design system divergence** | Components built outside the system | Custom modals hardcoded with raw values instead of tokens |
| **Token misuse** | Hardcoded values instead of design tokens | `color: #1A73E8` instead of `$color-brand-primary` |
| **Accessibility gap** | WCAG violations or incomplete a11y implementation | Missing focus states, low contrast, no ARIA labels |
| **Unresolved research** | Known user pain points never addressed | "Users can't find X" documented in 3 research sessions, no design response |
| **Content/copy debt** | Outdated labels, inconsistent terminology, stale microcopy | Legacy feature renamed in product but not in 6 UI screens |
| **Documentation debt** | Components undocumented, design decisions unrecorded | 40% of components have no usage guidelines |

### By Severity

| Level | Definition | Action |
|-------|-----------|--------|
| **P0 — Critical** | Causes user failure, legal/accessibility violation, brand damage | Fix this sprint or next |
| **P1 — High** | Frequent user confusion, measurable conversion or satisfaction impact | Schedule within quarter |
| **P2 — Medium** | Inconsistency visible to careful users, slows design velocity | Backlog with target quarter |
| **P3 — Low** | Polish item, minor drift, cosmetic only | Fix opportunistically |

---

## Debt Discovery Methods

### Structured Audits
- **Heuristic walkthrough:** Walk core flows using Nielsen's 10 heuristics. Tag any violation as potential debt. (Cross-reference: `heuristic_evaluation`)
- **Token audit:** Scan for hardcoded values and design system divergence. (Cross-reference: `token_audit`)
- **Accessibility scan:** Use axe, Lighthouse, or manual keyboard/screen reader testing. Flag WCAG failures. (Cross-reference: `accessibility_audit`)
- **Component inventory:** List every UI component in production. Check each against the design system. Document drift.

### Signals from Adjacent Sources
- **Support tickets:** Cluster by theme. Recurring UX complaints signal unresolved debt.
- **Analytics anomalies:** High rage-click rates, unexpected drop-offs, or low task completion on specific screens.
- **User feedback tags:** Sort NPS verbatims or session recording observations for "confusing," "broken," "different."
- **Engineering retros:** Developers flag places where specs are ambiguous or implementation required workarounds.
- **Design reviews:** When a designer says "this is a workaround" — that's debt being created in real time.

### Quick Triage: The 5-Minute Debt Scan
For each major screen or flow, ask:
1. Does this match the design system? (component, token, spacing)
2. Is this interaction consistent with how we handle the same action elsewhere?
3. Is there a documented user pain point here that hasn't been addressed?
4. Does this pass basic accessibility checks?
5. Is the content/copy still accurate and on-brand?

Any "no" answer is a candidate for the registry.

---

## Step-by-Step Procedure

### Step 1 — Set Up the Registry

Create a registry document or spreadsheet (see `design_debt_registry_template.md`) with the following fields per item:

| Field | Description |
|-------|-------------|
| `ID` | Unique identifier (e.g., DD-001) |
| `Title` | Short descriptive name |
| `Type` | From taxonomy above |
| `Severity` | P0–P3 |
| `Description` | What is wrong and why it matters |
| `Location` | Screen, component, or flow affected |
| `Discovery source` | How it was found |
| `Impact` | User/business effect (brief) |
| `Effort` | S/M/L/XL (relative fix complexity) |
| `Owner` | Designer or team responsible |
| `Status` | Open / In Progress / Resolved / Won't Fix |
| `Target sprint/quarter` | When to address |
| `Notes` | Dependencies, related items, links |

### Step 2 — Run Discovery Audit

Use the methods above. Timebox to 1–2 days for initial population. Aim for breadth over depth — you can add detail later. Invite engineering to co-discover: they often know about the workarounds.

### Step 3 — Classify and Score

For each item: assign Type, Severity, and Effort. Then apply **ICE scoring** for prioritization:
```
ICE Score = Impact (1–10) × Confidence (1–10) × Ease (1–10)
```

- **Impact:** How much does fixing this improve user experience or reduce rework?
- **Confidence:** How certain are we this is actually causing harm?
- **Ease:** How easy is the fix? (Ease = inverse of Effort)

Sort the registry by ICE score descending. This becomes your prioritized debt backlog.

### Step 4 — Build the Business Case

For P0/P1 items requiring dedicated sprint time, frame the case:

> "Fixing [debt item] will reduce [specific friction/cost]. Without it, every sprint we build on top of [inconsistency/violation], compounding future fix cost. Estimated effort: [S/M/L]. Expected outcome: [metric improvement or risk reduction]."

Tie to: conversion rate, CSAT, NPS, accessibility compliance %, engineering rework hours, or onboarding time.

### Step 5 — Integrate with Agile Workflow

Three integration patterns:

1. **Debt sprints:** Dedicate 1 sprint per quarter exclusively to debt reduction (works well for large P1/P2 backlogs)
2. **10% rule:** Reserve 10% of each sprint's capacity for debt items (sustainable, prevents accumulation)
3. **Opportunistic:** Fix debt items when working in the same screen/component as a feature (no overhead, good for P3)

Tag debt items in Jira/Linear with a `design-debt` label. Link to feature tickets when opportunistic fixing is appropriate.

### Step 6 — Track Health Metrics

Review quarterly. Measure:

| Metric | How to measure |
|--------|---------------|
| Total open debt items by severity | Count in registry |
| Debt resolution rate | Items closed / items added per quarter |
| Design system coverage % | DS components used / total UI components |
| Accessibility compliance % | WCAG AA passing / total screens |
| Debt age | Average days open per severity level |
| New debt introduction rate | Items added per sprint or release |

A healthy product: P0 items → 0, P1 items → trend declining, DS coverage → >80%.

---

## Prevention Strategies

The best debt is debt never created.

- **Design reviews before handoff:** Catch inconsistencies at spec stage, not after build.
- **Design system contribution guidelines:** Document how/when to add components vs reuse existing.
- **Token linting:** Enforce token usage in code with ESLint rules or Stylelint. (Cross-reference: `token_audit`)
- **QA gates:** Include design consistency check in definition of done. (Cross-reference: `design_qa_checklist`)
- **Design Decision Records (DDRs):** When making intentional exceptions, document why. Prevents "why did we do this?" debt.
- **Regular audits:** Quarterly token + component audits catch drift before it compounds.

---

## Templates / Canvases

See `knowledge/materials/design_debt_registry_template.md` for:
- Debt item card template
- Full registry table (CSV-compatible)
- Health scorecard baseline

**Quick debt item card format:**
```
## DD-[number]: [Title]
- **Type:** [Visual / Interaction / System / A11y / Research / Content / Docs]
- **Severity:** P[0-3]
- **Location:** [Screen or component]
- **What's wrong:** [1-2 sentences]
- **Impact:** [User/business effect]
- **Effort:** [S/M/L/XL]
- **ICE Score:** [n]
- **Owner:** [@name]
- **Status:** Open
- **Target:** Q[n] [Year]
```

---

## Business Case Template
```
## Design Debt Business Case: [Item or Cluster Name]

**Problem:**
[Current state and why it's a problem — be specific about user/business impact]

**Evidence:**
- [Support tickets, analytics data, user quotes, audit findings]

**Cost of inaction:**
[Every sprint we don't fix this, X happens — compounding cost described]

**Proposed resolution:**
[What the fix looks like — design and engineering effort estimate]

**Expected outcome:**
[Metric improvement, risk reduction, or velocity gain]

**Effort:** [T-shirt size or story points]
**Dependencies:** [Engineering, content, legal, etc.]
```

---

## Common Mistakes and Anti-patterns

**Registering without prioritizing.** A registry of 200 P2 items with no ICE scores just creates anxiety, not action. Always prioritize before sharing.

**Conflating debt with features.** "We should redesign this whole section" is a feature, not debt remediation. Debt items should be fixable within the existing product structure.

**Treating debt as shameful.** Debt isn't failure — it's the natural cost of shipping under constraints. Frame it neutrally with stakeholders.

**Never-ending discovery without action.** Timebox discovery. A 70% complete registry that drives action beats a 100% complete registry that doesn't.

**No ownership.** Every item needs an owner. Unowned debt doesn't move.

---

## FAQ

**Q: How is design debt different from a UX audit?**
A UX audit (see `ux_audit`) is a point-in-time evaluation that *discovers* issues. A design debt registry is an ongoing system that *tracks and manages* those issues over time. The audit feeds the registry.

**Q: Should design debt live in the engineering backlog or separately?**
Both. Maintain a design-owned registry for visibility and prioritization. Mirror high-priority items into the engineering backlog (Jira/Linear) for sprint planning.

**Q: How do we handle debt in a product with no design system?**
Start with a visual audit — catalog inconsistencies as debt items. Use the registry as motivation and evidence to build the case for a design system. The debt registry becomes your design system roadmap input.

**Q: What's a realistic cadence for debt reduction?**
10% of sprint capacity or one dedicated debt sprint per quarter is sustainable. Reserve 100% debt sprints for critical remediation events (e.g., post-rebrand, post-accessibility audit).

**Q: How granular should debt items be?**
Granular enough to assign to one person and complete in one sprint. "Inconsistent spacing" is too broad. "Standardize card component padding to 16px across 6 screens in Settings" is a debt item.

**Q: When should we mark debt as "Won't Fix"?**
When the product area is scheduled for deprecation, when the fix cost exceeds realistic benefit, or when a competing constraint (legacy system, legal requirement) prevents it. Document the reason.

---

## Related Tasks / Cross-References

| Task | Relationship |
|------|-------------|
| `token_audit` | Surfaces design system token debt — primary input for System Divergence items |
| `ux_audit` | Heuristic findings seed debt registry — run first for baseline |
| `heuristic_evaluation` | Deep-dive evaluation that produces debt candidates |
| `agile_lean_ux_frameworks` | Debt integration with sprint planning and UX backlog management |
| `design_qa_checklist` | Post-release QA findings that create new debt items |
| `accessibility_audit` | Surfaces accessibility debt — feeds A11y Gap items in registry |
| `component_documentation` | Documentation debt tracked and resolved through this guide |

---

## References

- Design Debt: The Hidden Cost of Shortcuts in UX Design, NNGroup: https://www.nngroup.com/
- Managing Design Debt, Brad Frost: https://bradfrost.com/blog/post/managing-design-debt/
- The Shape of Design Debt, Figma Blog: https://www.figma.com/blog/
- Design System Health Metrics, Atlassian Design: https://atlassian.design/
- ICE Scoring Model for Prioritization: https://www.productplan.com/glossary/ice-scoring-model/
- Measuring Design System Adoption, Sparkbox: https://sparkbox.com/foundry/design_system_adoption_tracking