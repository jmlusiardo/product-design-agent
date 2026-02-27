# Guide to Creating User Journey Maps and Event Storming Workshops

> **Executive Summary**  
> This guide explains how to create **Customer Journey Maps** and run **Event Storming** workshops. Both methods are powerful for visualizing user experiences, uncovering pain points, and aligning teams. Journey maps focus on a single persona’s emotional experience across phases, while event storming maps system-level events and frictions to clarify business processes.

---

## Overview

- **Purpose**: Visualize user experiences, identify friction points, and align cross-functional teams on customer goals.  
- **Scope**: Covers journey maps (persona-driven narratives) and event storming (domain-driven process events).  
- **Audience**: UX designers, product managers, developers, and stakeholders.  
- **Success Criteria**:
  - Clear mapping of actions, thoughts, and emotions (Journey Maps).
  - Identification of key events, hotspots, and system interactions (Event Storming).
  - Prioritized pain points and opportunities for improvements.

---

## Preparation

### Research & Planning
- Define persona(s) and scenario(s).
- Clarify scope of the journey (end-to-end vs. partial flow).
- Collect data: user research, customer interviews, analytics, and system logs.

*For structured customer interview questions to gather journey insights, pain points, and emotional responses, reference `user_feedback_questions.md` in the materials directory.*

### Checklist
- [ ] Define persona and user goal.
- [ ] Gather input from multiple stakeholders (support, sales, dev, etc.).
- [ ] Collect customer quotes, pain points, and expectations.
- [ ] Prepare workshop tools (digital boards like Miro, sticky notes, markers).
- [ ] Define clear start and end points for the mapping.

---

## Customer Journey Mapping

### Purpose
- It's very useful for mapping a user journey a persona does to complete a job.

### Structure
1. **Persona + Scenario**: Define a single persona and situation.  
2. **Expectations/Goals**: Note what the user hopes to achieve.  
3. **Phases**: Break down into major stages (Define, Compare, Negotiate, Select).  
4. **Actions**: List user activities at each stage.  
5. **Thoughts & Emotions**: Capture internal reactions, quotes, or frustrations.  
6. **Opportunities**: Highlight potential improvements.  
7. **Internal Ownership**: Assign departments or teams responsible.

### Key Principles
- Chronological flow from start to goal, and follow-up steps.
- One journey map per job.
- Must include **pain points**—otherwise, it’s incomplete.
- Outputs: clear touchpoints for improvement, shared organizational understanding.

### Journey Map Template & Usage
For structured journey mapping with consistent formatting, use the standardized framework provided in `materials/journey_map_template.md`. This template includes:
- Pre-defined entry points table with required fields
- Journey steps with scenario coverage (Positive, Negative, Edge cases)
- Follow-up actions across all timeframes (0-24 hours, 1-7 days, 1+ weeks)
- Success metrics framework and validation checklist

---

## Event Storming

### Purpose
- It's better used when there's many steps, or a lot of areas of improvement in the journey still and you want to get ideas.
- Messier but more comprehensive than journey maps.
- Maps **domain events** across systems and stakeholders.
- Useful for uncovering bottlenecks, hotspots, and system interactions.

### Process
1. **Map All Events**  
   - Capture events from start (Day 0) to goal completion.  
   - Use orange sticky notes in “Noun + Past Tense Verb” format.  

2. **Group Events into Milestones**  
   - Identify big phases or user milestones.  
   - Consolidate duplicates.  

3. **Clean Up & Categorize**  
   - **User struggles (frictions)**  
   - **User success moments**  
   - **Ideas and design opportunities**  
   - **Technical details & risks**  

4. **Prioritize Events**  
   - Use voting (e.g., 35 votes per person in 7 minutes).  
   - Identify top pain points and success factors.  

### Types of Notes (Legend)
- 🟨 **Key Event**: Critical for success.  
- 🟧 **Event**: Past-tense occurrence in the process.  
- 🟩 **People**: Roles involved.  
- 🟦 **Terminal Event**: Ends the process (e.g., cancellation).  
- 🩷 **System**: Tools or systems used.  
- 🟥 **Hotspot**: Current friction or unresolved issue.  

### Tips
- Start simple: map the “happy path” first.  
- Break long journeys into multiple phases.  
- Ensure domain experts can narrate the journey using only events.  
- Pay attention to **early events**—fixing them often has the biggest impact.  

---

## Aftermath / Follow-ups
- Share consolidated journey map or event storming output with all stakeholders.  
- Assign ownership of key touchpoints or pain points.  
- Define measurable actions (e.g., reduce support call time, simplify onboarding).  
- Revisit maps periodically to track progress and adapt.  

---

## Best Practices & Pitfalls

### Do
- Focus on the **user’s perspective** (not internal processes).  
- Involve cross-functional teams (UX, support, dev, sales).  
- Document emotions and quotes to keep it grounded in reality.  
- Prioritize improvements—don’t try to fix everything at once.  

### Avoid
- Mapping without real data (assumptions only).  
- Overcomplicating early drafts—start broad, refine later.  
- Ignoring hotspots or terminal events.  
- Treating mapping as a one-time activity—should be iterative.  

---

## Tools & Resources
1. Journey Map Tempalate and examples: `materials/journey_map_template.md`
2. A digital board (Like Figjam, or Miro), or (if you're doing an in-person activity) use a whiteboard, thick markers and sticky notes.  

---

## Cross-Guide Linkage

- **User Story Mapping** (`user_story_mapping.md`): The natural next step after journey mapping. Once you've mapped emotional pain points and touchpoints, use story mapping to translate those insights into a prioritized development plan. NNGroup frames this directly: journey maps reveal the problem; story maps plan the solution.

---

## References
- Event storming: The smartest approach to collaboration
beyond silo boundaries: https://www.eventstorming.com/  
- How To Run Your First Event Storming Session, by Agnieszka Pawlicka: https://selleo.com/blog/how-to-run-your-first-event-storming-session  
