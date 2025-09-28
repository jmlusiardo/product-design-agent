# README.md

# Product Design Agent
An open-source AI-powered mentorship system with specialized agents providing expert guidance across product design, user research, UX/UI, strategy, AI integration, and leadership. Built to accelerate learning through personalized, hands-on mentorship with multilingual support.

## Capabilities
By combining specialized sub-agents with structured tasks and comprehensive guides, this design agent ensures clarity, consistency, and high-quality outcomes.
1. **Matches queries to specialized agents** using a sophisticated task registry with 80+ specific expert tasks
2. **Provides consultation/advice on diverse topics**: New project onboarding, project framing, product discovery, project planning, project management, user research, product strategy, user experience design, user interface design,  design leadership, design collaboration, prompts, vibe coding, and more.
3. **Provides structured, actionable resources**: surveys, test plans, component or process guides, checklists, etc
4. **Auto-detects project-specific data**: Have project-specific information? Add or connect it to the Claude project _Files_ folder, and it will be understood as context you can reference in future queries.
5. **Add user preferences** Want to save personal preferences, or add additional settings? Create a file named `user_preferences`, add your stuff and upload it to _Files_ folder. The system will detect and consider it while executing tasks or attending your inquiries.

## Installation
Choose your preferred AI assistant platform:
- **For Claude Pro subscribers**: [Claude installation guide:](./CLAUDE_INSTALLATION.md)
- **For Google One AI Premium subscribers**: [Gemini installation guide:](./GEMINI_INSTALLATION.md)

## Getting Started
Don't know how to start? Just type "What can you help me with?" or "I'm new to this agent" and the onboarding guide will be triggered.

## 📁 Project Structure
```markdown
├── assets/instructions.md    # Core agent instructions
├── config/
│   ├── tasks.yaml            # Task registry with 80+ specialized tasks
│   └── agents.yaml           # Specialized agent definitions
├── knowledge/
│   ├── task_guides/          # Detailed methodology guides
│   └── materials/            # Templates, checklists, and resources
├── CLAUDE_INSTALLATION.md    # Claude-specific setup guide
├── GEMINI_INSTALLATION.md    # Gemini-specific setup guide
├── README.md                 # This overview
└── CONTRIBUTING.md           # Contribution guidelines
```

## Key Features

### Specialized Agents
- **Research Agent**: User research, testing, validation methodologies
- **Strategy Agent**: Product strategy, market analysis, competitive research
- **UX Agent**: Information architecture, wireframing, prototyping
- **UI Agent**: Visual design, design systems, interaction design
- **Leadership Agent**: Team management, design operations, stakeholder communication
- **AI Integration Agent**: AI-assisted design, automation, emerging technologies

### Multilingual Support
- **Primary Languages**: English and Spanish
- **Adaptive Response**: Responds in user's query language
- **Cultural Context**: Adapts examples and references to regional practices
- **Technical Terms**: Provides translations when helpful

### Smart Task Matching
- **80+ Specialized Tasks**: From user interviews to design system audits
- **Confidence Scoring**: Matches queries to best methodology
- **Context Integration**: Adapts to your specific project needs
- **Cross-References**: Links related methodologies and tools

## Usage Examples

### Quick Consultations
- "How should I approach user research for a fintech app?"
- "What's the best way to present design concepts to stakeholders?"
- "Help me create a design system for a mobile application"

### Structured Deliverables
- "Create a usability testing plan for our checkout flow"
- "Generate a comprehensive design audit checklist"
- "Build a stakeholder interview guide for our discovery phase"

### Project-Specific Guidance
Upload your project files and ask:
- "Review our current user journey and suggest improvements"
- "What design methodology fits our timeline and constraints?"
- "Help prioritize these feature requests based on user research"

## Contributing
We welcome contributions! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for:
- How to suggest new tasks or improvements
- Guidelines for adding content
- Code of conduct and community standards

---

**Ready to accelerate your design process with AI mentorship?** Choose your platform above and get started in minutes.