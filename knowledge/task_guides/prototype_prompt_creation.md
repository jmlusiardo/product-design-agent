# Prototype Prompt Creation Guide

> **Executive Summary** — This guide provides a structured methodology for transforming initial product ideas into comprehensive design specifications suitable for prototyping tools. It follows a sequential questioning approach that gathers essential information, identifies key user flows, and generates detailed component specifications. The process ensures consistent, actionable design specs that prototyping tools can interpret effectively.

---

## Overview & Objectives

- **Purpose:** Transform vague product ideas into structured, actionable design specifications for prototyping tools
- **Scope:** Complete workflow from initial concept to final markdown specification
- **Audience:** Product designers, UX designers, product managers, entrepreneurs, startup teams
- **Success Criteria:**
  - Clear product overview with defined platform and users
  - Focused user flow selection (maximum 5 flows identified)
  - Detailed component and interaction specifications
  - Prototyping-tool-ready markdown output

---

## Prerequisites

### Information Gathering Readiness
- [ ] User has initial product concept or problem statement
- [ ] Basic understanding of target users (even if rough)
- [ ] Platform preference identified or open to suggestions
- [ ] Willingness to answer sequential guided questions

### Tool Requirements
- [ ] Access to prototyping tools (Figma, Framer, Webflow, etc.)
- [ ] Markdown editor or text processing capability
- [ ] Understanding of component-based design principles

---

## Core Methodology: Sequential Information Gathering

### Step 1: Core Objective Discovery (5-10 minutes)

**Objective:** Establish clear product purpose and value proposition

**Script:** "What is the main goal of your product? For example:
- Help users track expenses
- Connect with others  
- Manage projects efficiently"

**Key Actions:**
- [ ] Ask open-ended question about product goal
- [ ] Listen for specific verbs (track, connect, manage, create, etc.)
- [ ] Clarify ambiguous statements
- [ ] Document core objective in one clear sentence

**Quality Checks:**
- Is the objective specific enough to guide design decisions?
- Does it avoid technical implementation details?
- Can you imagine specific user scenarios from this objective?

---

### Step 2: Target User Identification (5-10 minutes)

**Objective:** Define primary user segment to inform design decisions

**Script:** "Who are the intended users of your product? For example:
- Freelancers
- Students  
- Parents
- Small business owners"

**Key Actions:**
- [ ] Probe for specific user characteristics
- [ ] Ask about user needs, constraints, or contexts
- [ ] Clarify if multiple user types exist (focus on primary)
- [ ] Document user segment with relevant characteristics

**Quality Checks:**
- Is the user segment specific enough to make design trade-offs?
- Are there implied user needs or constraints?
- Would this user segment actually need the stated objective?

---

### Step 3: Platform Selection (3-5 minutes)

**Objective:** Establish technical constraints and interaction patterns

**Script:** "What platform is your product for? Please choose one from the following options:
1. Responsive Web (Mobile-optimized)
2. Responsive Web (Desktop-optimized)  
3. iOS Native Mobile App (iPhone-optimized)
4. Android Native Mobile App (Phone-optimized)
5. If none of the above, please specify (e.g., iOS Native Mobile App, iPad-optimized)"

**Key Actions:**
- [ ] Present standard platform options
- [ ] Clarify any custom platform requirements
- [ ] Note platform-specific design implications
- [ ] Document final platform choice

**Platform Implications:**
- **Mobile-optimized web:** Touch interactions, responsive breakpoints, progressive enhancement
- **Desktop-optimized web:** Mouse interactions, larger screens, complex layouts
- **iOS/Android native:** Platform-specific patterns, native components, gesture conventions

---

### Step 4: Ambiguity Resolution (Variable time)

**Objective:** Fill information gaps and clarify unclear aspects

**Common Clarification Areas:**
- Vague user descriptions ("professionals" → "freelance graphic designers")
- Broad objectives ("social platform" → "help photographers share and get feedback")
- Missing context ("booking app" → "restaurant reservation system for busy professionals")

**Script Templates:**
- "When you say [user statement], do you mean [specific interpretation] or [alternative interpretation]?"
- "Can you give me a specific example of how [target user] would use this?"
- "What problem are you solving that existing solutions don't address?"

---

### Step 5: User Flow Discovery & Selection (10-15 minutes)

**Objective:** Identify and prioritize the most essential user journeys

#### 5A: Flow Generation
**Process:**
- [ ] Break down user journey into distinct flows
- [ ] Limit to maximum 5 key flows
- [ ] Exclude sign-up/sign-in (these don't count toward limit)
- [ ] Focus on core value delivery

**Example Flow Generation:**
For a meal planning app:
1. Browse Recipes → Add to Meal Plan → Generate Shopping List
2. Create Custom Recipe → Save to Library → Share with Family  
3. View Weekly Plan → Adjust Meals → Update Shopping List
4. Scan Barcode → Check Nutrition → Add to Meal Plan
5. Set Dietary Preferences → Get Recipe Recommendations → Plan Week

#### 5B: Flow Selection
**Script:** "Here are the key user flows I've identified:
[List flows 1-5]

Which user flow would you like to proceed with?"

**Selection Criteria:**
- Most directly achieves core objective
- Represents primary user value
- Contains sufficient complexity for meaningful prototype
- User shows strongest interest or excitement

---

### Step 6: Component & Interaction Mapping (15-20 minutes)

**Objective:** Detail each step of selected flow with specific UI components and interactions

#### For Each Step in Selected Flow:

**Page Name Definition:**
- Clear, descriptive page names (Homepage, Search Results, Product Detail, Checkout)
- Reflect user mental model and navigation

**Component Identification:**
- List specific UI elements needed (Navigation bar, Search field, Product cards, Submit button)
- Focus on functional components, not decorative elements
- Consider required information architecture

**Interaction Specification:**
- Describe precise user actions (Clicking "Add to Cart," Tapping calendar to select date, Typing into form field)
- Note state changes and feedback
- Include error handling interactions

**Example Mapping:**
Flow Step: Browse Recipes
├── Page Name: Recipe Library
├── Components:
│   ├── Search bar with filters
│   ├── Recipe card grid
│   ├── Category navigation
│   └── Sort/filter controls
└── Key Interactions:
├── User types search query
├── User taps filter chips
├── User scrolls through results
└── User taps recipe card to view details

---

### Step 7: Design Specification Preview (5-10 minutes)

**Objective:** Validate completeness and accuracy before final generation

**Preview Structure:**
```markdown
## Product Overview
- Platform: [Selected platform]
- Target Users: [Defined user segment]

## Core Objective  
[Clear objective statement]

## Selected User Flow
[Flow name with key steps]

## Page & Component Details
### [Page Name]
- Components: [List]
- Key Interactions: [List]

[Repeat for each page]

**Validation Questions:**
- "Does this preview look good to you?"
- "If yes, I'll generate the final markdown format for you to copy"
- "If no, please make revisions and provide them back to me so I can generate the final markdown format"


### Step 8: Final Markdown Generation (3-5 minutes)
- Objective: Produce prototyping-tool-ready specification
- Final Format Structure:
```markdown
# Generate a clickable prototype based on the Design Spec below:

## 1. Product Overview
- **Platform:** [Platform choice]
- **Target Users:** [User segment]

## 2. Core Objective
[Objective statement]

## 3. Key User Flow
[Selected flow with arrow notation: Step 1 → Step 2 → Step 3]

## 4. Key Pages & Components

### [Page Name]
- **Components:** [Comma-separated list]
- **Key Interactions:** [Descriptive interaction list]

[Repeat for each page in flow]

## 5. Additional Notes
[Optional: Design preferences, accessibility requirements, style guidance]
```
---

## Quality Assurance Checklist

### Content Completeness
- [ ] All 5 core questions answered thoroughly
- [ ] Selected user flow clearly defined
- [ ] Each flow step has corresponding page specification
- [ ] Components list covers functional requirements
- [ ] Interactions are specific and actionable

### Specification Quality
- [ ] Components are prototyping-tool implementable
- [ ] Interactions match platform conventions
- [ ] No technical implementation details included
- [ ] Language is clear and unambiguous
- [ ] Flow achieves stated core objective

### Markdown Formatting
- [ ] Proper heading hierarchy (H1-H3)
- [ ] Consistent bullet point formatting
- [ ] Bold emphasis for key terms
- [ ] Clean, readable structure
- [ ] Ready for copy-paste into prototyping tools

---

## Common Challenges & Solutions

### Challenge: Vague Product Descriptions
**Solution:** Use analogy prompting
- "Is this similar to [existing product] but for [different audience]?"
- "Think of this like [familiar app] meets [another concept]"

### Challenge: Too Many User Types
**Solution:** Force prioritization
- "If you could only design for one type of user first, who would it be?"
- "Which user segment would be most likely to pay for this?"

### Challenge: Overly Complex Flows
**Solution:** Scope reduction
- "What's the minimum viable version of this flow?"
- "If users could only do one thing, what would create the most value?"

### Challenge: Technical Implementation Focus
**Solution:** Redirect to user experience
- "Instead of how it works technically, tell me what the user sees and does"
- "Focus on the experience, not the engineering"

---

## Integration with Prototyping Tools

### Figma Integration
- Use generated components list to create component library
- Map interactions to Figma's prototyping connections
- Consider responsive breakpoints for web platforms

### Framer Integration  
- Transform component specifications into Framer components
- Use interaction descriptions for animation triggers
- Leverage Framer's code component capabilities for complex interactions

### Webflow Integration
- Map page structure to Webflow's element hierarchy
- Use component list for symbol/component creation
- Apply responsive design considerations

---

## Advanced Techniques

### Multi-Flow Specifications
For complex products, repeat process for additional flows:
1. Complete first flow entirely
2. Return to Step 5 for second flow selection
3. Generate separate specifications
4. Consider flow interconnections

### Accessibility Integration
Include accessibility considerations:
- Screen reader interaction patterns
- Keyboard navigation specifications
- Color contrast requirements
- Touch target sizing

### Responsive Considerations
For web platforms, specify:
- Mobile/desktop component variations
- Responsive interaction adaptations
- Breakpoint-specific layouts

---

## Cross-References & Related Resources

### Directly Related Task Guides
- **[writing_prompts.md](writing_prompts.md)** — Apply CTEPFT framework (Context, Task, Examples, Persona, Format, Tone) when crafting the prototype creation prompts for optimal AI assistant responses
- **[component_documentation.md](component_documentation.md)** — Reference component documentation standards when detailing UI components in design specifications
- **[design_pitch.md](design_pitch.md)** — Use problem framing and solution narrative techniques from design pitches to strengthen core objective articulation

### Supporting Task Guides
- **[user_journey_mapping.md](user_journey_mapping.md)** — Apply journey mapping principles when breaking down user flows into component steps and identifying pain points
- **[wireframing.md](wireframing.md)** — Leverage wireframing best practices for component layout and information architecture decisions
- **[design_critique.md](design_critique.md)** — Use critique frameworks during the preview validation step to ensure specification quality
- **[stakeholder_management.md](stakeholder_management.md)** — Apply stakeholder alignment techniques when multiple user types are identified during target user definition

### Complementary Materials
- **[prompt_templates_registry.md](prompt_templates_registry.md)** — Access the complete prototype_design_spec_generator template and related prompt variations
- **[design_system_checklist.csv](design_system_checklist.csv)** — Reference component naming conventions and interaction patterns for consistency across specifications
- **[user_flow_templates.md](user_flow_templates.md)** — Use pre-built flow patterns for common product types (e-commerce, SaaS, mobile apps, etc.)

### Advanced Integration Workflows
- **[design_system_integration.md](design_system_integration.md)** — Connect generated specifications with existing design system components and tokens
- **[usability_testing_plan.md](usability_testing_plan.md)** — Transform finalized design specifications into testable prototype scenarios and user tasks
- **[accessibility_audit.md](accessibility_audit.md)** — Apply accessibility requirements to component specifications before prototyping tool implementation

### Process Enhancement Resources
- **[meeting_facilitation.md](meeting_facilitation.md)** — Use facilitation techniques when conducting the sequential questioning process with stakeholder groups
- **[prioritization.md](prioritization.md)** — Apply RICE scoring or effort-impact analysis when users struggle to select between multiple user flows
- **[agile_lean_ux_frameworks.md](agile_lean_ux_frameworks.md)** — Integrate prototype creation into sprint planning and lean UX validation cycles