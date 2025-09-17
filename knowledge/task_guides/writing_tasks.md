# Task Writing Guide: Essential Components and Structure

## Task Title Format
- **Structure:** `[{Project Name}] {Action} + {Object} + {Purpose}`
- **Include type tags:** `(design)`, `(research)`, `(development)`, `(handoff)`
- **Examples:**
  - `[Pausar Tarjeta] (design) Create error handling flows`
  - `[Mobile App] (research) Conduct user interviews for onboarding`
  - `[Dashboard] (development) Implement data visualization component`

## Required Fields for All Tasks
1. **Task Title** - Clear action and purpose
2. **Objective/Business Outcome** - Expected results and value
3. **Definition of Done** - 3-6 concrete, verifiable deliverables
4. **Context** - Background, dependencies, references

## Task Estimation Scale (Fibonacci)
| Points | Complexity | Time Estimate | Recommendation |
|--------|------------|---------------|----------------|
| 0 | Minimal | < 30 minutes | Group multiple 0-point tasks |
| 1 | Very Low | Few hours, < 1 day | Standard small task |
| 2 | Low | 1-2 days | Common task size |
| 3 | Medium | 2-4 days | Typical feature work |
| 5 | High | 5-8 days | Consider breaking down |
| 8 | Very High | Full sprint or more | Must be divided |
| 13 | Unmeasurable | Needs breakdown | Research spike required |

# Business Outcome Formats for Tasks

## User Story Format
`As a [user type], I want [action] so that [benefit]`

**Example:**
As a mobile app user, I want to save my payment method so that I can checkout faster on repeat purchases.

## Job Story Format  
`When I [situation], I want to [motivation], so I can [expected outcome]`

**Example:**
When I'm checking out on mobile during my commute, I want to complete payment in under 30 seconds, so I can finish my purchase before my train arrives.

## Hypothesis Format
`We believe that [solution] will achieve [outcome] as measured by [metrics]`

**Example:**
We believe that adding one-click payment options will reduce checkout abandonment by 25% as measured by conversion rate analytics over 4 weeks.

## Context Section Requirements
- **Origin:** What triggered this task?
- **Background:** Relevant history or previous decisions  
- **Dependencies:** Prerequisites or blockers
- **References:** Links to documentation, designs, research
- **Constraints:** Technical, business, or scope limitations

# Definition of Done Best Practices

## Writing Effective Completion Criteria
- **3-6 concrete, verifiable deliverables**
- Each criterion must be binary (done/not done)
- Include specific quality standards
- Avoid subjective language ("looks good", "feels right")

## Good Definition of Done Examples

### Design Tasks
- Wireframes exported to Figma with component specifications
- User flow diagram documenting happy path and 2 error scenarios  
- Component specifications documented for development handoff
- Stakeholder review completed with written approval
- Accessibility annotations included (WCAG 2.1 AA compliance)

### Research Tasks
- 8 user interviews conducted with prototype testing
- Quantitative metrics collected (task completion time, success rate)
- Qualitative insights synthesized into key findings report
- Recommendation provided with confidence level and rationale
- Findings presented to product team with recorded session

### Development Tasks
- Feature implemented according to acceptance criteria
- Unit tests written with >90% code coverage
- Code reviewed and approved by senior developer
- Integration tests passing in staging environment
- Documentation updated in team wiki
- Performance benchmarks meet defined thresholds

# Task Templates by Type

## Design Task Template

"[Project] (design) {Action and Object}
Business Outcome
{User story, job story, or hypothesis format}
Definition of Done

{Specific design deliverable with format/location}
{Review/approval requirement}
{Documentation requirement}
{Handoff requirement}

Context
{Background explaining why this task exists}
{Links to research, requirements, dependencies}"

## Research Task Template

"[Project] (research) {Research Activity}
Business Outcome
{Hypothesis or learning objective}
Definition of Done

{Number} {research method} conducted with {target users}
{Quantitative metrics} collected and analyzed
{Synthesis deliverable} completed
{Recommendation or insight} documented
{Presentation/sharing} completed

Context
{Research question and business rationale}
{Methodology and participant criteria}
{Links to research plan and tools}

## Development Task Template

[Project] (development) {Feature/Component}
Business Outcome
{User story format preferred}
Definition of Done

{Functionality} implemented per acceptance criteria
{Testing requirements} completed
{Code review} approved
{Documentation} updated
{Performance/security} requirements met

Context
{Technical background and constraints}
{API/integration requirements}
{Links to specifications and designs}

# Progress Tracking and Communication

## Journaling Method for Task Updates
Document significant progress within the task using dated entries.

### Format Structure
- Use `# [Date] - [Milestone Title]` headings
- Include key accomplishments and insights
- Note blockers or changes in scope
- Link to deliverables and artifacts

### Example Journal Entry

March 19, 2025 - Initial Research Findings
Completed 5 of 8 user interviews. Key insights emerging:

Navigation pattern A preferred by 80% of participants
Payment step causing confusion in all tests
Mobile performance concerns raised by 3 participants

Next steps: Complete remaining interviews, analyze quantitative data
March 22, 2025 - Final Report Complete
Research synthesis complete. Recommendation: proceed with Navigation Pattern A.
Deliverables:

Research report: [Figma link]
Presentation slides: [URL]

## Communication Guidelines
- When sharing updates in Slack/Teams, include link to journal entry
- For time-constrained projects, focus on final deliverables
- Include Slack/Teams link in journal when updates are shared externally
- Use brief updates for 0-1 point tasks, detailed journaling for larger work

# Task Quality Checklist and Common Pitfalls

## Pre-Creation Quality Check
Before creating any task, verify:

### Clarity
- [ ] Title clearly indicates the work to be done
- [ ] Objective explains the business value  
- [ ] Definition of Done is specific and measurable
- [ ] No ambiguous or subjective language used

### Completeness  
- [ ] All required fields populated
- [ ] Context provides sufficient background
- [ ] Dependencies and constraints identified
- [ ] Relevant links and references included

### Actionability
- [ ] Clear next steps for assignee
- [ ] Realistic timeline and scope
- [ ] Success criteria defined and testable
- [ ] Single owner/assignee identified

## Common Pitfalls to Avoid

### Vague Objectives
❌ **Bad:** "Improve the user experience"
✅ **Good:** "Reduce checkout abandonment by 15% through simplified payment flow"

### Unmeasurable Completion Criteria  
❌ **Bad:** "Design looks good"
✅ **Good:** "Design system components used consistently with documented specifications"

### Missing Context
❌ **Bad:** "Create login page"  
✅ **Good:** "Create login page to address 40% user drop-off at authentication step"

### Scope Creep
❌ **Bad:** "Design entire checkout flow with payments, shipping, and user accounts"
✅ **Good:** "Design payment method selection step with saved card support"

### Priority Confusion
- Use **High/Medium/Low** for planned work
- Use **Urgent** only for sprint interruptions that override other priorities
- Include business rationale for high-priority items