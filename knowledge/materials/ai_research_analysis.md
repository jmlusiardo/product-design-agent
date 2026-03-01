# AI-Assisted Research Analysis — Prompt Toolkit

> **Executive Summary** — Practitioner prompt toolkit for getting reliable, evidence-based insights from AI-assisted qualitative analysis. Organized around four failure modes that silently corrupt AI analysis outputs—invented evidence, false/generic insights, non-actionable signals, and contradictory findings—with copy-paste prompt blocks that work across Claude, ChatGPT, and Gemini, for both interview transcripts and survey data.

---

## Prerequisites

- Qualitative data ready for analysis (interview transcripts, survey exports, session notes, or video-based behavioral data)
- Access to at least one LLM (Claude recommended for analysis depth; see Model Selection below)
- Basic familiarity with your research goals and the decision the analysis will support

---

## Quickstart

1. Load the **Context Block** (Failure Mode #2 fix) into your prompt before any analysis
2. Add **Quote Selection Rules** (Failure Mode #1 fix) to your analysis prompt
3. Run analysis → get themes + quotes
4. Run **Verification Pass** to audit quote accuracy
5. Apply **Specificity prompts** if themes read as truisms
6. Run **Contradiction Detection** before finalizing findings

---

## Why AI Struggles with Qualitative Data

### Interviews are unstructured and messy
A 45-minute research interview wanders. Participants contradict themselves, go on tangents, say something important at minute 8 and reframe it completely at minute 35. LLMs handle this by imposing structure too fast—finding clean themes, pulling quotes that confirm them, producing tidy summaries. Real analysis requires sitting with the mess, noticing contradictions, and catching tone shifts. Without explicit guidance, AI flattens all of this into something that *looks* like insight but misses what matters.

### Surveys are messier than they appear
A CSV looks structured. But 200 responses to "Why did you cancel?" is as messy as transcripts—often worse, because you lose all context. LLMs also misread export formats: SurveyMonkey and Qualtrics structure headers differently, and some exports include metadata columns (timestamps, internal tags) sitting right next to customer responses. If you don't tell AI which columns contain the customer's voice, it analyzes everything as signal.

---

## Model Selection Guide

Choose your model based on what the analysis step needs:

| Model | Best for | Watch out for |
|-------|----------|---------------|
| **Claude** | Deep analysis, breadth of quotes, staying grounded in data | Delivers the whole "brain dump"—themes aren't always fully proven, needs your judgment to filter |
| **Gemini** (+ NotebookLM) | Highly evidenced themes, video/non-verbal analysis | Fewer themes per run; needs multiple prompts for completeness; ask explicitly for longer quotes |
| **ChatGPT** | Final framing, stakeholder communication, packaging findings | Most creative—including with "verbatim" quotes. Combines quotes from different parts of interviews. Least reliable for evidence |

**Recommendation:** Use Claude for analysis. Use ChatGPT to reframe final output for specific stakeholder audiences. Use Gemini when you have video data or need maximum evidence grounding.

---

## Failure Mode #1 — Invented Evidence

### What it looks like
- Completely fictionalized quotes (all three major LLMs)
- "Frankenstein quotes" sewn from multiple participant statements into a single attribution (most common in ChatGPT)
- Participant IDs and timestamps that look authoritative but are fabricated

### Why it happens
LLMs generate text that's statistically likely given context—they don't retrieve quotes like a search engine. A model predicts what a quote *should* look like. Adding prompts like "give a punchy representative quote in under 20 words" almost guarantees composite fabrications.

### Fix 1A — Quote Selection Rules

Add to your analysis prompt:
```
QUOTE SELECTION RULES
- Start where the thought begins, continue until fully expressed
- Include reasoning, not just conclusions
- Keep hedges and qualifiers — they signal uncertainty
- Include emotional language when present
- Cite with participant ID and approximate timestamp [P03, ~14:30]
- Do not combine statements from different parts of the interview
- If a quote would exceed 3 sentences, break it into separate quotes
```

### Fix 1B — Verification Pass

After initial analysis, run this as a follow-up prompt:
```
QUOTE VERIFICATION

For each quote in the analysis above:
1. Confirm the quote exists verbatim in the source transcript
2. If the quote is a close paraphrase but not exact, flag it and provide the actual wording
3. If the quote cannot be located, mark as NOT FOUND

Output format:
Quote: [the quote]
Status: VERIFIED / PARAPHRASE / NOT FOUND
If paraphrase: Actual wording: [what they said]
Location: [Participant ID, timestamp, or line number]
```

Run this before any quote enters a deliverable. It typically takes 5 extra minutes. Without it, paraphrased or fabricated quotes end up in decks attributed to real participants—sometimes without consequence, sometimes as the difference between product messaging that resonates and copy that doesn't convert.

---

## Failure Mode #2 — False or Generic Insights

### What it looks like
- Themes too broad to act on: "Price is a factor in decisions," "Users value reliability," "People want more real-time information"
- Insights that could describe any product in your category, not yours specifically
- Themes that parrot back what you already know

### Why it happens
LLMs are pattern-finding machines trained to find consensus. They surface what multiple participants mentioned and generate a pattern-matched theme. The truly important insight might be something only a few people said—but if it's a business signal, it matters. LLMs also bring training priors: if thousands of churn analyses highlight price as #1, the model will weight toward price even when your data doesn't support it. Survey analysis is worse: "It's not for me" could mean four completely different things, but without guidance, AI lumps it into a generic "value perception" theme.

### Fix — 4-Component Context Loading

Add this structured context block *before* your analysis prompt:
```
ANALYSIS CONTEXT

1. PROJECT CONTEXT
[What specific decision or question this research supports. Example: "Exploring whether to add a screen to a screenless wearable" — not "doing customer research."]

2. BUSINESS GOAL
[What you're trying to achieve. Example: "Determine whether adding a screen would attract new users vs. alienate existing loyal users who chose us for being screenless."]

3. PRODUCT CONTEXT
[Domain knowledge the model needs to interpret statements correctly. Example: "Screenless wearable competing against Apple Watch and Garmin. Screenlessness is a core differentiator for our target segment."]

4. PARTICIPANT OVERVIEW
[Who's speaking. Example: "10 churned users, 5 of whom switched to Garmin. 3 long-term subscribers who have never tried a competitor."]
```

This prevents AI from defaulting to category-level themes. The model now knows which signals are relevant to your decision, what "I want to see my data" means in your product context, and how to weight evidence from different participant segments.

---

## Failure Mode #3 — Non-Actionable Signals

### What it looks like
- Themes that don't make the next decision easier: "Users need better onboarding," "18% of churned users want more actionable guidance"
- Recommendations that read as truisms: "Improve error handling," "Clarify navigation"
- Cluster labels so broad they contain contradictory implications

### Why it happens
LLMs compress information. Edge cases and specificity get lost in the averaging. Survey cluster counts look precise ("18% of responses") but the clusters themselves are too wide to act on—the label "more actionable guidance" could mean clearer metrics, workout plans, integrations, or coaching features. Different implications, one bucket.

### Fix — Specificity Prompts

Add to your analysis or follow-up prompt:
```
SPECIFICITY REQUIREMENTS

For each theme or recommendation:
1. Name the specific trigger — what feature, moment, or condition caused this?
2. Name the specific user segment experiencing this — not "users" but which users
3. Name the specific action this implies — what would we build, change, or remove?
4. If a theme applies to multiple different user needs, split it into separate themes
5. Flag any theme where the evidence could support contradictory product directions

A theme is not actionable if a team meeting about it would produce the question "but which direction?"
```

---

## Failure Mode #4 — Contradictory Insights

### What it looks like
- A participant says X at minute 10, contradicts it at minute 35, and the analysis reports only X
- Themes that smooth over tension between what users say and what their behavior suggests
- Missing the difference between "I want this feature" and "I would pay for this feature"

### Why it happens
LLMs handle unstructured interview data by imposing structure and jumping to conclusions. A 45-minute interview that starts with enthusiasm and ends with skepticism gets summarized as enthusiastic. Without guidance, AI flattens the timeline.

### Fix — Contradiction Detection Prompts
```
CONTRADICTION DETECTION

After generating themes and quotes:

1. For each participant, flag any statement that contradicts an earlier statement in their session
2. Note any tone shifts — where did enthusiasm shift to hesitation, or vice versa?
3. Flag any "I would" vs "I have" gaps — stated preferences vs. actual behavior
4. For survey data: flag open-text responses that contradict how the same respondent answered a structured question
5. Do not resolve contradictions. Surface them with the quote pairs and timestamps so I can interpret them.
```

This is especially important before making product recommendations. The contradiction often *is* the insight.

---

## Multi-Model Workflow Use Cases

When reliability matters more than speed, run the same workflow across multiple models:

### 1. Cross-Model Evals
Run the same analysis (same data, same prompts) across Claude, ChatGPT, and Gemini. If outputs converge, the workflow is solid. If they diverge widely, the workflow is the problem—not the model. Consistent divergence is a signal to tighten your prompt structure before trusting any single output.

### 2. LLM-as-Judge
After one model completes analysis, pass its output + the raw data to a second model: *"Evaluate this analysis. What did it miss? Where did it overgeneralize? What contradictions in the data does it not address?"* Acts as a skeptical colleague who's reviewed the same source material.

### 3. Ensemble Analysis
Run analysis across 3 models → treat convergence as confidence. Themes all three models independently surface = highest-confidence findings. Themes only one model catches = "investigate further" list. Same triangulation logic as mixed-method research.

### 4. Model Routing
Map tasks to best model per step: Claude for depth analysis, Gemini for evidence grounding, ChatGPT for stakeholder framing. Stop asking one model to be good at everything.

### 5. Red-Teaming Recommendations
Before finalizing a product recommendation, give it plus the raw data to a different model: *"Build the strongest possible case against this recommendation. What would have to be true for this to be the wrong call? What in the data contradicts this direction?"* When the counter-case is weak, the recommendation holds. When it's strong, go back to the data.

---

## Troubleshooting

| Symptom | Likely cause | Fix |
|---------|-------------|-----|
| Quotes don't match transcript | Model generated plausible-sounding text | Run Verification Pass |
| All themes sound like a generic wearables study | No context loading | Add 4-component context block |
| 18% of users want X but we don't know what to build | Cluster too broad | Specificity prompts |
| Analysis ignores what P04 said at minute 38 | LLM imposed early structure | Contradiction detection pass |
| ChatGPT analysis looks confident but citations feel off | Frankenstein quotes | Quote rules + verification |
| Different model, wildly different recommendation | Workflow problem, not model problem | Cross-model eval to diagnose |

---

## FAQ

**Q: These prompt blocks are long. Will they hurt output quality?**  
A: No — structured prompts improve reliability. The model has less ambiguity to fill with assumptions.

**Q: Do I need to run all four failure mode fixes every time?**  
A: Run Quote Rules + Verification always. Context loading is mandatory for any analysis that will inform a product decision. Specificity and Contradiction prompts are most important when analysis will go into a stakeholder deliverable or will anchor a recommendation.

**Q: My team uses ChatGPT by default. Should I switch?**  
A: Use the best tool for the step. ChatGPT is weakest at evidence integrity and strongest at stakeholder framing. These prompts close the gap but don't eliminate it entirely. If quote accuracy is critical, run the Verification pass more aggressively with ChatGPT than with Claude.

**Q: Does this work with survey data, not just interviews?**  
A: Yes. Add column disambiguation to your context loading ("Column D = customer open-text response. Column E = internal tag — ignore for analysis"). For sparse responses ("It's not for me"), use Specificity prompts to force the model to enumerate possible interpretations rather than collapsing to one.

---

## References

- Sullivan, C. (2026, Feb 17). How to do AI analysis you can actually trust. Lenny's Newsletter. https://www.lennysnewsletter.com/p/how-to-do-ai-analysis-you-can-actually
- Sullivan, C. (2026, Feb 28). Pressure-test your AI workflows across models. AI Customer Research Newsletter. https://substack.com/home/post/p-158838225 (via aicustomerresearch@substack.com)

---

## Related Materials & Guides

- `affinity_diagramming.md` — Apply context loading and verification pass during synthesis clustering
- `usability_test_reporting.md` — Apply verification pass before attributing quotes to participants in reports
- `session_video_analysis.md` — Use Gemini + NotebookLM for non-verbal behavioral analysis; apply contradiction detection for behavioral vs. stated intent gaps
- `synthetic_user_generation.md` — Use cross-model evals to calibrate synthetic persona outputs against real research patterns