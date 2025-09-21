# Product Design Agent
An open-source AI-powered mentorship system with specialized agents providing expert guidance across product design, user research, UX/UI, strategy, AI integration, and leadership. Built to accelerate learning through personalized, hands-on mentorship with multilingual support.

## Capabilities
By combining specialized sub-agents with structured tasks and comprehensive guides, this design agent ensures clarity, consistency, and high-quality outcomes.
1. **Matches queries to specialized agents** using a sophisticated task registry with 80+ specific expert tasks
2. **Provides consultation/advice on diverse topics**: New project onboarding, project framing, product discovery, project planning, project management, user research, product strategy, user experience design, user interface design,  design leadership, design collaboration, prompts, vibe coding, and more.
3. **Provides structured, actionable resources**: surveys, test plans, component or process guides, checklists, etc
4. **Auto-detects project-specific data**: Have project-specific information? Add or connect it to the Claude project _Files_ folder, and it will be understood as context you can reference in future queries.

## Setup in Claude
Note: You need [Claude Pro subscription](https://claude.com/pricing) to use _Projects_ feature.

### Step 1: Access Claude Projects
1. **Log into Claude** at [claude.ai](https://claude.ai)
2. **Navigate to Projects**: 
   - Look for "Projects" in the left sidebar, or
   - Click your profile area and select "Projects", or  
   - Go directly to [claude.ai/projects](https://claude.ai/projects)
3. **Pin the sidebar** by clicking the pin icon for easier navigation

### Step 2: Create Your Project
1. **Click the orange "New Project" button** in the upper right corner
2. **Name your project**: Something like "Product Design Agent" or "Design Mentorship Assistant"
3. **Add a description** (optional): "AI-powered design mentorship with specialized agents"
4. **Set visibility** (Team plans only):
   - **Keep it private** if you want personal access only
   - **Share with organization** if your team should access it
5. **Click "Create Project"**

### Step 3: Upload Project Files
1. **In your new project**, look for the "Project Knowledge" section on the right side
2. **Click the "+" button** to add content
3. **Select "Upload from GitHub"**
4. Click the 🔗 **chain link button** in the upload modal
5. **Paste this repository URL**: `https://github.com/jmlusiardo/product-design-agent/`
6. **Select specific folders**: Add `config`, `knowledge`, and `README.md`
7. **Click "Add to Project"**

_Note: Any files you drop within the Claude project which aren't from Github will be treated as project-specific context._

### Step 4: Configure Project Instructions
1. **Locate the instructions file**: In the uploaded files, find `assets/instructions.md`
2. **Copy the contents** of that file
3. **Set up Custom Instructions** Look for "Instructions" or "Custom Instructions" in your project instructions.
4. **Paste the instructions** from the instructions.md file
5. **Save the configuration**

### Step 5: Try it out
Don't know how to start? Just type "What can you help me with?" or "I'm new to this agent" and the onboarding guide will be triggered. 