# Meet the Product Design Agent
An open-source AI-powered mentorship system with specialized agents providing expert guidance across product design, user research, UX/UI, strategy, AI integration, and leadership. Built to accelerate learning through personalized, hands-on mentorship with multilingual support.

## Capabilities
By combining specialized sub-agents with structured tasks and comprehensive guides, this design agent ensures clarity, consistency, and high-quality outcomes.
1. **Matches queries to specialized agents** using a sophisticated task registry with 80+ specific expert tasks
2. **Provides consultation/advice on diverse topics**: New project onboarding, project framing, product discovery, project planning, project management, user research, product strategy, user experience design, user interface design, design leadership, design collaboration, prompts, vibe coding, and more.
3. **Provides structured, actionable resources**: surveys, test plans, component or process guides, checklists, etc

## Platform Deployments

### Claude (Skills)
For Claude, the system runs as a set of installable Skills — there is no central runtime prompt. Each Skill is a self-contained orchestrator agent scoped to a design domain.

| Skill | Path | Best for |
|---|---|---|
| Researcher | `assets/claude/skills/researcher.md` | UX research planning, testing, analysis and measurement |
| Strategist | `assets/claude/skills/strategist.md` | Problem framing, opportunity mapping, strategy and prioritization |
| Team Lead | `assets/claude/skills/team_lead.md` | Team management, facilitation, onboarding and design leadership |
| Designer | `assets/claude/skills/designer.md` | UI design, design systems, visual identity and content |

### Gemini (Gems)
For Gemini, the system uses a single runtime prompt that activates the full multi-agent ecosystem. Configure your Gem using the file below.

**Path:** `assets/gemini/instructions.md`

**Project-specific context:** Upload your project files directly into the Gem conversation or attach them via Google Drive to add business context to any query.

**User preferences:** Create a `user_preferences.md` file with your personal settings (language, output format, focus areas)

## Installation
Choose your preferred AI assistant platform:
- **For Claude Pro subscribers**: [Claude installation guide:](./CLAUDE_INSTALLATION.md)
- **For Google One AI Premium subscribers**: [Gemini installation guide:](./GEMINI_INSTALLATION.md)

## Getting Started
Don't know how to start? **Just type "What can you help me with?"** and the onboarding guide will be triggered.

## Contributing
We welcome contributions! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for:
- How to suggest new tasks or improvements
- Guidelines for adding content
- Bug/issue report

---

**Ready to accelerate your design process with AI mentorship?** Choose your platform above and get started in minutes.