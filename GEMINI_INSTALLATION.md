# Product Design Agent: Setup in Google Gemini
Complete installation guide for setting up the Product Design Agent in Google Gemini using Gems.

## Prerequisites

**Required:** [Google One AI Premium subscription](https://one.google.com/about/plans) to access Gemini Advanced and Gems feature.

## Installation Steps

### Step 1: Access Gemini Gems
1. **Log into Gemini** at [gemini.google.com](https://gemini.google.com)
2. **Navigate to Gems**: 
   - Look for "Gems" in the left sidebar, or
   - Click the gem icon (💎) in the interface, or
   - Go directly to [gemini.google.com/gems](https://gemini.google.com/gems)

### Step 2: Create Your Design Agent Gem
1. **Click "New Gem"** or the "+" button
2. **Name your gem**: "Product Design Agent" or "Design Mentor Assistant"
3. **Add a description**: "AI-powered design mentorship with specialized agents for UX/UI, research, strategy, and leadership guidance"

### Step 3: Upload Project Knowledge
1. **In the gem creation interface**, look for the "Knowledge" or "Files" section
2. **Upload repository files**:
   - Download the repository as ZIP from GitHub
   - Extract and upload the `config/`, `knowledge/`, and `assets/` folders
   - Upload the `README.md` file
3. **Alternative method**:
   - Upload files individually through the file picker
   - Focus on essential directories: `config`, `knowledge`, `assets`

### Step 4: Configure Gem Instructions
1. **Locate the instructions file**: In the uploaded files, find `assets/instructions.md`
2. **Copy the contents** of that file
3. **Set up Custom Instructions**: Look for "Instructions" in your project settings
4. **Paste the instructions** from the instructions.md file
5. **Save the configuration**

2. **Paste the complete contents** from `assets/instructions.md` in the repository
3. **Adjust the instructions** to reference uploaded files properly for Gemini's context

### Step 5: Set Conversation Starters
Add these conversation starters to help users get started:

- "What can you help me with as a design mentor?"
- "I'm new to this agent - show me the capabilities"
- "Help me with user research for my project"
- "I need guidance on design strategy"
- "Can you review my design process?"

### Step 6: Configure Gem Settings
1. **Set the persona**: Professional, expert design mentor
2. **Choose conversation style**: Helpful, structured, actionable
3. **Set response length**: Comprehensive (to provide detailed guidance)
4. **Language settings**: Enable multilingual support (EN/ES)

### Step 7: Add User Preferences (Optional)
1. **Create a user preferences document** with your specific needs:
   - Response detail level (minimal/standard/comprehensive)
   - Primary language preference
   - Focus areas (research/strategy/execution/validation)
   - Output format preferences
2. **Upload as additional context** to the gem
3. **Reference in instructions** for personalized responses

### Step 8: Test Your Gem
1. **Save and create** the gem
2. **Start a new conversation** with your gem
3. **Test with sample queries**:
   - "What design methodology should I use for user research?"
   - "Help me create a usability testing plan"
   - "I need a design system strategy"

## Next Steps
Once your gem is active:
- **Explore Task Categories**: Ask "What design tasks can you help with?"
- **Upload Project Context**: Add your specific project files for tailored guidance
- **Request Specialized Help**: Ask for specific agent expertise (Research, Strategy, etc.)

---

**Ready to upgrade your design process?** Start with "I'm working on [your project type] and need help with [specific challenge]"