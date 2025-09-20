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
   - **Paste this repository URL**: `https://github.com/yourusername/product-design-assistant`
   - **Select specific folders**: Add `config`, `knowledge`, and `README.md`
   - **Click "Add to Project"**

**Alternative Method - Manual Upload:**
If GitHub upload doesn't work:
1. Download this repository as a ZIP file
2. Extract the files locally  
3. Upload the `config` and `knowledge` folders individually
4. Upload the `README.md` file

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
5. **Check bilingual support**: Try asking a question in Spanish if applicable

### Usage Tips for Beginners

**Getting Started:**
- Always start new conversations within your project (not the main Claude interface)
- Use natural language - ask questions as you would to a human mentor
- Try "What can you help me with?" for a complete capability overview

**Making the Most of Your Setup:**
- **Usage limits**: Pro plan has generous limits; monitor usage in project settings
- **Context retention**: Each chat within the project knows about your uploaded files
- **Organization**: Star your project for quick access from the sidebar

### Troubleshooting

**Common Issues:**

**"I don't see the Projects feature"**
- Ensure you have a Claude Pro or Team subscription
- Try refreshing your browser or logging out/in again

**"GitHub upload failed"**
- Try the manual upload method instead
- Check your internet connection
- Ensure the repository URL is correct and accessible

**"Agent isn't responding with specialized guidance"**
- Verify the instructions.md content was properly added to Custom Instructions
- Make sure you're chatting within the project, not the main Claude interface
- Try rephrasing your question or use the onboarding trigger phrase

**"File upload is slow or failing"**
- Try uploading smaller batches of files
- Ensure stable internet connection
- If persistent, contact Claude support through the help center

_Note: Any files you drop within the Claude project which aren't from Github will be treated as project-specific context._