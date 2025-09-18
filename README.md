# Product Design Agent

An open-source AI-powered mentorship system with specialized agents providing expert guidance across product design, user research, UX/UI, strategy, AI integration, and leadership. Built to accelerate learning through personalized, hands-on mentorship with multilingual support.

## Capabilities

This intelligent mentorship system:
- **Matches queries to specialized agents** using a sophisticated task registry with 80+ expert tasks
- **Provides structured, actionable resources** including guides, templates, and checklists
- **Supports multilingual learning** (English, Spanish) with seamless context switching
- **Accelerates professional growth** through personalized, adaptive mentorship
- **Delivers hands-on tools** for real-world design challenges
- **Integrates AI workflows** with specialized AI and prompt engineering guidance

## Setup in Claude

### What you need
- Claude account (Pro or Team recommended for optimal performance)
- Access to Claude Projects feature

### Using this repo in your Claude project
1. In the project in Claude, in **Files**, click on the **+** button and select **Github**
2. In the modal, click on the 🔗 button, and paste this repo URL.
3. Select **config** folder (contains tasks.yaml and agents.yaml), **task_guides** and **materials** folders.

_Note: Any files you drop within the project will be treated as project-specific context._

## How to use it

Simply ask questions related to:
- **Onboarding**: "How do I onboard new design leads?"
- **Project Framing**: "Help me run a kickoff meeting"
- **User Research**: "I need to do UX research without user access"
- **AI Integration**: "Optimize my AI prompts for design work"
- **Leadership**: "How do I boost UX culture in my organization?"
- **Visual Design**: "Create an AI image prompt for..."

Examples:
- "Create user personas for a fintech mobile app"
- "Write usability testing scripts for our dashboard"
- "Build a design system component library documentation"
- "Map the customer journey for our SaaS onboarding"
- "Prioritize features using RICE scoring methodology"
- "Design an accessibility audit checklist"
- "Write content guidelines for our design system"
- "Create a user research plan without direct user access"
- "Build a design critique framework for our team"
- "Design KPI metrics for measuring UX success"
- "Create onboarding materials for new design hires"
- "Plan stakeholder workshops for feature discovery"
- "Transform this image into a style JSON prompt"
- "Create a business model canvas for our new feature"
- "Plan a design sprint for solving payment friction"

## Current Knowledge Domains

### Onboarding
- Design lead onboarding
- Designer onboarding
- Team integration processes

### Project Framing
- Kickoff meetings
- Initiative canvas
- Project planning and management
- Requirements gathering

### Discovery & Research
- User personas
- Journey mapping
- Research without user access
- Usability testing and moderation
- User recruitment and evaluation
- Writing user statements and problem framing

### Strategy & Planning
- MVP definition and prioritization
- Value proposition design
- Business model development
- KPI framework design
- Brainstorming and ideation workshops

### AI & Prompting
- Prompt engineering and optimization
- AI image prompt creation
- Vibe coding and rapid prototyping
- Style specification systems
- AI workflow integration

### Visual & Systems
- Component documentation
- Design token systems
- Prototype creation
- Visual storytelling and presentations

### Content & Writing
- Content strategy and audits
- Writing task management
- Documentation standards
- Style guide development

### Leadership & Collaboration
- Team management
- UX culture building
- Hiring designers
- Stakeholder management
- Conflict resolution
- Executive presentations and summaries
- Meeting facilitation and critique

### Education & Culture
- Cognitive bias training
- B2B design principles
- Economics for designers
- UX culture transformation
- Design maturity assessment

## How It Works

The system operates through specialized agents, each with unique expertise:

1. **Query Processing**: Extracts keywords (English, Spanish) and identifies intent
2. **Agent Assignment**: Routes queries to specialized agents:
   - AI Specialist, Strategy Analyst, Research Analyst, Project Manager
   - Team Lead, Design Educator, Collaboration Facilitator, and more
3. **Task Matching**: Searches `config/tasks.yaml` for relevant tasks using:
   - Direct keyword matches
   - Fuzzy matching for variations
   - Confidence scoring (HIGH >80%, MEDIUM 50-80%, LOW <50%)
4. **Resource Assembly**: Accesses 80+ task guides and specialized materials
5. **Response Generation**: Agent-specific expertise provides contextualized, actionable guidance
