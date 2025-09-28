# Product Design Agent: Setup in Claude
Complete installation guide for setting up the Product Design Agent in Claude Projects.

## Prerequisites

**Required:** [Claude Pro subscription](https://claude.com/pricing) to access the Projects feature.

## Installation Steps

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

**Note:** Any files you drop within the Claude project which aren't from GitHub will be treated as project-specific context.

### Step 4: Configure Project Instructions
1. **Locate the instructions file**: In the uploaded files, find `assets/instructions.md`
2. **Copy the contents** of that file
3. **Set up Custom Instructions**: Look for "Instructions" or "Custom Instructions" in your project settings
4. **Paste the instructions** from the instructions.md file
5. **Save the configuration**

### Step 5: Add User Preferences (Optional)
1. **Create a user preferences file** if you want to customize behavior
2. **Name it exactly** `user_preferences.md` or `user_preferences.yaml`
3. **Upload to the project** through the "+" button in Project Knowledge
4. **Add your preferences** such as:
   - Preferred response detail level
   - Language preferences (EN/ES)
   - Output format preferences
   - Specific focus areas

### Step 6: Test Your Setup
Don't know how to start? Just type:
- "What can you help me with?" 
- "I'm new to this agent" 
- "Show me what capabilities you have"

The onboarding guide will be triggered automatically.

## Troubleshooting

### Common Issues

**GitHub Upload Fails**
- Ensure you're using the correct repository URL
- Try uploading folders individually if bulk upload fails
- Check your internet connection

**Instructions Not Working**
- Verify you copied the complete contents of `assets/instructions.md`
- Make sure you saved the configuration after pasting
- Try refreshing the project page

**Limited Responses**
- Confirm all required folders (`config`, `knowledge`, `README.md`) were uploaded
- Check that the instruction file was properly configured
- Verify your Claude Pro subscription is active

### Getting Help

- **Project Issues**: Check the main repository's issues page
- **Claude-Specific Problems**: Contact Claude support
- **Feature Requests**: Submit via the repository's issue tracker

## Next Steps
Once installed, explore these key features:
- **Task Registry**: Ask "What tasks can you help with?"
- **Project Analysis**: Upload your project files for contextual guidance
- **Specialized Agents**: Request specific expertise areas
- **Bilingual Support**: Switch between English and Spanish naturally

---

**Ready to upgrade your design process?** Start with "I'm working on [your project type] and need help with [specific challenge]"