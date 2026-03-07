# Product Design Agent: Setup in Claude
Complete installation guide for setting up the Product Design Agent in Claude. Works for any Claude mode (Chat, Cowork, or Code)

## Prerequisites

**Required:** A [Claude account](https://claude.ai) (any plan).

## Installation Steps

### Step 1: Choose and Install a Skill

Skills are role-specific instruction sets. Pick the one that matches your current focus and paste it as Custom Instructions in Claude.

| Skill | File path | Install when… |
|---|---|---|
| `researcher` | `assets/claude/skills/researcher.md` | Planning and running user research |
| `strategist` | `assets/claude/skills/strategist.md` | Framing problems and defining strategic direction |
| `team-lead` | `assets/claude/skills/team_lead.md` | Leading design teams and managing stakeholders |
| `designer` | `assets/claude/skills/designer.md` | Designing, documenting systems, and creating content |

**To install:**
1. Open the Skill file that matches your role
2. Copy its entire contents
3. Go to **Claude Settings → Custom Instructions**, paste, and save

> You can combine multiple Skills by pasting them one after another in the same Custom Instructions field.

### Step 2: Test Your Setup

Don't know how to start? Just type:
- "What can you help me with?"
- "I'm new to this agent"
- "Show me what capabilities you have"

The onboarding guide will be triggered automatically.

## Next Steps

Once installed, explore what the agent can do:
- **Discover tasks**: Ask "What tasks can you help with?"
- **Specialized agents**: Request specific expertise areas

---

**Ready to upgrade your design process?** Start with "I'm working on [your project type] and need help with [specific challenge]"