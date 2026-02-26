# UI Component Decision Trees / Árboles de Decisión para Componentes UI

**Task ID:** `ui_component_decision_trees`
**Archetype:** Playbook
**Agent:** `design_system_specialist`
**Sources:** Doctolib Design System, Workday Canvas, Lyft, NewsKit, Smashing Magazine (Vitaly Friedman, 2024)

---

## Executive Summary

Decision trees for UI components transform subjective design debates into systematic, documented choices. Instead of relitigating the same "modal vs. drawer" argument every sprint, teams codify the decision logic once — and reference it forever.

This guide covers the guiding principles, a full logic repository across six component categories, and a framework for building new trees from scratch. It serves as both a reference and a construction manual.

---

## Prerequisites

Before building a decision tree, confirm you have:

- [ ] A defined component category (forms, feedback, layout, loading, CTA, overflow)
- [ ] Access to your design system component inventory
- [ ] Agreement on binary (Yes/No) branching — no multi-branch forks
- [ ] Basic understanding of your product's user flows and interaction patterns

---

## Core Principles

These rules apply to every decision tree, regardless of component category.

**Atomic Decisions.** Every branch must be a binary Yes/No question. Avoid "sometimes" or "it depends" at branch nodes — that ambiguity belongs in the prerequisite context, not the tree.

**Context Over Aesthetics.** Component choice is driven by user flow priority (Primary Path vs. Secondary Path) and interaction urgency — not visual preference.

**The Commit Rule.** Distinguish between interactions that are *Instant* (change applies immediately → use Switch) and those that *Require Confirmation* (change needs explicit submit → use Checkbox). This single rule resolves most toggle-vs-checkbox debates.

**Scale Thresholds.** Use exact numerical thresholds to prevent subjective interpretation. Example: ≤5 options → Radio Group; >5 options → Select/Dropdown.

---

## Logic Repository: Six Component Categories

### A. Layout & Context (Doctolib)

**Root question:** Is this a blocking action?
```
Is it a BLOCKING action?
├── YES → Dialog
└── NO → Is it content-heavy?
    ├── YES → Drawer / Sidepanel
    └── NO → Modal
```

**Primary Path Rule:** If the user is on the primary conversion or task path, prefer full-page layouts or in-page entry points over overlays. Reserve overlays for secondary or supplemental interactions.

---

### B. Loading UX (Workday Canvas)

**Root question:** Can the system calculate progress?
```
Can system calculate % or time remaining?
├── YES → Progress Bar
└── NO → Is the layout known/fixed?
    ├── YES → Skeleton Loader
    └── NO → Is it a small, localized area?
        ├── YES → Spinner
        └── NO → Loading Dots
```

**Rule of thumb:** Skeleton loaders set clearer expectations than spinners — use them whenever the content shape is predictable.

---

### C. Selection & Forms (Doctolib / Lyft / Smashing)

**Root question:** Can the user select more than one option?
```
Multi-select?
├── YES → Needs visual emphasis?
│   ├── YES → Short labels? → YES: Pills | NO: Selectable Cards
│   └── NO → Checkbox Group
└── NO (single-select) → Count ≤ 5?
    ├── YES → Screen space available?
    │   ├── YES → Radio Group
    │   └── NO → Select / Dropdown
    └── NO (>5 options) → Select / Dropdown
```

**Dropdown as last resort.** Per Lyft's form tree: use dropdowns only when option count is high and labels are long. Prefer radio groups whenever space allows — they reduce interaction cost.

**Apply the Commit Rule here:** Single-option toggle that applies immediately → Switch. Single option requiring form submission → Checkbox.

---

### D. Feedback & Notifications (Workday Canvas)

**Root question:** Is this system-level or action-triggered?
```
System-level / Critical message?
├── YES → Banner
└── NO (action-triggered) → Self-dismissing required?
    ├── YES → Toast
    └── NO → User acknowledgement required?
        ├── YES → Dialog
        └── NO → Inline Alert
```

---

### E. Call to Action (CTA) Hierarchy (Workday Canvas)

No tree needed — apply this strict priority ladder:

| Priority | Condition | Component |
|----------|-----------|-----------|
| 1 | Most important action on screen | Primary Button |
| 2 | Destructive or irreversible | Danger / Red Button |
| 3 | Secondary supporting action | Secondary Button |
| 4 | Limited space or high repetition | Icon Button |

One Primary Button per view. If you have two competing "primary" actions, that's a hierarchy problem — resolve it before picking components.

---

### F. Text Overflow & Truncation (Workday Canvas)

**Root question:** Is the text critical for user comprehension?
```
Text critical for understanding?
├── NO → Truncation + Tooltip
└── YES → Is space constrained?
    ├── YES → Wrapping / Expandable Text
    └── NO → Show full text inline
```

---

## Tree Construction Framework

Use this sequence when building a new decision tree for a component category not listed above.

**Step 1 — Define the Root Node.** State the user's intent or the interaction type as a single question. Example: *"Is the user selecting one option or multiple?"*

**Step 2 — List all candidate components.** Pull from your design system inventory. Every component in scope must appear as a leaf node or be explicitly excluded with a reason.

**Step 3 — Identify the primary discriminator.** Find the one question that splits the candidate pool most cleanly. That's your root branch.

**Step 4 — Apply binary branching only.** If a branch has three outcomes, split it into two sequential Yes/No questions.

**Step 5 — Set scale thresholds explicitly.** Replace "few options" with exact numbers (e.g., ≤5). This eliminates subjective interpretation.

**Step 6 — Annotate each leaf node.** Include: component name, a one-line rationale, and one real UI example from your product or a reference system.

**Step 7 — Document exceptions.** Every tree has edge cases. List them separately — don't force exceptions into the tree logic itself.

**Step 8 — Publish and socialize.** A decision tree only works if it's visible. Embed it in your design system docs, Figma library, or team wiki. Make it the default reference in design reviews.

---

## Real-World Examples by Design System

| Design System | Trees Available |
|---------------|-----------------|
| **Doctolib Oxygen** | B2B navigation, form components, actions/CTAs, error design, help components |
| **Workday Canvas** | Notifications, errors & alerts, loading UX, calls to action, truncation/overflow |
| **Lyft** | Form controls (radio, checkbox, dropdown, toggle) |
| **NewsKit** | Onboarding component selection |
| **British Gas / Nucleus** | Design system contribution process flowcharts |

---

## Troubleshooting

**"We always end up overriding the tree in edge cases."**
Separate edge case logic from the main tree. Add an explicit "Exception Protocol" section so overrides are documented, not invisible.

**"The tree is too long and nobody uses it."**
Scope each tree to one component category. A 3-level tree with 6-8 leaf nodes is the practical ceiling for fast lookup.

**"Two designers get different answers from the same tree."**
Check for ambiguous branch questions. Any question that a reasonable person could answer differently needs a tighter definition or a numerical threshold.

**"We don't know where to start."**
Start with forms (the Lyft model) or notifications (the Workday model) — they're the highest-debate, highest-frequency decisions on most product teams.

---

## Checklist: Decision Tree Quality Review

- [ ] Every branch is a binary Yes/No question
- [ ] All candidate components appear as leaf nodes or are explicitly excluded
- [ ] Scale thresholds use exact numbers (not "few" or "many")
- [ ] The Commit Rule is applied to all toggle/checkbox decisions
- [ ] Each leaf node includes a rationale and a real UI example
- [ ] Edge cases are documented separately
- [ ] Tree is scoped to one component category
- [ ] Tree is published where designers actually work (Figma, Notion, Storybook)

---

## Cross-References

- `component_documentation.md` — Document selected components after tree decision
- `design_system_audit.md` — Audit existing components before building trees
- `design_token_management.md` — Ensure token consistency across component variants

---

## References
- Decision Trees For UI Components, by Vitaly Friedman: https://www.smashingmagazine.com/2024/05/decision-trees-ui-components/
- Choosing Form Components — Doctolib Oxygen Design System: https://oxygen.doctolib.design/60b411768/p/70925f-choosing-form-components
- B2B Navigation Patterns — Doctolib Oxygen Design System: https://oxygen.doctolib.design/60b411768/p/962135-b2b-navigation-patterns
- Notifications Decision Tree — Workday Canvas Design System: https://web.archive.org/web/20240118144833/https://canvas.workday.com/patterns/notifications/#tab=usage
- Loading UX Decision Tree — Workday Canvas Design System: https://web.archive.org/web/20240118144613/https://canvas.workday.com/patterns/loading/#tab=usage
- Calls to Action Decision Tree — Workday Canvas Design System: https://web.archive.org/web/20240118144311/https://canvas.workday.com/patterns/calls-to-action/#tab=usage
- A Better Segmented Control, by Runi Goswami (Lyft): https://medium.com/tap-to-dismiss/a-better-segmented-control-9e662de2ef57
- Choosing Onboarding Methods and Components — NewsKit (Figma Community): https://www.figma.com/community/file/1154728777780695374