# Agent Onboarding Detection Triggers

## Purpose
Keywords, phrases, and patterns that should trigger the agent onboarding guide for users unfamiliar with capabilities.

## Primary Trigger Phrases

### Direct Capability Questions
- "What can you help me with?"
- "What can you do?"
- "What are your capabilities?"
- "Show me what you can do"
- "What tasks can you perform?"
- "What services do you offer?"
- "Help me understand what this agent does"

### Getting Started Indicators  
- "I'm new to this agent"
- "First time using this"
- "How do I get started?"
- "Where do I begin?"
- "I don't know how to use this"
- "Getting started guide"
- "How does this work?"

### Task Discovery Requests
- "Show me all tasks"
- "List all capabilities"
- "What tasks are available?"
- "Task catalog"
- "Complete list of functions"
- "All available options"
- "Menu of services"

### Broad/Unfocused Questions
- "I need help with design"
- "Help me with my project"
- "I have a design problem"
- "I need assistance"
- "Can you help me?"
- "I'm stuck"
- "I don't know where to start"

### Navigation/Discovery Language
- "How do I find..."
- "Where can I get help with..."
- "Which task should I use for..."
- "What's the best way to..."
- "How do I choose..."
- "I need guidance on..."

## Secondary Indicators

### Role-Based Confusion
- "I'm a [role] but don't know what tasks apply to me"
- "What should a design manager use this for?"
- "Which features are for researchers?"
- "I'm new to product design"

### Overwhelm Signals
- "This seems complex"
- "Too many options"
- "I don't know what I need"
- "Feeling overwhelmed"
- "Where do I even start?"

### Comparison Language
- "How is this different from..."
- "What makes this unique?"
- "Why would I use this instead of..."
- "How does this compare to..."

## Language Pattern Recognition

### Question Structures That Indicate Onboarding Need
- Open-ended questions without specific task context
- Questions about the agent itself rather than specific work problems
- Meta-questions about using the agent effectively
- Requests for overviews, summaries, or comprehensive guides

### Contextual Clues
- Lack of domain-specific terminology
- Generic rather than specific problem statements
- No mention of specific deliverables or outcomes
- Focus on understanding the tool rather than solving problems

## Response Strategy

When these triggers are detected:
1. Acknowledge the onboarding need
2. Provide comprehensive task catalog with explanations
3. Offer role-based recommendations
4. Include getting started examples
5. Provide progressive learning path
6. Encourage specific follow-up questions

## Example Detection Logic

**High Confidence Onboarding Triggers:**
- Direct "what can you do" questions
- "New to this agent" statements  
- Requests for complete task lists

**Medium Confidence Indicators:**
- Broad problem statements without specifics
- Role confusion or navigation questions
- Overwhelm or complexity concerns

**Context Clues to Consider:**
- User's question specificity level
- Presence of domain knowledge in query
- Request scope (broad vs. narrow)
- Previous interaction history (if available)