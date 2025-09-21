# Guide to Reporting Usability Testing Results

> **Executive Summary** — A focused playbook for turning usability test data into concise, visual, and actionable reports. It covers what to include, how to structure findings, which visuals to use, and how to deliver results quickly and diplomatically. For *planning and running tests*, see `usability_testing.md`.

## Overview & Objectives
- **Purpose:** Make test outcomes clear, persuasive, and decision-ready.
- **Outcomes:** A short report (10–15 pages), an immediate executive email, and a stakeholder readout anchored in observed behavior and business priorities.
- **Principles:** Prioritize findings; use screenshots; include positive findings; distinguish user opinions from observer interpretations; keep tone neutral and constructive.

## Preparation (Post-Test Synthesis)
- Consolidate observers’ notes, recordings, and artifacts into themes.
- Calculate: task success rates, error/confusion counts, time-on-task, and severity (impact × frequency).
- Pull 6–12 representative verbatim quotes (positive + negative).
- Capture key screenshots (problem states + successful paths).
- Map every recommendation to a business/technology constraint.

### Reporting Checklist
- [ ] 3–5 *headline* insights for executives.  
- [ ] Visual summaries: success by task; errors/confusions; time on task; perceived ease/satisfaction.  
- [ ] Finding cards with **Observation → Evidence → Impact → Recommendation**.  
- [ ] Severity assigned using **impact vs. % affected**.  
- [ ] Positive findings called out.  
- [ ] Immediate email summary drafted.  
- [ ] Readout agenda and decision asks prepared.

## Main Flow / Report Structure
### 1) Executive Summary (1–2 pages)
- Study goal, participants (brief), top wins, top issues, and top recommendations.
- Send as a same-day **email summary**, followed by the full report.

### 2) Background (Concise)
- What was evaluated and why; who participated; high-level task list.
- Link to the original plan in `usability_testing.md` instead of repeating it.

### 3) Data Overview (Visual)
- **Success Rate by Task:** stacked pass/partial/fail bars.  
- **Task Performance by User:** per-participant success bars (optional).  
- **Time on Task:** line chart across tasks.  
- **Errors & Confusions:** grouped bars per task (separate “error” vs “confusion”).  
- **Subjective Satisfaction / Perceived Ease:** per-task ratings (Likert/smiley scale).

### 4) Key Findings (Themes or Tasks)
For each finding, use a compact card:
- **Observation (what happened):** plain description of behavior.
- **Evidence (how we know):** metric + screenshot + verbatim.
- **Impact (why it matters):** severity via **impact × frequency**.
- **Recommendation (what to change):** actionable, neutral phrasing.

### 5) Detailed Walk-Through (Appendix-style)
- Task-by-task vignettes showing blockers, misroutes, or delights.
- Annotated screenshots; callouts of error/confirmation message issues, labeling, localization, or performance.

### 6) Verbatim Quotes
- Curate *positive and negative* quotes to humanize findings.
- Attribute anonymously (e.g., “User 7, infrequent flyer”).

### 7) Recommendations & Next Steps
- Prioritize as **Critical / High / Medium / Low**.  
- Split into **Quick Wins** (copy, layout, messaging) vs **Larger Changes** (flows, architecture, platform).  
- For each item: owner, rationale, and success signal (what metric should improve).

## Metrics & Visualizations (What to Show)
- **Task Success / Failure / Partial:** primary outcome metric for each scenario.  
- **Time on Task:** interpret alongside perceived difficulty (spikes highlight friction).  
- **Errors vs. Confusions:** count per task; clarify definitions (error = incorrect action; confusion = visible uncertainty/frustration).  
- **Subjective Satisfaction & Perceived Effort:** capture per task; use simple scales (e.g., 1–5 with smiley anchors).  
- **Severity Rating:** judge by **impact on goal** and **% of participants affected**; visualize as a 2×2 or numeric scale.

> **Presentation tips:** Use screenshots to communicate findings; show per-task sub-ratings; include a thumbnail of the interface to refresh memory when presenting subjective scores.

## Templates / Canvases / Frameworks
### A) Finding Card (copy/paste)
Finding ID: F-<#>  |  Theme: <e.g., Forms / Search / Navigation>
Task(s): T1, T4
Observation: 
Evidence: <metric + brief note> —  — “”
Impact (Severity): <High/Med/Low>  (impact × frequency)
Recommendation:   → <owner/team>

### B) Theme Summary Table
| Theme | Key Issue | Evidence | Severity | Recommendation | Owner |
|---|---|---|---|---|---|

### C) Executive Email (same-day) Template
Subject: Usability Test – Top Findings & Next Steps

Thanks all. Highlights:
• Wins: <2–3 positives>.
• Issues: <3–5 most critical> (impact × frequency).
• Recommendations:  with proposed owners.

Full report to follow; readout scheduled on .

### D) Readout Agenda (45–60 min)
1. Objectives recap (2)  
2. Headline results (10)  
3. Visual data tour (10)  
4. Top findings & recommendations (20)  
5. Decisions & owners (10)

## Aftermath / Follow-ups
- Distribute the full report shortly after the email summary.  
- Host a readout; capture decisions and owners live.  
- Log recommendations in the backlog with severity tags.  
- Plan a light **validation test** after fixes to confirm improvements.

## Best Practices & Pitfalls
- **Do:** keep it short (10–15 pages); use screenshots; include positive findings; report promptly; add competitive/analyst notes when relevant; keep descriptions relevant and neutral.  
- **Avoid:** harsh wording; conflating user opinions with observer interpretations; “micro-usability” nitpicks overshadowing critical blockers; delaying delivery.

## Tools & Resources
- Charts: simple bar/line charts for success, errors/confusions, time; per-task Likert visuals for satisfaction.  
- Assets: annotated screenshots; session clips for pivotal moments.  
- Cross-reference: task list, questionnaires, and plan in `usability_testing.md` rather than duplicating content here.

## References
- User Research – Methods and Best Practices, Interaction Design Foundation (Course): https://www.interaction-design.org/courses/user-research-methods-and-best-practices
- How to analyze and report usability test results, Maze: https://maze.co/guides/usability-testing/results/
- Analyze Usability Test Data in 4 Steps, by Maria Rosala: https://www.nngroup.com/articles/analyze-usability-data/
