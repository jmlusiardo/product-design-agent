# Product Design Agent

An open-source AI-powered mentorship system with specialized agents providing expert guidance across product design, user research, UX/UI, strategy, AI integration, and leadership. Built to accelerate learning through personalized, hands-on mentorship with multilingual support.

## Capabilities

This intelligent mentorship system:
- **Matches queries to specialized agents** using a sophisticated task registry with 80+ expert tasks
- **Provides structured, actionable resources** including guides, templates, and checklists
- **Supports multilingual learning** (English, Spanish) with seamless context switching
- **Onboards new users automatically** with comprehensive capability discovery and guided learning paths
- **Accelerates professional growth** through personalized, adaptive mentorship
- **Delivers hands-on tools** for real-world design challenges
- **Integrates AI workflows** with specialized AI and prompt engineering guidance

## Setup in Claude

### Prerequisites

**Required:**
- Claude account (sign up at [claude.ai](https://claude.ai) if you don't have one)
- Claude Pro subscription ($20/month) or Claude Team plan for optimal performance
- Access to Claude Projects feature (included with Pro and Team plans)

**Recommended:**
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Stable internet connection for file uploads

### Step-by-Step Installation

#### Step 1: Access Claude Projects
1. **Log into Claude** at [claude.ai](https://claude.ai)
2. **Navigate to Projects**: 
   - Look for "Projects" in the left sidebar, or
   - Click your profile area and select "Projects", or  
   - Go directly to [claude.ai/projects](https://claude.ai/projects)
3. **Pin the sidebar** by clicking the pin icon for easier navigation

#### Step 2: Create Your Project
1. **Click the orange "New Project" button** in the upper right corner
2. **Name your project**: Something like "Product Design Agent" or "Design Mentorship Assistant"
3. **Add a description** (optional): "AI-powered design mentorship with specialized agents"
4. **Set visibility** (Team plans only):
   - **Keep it private** if you want personal access only
   - **Share with organization** if your team should access it
5. **Click "Create Project"**

#### Step 3: Upload Project Files
1. **In your new project**, look for the "Project Knowledge" section on the right side
2. **Click the "+" button** to add content
3. **Select "Upload from GitHub"**:
   - Click the 🔗 **chain link button** in the upload modal
   - **Paste this repository URL**: `https://github.com/product-design-assistant`
   - **Select specific folders**: Add `config`, `knowledge`, and `README.md`
   - **Click "Add to Project"**

_Note: Any files you drop within the Claude project which aren't from Github will be treated as project-specific context._

#### Step 4: Configure Project Instructions
1. **Locate the instructions file**: In the uploaded files, find `assets/instructions.md`
2. **Copy the contents** of that file
3. **Set up Custom Instructions**:
   - Look for "Instructions" or "Custom Instructions" in your project settings
   - **Paste the instructions** from the instructions.md file
   - **Save the configuration**

#### Step 5: Verify Installation
Test your setup with these verification steps:

1. **Start a new chat** within your project
2. **Try the onboarding trigger**: Type "What can you help me with?" or "I'm new to this agent"
3. **Verify response**: You should receive a comprehensive capability overview with task categories
4. **Test a specific task**: Try "Help me plan a kickoff meeting" or "I need UX research guidance"
