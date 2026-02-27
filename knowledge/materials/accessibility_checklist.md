# WCAG 2.2 AA Accessibility Checklist
**Scope:** WCAG 2.2 Level A + AA (all required criteria)
**Usage:** Use during design review, code review, and QA. Check ✅ when passing, ❌ when failing, 🔲 when not applicable.

---

## Principle 1 — Perceivable / Perceptible

### 1.1 Text Alternatives
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 1.1.1 | All images have meaningful alt text; decorative images have `alt=""` | A | 🔲 |
| 1.1.1 | Icon-only buttons have `aria-label` describing the action | A | 🔲 |
| 1.1.1 | Complex images (charts, diagrams) have extended description | A | 🔲 |

### 1.2 Time-based Media
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 1.2.1 | Audio-only content has text transcript | A | 🔲 |
| 1.2.2 | Prerecorded video with audio has synchronized captions | A | 🔲 |
| 1.2.4 | Live video with audio has real-time captions | AA | 🔲 |
| 1.2.5 | Prerecorded video has audio description track | AA | 🔲 |

### 1.3 Adaptable
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 1.3.1 | Headings are semantic (`<h1>`–`<h6>`), not styled `<div>` | A | 🔲 |
| 1.3.1 | Form inputs have programmatically associated `<label>` | A | 🔲 |
| 1.3.1 | Data tables have `<th>` with `scope` attributes | A | 🔲 |
| 1.3.2 | DOM reading order is logical (CSS reordering doesn't diverge) | A | 🔲 |
| 1.3.3 | Instructions don't rely solely on shape, color, size, or position | A | 🔲 |
| 1.3.4 | Content works in both portrait and landscape orientation | AA | 🔲 |
| 1.3.5 | Personal data inputs use correct `autocomplete` values | AA | 🔲 |

### 1.4 Distinguishable
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 1.4.1 | Color is not the only means of conveying information | A | 🔲 |
| 1.4.3 | Normal text contrast ≥ 4.5:1 | AA | 🔲 |
| 1.4.3 | Large text contrast ≥ 3:1 (≥18px or ≥14px bold) | AA | 🔲 |
| 1.4.4 | Text resizable to 200% without loss of content or function | AA | 🔲 |
| 1.4.10 | Content reflows at 320px width — no horizontal scroll | AA | 🔲 |
| 1.4.11 | UI component contrast ≥ 3:1 (borders, icons, chart lines) | AA | 🔲 |
| 1.4.12 | Text spacing adjustable (line height, letter/word spacing) without loss of function | AA | 🔲 |
| 1.4.13 | Hover/focus tooltip content stays visible on hover; dismissible; persistent | AA | 🔲 |

---

## Principle 2 — Operable / Operable

### 2.1 Keyboard Accessible
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 2.1.1 | All functionality available from keyboard | A | 🔲 |
| 2.1.2 | No keyboard trap (can always Tab away from any component) | A | 🔲 |
| 2.1.4 | Single-key shortcuts can be remapped or disabled | A | 🔲 |

### 2.4 Navigable
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 2.4.1 | Skip link to main content is first focusable element | A | 🔲 |
| 2.4.2 | Page has descriptive `<title>` | A | 🔲 |
| 2.4.3 | Focus order is logical and meaningful | A | 🔲 |
| 2.4.4 | Link purpose is clear from link text alone (or context) | A | 🔲 |
| 2.4.6 | Headings and labels are descriptive | AA | 🔲 |
| 2.4.7 | Keyboard focus indicator is visible | AA | 🔲 |
| **2.4.11** | **Focused element not fully obscured by sticky content** | **AA *(2.2)*** | 🔲 |
| **2.4.13** | **Focus indicator: area ≥ perimeter, contrast ≥ 3:1** | **AA *(2.2)*** | 🔲 |

### 2.5 Input Modalities
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 2.5.1 | Pointer gestures can be performed with single pointer | A | 🔲 |
| 2.5.3 | Button/label accessible name matches visible label | A | 🔲 |
| **2.5.7** | **All dragging operations have single-pointer alternative** | **AA *(2.2)*** | 🔲 |
| **2.5.8** | **Touch targets ≥ 24×24 CSS px** | **AA *(2.2)*** | 🔲 |

### 2.3 Seizures
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 2.3.1 | No content flashes more than 3 times per second | A | 🔲 |

### 2.2 Enough Time
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 2.2.1 | Timed sessions can be extended or disabled | A | 🔲 |
| 2.2.2 | Auto-moving/blinking content can be paused | A | 🔲 |

---

## Principle 3 — Understandable / Comprensible

### 3.1 Readable
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 3.1.1 | Page language is set in `<html lang="...">` | A | 🔲 |
| 3.1.2 | Language changes within content are marked | AA | 🔲 |

### 3.2 Predictable
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 3.2.1 | Focus does not trigger unexpected context change | A | 🔲 |
| 3.2.2 | Input does not trigger unexpected context change | A | 🔲 |
| 3.2.3 | Navigation is consistent across pages | AA | 🔲 |
| 3.2.4 | Components with same function have consistent labels | AA | 🔲 |
| **3.2.6** | **Help mechanisms appear in same location on every page** | **A *(2.2)*** | 🔲 |

### 3.3 Input Assistance
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 3.3.1 | Errors are identified in text, not color alone | A | 🔲 |
| 3.3.2 | Labels and instructions provided for user input | A | 🔲 |
| 3.3.3 | Error suggestions provided (not just "invalid") | AA | 🔲 |
| 3.3.4 | Errors reversible, checkable, or confirmable for legal/financial transactions | AA | 🔲 |
| **3.3.7** | **Previously entered information pre-filled — not re-asked** | **A *(2.2)*** | 🔲 |
| **3.3.8** | **Auth has no cognitive-only CAPTCHA — audio or alternatives provided** | **AA *(2.2)*** | 🔲 |

---

## Principle 4 — Robust / Robusto

### 4.1 Compatible
| # | Criterion | Level | Check |
|---|-----------|-------|-------|
| 4.1.2 | All UI components have name, role, and value exposed programmatically | A | 🔲 |
| 4.1.3 | Status messages are programmatically determinable (live regions) | AA | 🔲 |

---

## Quick Reference — WCAG 2.2 New/Changed Criteria

| ID | Name | Level | Summary |
|----|------|-------|---------|
| 2.4.11 | Focus Not Obscured (Min) | AA | Sticky content can't fully cover focused element |
| 2.4.12 | Focus Not Obscured (Enhanced) | AAA | Not even partially covered |
| 2.4.13 | Focus Appearance | AA | Focus indicator: ≥ component perimeter area, ≥ 3:1 contrast |
| 2.5.7 | Dragging Movements | AA | Single-pointer alternative for all drag ops |
| 2.5.8 | Target Size (Minimum) | AA | ≥ 24×24 CSS px |
| 3.2.6 | Consistent Help | A | Help in same spot on every page |
| 3.3.7 | Redundant Entry | A | Pre-fill previously entered data |
| 3.3.8 | Accessible Auth (Min) | AA | No cognitive-only CAPTCHA |
| ~~4.1.1~~ | ~~Parsing~~ | — | Removed — browsers handle malformed HTML |

---

*Bold + italic criteria = new in WCAG 2.2. All AA criteria in this checklist are legally required for EU EAA 2025 compliance.*