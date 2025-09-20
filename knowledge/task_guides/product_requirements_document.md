# Product Requirements Document (PRD) Creation Guide

## Overview

This guide enables systematic creation of comprehensive Product Requirements Documents using a structured RAG approach. The methodology transforms initial product concepts into detailed, stakeholder-aligned specifications that bridge business objectives with technical execution.

## Input Sources

### Required Information Gathering
Before PRD creation, collect these essential inputs:

**Product Context**
- Product name and type (web app, mobile app, feature, integration)
- Target user segments and primary personas
- Core problem statement and solution hypothesis
- Success metrics and business objectives

**Business Intelligence**
- Strategic priority level and justification
- Market opportunity size and timing analysis
- Competitive landscape and differentiation strategy
- Resource constraints (timeline, budget, team capacity)

**User Research Data**
- User personas with pain points and goals
- Current workflow documentation
- User feedback from interviews, surveys, support tickets
- Journey maps and behavioral insights

**Technical Foundation**
- Current system architecture and constraints
- Required integrations and dependencies
- Performance, security, and compliance requirements
- Platform and compatibility specifications

## Retrieval Strategy

### Knowledge Base Integration
Cross-reference these repository resources:

**Task Guides**
- `/task_guides/kickoff_meeting.md` - For stakeholder alignment processes
- `/task_guides/user_personas.md` - For persona validation techniques
- `/task_guides/journey_mapping.md` - For workflow documentation
- `/task_guides/prioritization.md` - For feature prioritization frameworks

**Materials**
- `/materials/prompt_templates_registry.md` - For PRD prompt templates
- Product metrics and KPI frameworks
- Requirements gathering templates

### Search Priority
1. **Project-specific context** (uploaded files, briefings, research data)
2. **Methodology frameworks** (task guides, templates)
3. **Industry standards** (compliance, accessibility, security)
4. **Best practices** (stakeholder management, technical architecture)

## Generation Instructions

### PRD Structure Template

#### 1. Executive Summary
- **Product Vision**: One-sentence product description with target user and use case
- **Strategic Alignment**: Business objectives and competitive advantages
- **Resource Requirements**: Development effort, timeline, team needs

#### 2. Problem Statement & Opportunity
- **Problem Definition**: Detailed user pain points with quantified impact
- **Opportunity Analysis**: Market size, user segments, revenue potential
- **Success Criteria**: Primary and secondary metrics with targets

#### 3. User Requirements & Stories
- **Primary Personas**: Detailed descriptions with goals and workflows
- **User Journey Mapping**: Current vs. proposed future state
- **Core User Stories**: Epic and feature-level stories with acceptance criteria

#### 4. Functional Requirements
- **Core Features (Must Have)**: Detailed descriptions with business logic
- **Secondary Features (Nice to Have)**: Enhancement opportunities
- **Feature Prioritization**: MoSCoW method with impact-effort analysis

#### 5. Technical Requirements
- **Architecture Specifications**: System overview and integration points
- **API Requirements**: Endpoints, authentication, rate limiting
- **Data Requirements**: Models, sources, validation, security
- **Performance Specifications**: Response times, capacity, scalability

#### 6. User Experience Requirements
- **Design Principles**: UX philosophy and accessibility standards
- **Interface Requirements**: Layouts, navigation, responsive design
- **Usability Criteria**: Task completion rates, satisfaction scores

#### 7. Non-Functional Requirements
- **Security**: Authentication, encryption, compliance (GDPR, HIPAA)
- **Performance**: Load times, concurrent users, database performance
- **Reliability**: Uptime targets, error tolerances, disaster recovery
- **Scalability**: Growth projections and infrastructure scaling

#### 8. Success Metrics & Analytics
- **KPIs**: User acquisition, engagement, feature adoption, revenue impact
- **Analytics Implementation**: Tracking events, dashboards, A/B testing
- **Success Measurement**: Baselines, targets, review processes

#### 9. Implementation Plan
- **Development Phases**: MVP scope, iterative phases, rollout strategy
- **Resource Allocation**: Team requirements across disciplines
- **Timeline & Milestones**: Kickoff through post-launch optimization

#### 10. Risk Assessment & Mitigation
- **Technical Risks**: Architecture, integration, performance challenges
- **Business Risks**: Market timing, user adoption, resource constraints
- **Mitigation Strategies**: Risk assessment, preventive measures, contingencies

### Quality Assurance Checklist
- [ ] Problem clearly defined with evidence
- [ ] Solution aligns with user needs and business goals
- [ ] Requirements are specific and measurable
- [ ] Acceptance criteria are testable
- [ ] Technical feasibility validated
- [ ] Success metrics defined and trackable
- [ ] Risks identified with mitigation plans
- [ ] Stakeholder alignment confirmed

## Example Output
```markdown
# PRD: Mobile Banking Quick Transfer Feature

## Executive Summary
**Product Vision**: Enable mobile banking users to transfer money instantly to frequent contacts with biometric authentication, reducing transaction time from 3 minutes to 30 seconds.

**Strategic Alignment**: Supports user retention strategy by eliminating friction in high-frequency use cases. Differentiates from competitors through speed and security.

**Resource Requirements**: 8-week development cycle, 4 engineers, 2 designers, 1 PM, $120K budget.

## Problem Statement & Opportunity
**Problem Definition**: Current transfer flow requires 8 steps including recipient verification, causing 35% task abandonment. Users cite "too many steps" as primary complaint (247 support tickets in Q3).

**Opportunity Analysis**: 68% of transfers go to same 5 recipients. Streamlining frequent transfers could increase usage 40% and reduce support burden 60%.

**Success Criteria**: 
- Primary: 90% task completion rate (vs. 65% current)
- Secondary: <30 second average completion time

## References

- The best product requirement doc (PRD) prompt i've ever used, by Jnik5: https://www.reddit.com/r/PromptEngineering/comments/1n2qzqr/the_best_product_requirement_doc_prd_prompt_ive/
- Prompt Requirements Document (PRD): A New Concept for the Vibe Coding Era, by Takafumi Endo: https://medium.com/@takafumi.endo/prompt-requirements-document-prd-a-new-concept-for-the-vibe-coding-era-0fb7bf339400
- Writing PRDs and product requirements, by Carlin Yuen: https://carlinyuen.medium.com/writing-prds-and-product-requirements-2effdb9c6def
- Product Requirements Documents (PRDs): A Modern Guide, by Aakash Gupta: https://www.news.aakashg.com/p/product-requirements-documents-prds
