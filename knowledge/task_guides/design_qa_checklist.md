# Design QA Checklist

## Executive Summary

Design QA is the structured process of verifying that an implemented feature matches its design specification — before it ships to users. It closes the loop between design intent and production reality, catching visual drift, missing states, broken interactions, and accessibility gaps that functional testing never sees.

**When to use this task:**
- After a developer marks a feature "ready for design review"
- Before sprint demo or release candidate sign-off
- During pre-launch QA sprints
- Whenever a significant refactor or design system update touches production UI

**When NOT to use this task:**
- Before implementation is code-complete (use design critique / heuristic evaluation instead)
- As a replacement for functional/regression testing (this is a design-specific layer, not a QA engineering process)
- For evaluating a competitor's product (use ux_audit or competitive_analysis instead)

---

## Prerequisites

Before starting a Design QA session:

- [ ] Feature is deployed to a staging or QA environment
- [ ] Link to design spec (Figma, Zeplin, or equivalent) is accessible and current
- [ ] Design spec includes all states: default, hover, focus, active, disabled, loading, empty, error
- [ ] Breakpoints and responsive behavior are documented in spec
- [ ] Access to BrowserStack or physical devices for cross-device testing
- [ ] Screen reader installed (VoiceOver on macOS/iOS, NVDA or JAWS on Windows)

---

## QA Workflow
```
Dev marks feature done
        ↓
Designer opens spec + staging side-by-side
        ↓
Run 5-pass checklist (Visual → Interaction → Responsive → A11y → Content)
        ↓
Log issues with severity, screenshots, spec links
        ↓
Triage with PM: P0/P1 must fix before release, P2/P3 backlog
        ↓
Dev fixes → Designer re-verifies targeted items
        ↓
Designer signs off (or escalates blockers)
```

**Who does Design QA?** Typically the designer who owns the feature, ideally with a second pair of eyes from PM or another designer. QA engineers handle functional testing — designers own visual and interaction integrity.

---

## Complete QA Checklist

### Dimension 1 — Visual

**Spacing & Layout**
- [ ] Component padding matches spec (all 4 sides)
- [ ] Margin between elements matches spacing scale
- [ ] Grid alignment is correct (columns, gutters, offsets)
- [ ] White space is consistent with adjacent components

**Color & Tokens**
- [ ] All colors reference design tokens (no hardcoded hex values)
- [ ] Background, text, border, and icon colors match spec exactly
- [ ] Dark mode / theme variants render correctly (if applicable)
- [ ] Color contrast meets WCAG AA in production context (not just isolated)

**Typography**
- [ ] Font family, weight, size, and line height match spec
- [ ] Heading hierarchy is visually correct (H1–H6)
- [ ] Letter spacing and paragraph spacing match
- [ ] Truncation with ellipsis appears at correct max-width

**Elevation & Effects**
- [ ] Box shadows match spec (blur, spread, color, offset)
- [ ] Border radius is consistent with design system tokens
- [ ] Opacity and layering are correct

**Icons & Images**
- [ ] Icon size matches spec (16px, 20px, 24px — per token)
- [ ] Icons are correct variant (outline vs filled vs colored)
- [ ] Images render at correct aspect ratio, no distortion or cropping
- [ ] SVGs render crisply at all zoom levels

---

### Dimension 2 — Interaction

**States**
- [ ] Hover state matches spec (color, underline, elevation change)
- [ ] Focus state is visible and matches spec (outline, ring style)
- [ ] Active/pressed state renders correctly
- [ ] Disabled state looks correct and is non-interactive
- [ ] Selected/checked state matches spec

**Transitions & Animation**
- [ ] Transition timing matches spec (easing, duration)
- [ ] Animations don't flash or jump unexpectedly
- [ ] `prefers-reduced-motion` disables or reduces animations

**Loading & Feedback**
- [ ] Loading states appear at correct trigger points
- [ ] Skeleton screens match layout of loaded content
- [ ] Success and error feedback (toasts, inline messages) appear correctly
- [ ] Spinners and progress indicators render correctly

**Keyboard Navigation**
- [ ] Tab order follows logical visual order
- [ ] All interactive elements are reachable by keyboard
- [ ] Enter/Space trigger correct actions on buttons and links
- [ ] Escape closes modals, dropdowns, and drawers

---

### Dimension 3 — Responsive

**Breakpoints**
- [ ] Layout shifts correctly at each defined breakpoint (mobile, tablet, desktop, wide)
- [ ] No elements overlap or get cut off at any breakpoint
- [ ] Side-by-side elements stack correctly on mobile
- [ ] Navigation collapses to correct mobile pattern

**Content Reflow**
- [ ] Long strings wrap without breaking layout
- [ ] Labels and buttons don't overflow their containers
- [ ] Images and media scale proportionally
- [ ] Tables have horizontal scroll or convert to card layout on mobile

**Touch Targets**
- [ ] Interactive elements are minimum 44×44px on touch screens
- [ ] Tap targets have sufficient spacing to prevent mis-taps
- [ ] Swipe gestures (if applicable) work as specified

---

### Dimension 4 — Accessibility

**Contrast in Context**
- [ ] Text contrast ≥ 4.5:1 (AA) in actual rendered state — not just spec colors
- [ ] UI components and icons contrast ≥ 3:1 against background
- [ ] Focus indicators are clearly visible against surrounding UI

**Screen Reader Flow**
- [ ] Headings convey correct page structure (H1 → H2 → H3)
- [ ] Images have appropriate alt text (empty `alt=""` for decorative images)
- [ ] Form fields have associated labels
- [ ] Error messages are announced to screen readers
- [ ] Modal/dialog traps focus and announces role correctly

**Keyboard & Motion**
- [ ] No keyboard traps (user can always navigate away)
- [ ] Skip navigation link present on page-level layouts
- [ ] Reduced motion preference respected

**Tools for A11y QA:**
- axe DevTools browser extension (automated scan, ~30% of issues caught automatically)
- VoiceOver (macOS: Cmd+F5) or NVDA (Windows, free) for manual screen reader pass
- Chrome DevTools → Accessibility tree
- WebAIM Contrast Checker for production context

---

### Dimension 5 — Content

**Copy Accuracy**
- [ ] All labels, button text, and headings match spec exactly
- [ ] Casing is correct (Title Case vs Sentence case per spec)
- [ ] No placeholder text (Lorem ipsum, "TBD", "Coming soon") remains
- [ ] Microcopy (tooltips, helper text, error messages) matches spec

**Edge Cases**
- [ ] Empty state renders correctly (no data, new user, filtered-to-zero)
- [ ] Error state shows correct message and recovery path
- [ ] Long text strings don't break layout (test with 2× normal content)
- [ ] Numbers, dates, currencies format correctly per locale (if applicable)
- [ ] Character limits enforce correctly with graceful truncation

---

## Severity Classification

| Level | Name | Definition | Action |
|-------|------|------------|--------|
| P0 | Critical | Broken, unusable, blocks core user flow | Block release. Fix immediately. |
| P1 | High | Significant deviation from spec, clearly noticeable to users | Must fix before release. |
| P2 | Medium | Inconsistency or polish issue, noticeable but not blocking | Fix in next sprint if possible. |
| P3 | Low | Minor tweak, only visible on close inspection | Backlog. Fix when convenient. |

**Tip:** When in doubt between P1 and P2, ask: "Would a user notice this on their first visit?" If yes → P1.

---

## Issue Reporting Template

File each QA issue with this structure in your project management tool (Jira, Linear, GitHub Issues):
```
**Screen / Component:** [e.g., "Checkout – Payment Form"]
**Issue:** [One clear sentence describing the deviation]
**Expected:** [What the spec shows — include Figma link and frame name]
**Actual:** [What is currently in staging — include screenshot or video]
**Severity:** [P0 / P1 / P2 / P3]
**Platform:** [Web, iOS, Android — browser/OS if relevant]
**Steps to reproduce:** [If interaction-dependent]
**Assigned to:** [Developer who built this]
```

**Annotation tools:** Loom (video), Cleanshot / ScreenCapture (annotated screenshots), Figma comments with staging screenshots side-by-side.

---

## QA Automation Recommendations

Manual QA is essential — but automation catches regressions automatically in CI.

| Tool | Best For | Cost |
|------|----------|------|
| Playwright `toHaveScreenshot()` | Zero-setup baseline for any stack | Free |
| BackstopJS | Open-source, flexible, page-level | Free |
| Chromatic | Component-level (Storybook-based design systems) | Free tier available |
| Percy by BrowserStack | CI-integrated full-page cross-browser | Free tier: 5K screenshots/month |
| Applitools Eyes | AI-powered, large-scale, enterprise | Paid |

**Recommended combo for most teams:** Chromatic for design system components + Percy for page-level staging flows. Manual designer QA on top of both.

---

## Common Mistakes & How to Avoid Them

**"QA-ing from memory"** — Always have the Figma spec open side-by-side. Never rely on what you remember the design looked like.

**Skipping state coverage** — The default state usually looks fine. The bugs hide in hover, focus, error, empty, and loading states. Always run all states.

**Filing vague issues** — "Button looks wrong" is not actionable. Always include the Figma frame link, actual screenshot, and specific deviation.

**Skipping mobile** — Resize a browser window is not a substitute for testing on actual devices or BrowserStack. At minimum, test on a real iPhone and Android.

**Approving before all P0/P1s are fixed** — Designer sign-off implies the implementation is shippable. Partial approvals create ambiguity. Don't sign off until blockers are resolved.

**Treating QA as punishment** — Frame Design QA as a quality investment, not a critique of the developer. The goal is shipping something you're proud of together.

---

## Templates / Canvases

### Quick QA Scorecard (per screen)
```
Screen: ___________________________   Date: _________   Reviewer: _________

Visual      [ ] Pass  [ ] Issues filed (#___)
Interaction [ ] Pass  [ ] Issues filed (#___)
Responsive  [ ] Pass  [ ] Issues filed (#___)
A11y        [ ] Pass  [ ] Issues filed (#___)
Content     [ ] Pass  [ ] Issues filed (#___)

Status: [ ] Approved  [ ] Approved with minor P3s  [ ] Blocked (P0/P1 open)
Sign-off: _________________________
```

---

## FAQ

**Q: How long does a Design QA session take?**
A single feature or screen: 30–60 minutes. A full sprint release: 2–4 hours depending on scope. Block dedicated time — don't squeeze it between other tasks.

**Q: Should the designer who designed the feature do the QA?**
Yes, ideally — they know the spec best. But a second reviewer catches things the original designer is blind to. Pair QA with PM or another designer when stakes are high.

**Q: What if there's no Figma spec / the spec is outdated?**
This is a process failure, not a QA failure. Pause and align with the designer on what the expected state is before proceeding. Don't QA against an incomplete or stale spec.

**Q: How do I handle disagreements with developers about what counts as a bug?**
Use the spec as the source of truth. If the spec is ambiguous, that's a design gap to address — not a dev error. Document the agreement reached and update the spec for future reference.

**Q: When should automated visual regression (Percy, Chromatic) replace manual QA?**
Never fully — but automation handles regression protection well. Manual QA is critical for new features where no baseline exists, for accessibility, and for judging subjective quality like feel and polish.

**Q: What about QA on native mobile (iOS/Android)?**
Same checklist applies, adapted for native conventions: touch targets (minimum 44×44pt), platform-specific navigation patterns, safe area insets, and OS accessibility tools (VoiceOver on iOS, TalkBack on Android).

---

## Related Tasks / Cross-References

- **`ux_audit`** — Use before implementation to identify UX issues at the design stage. Design QA happens after implementation.
- **`heuristic_evaluation`** — Expert heuristic review of design; pair with Design QA to ensure heuristic issues don't survive into production.
- **`token_audit`** — Audit token definitions at the system level; Design QA verifies token application in the actual production UI.
- **`design_handoff_spec`** — The handoff spec is the source of truth for Design QA. Gaps in the spec become QA ambiguities.
- **`component_documentation`** — Component docs define expected states; cross-reference when QA-ing individual design system components.

---

## References

- Design QA: A Very Scrappy, Practical Guide (Shannon Bain, Medium): https://medium.com/@shannonmbain/design-qa-a-very-scrappy-practical-guide-51fda5aab5c1
- DevChecklists — Design QA Process: https://devchecklists.com/en/checklist/design-qa-process
- Quality Assurance Checklist for UX Engineers (Think Company): https://www.thinkcompany.com/blog/quality-assurance-checklist-for-ux-engineers/
- Visual Regression Testing Tools Comparison (Bug0, 2026): https://bug0.com/knowledge-base/visual-regression-testing-tools
- WebAIM Keyboard Accessibility: https://webaim.org/techniques/keyboard/
- axe DevTools: https://www.deque.com/axe/devtools/
- Percy by BrowserStack: https://www.browserstack.com/percy
- Chromatic (Storybook visual testing): https://www.chromatic.com
- BackstopJS: https://github.com/garris/BackstopJS