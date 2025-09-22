# RAG Guide: Designing for AI Assistants

## Overview & Objectives

**Purpose**: Guide product teams in creating human-centered AI assistant experiences that are trustworthy, transparent, and genuinely useful.

**Scope**: Complete design methodology covering strategy, UX patterns, technical feasibility, and ethical implementation.

**Success Criteria**: 
- AI solutions uniquely address real user problems
- Users maintain agency and control over AI interactions
- Systems are transparent, explainable, and build trust
- Technical implementation aligns with user experience goals

## Core Principles & Paradigm Shift

### The New Interaction Paradigm
- **Invisible Technology**: Good AI design weaves seamlessly into everyday workflows
- **Unstructured Input**: Move beyond rigid forms to natural language interaction
- **Intent-Driven Interfaces**: Focus on user goals rather than system functions
- **Context Management**: Handle dynamic context for intelligent responses
- **Conversational Evolution**: Balance chat interfaces with expanding UI patterns

### Fundamental Design Questions
**Primary**: "How might we solve X?" (not "Can we use AI to X?")
**Secondary**: "Can AI solve this problem in a unique way?"

## Phase 1: Strategy & Value Alignment

### 1.1 AI Suitability Assessment

**When AI Adds Value**:
- Future event prediction (flight prices, demand forecasting)
- Personalization that improves over time
- Natural language understanding and processing
- Low-frequency event detection that evolves
- Tasks that are strenuous or ill-suited to traditional interfaces

**When AI May Not Be Appropriate**:
- Maintaining predictable, consistent behaviors
- Minimizing high-stakes errors
- Complete transparency requirements
- Automating tasks people enjoy
- Static information delivery

### 1.2 Automation vs Augmentation Decision

**Automate When**:
- Tasks are boring, repetitive, dangerous, or awkward
- Users lack necessary knowledge or ability
- Goal is increased efficiency or safety

**Augment When**:
- Tasks involve personal responsibility or social capital
- Users enjoy the activity
- Stakes are high (medical, financial, legal decisions)
- Goal is enhanced user control or capability

**Human-in-the-Loop**: Always provide options for human oversight, preview, editing, or reversal.

## Phase 2: UX Architecture & Interaction Design

### 2.1 Agent UX Design Principles (Microsoft Framework)

**Space (Environment)**:
- **Connecting, not collapsing**: Agents connect people and knowledge, never replace humans
- **Accessible yet invisible**: Background processes with visible, controllable actions via dashboards

**Time (Evolution)**:
- **Historical reflection**: Use memory and connected data for informed current decisions
- **Nudging over notifying**: Proactive engagement based on context and preferences
- **Adaptive evolution**: Learn from user behavior, feedback, and accessibility needs

**Core (Foundation)**:
- **Embrace uncertainty with trust**: Display confidence levels and reasoning transparently
- **Transparency, control, consistency**: User control over knowledge, tools, connections, and settings

### 2.2 AI UX Pattern Library

**Wayfinders** (Solving blank canvas problem):
- Nudges and contextual suggestions
- Template libraries and starting points
- Progressive disclosure of capabilities

**Input Patterns**:
- Open input fields for natural language
- Inline actions for contextual interaction
- Remix/blend capabilities for combining sources

**Tuners** (Refinement controls):
- Filters to constrain inputs/outputs
- Parameters for fine-tuning behavior
- Personal voice settings for consistent tone
- Primary source anchoring for responses

**Governors** (Maintaining user agency):
- Citation and source attribution
- Controls for managing flow and pausing requests
- "Show the work" previews before execution
- Regenerate and variation options

**Trust Indicators**:
- Memory controls and data transparency
- Incognito mode for sensitive interactions
- Watermarks on generated content
- Confidence scoring and uncertainty communication

### 2.3 Common AI Assistant Design Challenges & Solutions

**Challenge 1: Users don't know what the AI can do**
- **Proactive Discovery**: AI suggests actions at contextual moments (e.g., "Need help drafting a contract?" when legal document uploaded)
- **Visible Entry Points**: Dedicated buttons, sidebars, or embedded components where users expect AI
- **Progressive Onboarding**: Quick tutorials, empty states, and contextual hints showing capabilities
- **Contextual Suggestions**: Surface relevant actions based on current user activity and content

**Challenge 2: Users don't know how to interact with AI**
- **Guided Inputs**: Structured quick actions and suggested prompts instead of open-ended chat
- **Interactive Forms**: Structured fields that build prompts behind the scenes
- **Template Library**: Sample prompts showing effective interaction patterns
- **Progressive Complexity**: Start simple, reveal advanced options as users gain confidence

**Challenge 3: AI outputs can be unpredictable or inaccurate**
- **Clear Expectation Setting**: Disclaimers like "AI-generated content — review for accuracy"
- **Edit and Refine Options**: Allow users to modify outputs or request revisions
- **Structured Feedback Loops**: Thumbs-up/down ratings with specific improvement suggestions
- **Multiple Variations**: Provide alternative responses for user selection
- **Confidence Indicators**: Display certainty levels and suggest review when uncertain

**Challenge 4: AI can feel like a black box**
- **Process Transparency**: Step-by-step progress indicators showing AI reasoning
- **Source Attribution**: Highlight which information sources influenced decisions
- **Confidence Communication**: Display certainty levels with clear uncertainty indicators
- **Reasoning Explanation**: Show logic chains and decision factors when possible

**Challenge 5: AI responses can be slow**
- **Real-time Progress**: Animations, loaders, and status updates showing active processing
- **Asynchronous Processing**: Allow continued work while AI processes in background
- **Partial Results**: Show rough drafts or progress while final version processes
- **Time Estimates**: Communicate expected completion times for complex tasks

**Challenge 6: Users need control over AI outputs**
- **Direct Editing**: Allow modification of AI-generated content within interface
- **Clear Undo/Regenerate**: Simple options to retry or revert changes
- **Structured Refinements**: Specific adjustment options like "Make more detailed" or "Simplify language"
- **Override Mechanisms**: Easy ways to reject or completely replace AI suggestions

**Challenge 7: Integrating AI seamlessly into the product**
- **Contextual Integration**: Embed AI within existing workflows rather than separate tools
- **Consistent Design Language**: Match AI elements to product UI style with distinct AI indicators
- **Persistent Access**: Store AI outputs in logical locations, not just chat history
- **Native Feel**: Make AI feel like core functionality, not an external add-on

**Challenge 8: Finding the right tone for AI communication**
- **Context-Appropriate Voice**: Formal for legal/financial apps, conversational for support
- **Warm Microcopy**: Friendly but clear system messages that build trust
- **Brand Consistency**: Align AI messaging with overall brand voice across interactions
- **Error Communication**: Replace technical errors with helpful, human-friendly language

## Phase 3: Technical Feasibility & Prototyping

### 3.1 Feasibility Assessment Framework

**Data Requirements**:
- Data availability (open source, public, purchasable)
- Data labeling state (supervised vs unsupervised learning)
- Data quality and completeness

**Expertise Validation**:
- Human expert capability test ("intern test")
- Available SDK/API solutions
- Technical team capabilities and resources

**ML Task Framing**:
- Classification for categorical data (spam filtering)
- Regression for numerical prediction (pricing)
- Clustering for pattern finding in unlabeled data

### 3.2 Model Planning Worksheet

**Objective**: Specific question the AI answers
**Input**: Training and deployment data sets
**Features**: Important factors the model analyzes
**Output**: Machine response formatted as probability with confidence
**UX Impact**: How outcomes help users and create business value

### 3.3 Prototyping Without AI

**Simulation Techniques**:
- Role playing scenarios
- Wizard of Oz testing
- Personalized wireframes with real user data

**Research Focus Areas**:
- Mental models of intelligent, adaptive systems
- Machine teaching investment (data sharing, feedback)
- Ethical concerns and edge case scenarios
- Transparency importance and expectations

## Phase 4: Success Metrics & Ethical Implementation

### 4.1 Reward Function Design

**Confusion Matrix Analysis**:
- True Positives/Negatives (correct predictions)
- False Positives/Negatives (error types and impacts)
- Cost weighting for different error types

**Precision vs Recall Trade-off**:
- Precision: High confidence, fewer false positives
- Recall: Completeness, fewer false negatives
- Context-dependent optimization based on user impact

### 4.2 Continuous Evaluation Metrics

**System Performance**:
- LLM call error rate
- Token usage per interaction
- Latency per tool call

**Task Completion**:
- Task completion rate without human intervention
- Steps per task optimization

**Quality Control**:
- Output format success rate
- Context adherence scoring

**Tool Integration**:
- Tool selection accuracy
- Cross-tool workflow efficiency

### 4.3 Ethical Design & Risk Mitigation

**Core Ethical Challenges**:
- **User Trust & Transparency**: Explainability and graceful failure handling
- **User Autonomy**: Machine teaching, feedback loops, and intervention controls
- **Value Alignment**: Computational virtue and bias mitigation

**Design Tensions Management**:
- Privacy vs. personalization balance
- Accuracy vs. transparency trade-offs
- Efficiency vs. user control priorities

**Consequence Analysis**:
- Multi-level impact assessment (cultural, political, economic)
- Unintended consequence mapping
- "If this, then what?" scenario planning

### 4.4 Fault Tolerance & Guardrails

**System Resilience**:
- Redundancy through parallel agent processes
- Automated recovery mechanisms
- Stateful recovery for session continuity

**Safety Mechanisms**:
- Clear termination conditions preventing infinite loops
- Rule-based filters and input validation
- Explicit human-in-the-loop oversight points
- Graceful degradation when AI fails

## Implementation Checklist

**Strategy Phase**:
- [ ] AI suitability assessment completed
- [ ] Automation vs augmentation decision made
- [ ] Human-in-the-loop mechanisms defined

**Design Phase**:
- [ ] UX patterns selected and customized
- [ ] Agent principles integrated into designs
- [ ] Trust indicators implemented

**Technical Phase**:
- [ ] Feasibility assessment completed
- [ ] Model objectives clearly defined
- [ ] Prototyping and validation conducted

**Deployment Phase**:
- [ ] Success metrics established
- [ ] Ethical considerations addressed
- [ ] Guardrails and fault tolerance implemented
- [ ] Continuous monitoring system active

## References

### Project/Toolkit Resources
- "AI meets Design toolkit," by Nadia Piet: https://aimeets.design
- "AI meets Design Worksheets (Companion Material)," by Nadia Piet: https://aimeets.design
- "AI Brainstorming Kit," by Researchers at Carnegie Mellon University's HCI Institute: https://aidesignkit.github.io
- "The Shape of AI | UX Patterns for Artificial Intelligence Design," by Emily Campbell
- "UX design for agents: Microsoft principles and guidelines for building agentic experiences," by Microsoft Design
- "People + AI Guidebook: User Needs + Defining Success," from People + AI Research team (Google): https://pair.withgoogle.com
- "Designing for AI Assistants: Solving Key Challenges Through UI/UX", by Eleana Gkogka: https://medium.com/@eleana_gkogka/designing-for-ai-assistants-solving-key-challenges-through-ui-ux-e869358d048c

### External Tools and Resources
- "Human-centered machine learning," by Google Design (via Medium): https://medium.com/google-design/human-centered-machine-learning-a770d10562cd
- "strategic-data-acquisition," from Appanion (via Medium): https://medium.com/appanion/strategic-data-acquisition-6aa351d91ffb
- "Elements of AI," from elementsofai.com: https://elementsofai.com
- "Algorithms.design," from Algorithms.design: https://Algorithms.design
- "paperswithcode.com /sota" (Recent research developments), from paperswithcode.com: https://paperswithcode.com/sota

### The Shape of AI UX Patterns

**Wayfinders**:  
- "Follow up," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/follow-up"  
- "Nudges," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/nudges"  
- "Suggestions," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/suggestions"  
- "Templates," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/templates"  

**Input Patterns**:  
- "Auto Fill," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/auto-fill"  
- "Inline action," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/inline-action"  
- "Madlibs," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/madlibs"  
- "Open input," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/open-input"  
- "Remix / Blend," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/remix"  

**Output & Processing**:  
- "Summary," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/summary"  
- "Synthesis," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/synthesis"  
- "Token layering," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/token-layering"  

**Tuners & Controls**:  
- "Filters," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/filters"  
- "Inpainting," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/inpainting"  
- "Model management," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/model-management"  
- "Parameters," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/parameters"  
- "Personal voice," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/personal-voice"  
- "Primary sources," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/primary-sources"  
- "References," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/references"  
- "Workflows," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/workflows"  

**Governors & Transparency**:  
- "Citations," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/citations"  
- "Controls," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/controls"  
- "Footprints," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/footprints"  
- "Prompt transparency," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/prompt-transparency"  
- "Regenerate," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/regenerate"  
- "Sample response," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/sample-response"  
- "Show the work," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/plan-of-action"  
- "Token transparency," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/token-transparency"  
- "Variations," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/variations"  

**Trust & Privacy**:  
- "Incognito mode," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/incognito-mode"  
- "Memory," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/memory"  
- "Watermarks," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/watermark"  
- "Data ownership," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/data-ownership"  
- "Rating," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/rating"  

**Interface Elements**:  
- "Caveat," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/caveat"  
- "Color scheme," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/color"  
- "Disclosure," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/disclosure"  
- "Initial CTA," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/cta"  
- "Name," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/name"  
- "Personality," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/personality"  
- "Symbols," from The Shape of AI | UX Patterns for Artificial Intelligence Design: "https://www.shapeof.ai/patterns/iconography"  

### LukeW AI-Related Writings (Luke Wroblewski)

**Interface Evolution & Paradigms**:
- "Defining Chat Apps," by Luke W: https://lukew.com/ff/entry.asp?1909
- "Letting the Machines Learn," by Luke W: https://lukew.com/ff/entry.asp?1908
- "Unstructured Input in AI Apps Instead of Web Forms," by Luke W: https://lukew.com/ff/entry.asp?1907
- "World Knowledge Improves AI Apps," by Luke W: https://lukew.com/ff/entry.asp?1906
- "Chat is: the Future or a Terrible UI," by Luke W: https://lukew.com/ff/entry.asp?1905
- "Rethinking Applications for AI," by Luke W: https://lukew.com/ff/entry.asp?1904

**Context & Prompt Management**:
- "Dynamic Context for AI Agents," by Luke W: https://lukew.com/ff/entry.asp?1903
- "Prompt Building User Interfaces," by Luke W: https://lukew.com/ff/entry.asp?1902
- "Context Management UI in AI Products," by Luke W: https://lukew.com/ff/entry.asp?1899
- "Background Agents Reduce Context Window Issues," by Luke W: https://lukew.com/ff/entry.asp?1891
- "Enhancing Prompts with Contextual Retrieval," by Luke W: https://lukew.com/ff/entry.asp?1890
- "Make the AI Models do the Prompting," by Luke W: https://lukew.com/ff/entry.asp?1887

**Development & Product Strategy**:
- "AI Has Flipped Software Development," by Luke W: https://lukew.com/ff/entry.asp?1901
- "Designing Software for AI Agents," by Luke W: https://lukew.com/ff/entry.asp?1900
- "What Do You Want To AI?," by Luke W: https://lukew.com/ff/entry.asp?1898
- "Common AI Product Issues," by Luke W: https://lukew.com/ff/entry.asp?1896
- "The Evolution of AI Products," by Luke W: https://lukew.com/ff/entry.asp?1886
- "AI Models Enable New Capabilities," by Luke W: https://lukew.com/ff/entry.asp?1874

**Agent Management & Interfaces**:
- "Agent Management Interface Patterns," by Luke W: https://lukew.com/ff/entry.asp?1895
- "The Receding Role of AI Chat," by Luke W: https://lukew.com/ff/entry.asp?1894
- "MCP: Model-Context-Protocol," by Luke W: https://lukew.com/ff/entry.asp?1892
- "Designing Perplexity," by Luke W: https://lukew.com/ff/entry.asp?1885
- "Usable Chat Interfaces to AI Models," by Luke W: https://lukew.com/ff/entry.asp?1884
- "Chat Interfaces & Declaring Intent," by Luke W: https://lukew.com/ff/entry.asp?1880

**Testing & UX Research**:
- "Ask LukeW: Generation Model Testing," by Luke W: https://lukew.com/ff/entry.asp?1893
- "UXPA: Using AI to Streamline Persona & Journey Map Creation," by Luke W: https://lukew.com/ff/entry.asp?1889
- "UXPA: Bridging AI and Human Expertise," by Luke W: https://lukew.com/ff/entry.asp?1888
- "Ask LukeW: Conversational AI Usability Study," by Luke W: https://lukew.com/ff/entry.asp?1881

**Personal Assistants & Advanced Features**:
- "Do All AI Models Need To Be Assistants?," by Luke W: https://lukew.com/ff/entry.asp?1879
- "Early Glimpses of Really Personal Assistants," by Luke W: https://lukew.com/ff/entry.asp?1873
- "Multi-Modal Personal Assistants: Early Explorations," by Luke W: https://lukew.com/ff/entry.asp?1871
- "Generative Agents," by Luke W: https://lukew.com/ff/entry.asp?1870
- "Personal Computation Mediums & AI," by Luke W: https://lukew.com/ff/entry.asp?1869

**Technical Implementation & Standards**:
- "Improving AI Models Through Inference Scaling," by Luke W: https://lukew.com/ff/entry.asp?1878
- "AI Models in Software UI," by Luke W: https://lukew.com/ff/entry.asp?1872
- "An AI Icon Standard for Apps?," by Luke W: https://lukew.com/ff/entry.asp?1868
- "Molecular Sequence Modeling & Design," by Luke W: https://lukew.com/ff/entry.asp?1882

**Content & Publishing**:
- "More on Generative Publishing," by Luke W: https://lukew.com/ff/entry.asp?1897
- "Publishing in the Generative AI Age," by Luke W: https://lukew.com/ff/entry.asp?1877

**Accessibility & Conference Content**:
- "Smashing Conf: How to Use AI to Build Accessible Products," by Luke W: https://lukew.com/ff/entry.asp?1876
- "Designing for AI: Panel Notes," by Luke W: https://lukew.com/ff/entry.asp?1875
- "Ask LukeW: 2 Years and 27,000 Answers," by Luke W: https://lukew.com/ff/entry.asp?1883

### Books, Magazines, and Courses
- "AI for Everyone on Coursera," by Andrew Ng
- "AI-driven design e-book series," by Adyen & AWWWARDS
- "Machine Learning for Designers," by Patrick Hebron
- "Mastering AI Agents," by Pratik Bhavsar
- "STRAT's AI Bootcamp for UX Teams," by Greg Nudelman
- "UX for AI: A Framework for Designing AI-Driven Products," by Greg Nudelman