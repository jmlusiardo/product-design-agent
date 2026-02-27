# Design Debt Registry Template

---

## Registry Table

| ID | Title | Type | Severity | Location | Impact | Effort | ICE | Owner | Status | Target | Notes |
|----|-------|------|----------|----------|--------|--------|-----|-------|--------|--------|-------|
| DD-001 | [Example] Button variant inconsistency | Visual | P2 | Checkout flow | Low conversion clarity | S | 72 | @designer | Open | Q2 2025 | Affects 4 screens |
| DD-002 | [Example] Missing focus states on modals | A11y | P1 | All modals | WCAG 2.4.7 violation | M | 90 | @designer | In Progress | Q1 2025 | |
| DD-003 | [Replace with your items] | | | | | | | | | | |

---

## Debt Item Card Template
```
## DD-[number]: [Title]
- **Type:** Visual / Interaction / Design System / Token / A11y / Research / Content / Documentation
- **Severity:** P0 (Critical) / P1 (High) / P2 (Medium) / P3 (Low)
- **Location:** [Screen name, component, or user flow]
- **What's wrong:**
  [1–2 sentences describing the specific problem]
- **Impact:**
  [How this affects users or the business]
- **Discovery source:**
  [Audit / Analytics / Support tickets / Design review / User research]
- **Effort:** S (<4h) / M (1–3 days) / L (1 week) / XL (>1 week)
- **ICE Score:** [Impact × Confidence × Ease — max 1000]
- **Owner:** [@name or team]
- **Status:** Open / In Progress / Resolved / Won't Fix
- **Target:** Q[n] [Year] or Sprint [n]
- **Dependencies:** [Engineering, content, design system contribution, etc.]
- **Notes:** [Links, related tickets, edge cases]
```

---

## ICE Scoring Reference

| Score | Impact (1–10) | Confidence (1–10) | Ease (1–10) |
|-------|--------------|-------------------|-------------|
| 10 | Causes user failure / legal risk | Confirmed by multiple data sources | Fix in under 1 hour |
| 7 | Measurable UX degradation | Confirmed by 1 source | Fix in a day |
| 4 | Minor inconsistency | Assumed, not validated | Fix in a week |
| 1 | Polish only | Guessed | Requires major rework |

`ICE = Impact × Confidence × Ease`
Scores above 500 → strong candidates for next sprint. Below 200 → backlog.

---

## Health Scorecard Baseline

Complete this quarterly:

| Metric | Baseline (Q[n]) | Target | Current |
|--------|-----------------|--------|---------|
| Open P0 items | | 0 | |
| Open P1 items | | <5 | |
| Total open items | | | |
| Items resolved this quarter | | | |
| New items added this quarter | | | |
| Design system coverage % | | >80% | |
| Accessibility compliance % | | >95% WCAG AA | |
| Avg age of P1 items (days) | | <90 | |

---

## Debt Types Quick Reference

| Type | Keywords to watch for |
|------|----------------------|
| Visual | spacing, color, typography, icon, elevation, radius |
| Interaction | multiple ways to do X, inconsistent pattern, unexpected behavior |
| Design System | custom component, hardcoded value, off-spec, not in library |
| Token | hex value, raw pixel, hardcoded color/spacing |
| Accessibility | contrast, focus, keyboard, ARIA, screen reader, WCAG |
| Research | "users reported," "pain point," "known issue," unactioned findings |
| Content/Copy | outdated label, wrong name, inconsistent terminology |
| Documentation | undocumented, no usage guide, missing spec |