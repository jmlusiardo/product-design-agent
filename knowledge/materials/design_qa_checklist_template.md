<!-- knowledge/materials/design_qa_checklist.md -->
# Design QA Checklist — Standalone Reference
<!-- Reusable checklist. Copy into Notion, Confluence, Jira, Linear, or Figma. -->

## Pre-QA Setup
- [ ] Feature is deployed to staging
- [ ] Figma spec is open and current (confirm with designer)
- [ ] All states are documented in spec (default, hover, focus, active, disabled, loading, empty, error)
- [ ] Breakpoints are documented

---

## ✦ VISUAL
- [ ] Padding and margin match spec (all 4 sides per component)
- [ ] Elements align to grid/columns
- [ ] Colors use design tokens (no hardcoded hex)
- [ ] Text colors, backgrounds, borders match spec
- [ ] Font family, weight, size, line-height match spec
- [ ] Heading hierarchy is correct
- [ ] Text truncates with ellipsis at correct max-width
- [ ] Box shadows match token values
- [ ] Border radius is consistent with system
- [ ] Icons are correct size, variant, and weight
- [ ] Images render at correct ratio (no distortion)

## ✦ INTERACTION
- [ ] Hover state matches spec
- [ ] Focus state is visible and correct style
- [ ] Active/pressed state renders correctly
- [ ] Disabled state looks right and is non-interactive
- [ ] Loading states appear at correct moments
- [ ] Skeleton screens match loaded layout
- [ ] Transitions match spec (easing, duration)
- [ ] `prefers-reduced-motion` reduces/removes animation
- [ ] All interactive elements reachable by Tab key
- [ ] Enter/Space trigger correct actions
- [ ] Escape closes modals and overlays

## ✦ RESPONSIVE
- [ ] Layout shifts correctly at all breakpoints
- [ ] No elements overlap or get cut off
- [ ] Long strings wrap without breaking layout
- [ ] Touch targets ≥ 44×44px
- [ ] Images scale proportionally
- [ ] Navigation pattern correct on mobile

## ✦ ACCESSIBILITY
- [ ] Text contrast ≥ 4.5:1 in context (AA)
- [ ] UI components contrast ≥ 3:1
- [ ] Focus indicators visible in all states
- [ ] Heading structure logical (H1 → H2 → H3)
- [ ] Images have alt text (empty for decorative)
- [ ] Form fields have labels
- [ ] Error messages announced by screen reader
- [ ] No keyboard traps
- [ ] Axe DevTools scan passes (0 critical violations)

## ✦ CONTENT
- [ ] Copy matches spec exactly (labels, buttons, headings)
- [ ] Casing correct (Title Case vs Sentence case)
- [ ] No placeholder text remains
- [ ] Empty state renders correctly
- [ ] Error state shows correct message + recovery
- [ ] Long text tested (2× normal content)
- [ ] Numbers, dates, currencies format correctly

---

## Issue Log

| # | Screen/Component | Issue | Severity | Spec Link | Screenshot | Assigned |
|---|-----------------|-------|----------|-----------|------------|---------|
| 1 | | | P0/P1/P2/P3 | | | |
| 2 | | | | | | |

---

## Severity Guide
| Level | Definition |
|-------|-----------|
| **P0 Critical** | Broken, blocks core flow — do not ship |
| **P1 High** | Significant deviation, clearly noticeable — must fix before release |
| **P2 Medium** | Inconsistency or polish — fix in next sprint |
| **P3 Low** | Minor tweak — backlog |

---

## Sign-Off
- Reviewer: _______________________
- Date: ___________________________
- Status: `[ ] Approved` `[ ] Approved with P3s` `[ ] Blocked`