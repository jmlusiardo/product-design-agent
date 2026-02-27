# Accessibility Audit

## Executive Summary

An accessibility audit is a systematic review of a digital product against the Web Content Accessibility Guidelines (WCAG) 2.2. The goal is to identify barriers that prevent people with disabilities — including users of screen readers, keyboard-only navigation, switch access, or low vision tools — from using your product effectively.

**Standard target: WCAG 2.2 AA.** This is the legally required level in most jurisdictions (EU EAA 2025, ADA, Section 508, EN 301 549). AAA is best-effort. Level A is the floor, not the goal.

**Audits differ from ux_audit:** A UX audit assesses usability and heuristics. An accessibility audit assesses WCAG conformance. Both are valuable; they are not substitutes.

---

## When to Use / When NOT to Use

**Use when:**
- Preparing for regulatory compliance review (EU EAA 2025, VPAT, WCAG audit)
- Before a major product launch or release
- Onboarding a new component or design system addition
- After user reports of accessibility barriers
- As part of Design QA (post-implementation sprint review)
- During design phase, before a single line of code is written

**Don't use when:**
- You need a general usability review → use `ux_audit` or `heuristic_evaluation`
- You need a full QA pass across visual/interaction/content → use `design_qa_checklist`
- You need to document component specs → use `component_documentation`

---

## WCAG 2.2 Level Comparison

| Level | Criteria count | Required for... |
|-------|---------------|-----------------|
| **A** | 30 | Minimum baseline. Must pass before targeting AA. |
| **AA** | 50 (A + 20 more) | Legal standard in EU, US federal, most enterprise requirements. |
| **AAA** | 78 (AA + 28 more) | Best-effort. Not required for full-site compliance. |

### WCAG 2.2 — New Criteria vs. 2.1 (9 added, 1 removed)

| Criterion | Name | Level | What it means |
|-----------|------|-------|---------------|
| 2.4.11 | Focus Not Obscured (Min) | **AA** | Focused element must not be fully hidden by sticky headers/banners |
| 2.4.12 | Focus Not Obscured (Enhanced) | AAA | Not even partially hidden |
| 2.4.13 | Focus Appearance | **AA** | Focus indicator: area ≥ component perimeter, contrast ≥ 3:1 |
| 2.5.7 | Dragging Movements | **AA** | All drag operations have a single-pointer alternative |
| 2.5.8 | Target Size (Minimum) | **AA** | Touch targets ≥ 24×24 CSS px |
| 3.2.6 | Consistent Help | **A** | Help mechanisms appear in same location on every page |
| 3.3.7 | Redundant Entry | **A** | Don't re-ask data already entered in the same session |
| 3.3.8 | Accessible Authentication (Min) | **AA** | No cognitive-only auth — CAPTCHAs need alternatives |
| 3.3.9 | Accessible Authentication (Enhanced) | AAA | No cognitive tests in auth at all |
| ~~4.1.1~~ | ~~Parsing~~ | — | **Removed** in WCAG 2.2 — browsers handle malformed HTML now |

---

## Audit Modes

Every audit combines one or more of these three modes:

### Mode 1 — Design Audit (before code)

Catch issues at the source. Cheaper to fix than in production.

**Design-phase checklist:**

**Color & Contrast**
- [ ] Normal text contrast ≥ 4.5:1 (1.4.3 AA)
- [ ] Large text (≥18px / ≥14px bold) contrast ≥ 3:1 (1.4.3 AA)
- [ ] UI components (input borders, icon lines, button outlines) contrast ≥ 3:1 (1.4.11 AA)
- [ ] Color is never the only differentiator — errors use icon + text, not color alone (1.4.1 A)

**Focus States**
- [ ] Every interactive element has a visible focus indicator (2.4.7 AA)
- [ ] Focus indicator meets 2.4.13 AA: surrounds the component, contrast ≥ 3:1
- [ ] Focused element not fully obscured by sticky headers/footers (2.4.11 AA)
- [ ] Recommended: 3px solid outline, 2px offset, verified contrast on all backgrounds

**Interactive States — every component needs all of these, visually distinct without color alone:**
- [ ] default · hover · focus · active · disabled · error · loading

**Touch Targets**
- [ ] All tap targets ≥ 24×24 CSS px (2.5.8 AA)
- [ ] Recommended: 44×44 CSS px for primary actions
- [ ] Every drag/swipe has a single-tap alternative (2.5.7 AA)

**Layout & Content**
- [ ] Labels always visible — never placeholder-only (3.3.2 A)
- [ ] Error messages name the problem AND suggest a fix — not just "invalid" (3.3.3 A)
- [ ] Multi-step flows pre-fill previously entered data (3.3.7 A)
- [ ] Content reflows at 320px width without horizontal scroll (1.4.10 AA)
- [ ] Help widget appears in same location on every screen (3.2.6 A)
- [ ] Authentication: CAPTCHA has audio alternative; prefer passkey/magic link (3.3.8 AA)

---

### Mode 2 — Automated Audit (after code)

**Tools (use minimum 2 for coverage):**

| Tool | Best for | Coverage |
|------|----------|----------|
| axe DevTools (browser ext) | Dev-time, component level | ~40% of WCAG issues |
| WAVE | Visual overview, quick scan | ~35% |
| Lighthouse | CI/CD, scored report, structured output | ~30% |
| Colour Contrast Analyser (desktop) | Any color pair, on-screen sampling | Contrast only |

**What automated tools catch well:**
- Missing alt text on images
- Form inputs without labels
- Color contrast failures
- Missing document language
- Duplicate IDs
- Empty link/button text

**What automated tools miss (always requires manual testing):**
- Focus order logic
- Meaningful alt text quality
- Screen reader announcement quality
- Keyboard trap detection
- Contextual error message clarity
- Live region behavior

---

### Mode 3 — Manual Audit

#### Keyboard-Only Test Protocol
1. Unplug or disable mouse
2. Tab through the entire page — every interactive element must receive focus
3. Verify focus is always visible (no invisible focus state)
4. Verify Tab order matches visual/logical reading order
5. Activate all controls (Enter for buttons, Space for checkboxes, arrows for radios)
6. Open modal → focus moves to first element inside → Esc closes → focus returns to trigger
7. Verify no keyboard traps (can always Tab away from any control)
8. Verify all drag/swipe interactions have keyboard alternatives

#### Screen Reader Test Protocol

**Recommended pairings:**
- macOS: VoiceOver (Cmd+F5) + Safari
- Windows: NVDA (free) + Firefox or Chrome, or JAWS + Chrome
- iOS: VoiceOver + Safari
- Android: TalkBack + Chrome

**Test checklist:**
- [ ] Page title is unique and descriptive (announced on page load)
- [ ] Heading hierarchy is logical (H1 → H2 → H3, no skipped levels)
- [ ] All images have appropriate alt text (decorative = empty alt)
- [ ] Form inputs announce their label on focus
- [ ] Required fields are announced as required
- [ ] Error messages are announced when they appear (use `role="alert"` or `aria-live="assertive"`)
- [ ] Buttons and links have descriptive names (not "click here", "read more")
- [ ] Modal: background content is `aria-hidden="true"` when modal is open
- [ ] Live regions announce dynamic updates (cart count, toast, save confirmation)
- [ ] Tables have `<th>` with `scope` attributes

---

## Component-Specific Accessibility Patterns

### Forms
- Every `<input>` has a `<label>` with matching `for`/`id` — never rely on placeholder alone
- Required: `required` + `aria-required="true"` + visible non-color indicator (asterisk + legend)
- Errors: `aria-invalid="true"` + `aria-describedby` → error element + `role="alert"`
- Personal data fields use correct `autocomplete` values (name, email, tel, address)

### Navigation
- Landmark regions: `<header>`, `<nav>`, `<main>`, `<footer>` (or ARIA equivalents)
- Multiple `<nav>` elements each need `aria-label` to differentiate
- Skip link: first focusable element, links to `#main-content`
- Current page: `aria-current="page"` on active nav item

### Modals & Dialogs
- `role="dialog"` + `aria-modal="true"` + `aria-labelledby` → heading ID
- On open: move focus to first interactive element
- Trap focus inside modal (Tab and Shift+Tab cycle within)
- On close: return focus to the trigger
- Background: `aria-hidden="true"` when modal is open
- Esc always closes

### Data Tables
- `<table>` with `<caption>` describing the data
- Column headers: `<th scope="col">`, row headers: `<th scope="row">`
- Complex tables: use `id`/`headers` attributes

### Custom Controls (non-native HTML)
- Assign correct ARIA `role` (button, checkbox, listbox, combobox, etc.)
- Add `tabindex="0"` to receive keyboard focus
- Implement expected keyboard interaction for the role
- Expose current state: `aria-expanded`, `aria-pressed`, `aria-selected`

---

## Severity Classification

Use this system consistently so teams can prioritize fixes:

| Severity | Definition | Example | Action |
|----------|------------|---------|--------|
| **Critical** | Blocks access entirely for some users | Keyboard trap, modal with no accessible name, form with no labels | Fix before release |
| **Serious** | Major barrier, hard to work around | Contrast ratio 2:1, focus indicator invisible, screen reader skips nav | Fix in current sprint |
| **Moderate** | Real friction, some users will struggle | Placeholder-only labels, ambiguous button names | Fix within 2 sprints |
| **Minor** | Small improvement opportunity | Redundant alt text, minor heading order issue | Backlog |

---

## Remediation Priority Matrix

After audit, assign fixes using this framework:

1. **Critical issues** → fix before release, no exceptions
2. **Serious issues on critical user paths** (checkout, login, core features) → fix before release
3. **Serious issues on secondary paths** → fix within current quarter
4. **Moderate issues** → schedule in upcoming sprints
5. **Minor issues** → add to design system backlog

---

## Audit Report Template
```markdown
# Accessibility Audit Report — [Product / Component Name]
**Date:** [YYYY-MM-DD]
**Auditor:** [Name]
**Scope:** [Pages / components audited]
**Conformance target:** WCAG 2.2 Level AA
**Tools used:** [axe DevTools, WAVE, Lighthouse, VoiceOver/NVDA]

## Executive Summary
- **Compliance level:** [Fails A / Passes A / Passes AA / Passes AAA]
- **Issues found:** [X] Critical · [X] Serious · [X] Moderate · [X] Minor
- **Top 3 priority fixes:**
  1. …
  2. …
  3. …

## Issues

### Issue 1
- **Criterion:** 1.4.3 Contrast (Minimum) — Level AA
- **Severity:** Serious
- **Location:** [Component / page / screenshot reference]
- **What's wrong:** Button text (#757575 on #FFFFFF) has 4.1:1 contrast. Fails AA (requires 4.5:1).
- **Who it affects:** Low vision users, users in bright sunlight.
- **Fix:** Change button text to #595959 — achieves 7:1. Alternatively use a darker background.

[Repeat per issue]

## Summary Table
| ID | Criterion | Severity | Status |
|----|-----------|----------|--------|
| A-01 | 1.4.3 Contrast | Serious | Open |
| A-02 | 2.4.7 Focus Visible | Critical | Open |
```

---

## Accessibility in Design Systems

If you're auditing a design system — not just a feature — prioritize these:

- **Token-level:** Are color tokens guaranteed to meet contrast ratios? (e.g., `color.text.primary` on `color.bg.primary` passes 4.5:1?)
- **Focus tokens:** Is there a system-level focus token (outline color, offset, width)?
- **State tokens:** Does every component variant have all interactive states?
- **Component contracts:** Does each component's spec include accessibility requirements?
- **Documentation:** Does `component_documentation` include the ARIA role, keyboard behavior, and AT notes for each component?

---

## Common Mistakes and How to Avoid Them

| Mistake | Why it happens | Fix |
|---------|----------------|-----|
| Only running automated tools | Fast and feels comprehensive | Automated tools catch ~30–40% of issues. Always follow with keyboard + SR testing. |
| Treating WCAG as a checklist to pass once | Teams think "we passed the audit" = done | Accessibility is ongoing. Bake it into the design system and Definition of Done. |
| Filing issues without fix guidance | Developers don't know what to do | Every issue needs a specific, actionable fix. Vague: "improve contrast." Specific: "change #AAA to #595959 — achieves 7:1." |
| Testing only with one screen reader | VoiceOver ≠ NVDA behavior | Test with at minimum VoiceOver (Mac/iOS) + NVDA or JAWS (Windows). |
| Designing focus states last | Focus is treated as a dev concern | Design the focus indicator explicitly. Specify outline width, color, and offset in design specs. |
| Using ARIA when native HTML works | ARIA seems "more powerful" | Native HTML has implicit semantics + AT support. Always prefer `<button>` over `<div role="button">`. |

---

## FAQ

**Q: What's the difference between WCAG 2.1 and 2.2?**
WCAG 2.2 adds 9 new success criteria (mostly AA) focused on focus appearance, touch targets, dragging alternatives, redundant entry, and cognitive-safe authentication. It also removes 4.1.1 Parsing. If you're targeting AA, you must meet all 2.2 AA criteria.

**Q: Does WCAG compliance mean the product is accessible?**
No. WCAG is a specification, not a ceiling. A product can pass all criteria and still create friction for users with disabilities. Complement audits with user testing with disabled participants.

**Q: What about the European Accessibility Act (EAA 2025)?**
The EAA requires products and services sold in the EU to meet EN 301 549, which maps to WCAG 2.1 AA (and partially 2.2). For new products after June 2025, target WCAG 2.2 AA to be future-proof.

**Q: Should we test with real users with disabilities?**
Yes — whenever possible. Automated and expert audits are necessary but not sufficient. Even 3–5 sessions with screen reader users, keyboard-only users, or low-vision users reveal issues that no checklist catches.

**Q: Who should own accessibility on the team?**
Everyone. Design owns visual states, focus design, and color. Engineering owns ARIA implementation and keyboard behavior. QA owns inclusion in the Definition of Done. A single "accessibility person" is not a scalable model.

**Q: How do we handle iframes and third-party embeds?**
You're responsible for conformance of your entire page, including third-party content. Document known barriers, work with vendors, and use the "accessibility support statement" approach for items outside your control.

---

## References

- WCAG 2.2 Official Specification: https://www.w3.org/TR/WCAG22/
- WCAG 2.2 Understanding Docs: https://www.w3.org/WAI/WCAG22/Understanding/
- ARIA Authoring Practices Guide: https://www.w3.org/WAI/ARIA/apg/
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- axe DevTools: https://www.deque.com/axe/devtools/
- WAVE Web Accessibility Evaluator: https://wave.webaim.org/
- Colour Contrast Analyser (desktop app): https://www.tpgi.com/color-contrast-checker/
- NVDA Screen Reader (free): https://www.nvaccess.org/
- European Accessibility Act overview: https://ec.europa.eu/social/main.jsp?catId=1202
- Inclusive Design Principles: https://inclusivedesignprinciples.org/

---

## Cross-References

- → `component_documentation` — Embed accessibility requirements in every component spec
- → `ux_audit` — Heuristic review; complements but does not replace WCAG audit
- → `design_qa_checklist` — Include accessibility checks in post-implementation QA
- → `design_handoff_spec` — Handoff specs must include ARIA roles, focus behavior, and state documentation