# Design Handoff Spec Generator

> **Executive Summary** — A design handoff spec is the complete translation package from design intent to buildable code. It documents every visual property, interaction state, responsive behavior, and accessibility requirement a developer needs to implement a feature without guessing. This guide covers the full workflow: from pre-handoff readiness checks through accessibility annotations, with checklists, templates, and common failure patterns to avoid.

---

## Overview

- **Purpose:** Produce developer-ready specification documents that eliminate ambiguity and reduce back-and-forth between design and engineering
- **Audience:** Product designers, design leads, design system contributors
- **Success Criteria:** Developer can implement the feature end-to-end with zero clarification requests; QA passes visual and functional review on first pass
- **Estimated Time:** 2–6 hours per feature flow depending on complexity

---

## When to Use / When NOT to Use

### Use this task when:
- A feature is approved and ready for engineering sprint planning
- Handing off to a new engineer unfamiliar with the design system
- Documenting a complex interactive component or multi-screen flow
- No dedicated handoff tool (Figma Dev Mode, Zeplin) is available or accessible to devs
- Compliance or audit requires written specification records

### Do NOT use this task when:
- Design is still exploratory (hand off after stakeholder sign-off only)
- The feature uses 100% pre-built design system components with no custom logic (link to component docs instead)
- You're documenting a design system component itself (use `component_documentation.md` workflow)

---

## Prerequisites

Before writing the spec:

- [ ] Design approved by product, legal, and relevant stakeholders
- [ ] All screens marked "Ready for Development" in Figma (or equivalent tool)
- [ ] Design tokens applied consistently (run `token_audit` if uncertain)
- [ ] Prototype linked showing key user flows
- [ ] Edge cases identified with product/engineering
- [ ] Copy finalized or placeholder guidelines defined

---

## Step-by-Step Procedure

### Step 1 — Build the Component Inventory

List every component and screen in scope. For each, document:

| Property | What to include |
|---|---|
| Component name | Match Figma layer name or design system name |
| Design system reference | Link to component doc or Storybook story |
| Custom variants | List any non-standard modifications |
| Responsive behavior | Note if component changes at any breakpoint |

**If using Figma Dev Mode or Zeplin:** These tools auto-generate spacing, color, and typography specs. Your job is to add context: the *why*, edge cases, and anything the tool can't infer.

**If no tooling:** Export annotated screenshots and document each property manually using the spec template below.

---

### Step 2 — Document All Interaction States

Every interactive element must have every applicable state documented. Use the master state checklist.

#### Master UI State Checklist

**Visual / Resting States**
- [ ] Default / Resting
- [ ] Hover (desktop only)
- [ ] Focus (keyboard navigation — must show visible focus indicator)
- [ ] Active / Pressed
- [ ] Visited (links)
- [ ] Selected / Checked

**Availability States**
- [ ] Disabled (non-interactive; document visual treatment + whether tooltip explains why)
- [ ] Read-only (visually different from disabled)
- [ ] No permission / Locked (document what user sees and what action is available)

**Process States**
- [ ] Loading / Pending (skeleton screen, spinner, or progress indicator — specify which)
- [ ] Submitting (form/button during async operation)
- [ ] Success / Confirmation (timing, auto-dismiss vs. persistent)
- [ ] Error — Inline (field-level; adjacent to the element)
- [ ] Error — Toast / Snackbar (system-level; specify position, duration, dismiss behavior)
- [ ] Error — Page-level / Full-screen (blocking errors, server failures)

**Data States**
- [ ] Empty / Zero-data (first time or no results — document illustration, CTA, and messaging)
- [ ] Partial data (some items loaded, others pending)
- [ ] Overflow / Truncation (what happens when content exceeds container — ellipsis? expand? scroll?)

**Context States**
- [ ] First-use / Onboarding (tips, tooltips, coach marks — specify trigger condition)
- [ ] Offline / Degraded (what's shown when connectivity is lost)
- [ ] Maintenance (scheduled downtime messaging)
- [ ] Timeout (session or operation timeout behavior)

**Responsive States**
- [ ] Mobile (≤767px)
- [ ] Tablet (768–1023px)
- [ ] Desktop (≥1024px)
- [ ] Wide / XL (≥1440px, if applicable)

For each state, document: **visual appearance** (screenshot or description) + **trigger condition** + **exit condition** (what ends the state).

---

### Step 3 — Responsive Specification

For each screen/component, create a breakpoint behavior table:

| Element | Mobile (≤767px) | Tablet (768–1023px) | Desktop (≥1024px) |
|---|---|---|---|
| Navigation | Bottom tab bar | Sidebar collapsed | Sidebar expanded |
| Card grid | 1 column | 2 columns | 3 columns |
| CTA button | Full width | Auto width | Auto width |
| Hero image | 16:9 ratio | 16:9 ratio | Fixed 480px height |
| Data table | Horizontal scroll | Horizontal scroll | Full visible |

**Also document:**
- Fluid vs. fixed layout behavior between breakpoints (does the layout scale linearly or snap?)
- Content priority changes (what gets hidden or collapsed at smaller sizes)
- Touch target sizes: **44×44px minimum** on all interactive elements at mobile breakpoints
- Text size adjustments (never below 16px body text on mobile)
- Gesture support required (swipe, pinch-to-zoom, long press)

---

### Step 4 — Accessibility Annotations

Accessibility must be documented explicitly in every handoff spec — it cannot be assumed.

#### Required Accessibility Annotations

**Semantic Structure**
- [ ] Heading hierarchy (H1 → H2 → H3; never skip levels)
- [ ] Landmark regions: `<main>`, `<nav>`, `<header>`, `<footer>`, `<aside>` — note where each applies
- [ ] List semantics for nav items, card grids, option lists

**ARIA Roles and States** (document for custom components only — native HTML elements have built-in roles)

| Component | ARIA Role | ARIA States to Document |
|---|---|---|
| Custom dropdown | `role="combobox"` | `aria-expanded`, `aria-controls`, `aria-activedescendant` |
| Tab panel | `role="tablist"` + `role="tab"` | `aria-selected`, `aria-controls` |
| Modal dialog | `role="dialog"` | `aria-modal="true"`, `aria-labelledby`, `aria-describedby` |
| Toggle switch | `role="switch"` | `aria-checked` |
| Alert/notification | `role="alert"` or `role="status"` | `aria-live` value (polite vs assertive) |
| Loading indicator | `role="progressbar"` | `aria-valuenow`, `aria-valuemin`, `aria-valuemax` |
| Icon-only button | `role="button"` | `aria-label` (required — describe the action, not the icon) |

**Keyboard Navigation**
Document the complete keyboard interaction model for every interactive component:

| Key | Expected behavior |
|---|---|
| Tab / Shift+Tab | Move between focusable elements |
| Enter / Space | Activate button, open dropdown, check checkbox |
| Arrow keys | Navigate within composite widgets (menus, tabs, sliders) |
| Escape | Close modal, dismiss dropdown, cancel action |
| Home / End | Jump to first/last item in list or menu |

Note: Follow WAI-ARIA Authoring Practices Guide (APG) patterns. Link: https://www.w3.org/WAI/ARIA/apg/patterns/

**Focus Management**
- [ ] Document focus destination when modal opens (first interactive element or modal title)
- [ ] Document focus trap inside modals and drawers
- [ ] Document focus return point when modal closes (the trigger element)
- [ ] Specify `tabindex` requirements for custom interactive elements

**Visual Accessibility**
- [ ] Color contrast: text must meet 4.5:1 (AA) or 7:1 (AAA); UI components and states must meet 3:1
- [ ] Focus indicator must be visible and meet 3:1 contrast against adjacent colors
- [ ] Do not rely on color alone to convey state (add icon, text, or pattern)
- [ ] Alt text decisions: decorative images → `alt=""`, informative → descriptive `alt` text, functional → describe the action

**Screen Reader Announcements**
- [ ] Document live regions: when does the page announce dynamic content? (`aria-live="polite"` or `aria-live="assertive"`)
- [ ] Error messages: must be announced when triggered — use `aria-describedby` linking to error text
- [ ] Success confirmations: document timing and announcement method
- [ ] Loading states: specify what screen readers announce during async operations

---

### Step 5 — Assets Inventory

| Asset | Format(s) | Size | Naming Convention | Notes |
|---|---|---|---|---|
| App icon | PNG, SVG | 16, 32, 64, 128, 256px | `icon-{name}-{size}.png` | |
| Hero illustration | SVG, WebP | As designed | `illustration-{name}.svg` | Include @2x |
| Product photos | WebP, AVIF | 400w, 800w, 1200w | `photo-{name}-{w}w.webp` | Responsive srcset |
| UI icons | SVG | 16, 24px | `icon-{name}-{size}.svg` | Stroke icons export at 1x |
| Brand logo | SVG, PNG | — | `logo-{variant}.svg` | light, dark, mono variants |

**Export requirements to specify:** pixel density (1x, 2x, 3x), file format per platform (SVG for web, PDF for iOS, XML for Android), background treatment (transparent vs. white), color mode variants (light/dark).

---

### Step 6 — Open Questions Log

Capture unresolved decisions that need engineering or product input before or during development:

| # | Question | Owner | Priority | Resolved? |
|---|---|---|---|---|
| 1 | What's the API response for partial data on the dashboard? | Engineering | High | ☐ |
| 2 | Is the offline state cached content or error only? | Product | Medium | ☐ |
| 3 | Confirm animation duration with motion guidelines | Design lead | Low | ☐ |

---

## Spec Canvas / Template

Use this as the starting structure for any handoff document:
```
# [Feature Name] — Design Handoff Spec
**Designer:** [Name]  
**Date:** [YYYY-MM-DD]  
**Version:** 1.0  
**Figma Link:** [URL]  
**Prototype Link:** [URL]  
**Status:** Ready for Development

---

## Scope
[What's included. What's explicitly out of scope.]

## Component Inventory
[Table: component name → design system ref → custom notes]

## State Documentation
[Per component: all applicable states from master checklist]

## Responsive Specification
[Breakpoint table per screen/component]

## Accessibility Annotations
[ARIA, keyboard, focus management, screen reader notes]

## Assets
[Export table]

## Animation & Micro-interaction Specs
[Timing, easing, triggers per interaction]

## Content Rules
[Character limits, truncation, placeholder text, empty state copy]

## Open Questions
[Log table]
```

---

## Common Mistakes and How to Avoid Them

**Mistake 1: Handing off only the happy path**  
→ Fix: Before writing the spec, explicitly ask: "What can go wrong?" Run through the state checklist for every component.

**Mistake 2: Using hard-coded values instead of tokens**  
→ Fix: Run a token audit before handoff. Every color, spacing, and typography value should reference a token name, not a hex code or pixel value.

**Mistake 3: Skipping accessibility annotations**  
→ Fix: Treat ARIA and keyboard behavior as required spec sections, not optional extras. Flag accessibility as a blocking item in the open questions log if unresolved.

**Mistake 4: Responsive specs only at 3 breakpoints without describing the in-between**  
→ Fix: Specify whether layout is fluid (scales proportionally) or snaps (fixed widths). Fluid layouts need min/max width constraints documented.

**Mistake 5: Annotating design intent but not developer implementation guidance**  
→ Fix: For complex interactions, add a "How to implement" note alongside the visual description. E.g., "This uses a CSS sticky header at scroll position > 64px."

**Mistake 6: Creating the spec after stakeholder review has closed**  
→ Fix: Create a draft spec outline before final review so stakeholders can flag edge cases during review rather than in dev.

---

## Handoff Workflow
```
1. Design approval ← stakeholder review
2. Pre-handoff checklist (tokens, states, assets)
3. Write spec (this task)
4. Sync meeting: walk engineering through the spec (30–60 min)
5. Engineer reviews spec, files open questions
6. Spec updated with answers
7. Development begins
8. Design QA during implementation → see design_qa_checklist.md
```

---

## FAQ

**Q: Do I need a handoff spec if we use Figma Dev Mode?**  
A: Figma Dev Mode handles visual specs (spacing, colors, typography) well, but it can't document interaction states, accessibility requirements, responsive logic, or the reasoning behind design decisions. You still need supplementary documentation for these.

**Q: How detailed should animation specs be?**  
A: At minimum: duration (ms), easing function (ease-in-out, spring, linear), delay, and what triggers/ends the animation. Reference your motion design system tokens where available.

**Q: Who owns the open questions log?**  
A: The designer owns the log and is responsible for getting questions answered before or at the start of the engineering sprint.

**Q: Should I include copy in the handoff spec?**  
A: Yes — include finalized strings, placeholder text, validation messages, empty state copy, and any character limits. Link to the content style guide if applicable.

**Q: What if a state wasn't designed yet?**  
A: Flag it in the open questions log immediately. Never let a state go undocumented into development — engineers will make arbitrary decisions without guidance.

**Q: When is the spec "done"?**  
A: When all state checklist items are addressed (even if the answer is "this state doesn't apply"), accessibility annotations are complete, and the open questions log has no unresolved High-priority items.

---

## Cross-Guide References

### Related Task Guides
- **Component Documentation:** `component_documentation.md` — Use when creating system-level documentation for reusable components; handoff spec references component docs rather than duplicating them
- **UX Audit:** `ux_audit.md` — Run UX audit before handoff to catch usability issues that would become dev debt
- **Style Guide / Design System:** `style_guide.md` — All visual specs in handoff should reference the style guide; the handoff spec applies the style guide to a specific feature
- **Token Audit:** `token_audit.md` — Run before handoff to ensure all design tokens are consistent and correctly applied; findings feed directly into the handoff spec
- **Design QA Checklist:** `design_qa_checklist.md` — The handoff spec defines what was designed; the QA checklist verifies the build matches it

### Support Materials
- **Handoff Spec Template:** `handoff_spec_template.md` — Copy-paste canvas for starting a new spec document

---

## References

- Guide to Developer Handoff in Figma: https://www.figma.com/best-practices/guide-to-developer-handoff/
- Design Handoff 101, Zeplin Gazette: https://blog.zeplin.io/design-handoff-101-how-to-handoff-designs-to-developers
- Accessibility Annotations for Design to Dev Handoff, Knowbility: https://knowbility.org/programs/john-slatin-accessu-2023/live-accessibility-annotations-for-design-to-dev-handoff
- A Designer's Guide to Documenting Accessibility, Stéphanie Walter: https://stephaniewalter.design/blog/a-designers-guide-to-documenting-accessibility-user-interactions/
- WAI-ARIA Authoring Practices Guide (APG): https://www.w3.org/WAI/ARIA/apg/patterns/
- 10 Annotation Examples for Clear Developer Handoff, UXPin: https://www.uxpin.com/studio/blog/10-annotation-examples-for-clear-developer-handoff/
- What Are Design Handoffs, IxDF: https://www.interaction-design.org/literature/topics/design-handoffs
- WCAG 2.1 Contrast Requirements: https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html