# Journey Map Template

## Template Customization Rules

### REQUIRED Elements (Never Remove)
1. **Entry Points Table**: Must include minimum 2 entry points to prevent single-channel bias
2. **Journey Steps**: Minimum 3 steps required (Discovery/Awareness → Core Action → Follow-up)
3. **Scenario Coverage**: Each step MUST include Positive, Negative, and at least one edge case scenario
4. **Follow-up Actions**: All three timeframes (0-24 hours, 1-7 days, 1+ weeks) must be addressed
5. **Success Metrics**: Primary and secondary metrics required for measurable outcomes

### FLEXIBLE Elements (Can Modify)
- Step names and descriptions (adapt to specific journey context)
- Number of journey steps (3-7 recommended, can extend for complex flows)
- Scenario types within steps (add domain-specific edge cases)
- Touchpoint categories (customize based on available channels)
- Opportunity descriptions (tailor to business priorities)

### VALIDATION Checklist
Before using this template, ensure:
- [ ] User persona clearly defined with specific goals and context
- [ ] Journey scope boundaries set (what triggers start, what defines completion)
- [ ] Multiple entry points identified to avoid tunnel vision
- [ ] Each step includes user emotions and system responses
- [ ] Pain points documented with specific improvement opportunities
- [ ] Success criteria tied to measurable business/user outcomes

### INTEGRATION Requirements
- **User Stories**: When job or user story needed, follow `writing_statements.md` format
- **Persona Validation**: Cross-reference journey insights with `user_personas.md` profiles
- **Emotion Mapping**: Use `empathy_mapping.md` for deeper emotional state analysis
- **Process Discovery**: For complex system interactions, consider `journey_mapping.md` event storming approach

---

## Related Task Guides

**Before Journey Mapping:**
- `user_personas.md` - Validate persona accuracy and completeness
- `empathy_mapping.md` - Understand emotional drivers and pain points
- `writing_statements.md` - Craft supporting user stories and hypotheses

**During Journey Mapping:**
- `journey_mapping.md` - Advanced techniques for complex multi-system journeys
- `requirements_gathering.md` - Stakeholder input and validation methods
- `mental_modeling.md` - Understanding user assumptions and workflows

**After Journey Mapping:**
- `usability_testing.md` - Validate journey assumptions with real users
- `ux_audit.md` - Expert review of touchpoints and interactions
- `product_requirements_document.md` - Translate insights into feature specifications

**For Research Integration:**
- `user_feedback_questions.md` (materials) - Journey-specific interview questions
- `initiative_canvas.md` - Strategic alignment with business outcomes
- `prioritization.md` - Rank journey improvements by impact and effort

---

## Template Structure
```markdown
# [JOURNEY NAME] - User Journey Map

## Journey Overview
- **User Type:** [Primary persona/user segment]  
- **Goal:** [What the user wants to accomplish]  
- **Context:** [Situation, environment, or trigger for this journey]  
- **Success Criteria:** [How we measure journey completion]  

---

## Entry Points
Different locations/touchpoints that trigger the feature or start the user flow.

| Entry Point  | Channel               | Trigger              | User State           |
|--------------|-----------------------|----------------------|----------------------|
| [Location 1] | [Web/Mobile/Email/etc]| [What causes entry]  | [User context/mood]  |
| [Location 2] | [Web/Mobile/Email/etc]| [What causes entry]  | [User context/mood]  |

---

## Journey Steps

### Step 1: [Step Name – e.g., Discovery/Awareness]
**User Goal:** [What user wants to achieve in this step]  
**Duration:** [Estimated time]  

#### Scenarios
| Scenario Type | User Actions               | System Response            | User Thoughts/Feelings    | Opportunities          |
|---------------|----------------------------|----------------------------|---------------------------|------------------------|
| Positive      | [Ideal user behavior]      | [System works correctly]   | [Positive emotions/thoughts] | [Enhancement ideas] |
| Negative      | [User struggles/errors]    | [System errors/confusion]  | [Frustration/confusion]   | [Fix priorities]       |
| No Data       | [User has no content/info] | [Empty states shown]       | [Uncertainty/hesitation]  | [Onboarding needs]     |

#### Touchpoints & Channels
- [List relevant touchpoints: web app, mobile, email, support, etc.]

#### Pain Points & Opportunities
- **Pain Points:** [Specific friction areas]  
- **Opportunities:** [Improvement suggestions]  

---

### Step 2: [Step Name – e.g., Configuration/Setup]
**User Goal:** [What user wants to achieve in this step]  
**Duration:** [Estimated time]  

#### Scenarios
| Scenario Type  | User Actions               | System Response            | User Thoughts/Feelings     | Opportunities            |
|----------------|----------------------------|----------------------------|----------------------------|--------------------------|
| Positive       | [Ideal user behavior]      | [System works correctly]   | [Positive emotions/thoughts] | [Enhancement ideas]   |
| Negative       | [User struggles/errors]    | [System errors/confusion]  | [Frustration/confusion]    | [Fix priorities]         |
| Complex Setup  | [Advanced configuration]   | [Advanced options shown]   | [Overwhelm/confusion]      | [Simplification needs]   |

#### Touchpoints & Channels
- [List relevant touchpoints]

#### Pain Points & Opportunities
- **Pain Points:** [Specific friction areas]  
- **Opportunities:** [Improvement suggestions]  

---

### Step 3: [Step Name – e.g., Execution/Usage]
**User Goal:** [What user wants to achieve in this step]  
**Duration:** [Estimated time]  

#### Scenarios
| Scenario Type   | User Actions            | System Response    | User Thoughts/Feelings       | Opportunities              |
|-----------------|-------------------------|-------------------|------------------------------|----------------------------|
| Positive        | [Successful completion] | [Expected results] | [Satisfaction/accomplishment]| [Enhancement ideas]        |
| Partial Success | [Some steps completed]  | [Mixed results]    | [Partial satisfaction]       | [Completion support]       |
| Failure         | [Unable to complete]    | [Error states]     | [Frustration/abandonment]    | [Recovery mechanisms]      |

#### Touchpoints & Channels
- [List relevant touchpoints]

#### Pain Points & Opportunities
- **Pain Points:** [Specific friction areas]  
- **Opportunities:** [Improvement suggestions]  

---

## Follow-up Actions
All possible scenarios after job completion.

### Immediate Follow-ups (0–24 hours)
| Scenario       | User Action                | System Support             | Desired Outcome          |
|----------------|----------------------------|----------------------------|--------------------------|
| Success        | [Celebrate/share/continue] | [Confirmation/next steps]  | [Continued engagement]   |
| Partial Success| [Try to complete remaining]| [Guidance/tutorials]       | [Task completion]        |
| Failure        | [Retry/seek help/abandon]  | [Support/recovery options] | [Problem resolution]     |

### Medium-term Follow-ups (1–7 days)
| Scenario       | User Action              | System Support             | Desired Outcome          |
|----------------|--------------------------|----------------------------|--------------------------|
| High Engagement| [Regular usage/exploration] | [Advanced features/tips] | [Power user conversion]  |
| Low Engagement | [Minimal usage/dormant]  | [Re-engagement campaigns]  | [Usage activation]       |
| Expansion      | [Looking for more features]| [Upgrade prompts/demos]   | [Feature adoption]       |

### Long-term Follow-ups (1+ weeks)
| Scenario  | User Action              | System Support              | Desired Outcome         |
|-----------|--------------------------|-----------------------------|-------------------------|
| Retention | [Continued regular use]  | [Loyalty rewards/features]  | [Long-term retention]   |
| Churn Risk| [Decreased usage]        | [Win-back campaigns]        | [Re-activation]         |
| Advocacy  | [Recommending to others] | [Referral programs]         | [Growth/acquisition]    |

---

## Success Metrics
- **Primary:** [Main KPI for journey success]  
- **Secondary:** [Supporting metrics]  
- **Leading Indicators:** [Early success signals]  

---

## Key Insights & Recommendations
- [Major findings from this journey mapping exercise]  
- [Priority recommendations for improvement]  
- [Cross-functional coordination needs]
```

---

## Journey Map Examples

### Example 1: B2B SaaS Platform Onboarding
```markdown
# Enterprise Analytics Platform Onboarding - User Journey Map

## Journey Overview
- **User Type:** Data Analytics Manager at mid-size technology company
- **Goal:** Successfully implement analytics platform for quarterly business reporting
- **Context:** Recently hired to modernize reporting processes, replacing manual Excel workflows with automated dashboards
- **Success Criteria:** Platform configured, team trained, first automated report generated within 30 days

---

## Entry Points
| Entry Point | Channel | Trigger | User State |
|-------------|---------|---------|------------|
| Sales Demo Follow-up | Email/Calendar | Scheduled implementation kickoff after contract signing | Optimistic but concerned about timeline pressure |
| Self-Service Setup | Web Portal | Direct login after receiving account credentials | Eager to explore but uncertain about where to start |
| Support Referral | Phone/Chat | Escalated from technical difficulties during initial setup | Frustrated from previous failed attempts |

---

## Journey Steps

### Step 1: Initial Platform Access and Orientation
**User Goal:** Gain access to platform and understand core functionality
**Duration:** 2-4 hours over first week

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|------------------------|---------------|
| Positive | Logs in successfully, explores guided tour, completes initial profile setup | Clear navigation, helpful tooltips, progress indicators work correctly | "This looks intuitive. I can see how this will save us time." | Add role-specific onboarding paths |
| Negative | Multiple login failures, confused by interface layout, abandons setup halfway | Password reset emails delayed, no clear next steps provided | "This is more complex than promised. Maybe we made the wrong choice." | Improve credential delivery process and add progress recovery |
| No Data | Logs in to empty dashboard with no sample data or templates | Generic empty state with basic getting started links | "How do I know if this will work for our specific needs?" | Provide industry-specific sample datasets and templates |

#### Touchpoints & Channels
- Web application dashboard, Welcome email sequence, Setup wizard, In-app help documentation

### Step 2: Data Integration and Configuration
**User Goal:** Connect company data sources and create first meaningful visualization
**Duration:** 1-2 weeks

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|------------------------|---------------|
| Positive | Successfully connects to primary database, creates basic chart, shares with colleague | Data imports cleanly, chart renders correctly, sharing works seamlessly | "Finally seeing our data in real-time. This will transform how we report." | Create templates for common integration patterns |
| Negative | Database connection fails repeatedly, data formatting issues, chart displays incorrectly | Error messages are technical, no clear resolution steps provided | "I'm spending more time troubleshooting than analyzing. This is becoming a project risk." | Improve error messaging and provide direct support escalation |
| Edge Case | Needs to integrate with legacy system not in standard connector list | Platform shows unsupported connector message with manual workaround documentation | "This might require IT resources I don't have access to." | Develop custom connector request process with timeline estimates |

#### Touchpoints & Channels
- Data connector interface, Configuration wizard, Technical documentation, Customer success email check-ins

### Step 3: Team Training and Rollout
**User Goal:** Train team members and establish new reporting workflows
**Duration:** 2-3 weeks

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|------------------------|---------------|
| Positive | Schedules team training, creates user accounts, establishes permissions, team adopts new workflows | Training materials work well, user management is straightforward, permissions function correctly | "The team is embracing this. We're already seeing better insights." | Create change management templates and adoption tracking |
| Negative | Team resists new process, training sessions poorly attended, multiple user access issues | No engagement tracking, limited training format options, user management errors | "Getting people to change is harder than I expected. This rollout is behind schedule." | Develop engagement analytics and flexible training delivery options |
| Edge Case | Key team member leaves during rollout, knowledge transfer needed urgently | Standard user deactivation process, no knowledge transfer support | "We're losing institutional knowledge right when we need it most." | Create documentation templates and knowledge transfer workflows |

#### Touchpoints & Channels
- User management interface, Training webinars, Team collaboration features, Email announcements

---

## Follow-up Actions

### Immediate Follow-ups (0–24 hours)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| Success | Shares initial success with leadership, explores advanced features | Automated success celebration, advanced feature recommendations | Increased confidence and platform advocacy |
| Partial Success | Reviews incomplete setup items, seeks help for remaining issues | Checkpoint reminders, targeted help resources | Task completion and momentum maintenance |
| Failure | Contacts support for emergency assistance, considers project timeline revision | Priority support routing, dedicated success manager assignment | Rapid problem resolution and relationship repair |

### Medium-term Follow-ups (1–7 days)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| High Engagement | Regular daily usage, creates multiple dashboards, trains additional users | Usage analytics insights, power user feature unveiling | Advanced feature adoption and increased seat count |
| Low Engagement | Sporadic usage, limited dashboard creation, team adoption stalled | Re-engagement campaign, additional training offers | Usage activation and workflow integration |
| Expansion | Requests additional integrations, explores advanced analytics features | Expansion consultation, upgrade path guidance | Account growth and deeper platform integration |

### Long-term Follow-ups (1+ weeks)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| Retention | Regular platform usage, established reporting cadence, positive ROI measurement | Quarterly business reviews, optimization recommendations | Contract renewal and reference customer development |
| Churn Risk | Decreased platform usage, team reverted to old processes, questioning ROI | Executive sponsor engagement, success recovery plan | Re-activation and relationship recovery |
| Advocacy | Recommending platform to industry peers, participating in case studies | Reference program enrollment, speaking opportunity invitations | Customer advocacy and word-of-mouth acquisition |

---

## Success Metrics
- **Primary:** Time to first automated report (target: 30 days)
- **Secondary:** Team adoption rate (target: 80% active users within 60 days), Data accuracy improvement (target: 95% automated vs manual reconciliation)
- **Leading Indicators:** Login frequency, dashboard creation rate, support ticket volume trend

---

## Key Insights & Recommendations
- Integration complexity is the primary barrier to success, requiring dedicated IT support coordination
- Change management is equally important as technical implementation, suggesting need for organizational readiness assessment
- Success depends heavily on having an internal champion with both technical aptitude and organizational influence
- Priority recommendations: Improve integration error messaging, develop change management toolkit, create executive sponsor engagement playbook
```

### Example 2: Healthcare Patient Appointment Journey
```markdown
# Primary Care Appointment Scheduling - Patient Journey Map

## Journey Overview
- **User Type:** Working parent (age 35-45) with employer health insurance
- **Goal:** Schedule and complete routine primary care appointment for annual physical
- **Context:** Busy schedule, managing family healthcare needs, prefers digital-first interactions but values human touch for complex issues
- **Success Criteria:** Appointment scheduled within preferred timeframe, minimal wait times, all health concerns addressed, next steps clearly communicated

---

## Entry Points
| Entry Point | Channel | Trigger | User State |
|-------------|---------|---------|------------|
| Health Plan Reminder | Email/Mail | Annual wellness benefit notification from employer | Proactive but time-pressured |
| Symptom Concern | Web Search | Specific health concern requiring professional consultation | Anxious and seeking quick resolution |
| Referral Follow-up | Phone/Portal | Specialist recommended primary care consultation | Motivated by medical necessity |
| Routine Maintenance | Mobile App | Calendar reminder or health tracking app prompt | Systematic but seeking convenience |

---

## Journey Steps

### Step 1: Appointment Scheduling and Preparation
**User Goal:** Find suitable appointment slot and complete necessary preparation
**Duration:** 30 minutes to 3 days

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|------------------------|---------------|
| Positive | Uses online portal, finds convenient appointment slot, completes pre-visit forms digitally | Portal loads quickly, shows real-time availability, forms are mobile-optimized | "This was easier than expected. I can handle this during my lunch break." | Add calendar integration and appointment type recommendations |
| Negative | Portal crashes repeatedly, limited appointment availability, paper forms required | System timeouts, phone-only booking offered, forms must be printed and completed | "Why is this so complicated? I might just postpone this again." | Improve portal stability and expand digital form options |
| Edge Case | Needs specific provider due to language preference or medical history | Limited provider search filters, no cultural competency indicators | "I hope this doctor will understand my background and concerns." | Add provider preference filters and cultural competency badges |

#### Touchpoints & Channels
- Online patient portal, Mobile app, Phone scheduling line, Pre-visit preparation emails

### Step 2: Arrival and Check-in Experience
**User Goal:** Efficient check-in process with minimal waiting and accurate information capture
**Duration:** 15-45 minutes

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|-------------------------|---------------|
| Positive | Arrives on time, mobile check-in works smoothly, insurance verification completed, called for appointment promptly | Self-service kiosks functional, staff friendly and efficient, wait time as promised | "This is running like clockwork. I appreciate the respect for my time." | Add real-time wait updates and comfort amenity notifications |
| Negative | Insurance card not accepted, forms not received, significant wait time without updates | Staff overwhelmed, outdated systems, no communication about delays | "I took time off work for this. This disorganization reflects poorly on the care quality." | Implement insurance verification automation and wait time communication system |
| Edge Case | Brings children due to childcare issues, needs accommodation for mobility device | Limited child-friendly space, accessibility features not clearly marked | "I hope they can accommodate my situation without making me feel like a burden." | Create family-friendly check-in options and improve accessibility signage |

#### Touchpoints & Channels
- Reception desk, Self-service kiosks, Waiting area, Insurance verification systems

### Step 3: Clinical Consultation and Care Planning
**User Goal:** Comprehensive health assessment with clear communication and actionable next steps
**Duration:** 20-60 minutes

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|-------------------------|---------------|
| Positive | Doctor reviews history thoroughly, listens to concerns, explains findings clearly, provides written care plan | EHR system enables comprehensive review, provider has adequate time, care plan includes specific follow-up actions | "I feel heard and confident about my health. The doctor really understands my situation." | Add patient communication preferences and shared decision-making tools |
| Negative | Doctor seems rushed, interrupts frequently, medical terminology not explained, vague next steps provided | EHR system glitches, provider running behind schedule, limited patient education resources | "I left with more questions than answers. I'm not sure I got the care I needed." | Implement consultation time buffers and patient education resource integration |
| Edge Case | Complex health issue requires specialist referral, insurance pre-authorization needed | Referral process unclear, authorization timeline unknown, patient responsibility uncertain | "Now I have to navigate another system. I wish this could be coordinated for me." | Create integrated referral management with transparent timeline communication |

#### Touchpoints & Channels
- Examination room, Provider consultation, EHR system, Patient education materials

---

## Follow-up Actions

### Immediate Follow-ups (0–24 hours)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| Success | Reviews visit summary, schedules recommended follow-up, shares positive experience | Automated visit summary delivery, easy follow-up scheduling, feedback request | Continued engagement with healthcare system |
| Partial Success | Seeks clarification on provider instructions, researches recommended treatments | Patient portal messaging, nurse triage support | Understanding and compliance with care plan |
| Failure | Files complaint, seeks second opinion, considers changing providers | Patient advocacy response, retention outreach | Service recovery and relationship repair |

### Medium-term Follow-ups (1–7 days)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| High Engagement | Follows treatment plan, uses patient portal regularly, schedules preventive care | Care plan tracking, medication reminders, wellness program invitations | Improved health outcomes and system loyalty |
| Low Engagement | Limited follow-through on recommendations, minimal portal usage | Care gap alerts, nurse outreach, simplified communication options | Care plan adherence and health engagement |
| Expansion | Family members request same provider, asks about additional services | Family member scheduling options, service expansion information | Household healthcare management and revenue growth |

### Long-term Follow-ups (1+ weeks)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| Retention | Maintains regular primary care relationship, refers friends and family | Annual care planning, referral appreciation programs | Long-term patient relationship and advocacy |
| Churn Risk | Misses follow-up appointments, considers changing providers | Re-engagement outreach, care coordination support | Patient retention and health continuity |
| Advocacy | Recommends provider to friends, participates in patient satisfaction surveys | Patient testimonial programs, community health engagement | Reputation building and new patient acquisition |

---

## Success Metrics
- **Primary:** Patient satisfaction scores (target: >90%), Appointment completion rate (target: >95%)
- **Secondary:** Average wait time (target: <15 minutes), Care plan adherence (target: >80%), Provider utilization efficiency
- **Leading Indicators:** Online scheduling adoption rate, portal engagement, referral follow-through rate

---

## Key Insights & Recommendations
- Digital convenience is expected but human empathy remains crucial for healthcare satisfaction
- Care coordination complexity significantly impacts patient experience, particularly for referrals and specialist care
- Time respect is fundamental to patient satisfaction, affecting perception of overall care quality
- Priority recommendations: Integrate referral management systems, implement proactive wait time communication, expand digital-first options while maintaining human touch points
```

### Example 3: E-commerce Product Discovery and Purchase
```markdown
# Home Office Furniture Shopping - E-commerce Journey Map

## Journey Overview
- **User Type:** Remote professional setting up dedicated home office space
- **Goal:** Purchase ergonomic desk chair within budget that meets specific comfort and aesthetic requirements
- **Context:** Recently transitioned to permanent remote work, experiencing back pain from current setup, limited space in apartment
- **Success Criteria:** Chair purchased within budget ($400-800), delivery within 2 weeks, fits space constraints, improves comfort

---

## Entry Points
| Entry Point | Channel | Trigger | User State |
|-------------|---------|---------|------------|
| Search Engine | Google/Bing | "Best ergonomic office chairs 2025" search after experiencing back pain | Research-focused and price-conscious |
| Social Media Ad | Instagram/Facebook | Targeted ad for office furniture sale | Curious but skeptical of advertising claims |
| Direct Navigation | Company Website | Returning after previous browsing session or recommendation | Familiar with brand and ready to evaluate |
| Email Campaign | Newsletter/Promotional | Sale notification or abandoned cart reminder | Deal-motivated and time-sensitive |

---

## Journey Steps

### Step 1: Product Discovery and Research
**User Goal:** Find chairs that meet functional requirements within budget constraints
**Duration:** 2-5 hours across multiple sessions

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|-------------------------|---------------|
| Positive | Uses filters effectively, finds multiple suitable options, reads helpful reviews, compares features easily | Search filters work accurately, product pages load quickly, reviews are detailed and authentic | "I'm finding exactly what I need. The reviews give me confidence in these choices." | Add comparison tools and size/space fit visualization |
| Negative | Overwhelmed by options, unclear product differences, reviews seem fake, difficult mobile experience | Poor filter logic, slow page loads, limited product information, suspicious review patterns | "There are too many options and I can't tell what's actually good. This is frustrating." | Improve curation algorithms and review authenticity verification |
| Edge Case | Needs specific accessibility features not commonly available | Limited accessibility filter options, unclear compliance information | "I hope I can find something that works for my specific needs without custom ordering." | Add accessibility-focused product categories and compliance information |

#### Touchpoints & Channels
- Product listing pages, Search and filter systems, Product detail pages, Customer review sections

### Step 2: Evaluation and Decision Making
**User Goal:** Narrow down to final choice with confidence in purchase decision
**Duration:** 1-3 hours

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|-------------------------|---------------|
| Positive | Compares top 3 options, checks delivery timeframes, confirms return policy, reads recent reviews | Comparison tool works well, delivery information clear, return policy easily accessible | "I feel confident about this choice. The company seems reliable and customer-focused." | Add augmented reality room fit preview and expert consultation options |
| Negative | Uncertain between options, delivery timeline unclear, return policy confusing, price changes unexpectedly | Limited comparison functionality, ambiguous shipping info, complex return terms | "I'm still not sure which is best. What if I choose wrong and can't return it easily?" | Implement price lock for consideration period and simplified decision support tools |
| Edge Case | Needs to coordinate delivery timing with apartment building restrictions | Standard delivery options don't account for building access requirements | "I need to make sure this can actually be delivered to my apartment. The logistics seem complicated." | Add delivery customization options and building access accommodation |

#### Touchpoints & Channels
- Product comparison tools, Shipping and delivery information, Return policy pages, Customer service chat

### Step 3: Purchase and Order Completion
**User Goal:** Complete purchase with confidence and receive confirmation of order details
**Duration:** 10-30 minutes

#### Scenarios
| Scenario Type | User Actions | System Response | User Thoughts/Feelings | Opportunities |
|---------------|--------------|-----------------|-------------------------|---------------|
| Positive | Checkout process smooth, payment secure, receives immediate confirmation with tracking, delivery scheduled | Checkout loads quickly, payment processed without issues, confirmation email detailed and helpful | "That was easy. I'm excited to receive this and finally have a comfortable workspace." | Add order customization options and delivery day preparation tips |
| Negative | Checkout errors, payment declined, unclear total costs, no immediate confirmation received | Site crashes during checkout, payment processing issues, hidden fees appear, delayed confirmation | "This is stressful. I'm worried about whether my order actually went through and what I'll be charged." | Improve checkout stability and implement transparent pricing with immediate confirmation |
| Edge Case | Wants to split payment across multiple cards or use business expense account | Limited payment options, no business account integration | "This purchase is for my home office business. I need the right payment and receipt options." | Add flexible payment options and business purchase accommodation |

#### Touchpoints & Channels
- Shopping cart, Checkout flow, Payment processing, Order confirmation system

---

## Follow-up Actions

### Immediate Follow-ups (0–24 hours)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| Success | Shares purchase excitement on social media, begins preparing workspace | Social sharing incentives, space preparation guides | Brand advocacy and delivery anticipation |
| Partial Success | Double-checks order details, seeks delivery timeline clarification | Order tracking availability, proactive delivery communication | Confidence in purchase decision and delivery process |
| Failure | Attempts to cancel or modify order, seeks customer service assistance | Easy order modification tools, responsive customer service | Order resolution and customer satisfaction recovery |

### Medium-term Follow-ups (1–7 days)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| High Engagement | Tracks shipment daily, researches assembly instructions, prepares workspace | Detailed tracking updates, assembly video tutorials, workspace tips | Successful product setup and satisfaction |
| Low Engagement | Minimal order interaction, concerned about delivery timeline | Proactive delivery updates, timeline reassurance communication | Maintained confidence and satisfaction |
| Expansion | Looks for matching desk accessories, considers additional office furniture | Product recommendation engine, complementary product suggestions | Increased order value and complete workspace solution |

### Long-term Follow-ups (1+ weeks)
| Scenario | User Action | System Support | Desired Outcome |
|----------|-------------|----------------|-----------------|
| Retention | Product performs well, considers future purchases, recommends to colleagues | Satisfaction surveys, loyalty program enrollment, referral incentives | Customer lifetime value and advocacy |
| Churn Risk | Product issues, difficult returns process, negative experience overall | Proactive quality follow-up, easy return process, service recovery | Issue resolution and relationship repair |
| Advocacy | Writes positive reviews, recommends brand to friends, shares workspace photos | Review incentives, user-generated content programs, brand community | Social proof generation and organic marketing |

---

## Success Metrics
- **Primary:** Conversion rate from product view to purchase (target: >3%), Customer satisfaction score (target: >4.5/5)
- **Secondary:** Average order value (target: $650), Return rate (target: <8%), Time to purchase decision (target: <3 sessions)
- **Leading Indicators:** Product page engagement time, comparison tool usage, cart abandonment rate

---

## Key Insights & Recommendations
- Product discovery complexity requires better curation and decision support tools rather than just more options
- Trust-building through authentic reviews and transparent policies is crucial for high-consideration purchases
- Delivery logistics and post-purchase communication significantly impact overall satisfaction and likelihood to recommend
- Priority recommendations: Implement augmented reality fit preview, develop decision support wizard, create comprehensive delivery coordination system
```