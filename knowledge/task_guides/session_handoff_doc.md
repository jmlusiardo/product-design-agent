# Session Handoff Guide

## Executive Summary

This guide enables the design assistant to generate session continuity documents that prevent context degradation (context rot) across AI sessions. It covers two modes: **Session Handoff** (end-of-session capture) and **Multi-Phase Planning** (upfront decomposition of complex requests into independent threads).

Use this task when the user explicitly requests a handoff document, asks to "split this into phases," wants to prepare for a new session, or signals awareness of context window limits.

---

## Prerequisites

- An active session with meaningful work completed (Mode 1), or
- A complex prompt that the user has identified as multi-phase (Mode 2)
- No uploaded files required — the assistant synthesizes from conversation history

---

## Why This Matters: Context Rot

AI sessions degrade when context windows fill and continuous compaction occurs. Each compaction summarizes and loses nuance. The model is sharpest at the **start** of each new session — not mid-session after multiple compactions.

The solution: instead of compacting, close the session cleanly and open the next one with a precise, human-curated context primer. This preserves output quality across long-running projects.

---

## Mode 1 — Session Handoff

### When to trigger
- User says: "generate a handoff document," "prepare the next session," "let's wrap up," "create a session summary"
- User signals context concern: "we're running out of context," "let's start fresh next time"

### Step-by-Step Workflow

#### Step 1 — Reconstruct the session
Review the full conversation and identify:
- **Goal(s):** What the user was trying to accomplish
- **Work completed:** Tasks executed, outputs delivered
- **Decisions made:** Key choices, rationale, and who decided
- **Artifacts:** Files created, templates filled, configs updated (name every one)
- **Methodologies applied:** Which task guides or frameworks were used

#### Step 2 — Identify carry-forwards
Surface everything the next session needs to know:
- Open questions and unresolved blockers
- Pending tasks or next steps
- Constraints or preferences established during the session
- Any context that was implicit but important (e.g., "user is designing for enterprise B2B")

#### Step 3 — Write the compressed context primer
This is the most important section. Write a tight, information-dense block (100–200 words max) that:
- States the project name and current phase
- Summarizes what was built and what decisions were locked
- Lists the 2–3 most important things the next session must know
- Is written in second person, as if briefing a new instance: "You are continuing work on..."

#### Step 4 — Suggest the opening prompt
Write one ready-to-use prompt the user can paste to open the next session, with the context primer embedded.

### Output Structure
``````markdown
# Session Handoff — [Project Name] — [Date]

## What We Did
[Narrative summary of session work]

## Decisions Made
| Decision | Rationale | Status |
|---|---|---|

## Artifacts Produced
- [filename or description] — [brief note]

## Open Questions & Blockers
- [ ] ...

## Context Primer for Next Session
> [Compressed 100–200 word block written as a briefing]

## Suggested Opening Prompt
`````[ready-to-paste prompt]```
`````

---

## Mode 2 — Multi-Phase Planning

### When to trigger
- User says: "split this into phases," "let's do this in separate threads," "break this into steps," "I don't want to hit context limits"
- User submits a complex prompt that involves 3+ distinct task types or sequential deliverables

### Step-by-Step Workflow

#### Step 1 — Analyze the request
Identify all distinct task components. Map them to `task_id`s from the task registry where possible. Note dependencies: which tasks require output from a prior phase as input.

#### Step 2 — Define phase boundaries
Split at natural dependency boundaries — not arbitrary size limits. Each phase must be **independently executable**: it should contain all context needed to run without the prior session.

Good split points:
- Research → Synthesis (different modes of thinking)
- Strategy → Execution (different output types)
- Draft → Review → Finalize (sequential refinement)
- Discovery → Definition → Design (distinct UX phases)

#### Step 3 — Write self-contained phase prompts
For each phase, write a prompt that:
- Opens with a context block summarizing what was established in prior phases (even if not yet done — write it as a template the user will fill in)
- States the specific goal of this phase
- Specifies the expected output format
- Notes what the next phase will need from this one

#### Step 4 — Produce the phase plan
Deliver a numbered phase list with rationale, then the individual phase prompts as copy-paste blocks.

### Output Structure
`````markdown
# Multi-Phase Plan — [Project/Task Name]

## Phase Overview
| Phase | Goal | Depends On | Output Needed by Next Phase |
|---|---|---|---|

## Phase 1 — [Name]
**Goal:** ...
**Context to paste at start:**
> ...
**Prompt:**
```[self-contained prompt]```

## Phase 2 — [Name]
...
```

---

## Quality Checks

Before delivering either mode:
- [ ] Every artifact from the session is named in Mode 1
- [ ] Context primer can stand alone without the conversation (test: could a new session understand it?)
- [ ] Each phase prompt in Mode 2 is truly self-contained (no implicit dependency on prior session)
- [ ] Decisions include rationale, not just outcomes
- [ ] Next steps are specific and actionable, not vague

---

## Cross-Guide References

- **`project_context.md` system** — The context primer from Mode 1 can be pasted into `project_context.md` to persist across all future sessions
- **`prompt_minification.md`** — Use to compress verbose context primers if needed
- **`agile_lean_ux_frameworks.md`** — For projects using sprint cycles, align phase boundaries with sprint structure

---

## References

- Context Window Management, Anthropic Documentation: https://docs.anthropic.com/en/docs/build-with-claude/context-windows
- Prompt Engineering Overview, Anthropic: https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
`````

---
`````markdown
# Session Handoff Template

> **Usage:** Copy this template at the end of a working session. Fill in each section before closing the thread. Upload the completed file to your Claude Project Knowledge to prime the next session.

---

# Session Handoff — [Project Name]
**Date:** [YYYY-MM-DD]
**Session #:** [N]
**Agent/Task Focus:** [e.g., design_handoff_spec, user_story_mapping]

---

## 🏁 What We Accomplished
<!-- 3–5 sentences. What was the goal and what did we deliver? -->

---

## ✅ Decisions Made
| # | Decision | Rationale | Locked? |
|---|---|---|---|
| 1 | | | ✅ / 🔄 |
| 2 | | | ✅ / 🔄 |

---

## 📦 Artifacts Produced
<!-- List every file, document, config, or output created this session -->
- [ ] [Artifact name] — [Brief description / location]

---

## ❓ Open Questions & Blockers
<!-- Carry these forward — the next session needs to address them -->
- [ ] ...
- [ ] ...

---

## 🧠 Context Primer
<!-- Write this as a briefing for a fresh Claude session. 100–200 words max. -->
<!-- Start with: "You are continuing work on..." -->

> You are continuing work on **[Project Name]**, currently in the **[phase]** phase.
>
> So far: [2–3 sentences on what's been built/decided]
>
> Critical context: [1–2 sentences on constraints, user type, platform, or key decisions]
>
> Next priority: [What the user wants to accomplish in this session]

---

## 🚀 Suggested Opening Prompt for Next Session
```
[Paste the context primer above here, then add the specific task request below it]

Now I'd like you to: [specific next task]
```

---

*Generated by product-design-assistant · session_handoff_doc task*
`````

---

## Prompt Packs para threads separados

Estos son dos prompts autocontenidos, listos para pegar en threads nuevos.

---

### Prompt Pack — Option C: Embedded Handoff en Task Guides
``````
# DAU Task — Option C: Embedded Session Handoff Triggers in Complex Task Guides

You are Design Assistant Updater (DAU), maintainer of the product-design-assistant ecosystem.

## Context
The project recently added a `session_handoff_doc` task (task_id: session_handoff_doc) that generates 
end-of-session continuity documents and multi-phase prompt plans. That task is now live in tasks.yaml, 
with a guide at knowledge/task_guides/session_handoff.md and a template at 
knowledge/materials/session_handoff_template.md.

## Goal
Embed an optional handoff prompt at the end of selected high-complexity task guides. The trigger 
should appear as a closing section that the agent delivers after completing the main task output, 
offering the user the option to generate a handoff doc.

The embedded prompt should be lightweight — one or two lines, not a full section — and only appear 
in task guides where sessions are likely to run long or produce multiple artifacts.

## Your Job
1. Search project knowledge for task guides that meet these criteria:
   - Multi-step workflows (5+ steps)
   - Produce multiple artifacts in a single session
   - Involve iterative work (e.g., design systems, research, strategy, component documentation)

2. For each identified guide, propose the minimal addition: a closing `## Session Continuity` 
   section (or equivalent) with a 1–2 line prompt like:
   > "This session produced several artifacts. Would you like me to generate a session handoff 
   > document to prime your next session? Just say 'generate handoff.'"

3. Deliver a DAU output (CHANGELOG + UNIFIED DIFF + FULL UPDATED FILES) covering all 
   modified task guides.

## Constraints
- Minimal diff: add only the closing section, touch nothing else in each guide
- Do not add to simple or single-artifact tasks
- The trigger phrase must route correctly to session_handoff_doc via the router
- Suggest no more than 6–8 task guides for the first pass

Begin by searching project knowledge to identify candidate task guides.
``````

---

### Prompt Pack — Option B: project_context.md as Handoff Vehicle
``````
# DAU Task — Option B: project_context.md as Living Session Handoff

You are Design Assistant Updater (DAU), maintainer of the product-design-assistant ecosystem.

## Context
The project has a `project_context.md` system — a file users can add to their Claude Project 
Knowledge to inject business/client context into task execution. It sits in the hierarchy below 
task requirements but above user preferences.

The project also recently added a `session_handoff_doc` task (task_id: session_handoff_doc) that 
generates compressed context primers at the end of sessions.

## Goal
Design and implement the integration between `session_handoff_doc` (Mode 1 output) and the 
`project_context.md` system. Specifically:

1. **Update the `session_handoff.md` task guide** to include a section explaining that the 
   Context Primer section of the handoff doc is designed to be pasted into `project_context.md`, 
   replacing or extending the prior session's context block.

2. **Update or create a `project_context_template.md`** (in knowledge/materials/) that includes 
   a dedicated `## Session History` block — a versioned log where each session's context primer 
   gets appended (most recent first), so the file becomes a living project memory.

3. **Add 2–3 router signals** to router_index.md for update-project-context patterns 
   (e.g., "update context file", "add to project context", "save session to context").

4. **Document the workflow** clearly in the template: 
   - At end of session → generate handoff doc → copy Context Primer → paste into project_context.md
   - At start of next session → project_context.md is already in Project Knowledge → assistant 
     reads it automatically at Step 0

## Constraints
- Minimal diff: update session_handoff.md (add one cross-reference section), create/update 
  project_context_template.md, add signals to router_index.md
- Do not modify assets/instructions.md unless the project_context.md detection logic needs updating
- Keep the session history log format simple: date + 100-word primer per entry

Deliver a DAU output (CHANGELOG + UNIFIED DIFF + FULL UPDATED FILES) for all affected files.
Begin by searching project knowledge for the current project_context.md documentation and 
session_handoff.md to avoid conflicts.
``````