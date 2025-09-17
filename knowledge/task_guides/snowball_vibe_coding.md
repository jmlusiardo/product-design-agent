# Snowball Vibe Coding: AI-Driven Prototyping for UX Designers

**Executive Summary** — Snowball Vibe Coding enables UX designers to rapidly build functional AI prototypes using Python and LLMs. This methodology combines user-centered design with working code to validate concepts with customers, align with developers, and demonstrate real AI value. The approach emphasizes speed over perfection, customer feedback over internal assumptions, and iterative building through Plan → Code → Test → Judge cycles.

## Overview & Objectives

- **Purpose:** Enable UX designers to create functional AI prototypes that customers can evaluate and provide feedback on
- **Scope:** Covers the complete Snowball methodology from design exercises through vibe coding implementation
- **Audience:** UX designers, product managers, AI product teams seeking rapid validation
- **Success Criteria:**
 - Working AI prototypes that demonstrate core value propositions
 - Customer feedback gathered on actual functioning systems
 - Alignment between design vision and technical implementation
 - Faster iteration cycles from concept to validation

## The Snowball Manifesto

### Core Principles

1. **Start with Data** — your only moat
2. **Customer at the Center** — toss Snowball at users
3. **Working Code = the Only Thing** — code rules
4. **Lightweight over Heavy** — 10-minute sketches
5. **No Silos, No Handoffs** — one Snowball, one team
6. **Balance Disciplines** — data, AI, and UX roll together
7. **Evaluation Built-In** — measure as you build
8. **Clarity Through Iteration** — requirements = hypotheses
9. **Decide Fast, Adjust Often** — speed > consensus
10. **Code Talks, Bullshit Walks** — ship something real

### Philosophy

Principles only matter if you can test them with running code. Vibe coding rapidly builds prototypes to show customers how AI works and aligns with developers on how AI creates real user value. The goal is giving designers a seat at the table with a running AI-driven prototype that allows customers to evaluate the beating heart of your growing AI system.

## Preparation

### Environment Setup

#### 1. Pick Your LLM
- Start with the one you already use
- Options: Claude, ChatGPT, Gemini (Copilot, Cursor, etc.)
- No need to learn a new tool

#### 2. Set Up Python
**Why Python?**
- Standard for AI prototyping
- Tons of examples, libraries, and community help
- Easy to run small scripts → perfect for vibe coding

#### 3. Troubleshooting Strategy
- Copy/paste error messages into your LLM
- It will walk you through fixes step by step
- Treat the LLM as your live coding coach

#### 4. Install a Code Editor
- VS Code, Thonny, TextMate, etc.
- Helps keep spacing clean and quotes correct
- Don't use Notepad

#### Setup Checklist
- [ ] LLM access confirmed
- [ ] Python installed and working
- [ ] Code editor installed
- [ ] Basic "Hello World" test completed
- [ ] Error troubleshooting process understood

## Strategic Design Exercises

### Low-Fi Problem Framing

Before coding, use lightweight design exercises to frame the problem:

#### 1. Storyboard (4-6 panels)
- Map the user's journey
- What use case are you addressing?
- Show where AI steps in
- End with the value delivered

#### 2. Digital Twin Diagram
- Diagram system's inputs
- What data sources will AI need?
- What is being created by AI?
- Expose assumptions visually

#### 3. Screen Flow Prototyping (5 minutes)
- Use 3x5-inch stickies (mobile screen size)
- Arrange screen layout, controls, buttons, images
- Make multiple versions
- Physical prototype to test concepts with customers and team
- Use RITE: iterate design quickly and retest immediately

## Main Flow: The Vibe Coding Loop

### Step 1: Plan

#### Planning Approach
- Describe your intent in plain English
- Specify: "Plan only -- no code yet!"
- Move from big plan to individual step plans
- Keep each step simple to make coding smooth
- Example: "Python web server that prints hello world in the browser"
- Remember: "Slow is Smooth. Smooth is Fast."

#### Planning Prompts
Write a simple Python web server that prints 'Hello World' in the browser.
Tell me how to deploy it step by step.

### Step 3: Test + Debug

#### Testing Checklist
- [ ] Check server logs (HTTP 200 = success)
- [ ] Check output in browser
- [ ] Verify expected functionality
- [ ] Note any errors or unexpected behavior

#### When It Breaks
- Copy/paste the exact error into your LLM
- Ask: "Explain what this means and how I can fix it step by step"
- Rinse, repeat until it works
- Common issues: encoding problems, port conflicts, indentation errors

### Step 4: Judge

#### Judge Mode Process
Use "Act as a judge" prompts to evaluate code:
- Compare to Intent: Did the code do what you asked for?
- Spot Gaps: Have the LLM check for larger mistakes in system behavior
- Ask for Fixes: Have the judge find opportunities for improvement
- Check readiness: Is the code ready for adding the next step?
- Decide Next Step: good enough? "Ship it!" — plan + code the next step
- If Not: simply say "implement suggested fixes." Test, judge, repeat

#### Judge Prompts
Act as a judge and review this code against plan: does it do what the plan intended?
What are the opportunities for improvement? Any other issues I should be aware of?
Is this code ready for the next step in the larger plan: [next plan step]?

**Important:** Judge mode is for technical review only. The AI helps you debug and improve code. Only customers can decide if it delivers customer value!

## Essential Prompts for Vibe Coding

### Setup & Environment

**Important:** Judge mode is for technical review only. The AI helps you debug and improve code. Only customers can decide if it delivers customer value!

## Essential Prompts for Vibe Coding

### Setup & Environment
Help me install Python and VS Code step by step. I'm a designer, not a developer.

### Hello World Server
Write a simple Python web server that prints 'Hello World' in the browser.
Tell me how to deploy it step by step.

### Debug Errors
Here's the error I got [paste error]. Explain what it means and how to fix it in plain English.

### Refactor Large Files
Break this 700+ line file into smaller modules. Apply modularization and
separation of concerns: each module should do one thing. List the new file
names and their responsibilities before writing the code.

### Documentation & Diagrams
Analyze this code and write code documentation for teammates.
Generate a Mermaid architecture diagram for this code.

## Common Pitfalls & Solutions

### 1. Python Version Mismatch
**Problem:** Libraries don't install or won't run
**Fix:** Ask your LLM: "What Python version do I need for this library?" Install via python.org or pyenv

### 2. Indentation Errors
**Problem:** "IndentationError" crashes your script
**Fix:** Don't use Notepad. Use a real editor (VS Code, Thonny). Make sure "spaces, not tabs" is enabled

### 3. Smart Quotes & Hidden Characters
**Problem:** Code won't run because of " " instead of " " or hidden line endings
**Fix:** Copy/paste into your LLM and ask it to normalize formatting

### 4. Firewall/Port Blocks
**Problem:** Browser can't connect to localhost:8000
**Fix:** Try a different port, e.g. 8080

### 5. Overgrown Files
**Problem:** LLM gets confused with huge monolithic files
**Fix:** Keep code modular (small files, focused functions). Ask the judge to review and refactor regularly

## Pro Tips

### Essential Practices
- **Backup early & often:** Git, or zip + Dropbox. Vibe Coding = elephant wrangling: crashes aren't an IF, it's a WHEN
- **Use a real IDE:** VS Code + Claude plugin = KILLER combination
- **Go Slow:** "Slow is smooth, smooth is fast"
- **Write CLI tests for every step:** Don't wait for elephant stampede
- **Refactor aggressively:** LLMs choke around ~700 lines. Keep Python files modular & practice separation of concerns

### Advanced Techniques
- **Use LLM to draft your RAG files** (then you tune them)
- **Deploy to AWS Lambda:** Secure, disposable, and cheap. Perfect for prototypes you want to share with test users
- **Generate documentation:** "Explain this codebase in plain English, write code docs for teammates, and generate system architecture diagrams"
- **Create diagrams:** For teams who like code diagrams, use Mermaid CLI

## Customer Validation

The Snowball process is not about turning UXers into engineers. It's about giving you a seat at the table with a running AI-driven prototype that allows customers to evaluate the beating heart of your growing AI system and make changes fast.

### Key Principles
- Customer at the center always
- Working prototypes enable real feedback
- Speed over perfection
- Iteration based on actual usage
- Technical validation through judge mode
- Customer validation through testing

## Tools & Resources

### Required Tools
- Python 3.x
- Code editor (VS Code recommended)
- LLM access (Claude, ChatGPT, Gemini)
- Web browser for testing

### Optional Advanced Tools
- Git for version control
- AWS Lambda for deployment
- Mermaid CLI for diagrams
- VS Code extensions for Python

### Backup Solutions
- Regular code backups (Git, Dropbox, etc.)
- Version control for iteration tracking
- Documentation of working configurations

## References
- Snowball Vibe Coding Guide, UXforAI.com: https://drive.google.com/file/d/1iNSqpryo37-gndq6hNS2laHG1hUrJhfK/view?usp=sharing