# Research Analysis QA Guide
### AI-Generated Analysis Verification & Stakeholder Readiness Check

---

## Executive Summary

AI analysis always looks confident — even when it's wrong. Hallucinated quotes, generic themes, and missed contradictions are invisible until a stakeholder asks a question you can't answer, or a decision falls apart three months later. This guide operationalizes a structured five-stage QA pass that catches those errors before they become product decisions.

The five stages are: (1) quote verification, (2) theme specificity audit, (3) contradiction scan, (4) evidence confidence scoring, and (5) pre-stakeholder readiness check. Each stage is independent — you can run all five sequentially or apply individual stages as spot-checks.

---

## Prerequisites

Before starting, confirm you have:

- **Source transcripts or raw data** — the original files the AI analyzed (interview transcripts, survey CSVs, session notes). You need these to verify quotes; without them, stage 1 is blocked.
- **AI-generated analysis output** — the draft report, themes, quotes, and recommendations produced by your AI tool.
- **Participant ID mapping** — a key linking participant codes (P01, P02, etc.) to actual participants. Even if informal, this is needed for citation credibility.
- **Decision context** — the product or design question this research is meant to answer. Needed for the specificity audit (stage 2).
- **Optional:** the `ai_research_analysis.md` material for additional prompt templates.

---

## Quickstart (5-minute version)

Run the quote verification prompt (Stage 1) on your AI output before doing anything else. If more than 20% of quotes come back as PARAPHRASE or NOT FOUND, the analysis needs a full pass through all five stages before it's shareable.

---

## Procedure

### Stage 1 — Quote Verification

**Goal:** Confirm that every quote in the AI output exists verbatim in source data. LLMs generate text statistically — they don't retrieve quotes like a search engine. Frankenstein quotes (sewn from multiple sources) and outright fabrications are common, especially in ChatGPT outputs.

**How to run it:**

1. Copy your AI analysis output into a fresh conversation with your LLM.
2. Attach or paste the source transcript(s).
3. Run the prompt below.

**Prompt — Quote Verification Pass:**
```
QUOTE VERIFICATION

You are a research QA assistant. For each quote in the analysis below,
check it against the source transcript provided.

For every quote:
1. Confirm the quote exists verbatim in the source transcript
2. If it is a close paraphrase but not exact, flag it and provide
   the actual wording
3. If the quote cannot be located in the source, mark it NOT FOUND

Output format for each quote:
  Quote: [the quote as it appears in the analysis]
  Status: VERIFIED / PARAPHRASE / NOT FOUND
  If paraphrase → Actual wording: [what they actually said]
  Location: [Participant ID, timestamp, or line number]

[PASTE YOUR AI ANALYSIS HERE]
[PASTE SOURCE TRANSCRIPT(S) HERE]
```

**What to do with results:**
- **VERIFIED** → keep as-is.
- **PARAPHRASE** → replace with actual wording or remove. Never use paraphrases as direct quotes in stakeholder materials.
- **NOT FOUND** → remove immediately. Flag the theme it supported for re-examination in Stage 4.

**Note on quote selection rules:** Before your next analysis run, add these rules to your analysis prompt to reduce hallucinations upstream:
```
QUOTE SELECTION RULES
- Start where the thought begins, continue until fully expressed
- Include reasoning, not just conclusions
- Keep hedges and qualifiers — they signal uncertainty
- Include emotional language when present
- Cite with participant ID and approximate timestamp [P01, ~14:30]
- Do not combine statements from different parts of the interview
- If a quote would exceed 3 sentences, break into separate quotes
```

---

### Stage 2 — Theme Specificity Audit

**Goal:** Identify themes that are too broad or generic to drive a decision. Themes like "users value reliability" or "price is a factor" are true of nearly any product — they don't help you decide anything specific.

A good theme is **specific enough that a product team could act on it differently** than they would on a vague alternative. It should reference *who* (a segment), *what* (a specific behavior or need), and *why it matters for this decision*.

**Prompt — Theme Specificity Audit:**
```
THEME SPECIFICITY AUDIT

Review each theme in this analysis against our decision context below.

Decision context: [paste your research question / product decision here]

For each theme, rate it:
  ACTIONABLE — specific enough to guide this decision; names a
    segment, behavior, or mechanism
  TOO GENERIC — could describe any product in this category;
    not tied to a decision direction
  REFRAMEABLE — has useful signal buried in it; needs sharper framing

For GENERIC and REFRAMEABLE themes, suggest a more specific version
based only on evidence present in the analysis.

[PASTE THEMES AND SUPPORTING QUOTES HERE]
```

**What to do with results:**
- ACTIONABLE themes → keep.
- GENERIC themes with no supporting specifics → remove or downgrade to "background context."
- REFRAMEABLE themes → use the AI's suggested reframe as a draft, then verify it against source data.

---

### Stage 3 — Contradiction Scan

**Goal:** Surface conflicting signals that the AI flattened into a single theme. Real qualitative data contains contradictions — participants who explicitly want the same feature for opposite reasons, or who say one thing but describe behavior that contradicts it.

AI defaults to consensus. It surfaces patterns that "rise to the top" and deprioritizes edge cases. The most important insight is often the one only two people mentioned — or the tension between what people say they want and what their behavior suggests.

**Prompt — Contradiction Scan:**
```
CONTRADICTION SCAN

Review the full analysis and identify:

1. Participants whose views directly contradict each other on the
   same theme — cite participant IDs and the conflicting statements
2. Participants who contradict themselves within their own session
   (e.g., says they want X, but describes behavior that avoids X)
3. Any theme where the supporting evidence is one-sided — where
   dissenting voices exist in the data but weren't represented

Format:
  Contradiction: [brief description]
  Participants: [P01 vs P03, or P02 internal]
  Evidence A: [quote or paraphrase + location]
  Evidence B: [conflicting quote or paraphrase + location]
  Implication: [what this tension means for the decision]

[PASTE FULL AI ANALYSIS + SOURCE DATA OR TRANSCRIPT SUMMARIES]
```

**What to do with results:**
- Add contradictions to your findings as a "tensions" or "conflicting signals" section — this is often the most valuable part of a research report.
- Never smooth contradictions into a consensus statement. Present them as design tensions to resolve.

---

### Stage 4 — Evidence Confidence Scoring

**Goal:** Rate each theme by the strength and breadth of its support. A theme mentioned by one participant in passing should carry a different weight than one explicitly raised by eight participants in five different ways.

**Scoring rubric:**

| Score | Criteria |
|---|---|
| **High** | 3+ participants, verbatim evidence, unprompted, consistent across methods |
| **Medium** | 2 participants OR prompted but strongly affirmed OR single participant with rich detail |
| **Low** | 1 participant, paraphrase only, inconsistent with other signals, or contradicted elsewhere |

**Prompt — Evidence Confidence Scoring:**
```
EVIDENCE CONFIDENCE SCORING

For each theme in this analysis, assign a confidence score:
  HIGH / MEDIUM / LOW

Use these criteria:
  HIGH: 3+ participants mentioned it; evidence is verbatim and unprompted;
    consistent across data sources
  MEDIUM: 2 participants OR strongly affirmed when prompted OR one
    participant with rich, specific detail
  LOW: Single participant; paraphrase-only; contradicted elsewhere in data;
    or theme was prompted by the researcher

Output:
  Theme: [theme name]
  Score: HIGH / MEDIUM / LOW
  Evidence count: [n participants]
  Confidence rationale: [1–2 sentences]
  Risk flag: [any reason to be cautious presenting this]

[PASTE THEMES WITH SUPPORTING EVIDENCE]
```

**What to do with results:**
- LOW-confidence themes should be labeled as "hypotheses to validate" rather than findings.
- HIGH-confidence themes are your lead findings.
- In stakeholder reports, always show confidence scores alongside themes — this forces honest communication about certainty levels.

---

### Stage 5 — Pre-Stakeholder Readiness Check

**Goal:** Final gate. Run this checklist before any findings leave the research team.
```
PRE-STAKEHOLDER READINESS CHECKLIST

Quote integrity
  [ ] All quotes marked VERIFIED (or paraphrases removed/replaced)
  [ ] No NOT FOUND quotes remain in the deliverable
  [ ] All quotes cite participant ID and approximate location

Theme quality
  [ ] All themes rated ACTIONABLE (generic themes removed or reframed)
  [ ] Each theme is tied to the specific product/design decision
  [ ] No theme relies solely on LOW-confidence evidence without a caveat

Contradictions
  [ ] Conflicting signals documented in a "tensions" section
  [ ] No contradiction has been smoothed into false consensus

Evidence transparency
  [ ] Confidence scores visible for each major finding
  [ ] LOW-confidence themes labeled as "hypotheses" not "findings"
  [ ] Sample size and data sources stated in methodology section

Decision readiness
  [ ] Report answers the original research question
  [ ] At least one clear recommended action per HIGH-confidence finding
  [ ] Known limitations and gaps explicitly called out
```

All boxes checked → analysis is ready to share.
Any unchecked box → address before delivery.

---

## Troubleshooting

**"The AI can't find quotes because the transcript is too long."**
Split the transcript into segments (by participant or session), run verification per segment, then consolidate.

**"All my themes are coming back as GENERIC."**
This usually means your original analysis prompt lacked decision context. Add the four context components to your next analysis run: project context, business goal, product context, and participant overview. Re-run analysis before QA.

**"The contradiction scan found too many conflicts — the data feels unusable."**
Contradictions are a feature, not a bug. If multiple genuine tensions exist, that's the finding: the user population is segmented. Use the contradictions to define distinct user segments rather than seeking a single consensus answer.

**"My stakeholder wants the report NOW and there's no time for QA."**
Run Stage 1 only (quote verification). It takes 5–10 minutes and prevents the most credibility-damaging error: presenting fabricated quotes as customer evidence.

**"I don't have the original transcripts."**
You cannot run Stage 1. Flag this as a limitation in your report. Remove all verbatim quotes and replace with paraphrases explicitly labeled as such. Never present AI-generated quotes as verbatim without source verification.

---

## Examples

**Example: Stage 1 catch**
AI output included the quote: *"Good enough beats best-in-class for one thing."*
Quote verification returned: PARAPHRASE.
Actual wording (P01, line 234): *"The Suunto was good enough… that beats 'best in class' for just one thing."*
Action: Replace quote with actual wording before including in deck.

**Example: Stage 2 catch**
Theme: *"Users value reliability."*
Specificity audit: TOO GENERIC.
Suggested reframe: *"Power users who train daily explicitly reject app-dependent wearables — they need always-visible data without requiring phone interaction."*
Action: Verify reframe against source, then replace.

**Example: Stage 3 catch**
Contradiction found: P02 says *"I want a screen"* but describes deliberately leaving wearable at home on rest days to reduce data anxiety.
Implication: Screen request may reflect a data access need, not a form-factor preference. Don't interpret as literal hardware request.

---

## Cross-References

- **Affinity Diagramming** (`affinity_diagramming.md`): Run this QA pass after affinity clustering to verify that cluster labels accurately reflect participant language, not researcher-imposed categories.
- **Usability Test Reporting** (`usability_test_reporting.md`): Apply quote verification and confidence scoring before finalizing the findings section of any usability report.
- **AI Research Analysis** (`ai_research_analysis.md`): Upstream methodology guide for structuring the AI analysis pass that this QA task validates. Contains context-loading templates and model selection guidance.

---

## References

- Sullivan, Caitlin. "How to do AI analysis you can actually trust." Lenny's Newsletter, February 17, 2026. https://www.lennysnewsletter.com/p/how-to-do-ai-analysis-you-can-actually
- Sullivan, Caitlin. "Pressure-test your AI workflows across models." AI Customer Research Newsletter, February 28, 2026. https://aicustomerresearch.substack.com
- Nielsen Norman Group — Research methods and analysis validity: https://www.nngroup.com/articles/