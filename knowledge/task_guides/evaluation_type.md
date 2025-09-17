# Evaluation Type Definition Playbook: From Questions to Validation

> **Executive Summary** — This guide helps you define the right evaluation for your project by clarifying learning goals, selecting method families, deciding where and whom to study, planning measures, and translating data into decisions and validation. Use the checklists and step-by-step flow to scope a practical, context-aware evaluation that mixes methods when needed and anchors against comparisons that matter.

## Overview

- **Purpose:** Provide a concise, repeatable way to define “what evaluation do we need?” anchored in project context, questions, and validation needs.
- **Scope:** From framing questions → choosing evaluation type → sampling & tasks → measures & analysis → interpretation → validation.
- **Audience:** PMs, Designers, Researchers, Data/Eng leads planning product or research evaluations.
- **Success Criteria / KPIs:** Clear evaluation brief (objectives, methods, setting, participants, tasks, measures, comparator) and a validation plan beyond raw evaluation results.

## Preparation

### Research & Planning Inputs
- Clarify **what you want to understand** before setup.
- List **initial assumptions / principles / theories** to interpret results and adapt as needed.
- Decide **evaluation focus** (signal) vs. everything else (noise).

### Context & Constraints
- Expect to **combine methods**; pick what’s reasonable for your context.
- Early stages: consider **investigative evaluations**.
- **Lab** = more control, less realism; **real world** = more realism, often qualitative.

### Preparation Checklist
- - [ ] Document learning goals (“what we want to understand”).
- - [ ] Write current assumptions / theories to apply.
- - [ ] Identify core signal you’re trying to find; list likely noise.
- - [ ] Choose study setting (lab vs. field) and timing (stage).
- - [ ] Draft participant profile(s) and sampling approach.
- - [ ] List products/services in scope and boundaries.
- - [ ] Draft task list and sequence (include possible distracter task).
- - [ ] Define measures & analysis approach (incl. stats plan).
- - [ ] Define comparator(s) / benchmark(s).
- - [ ] Outline validation plan (beyond the evaluation itself).

## Main Flow / Process

### 1) Frame the Learning Goals (10 minutes)
- Capture the main question(s) the evaluation must answer.
- Write assumptions/theories that shape interpretation.

### 2) Select the Evaluation Type (15 minutes)
- **Method focus:** Use a mix; pick approaches aligned to whether you need “how often/does it happen?” vs. “why/what’s new?”.
- **Improvement vs. judgement:**  
  - *Formative* → find flaws, pain points, opportunities (improve the thing).  
  - *Summative* → determine if the solution is good enough.
- **Stage & setting:**  
  - *Investigative* for early exploration.  
  - *Lab* (control) vs. *Real world* (ecology; often qualitative).

### 3) Define Environment & Comparators (10 minutes)
- Choose **lab vs. field** per realism/control trade-off.
- Identify **what you’ll compare results to** (baseline, prior version, benchmark). It’s required to judge good vs. bad and not always obvious.

### 4) Recruit & Sample (15 minutes)
- **Who & how many:** Expert reviews are quick/cheap; real-user evaluations are the ultimate check—aim to capture real usage. More users ⇒ more power/sensitivity; adjust to problem and fix costs.
- **Segmenting:** People differ; use participants from the **same segment/group** to reduce individual variability.

### 5) Task & Interaction Design (15 minutes)
- List **products/services** users will touch and the **tasks/activities** they’ll perform.
- **Ordering matters** (initial vs. long-term behavior); consider a **distracter task** to test without full attention.

### 6) Measures & Analysis Plan (10 minutes)
- Plan for **frequency/coverage** (e.g., “how often do users hit the issue?”) and **judgement** of sufficiency. Use appropriate statistics.
- Pointers: **contingency tables**; use a stats package or social statistics calculator.

### 7) From Data to Knowledge (15 minutes)
- Inspect the **dips**—areas without participant agreement.
- When possible, **test both original and modified solutions over multiple days**.
- Understand knowledge forms: **Descriptive** (what happened), **Predictive** (what will happen; cause→effect), **Synthetic** (what to do to reach desired outcome).
- **Generalization:** Interpolate within data; be cautious with extrapolation. Combine **reduction & reconstruction** (precise sub-studies) with **holistic analysis** (end-to-end realism). Usually both are needed.

### 8) Wrap-up & Decision/Validation (10 minutes)
- Evaluation answers “is it good enough?” but **evaluation alone isn’t sufficient for validation**.
- **Sampling** addresses singularity of people and context; for **generative artifacts** (e.g., toolkits, interfaces), sampling can be impossible—use **justifications** (expert opinion, prior research, or new experiments) and target **weak spots** in those justifications.

## Templates / Canvases

### Evaluation Definition Questionnaire (Use as a one-pager)
- **Learning Goal**  
  - What do we want to understand? (primary question; scope)
- **Assumptions / Theories**  
  - Which assumptions, principles, or theories will we apply when interpreting results?
- **Evaluation Focus**  
  - What are we trying to find? (treat the rest as noise)
- **Method & Setting**  
  - Mix of methods (as context requires); investigative (early), lab (control), real world (ecology).  
  - Formative (improve) vs. Summative (judge).
- **Participants & Sampling**  
  - Who and how many? Experts vs. users; plan for power & sensitivity; segment to reduce variability.
- **Prior Knowledge / Experience**  
  - Relevant experience with device/app/similar apps.
- **Products / Services in Scope**  
  - What systems are included/excluded?
- **Tasks / Activities & Sequence**  
  - What tasks? In what order (initial vs. long-term)? Include distracter tasks if needed.
- **Measures & Analysis**  
  - Stats approach (significance, CIs; contingency tables; calculator/package).
- **Comparator(s)**  
  - What will we compare against (baseline, benchmark, prior version)?
- **Validation Plan**  
  - Beyond evaluation: sampling, justifications, and targeted follow-up studies.

### Execution Checklist (Print & bring)
- - [ ] Learning goal and assumptions documented.
- - [ ] Evaluation type & setting chosen (investigative / formative / summative; lab / field).
- - [ ] Participant criteria, segment(s), N, and sampling plan approved.
- - [ ] Products/services in scope confirmed.
- - [ ] Tasks scripted and sequenced; distracter task (if used) defined.
- - [ ] Measures & analysis plan prepared (incl. contingency table design or applicable tests).
- - [ ] Comparator defined and instrumented (A/B, baseline run, benchmark).
- - [ ] Schedule spans multiple days if comparing original vs. modified solutions.
- - [ ] Risk log for generalization limits and planned follow-ups.
- - [ ] Validation justifications listed with weakest links to probe.

## Aftermath / Follow-ups
- **Synthesize findings** into descriptive, predictive, and synthetic knowledge; call out areas of disagreement (“dips”).
- **Address generalization**: identify where results are safe to interpolate; avoid extrapolation claims without new evidence.
- **Plan validation**: if evaluation is insufficient, add expert reviews, literature grounding, or new experiments focused on weak justifications.

## Best Practices & Pitfalls
- **Do:** Combine methods to fit context; keep signal clear; compare against something meaningful.
- **Do:** Align tasks with desired learning (initial vs. long-term use).
- **Avoid:** Over-relying on lab control when field realism is needed—or vice versa.
- **Avoid:** Treating evaluation results as validation without justifications and sampling considerations.
- **Remember:** People vary; segment to reduce noise and plan N for sensitivity.

## Tools & Resources
- **Contingency tables (design & interpretation)** — Wikipedia.  
  https://en.wikipedia.org/wiki/Contingency_table
- **Repeated-Measures ANOVA (calculator)** — SocSciStatistics.  
  https://www.socscistatistics.com/tests/anovarepeated/default.aspx
- **Sampling (statistics)** — Wikipedia.  
  https://en.wikipedia.org/wiki/Sampling_(statistics)

#references
- What I want to understand? — https://www.notion.so/What-I-want-to-understand-aa264a65647c46ebb35af3a2d65bd22f?pvs=21
- Which are the initial assumptions / principles / theories? — https://www.notion.so/Which-are-the-initial-assumptions-Which-principles-or-theories-you-want-to-apply-4301790b37c64aef845f1ac48099aaa7?pvs=21
- Which type of evaluation it will be? — https://www.notion.so/Which-type-of-evaluation-it-will-be-What-I-am-trying-to-find-about-the-rest-is-noise-1446a4803680469388784cd769f75fe9?pvs=21
- How many individuals or groups will I need? Who to choose? — https://www.notion.so/How-many-individuals-or-groups-I-will-need-for-the-study-Who-am-I-going-to-choose-bb851ad7473c46979c96cc491237c6d9?pvs=21
- Which prior knowledge or experience do they have? — https://www.notion.so/Which-prior-knowledge-or-experience-they-have-on-that-device-or-in-that-application-or-with-simila-713ab0402bc24f09a283d7aea381f84b?pvs=21
- Which products or services will they interact with? — https://www.notion.so/Which-are-the-products-or-services-they-will-have-to-interact-with-5cd428a1a798479a896feeaff87534e3?pvs=21
- Which tasks or activities will they perform? — https://www.notion.so/Which-are-the-tasks-or-activities-they-will-make-c9c8108fa23a49a295ccb837c4cef766?pvs=21
- To what will I compare the results? — https://www.notion.so/To-what-I-will-be-comparing-the-results-3108ec664542464aa9f6d4d3edb992dd?pvs=21
- Contingency table — https://en.wikipedia.org/wiki/Contingency_table
- Repeated-Measures ANOVA calculator — https://www.socscistatistics.com/tests/anovarepeated/default.aspx
- Sampling (statistics) — https://en.wikipedia.org/wiki/Sampling_(statistics)