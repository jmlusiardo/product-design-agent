# Product Design Assistant

An open-source AI-powered mentorship system that provides expert guidance across product design, user research, UX/UI, strategy, and leadership. Built to accelerate learning through personalized, hands-on mentorship with multilingual support.

## Capabilities

This intelligent mentorship system:
- **Matches queries to expert guidance** using a sophisticated task registry
- **Provides structured, actionable resources** including guides, templates, and checklists
- **Supports multilingual learning** (English, Spanish, and French) with seamless context switching
- **Accelerates professional growth** through personalized, adaptive mentorship
- **Delivers hands-on tools** for real-world design challenges

## Setup in Claude

### What you need
- Claude account (Pro or Team recommended for optimal performance)
- Access to Claude Projects feature

### Using this repo in your Claude project
1. In the project in Claude, in **Files**, click on the **+*** button and select **Github**
2. In the modal, click on the 🔗 button, and paste this repo URL.
3. Select **task_registry.md** file, and **task_guides** and **materials** folders.

## How to use it

Simply ask questions related to:
- **Onboarding**: "How do I onboard new design leads?"
- **Project Framing**: "Help me run a kickoff meeting"
- **User Research**: "I need to do UX research without user access"
- **Leadership**: "How do I boost UX culture in my organization?"
- **Visual Design**: "Create an AI image prompt for..."

Note: Currently supports English, Spanish, and French languages.

Examples:
- "Create a usability test plan for a mobile app"
- "Necesito documentar componentes de mi design system"
- "Comment résoudre les conflits entre design et ingénierie ?"
- "Onboarding checklist for new designers"
- "Generate journey map for e-commerce checkout"

## Current Knowledge Domains

### Onboarding
- Design lead onboarding
- Designer onboarding
- Team integration processes

### Project Framing
- Kickoff meetings
- Initiative canvas
- Project type strategy

### Discovery & Research
- User personas
- Journey mapping
- Research without user access
- Usability testing
- User recruitment

### Visual & Systems
- Component documentation
- AI image prompts
- Design token systems
- Prototype creation

### Leadership & Collaboration
- Team management
- UX culture building
- Hiring designers
- Stakeholder management
- Conflict resolution

## How It Works

1. **Query Processing**: Extracts keywords (English, Spanish, French) and identifies intent
2. **Task Matching**: Searches `task_registry.md` for relevant tasks using:
   - Direct keyword matches
   - Fuzzy matching for variations
   - Confidence scoring (HIGH >80%, MEDIUM 50-80%, LOW <50%)
3. **Resource Assembly**: Accesses task guides and materials
4. **Response Generation**: Synthesizes information into actionable guidance
5. **Quality Validation**: Runs comprehensive checklist before delivery

## How you can collaborate with this project

We welcome contributions to improve any aspect of this system! Here's how you can help:

### Ways to Contribute

#### Quick Improvements
1. **Open an Issue** describing the improvement
2. **Label appropriately**: `enhancement`, `bug`, `documentation`, `new-feature`
3. **Provide context**: What's missing? Why is it important?

#### Major Contributions
1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b improve-usability-testing`
3. **Make your changes** following our conventions
4. **Test thoroughly** across different scenarios
5. **Submit a Pull Request** with detailed description
