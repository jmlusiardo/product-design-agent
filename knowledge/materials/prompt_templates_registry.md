# Prompt Templates Registry

## RESEARCH PROMPTS

- prompt_id: research_user_flow
 prompt: "Create a user flow for a [fitness app] that helps users set goals, track workouts, and view progress over time."
 usefulness: Helps define structured user flows for apps with goals and progress tracking.
 tags: ["research", "user flow", "flujo de usuario", "ux research"]

- prompt_id: research_user_group
 prompt: "Analyze [target audience/user group] and their pain points when [specific task]. Include motivations, frustrations, workarounds, behavioral patterns, and emotional triggers."
 usefulness: Supports deep understanding of users, motivations, and triggers.
 tags: ["research", "audience analysis", "análisis de usuarios", "ux"]

- prompt_id: research_trends
 prompt: "Research current design trends in [industry/category] and identify what's working and what's outdated. Provide examples and explain why."
 usefulness: Keeps designs modern and aligned with industry shifts.
 tags: ["research", "design trends", "tendencias de diseño"]

- prompt_id: competitor_analysis
 prompt: "Conduct a competitive analysis of [competitor names] focusing on their UX/UI approach to [specific feature]. What are their strengths and weaknesses?"
 usefulness: Benchmarks design strategies against competitors.
 tags: ["research", "competitive analysis", "benchmarking"]

- prompt_id: competitive_market_analysis
 prompt: "Research the [industry] market landscape, analyze top 5 competitors, investigate pricing strategies, partnerships, and identify 3 key opportunities."
 usefulness: Comprehensive market analysis for strategic planning.
 tags: ["research", "analyze", "market research"]

- prompt_id: unconventional_solutions
 prompt: "I need to solve [specific problem] for [user type]. Brainstorm unconventional approaches that challenge typical design assumptions."
 usefulness: Fosters innovative problem solving.
 tags: ["research", "problem solving", "innovación"]

---

## PROTOTYPE PROMPTS

- prompt_id: prototype_mobile_interface
  prompt: "Design a mobile-first interface for [specific function] that prioritizes [key user action]. Consider thumb-friendly navigation and progressive disclosure."
  usefulness: Ergonomic, usable mobile-first prototypes.
  tags: ["prototype", "mobile", "interfaz móvil"]

- prompt_id: product_design_spec_builder
 prompt: "You are a helpful assistant for product designers. Your job is to take their initial thoughts about a product and transform them into a structured design spec that can be used in a prototyping tool to generate relevant prototypes. Follow these steps: --- ## 1. Request Input from the User Ask the user for the following details, one question at a time: ### Question 1: Core Objective - **Ask:** 'What is the main goal of your product? For example: - Help users track expenses - Connect with others - Manage projects efficiently.' --- ### Question 2: Target Users - **Ask:** 'Who are the intended users of your product? For example: - Freelancers - Students - Parents - Small business owners.' --- ### Question 3: Platform - **Ask:** 'What platform is your product for? Please choose one from the following options: 1. Responsive Web (Mobile-optimized) 2. Responsive Web (Desktop-optimized) 3. iOS Native Mobile App (iPhone-optimized) 4. Android Native Mobile App (Phone-optimized) 5. If none of the above, please specify (e.g., iOS Native Mobile App, iPad-optimized).' --- ## 2. Clarify Ambiguities If the user's input is incomplete or unclear, ask follow-up questions to ensure you have enough information to create a meaningful spec. --- ## 3. Key User Flow 1. Break down the user journey into **a maximum of 5 key flows** that are essential to achieving the product's core objective. - Exclude sign-up and sign-in flows, as these do not count toward the key flows. 2. Display up to five flows (if applicable) and ask the user: - 'Which user flow would you like to proceed with?' 3. Once the user confirms the flow, proceed to generate the spec using **only the chosen flow**. --- ## 4. Key Pages & Components For **each step in the selected user flow**, generate the following details: - **Page Name:** Name the page associated with the step (e.g., Homepage, Search Results Page, Checkout Page). - **Components:** List the key elements required on the page to support the user action (e.g., Navigation bar, Search field, Submit button, Product cards). - **Key Interactions:** Describe how users interact with the components on the page (e.g., Clicking 'Add to Cart,' Tapping a calendar to select a date, Typing into a form field). --- ## 5. Preview the Design Spec Before generating the final spec, present a **preview** to the user: 1. Display the generated design spec in a simple, readable format. 2. Ask the user: - 'Does this preview look good to you?' - 'If yes, I'll generate the final markdown format for you to copy.' - 'If no, please make revisions and provide them back to me so I can generate the final markdown format.' --- ## 6. Generate Final Markdown Format If the user confirms the preview is good, generate the final design spec in markdown format. Structure it as follows: --- ### Final Markdown Format Example: ```markdown # Generate a clickable prototype based on the Design Spec below: ## 1. Product Overview - **Platform:** Mobile App (iOS) - **Target Users:** Busy parents ## 2. Core Objective - Help parents plan weekly meals efficiently. ## 3. Key User Flow - Browse Recipes → Add to Meal Plan → Generate Shopping List ## 4. Key Pages & Components ### Homepage - **Components:** Recipe library, Search bar, Filters (e.g., dietary restrictions) - **Key Interactions:** User searches for recipes and selects one to view details. ### Recipe Details Page - **Components:** Recipe image, Ingredients list, 'Add to Meal Plan' button - **Key Interactions:** User taps 'Add to Meal Plan' to save the recipe. ### Shopping List Page - **Components:** Auto-generated list, Checkboxes for each item, Share button - **Key Interactions:** User checks off purchased items or shares the list with a partner. ## 5. Additional Notes - Minimalist style with calming colors, accessibility features for colorblind users.```"
 usefulness: Transforms initial product ideas into structured design specs for prototyping tools through guided questioning.
 tags: ["prototype", "design spec", "product design", "user flow", "create vibe coding webiste"]

- prompt_id: prototype_extract_tokens
  prompt: "Extract all design tokens from the current Figma file and generate a complete token system. Create CSS properties, TypeScript definitions, Tailwind config. Sync changes back to Figma."
  usefulness: Bridges design with development pipelines.
  tags: ["prototype", "tokens", "figma", "typescript"]

- prompt_id: prototype_framework_component
  prompt: "Create a [framework] component for [specific functionality] following [design system/style guide]. Include TypeScript types, error handling, and accessibility."
  usefulness: Generates framework-ready coded components.
  tags: ["prototype", "component", "typescript", "a11y"]

- prompt_id: prototype_healthcare
  prompt: "Create a healthcare prototype for [specific workflow] with: patient data management, appointment scheduling, telemedicine interface, HIPAA compliance."
  usefulness: Specialized healthcare prototypes.
  tags: ["prototype", "healthcare", "workflow"]

- prompt_id: prototype_readme
  prompt: "Create a README.md for this project that includes setup instructions, API documentation, and contribution guidelines. Project details: [project description]."
  usefulness: Generates clear documentation.
  tags: ["prototype", "readme", "documentation"]

- prompt_id: prototype_comprehensive
  prompt: "Create a prototype with comprehensive documentation: component specs, interactions, APIs, requirements, implementation notes."
  usefulness: Ensures detailed handoff-ready prototypes.
  tags: ["prototype", "documentation", "handoff"]

- prompt_id: prototype_ab_testing
  prompt: "Create a prototype with built-in A/B testing: variant switching, metrics collection, significance tracking, results visualization."
  usefulness: Validates design decisions with data.
  tags: ["prototype", "ab testing", "experiments"]

---

## DESIGN TOKENS PROMPTS

- prompt_id: tokens_generate_complete
  prompt: "Generate a complete design token system for [brand/product] using [CSS/JSON/YAML]. Include color, typography, spacing, component tokens."
  usefulness: Builds scalable design token systems.
  tags: ["tokens", "design system", "css", "json"]

- prompt_id: tokens_create_structure
  prompt: "Create tokens following [naming convention] for [use case]. Structure with hierarchy and inheritance."
  usefulness: Standardizes token structures.
  tags: ["tokens", "naming", "estructura"]

- prompt_id: tokens_typography
  prompt: "Create typography tokens: font-family/size/weight/line-height/scale/variant. Include responsive scaling and semantic hierarchy."
  usefulness: Consistent, responsive typography.
  tags: ["tokens", "typography", "tipografía"]

- prompt_id: tokens_accessibility
  prompt: "Build accessibility tokens for focus indicators, high contrast, reduced motion, screen reader states. Include WCAG markers."
  usefulness: Ensures accessible systems.
  tags: ["tokens", "accessibility", "a11y"]

- prompt_id: tokens_audit
  prompt: "Audit design tokens for consistency, hierarchy, accessibility, missing variants. Suggest improvements."
  usefulness: Token quality assurance.
  tags: ["tokens", "audit", "qa"]

- prompt_id: tokens_implementation_table
  prompt: "Create a token implementation table with: Token Name | Design Status | Dev Status | Testing Status | Docs | Release | Issues."
  usefulness: Tracks adoption status.
  tags: ["tokens", "tracking", "status"]

- prompt_id: tokens_json_array
  prompt: "Generate a JSON array of token objects for spreadsheets: { 'tokenName': 'color-primary-500', 'value': '#382B76', ... }."
  usefulness: Data portability of tokens.
  tags: ["tokens", "json", "spreadsheet"]

- prompt_id: tokens_compare_figma
  prompt: "Compare Figma variables with tokens in code. Identify missing variables, unused tokens, sync issues."
  usefulness: Maintains design-code alignment.
  tags: ["tokens", "figma", "sync"]

---

## MOTION PROMPTS

- prompt_id: animation_scroll
  prompt: "Develop scroll-triggered animations for [landing page] to guide user attention."
  usefulness: Motion-driven focus in UIs.
  tags: ["animation", "motion", "scroll"]

- prompt_id: animation_loading
  prompt: "Design a comprehensive loading animation for [SaaS platform] using Framer Motion and React. Include skeletons, shimmer, fallback, error states."
  usefulness: Improves perceived performance.
  tags: ["animation", "loading", "framer motion"]

- prompt_id: animation_hero_section
  prompt: "Build a hero animation for [product page]: headline fades in, subtitle delay, CTA button. Use CSS or GSAP."
  usefulness: Engaging hero section design.
  tags: ["animation", "hero section", "gsap"]

- prompt_id: animation_heart_button
  prompt: "Animate a heart button for [card/post]. Start with outline, fill, scale bounce, color transition, particles, fade-out."
  usefulness: Fun micro-interactions.
  tags: ["animation", "microinteraction", "button"]

---

## ANALYSIS & EVALUATION PROMPTS

- prompt_id: rate_content
 prompt: "Rate the above [article] in different aspects and suggest how I can improve it in those areas."
 usefulness: Provides structured feedback for content improvement.
 tags: ["ideation", "understanding", "brainstorming"]

- prompt_id: tldr_summarize
 prompt: "You are an experienced grammar teacher with over 20 years of experience. Your task is to provide a concise summary (TL;DR) of the text provided to you. Ensure that the summary captures the main ideas and key points without altering the original context or meaning of the text. Keep the summary brief and to the point."
 usefulness: Generates clear, contextual summaries without losing meaning.
 tags: ["productivity", "writing", "analyzing"]

- prompt_id: case_study_accelerator
 prompt: "Break down [case study] into key elements. Show root problems, impact factors, and solution strategies. Create a decision guide with outcome predictions. Generate an analysis score. Case: [Enter case details]."
 usefulness: Structured case study analysis with decision frameworks.
 tags: ["analyzing"]

- prompt_id: visual_simplify_complex
  prompt: "Explain this [chart/diagram/visual] in simple terms. Break down what it shows and what the key insights are. Focus on making complex information accessible to [target audience]."
  usefulness: Simplifies complex visuals and data for better understanding across different audience levels.
  tags: ["visual", "analysis", "simplification", "accessibility", "chart analysis"]

- prompt_id: assumption_challenger
  prompt: "Challenge my assumptions about [topic/problem]. Start a conversation that can help rewire the way I'm thinking about this particular issue. Point out potential blind spots and alternative perspectives."
  usefulness: Breaks through mental barriers and explores alternative viewpoints.
  tags: ["critical thinking", "assumptions", "problem solving", "perspective", "analysis"]

---

## LEARNING & SKILL DEVELOPMENT PROMPTS

- prompt_id: complex_concept_mastery
 prompt: "Break down [concept] into understandable parts for beginners. Create visual diagrams, real-world examples, and step-by-step explanations. Show common mistakes and how to fix them quickly. Include practice questions with solutions. Generate a comprehension score. Topic: [Enter topic]."
 usefulness: Complex concept breakdown with practical learning tools.
 tags: ["analyzing", "ideating"]

- prompt_id: strategic_learning_accelerator
 prompt: "Design a fast learning path for [skill/subject]. Create a 30-day mastery plan with daily mini-goals. Show quick wins, practice exercises, and progress checkpoints. Include resource recommendations. Generate a readiness score. Subject: [Enter subject]."
 usefulness: Creates structured 30-day learning plans with progress tracking.
 tags: ["learning", "analyzing"]

- prompt_id: book_intelligence_extractor
 prompt: "Extract key insights from [book]. Show main ideas, practical lessons, and action steps. Create an implementation guide with progress markers. Include success examples. Generate a value score. Book: [Enter title]."
 usefulness: Extracts actionable insights from books with implementation guides.
 tags: ["learning"]

---

## BUSINESS & SALES PROMPTS

- prompt_id: personal_sales_improvement
 prompt: "Act as a seasoned sales expert trained in Chris Voss's FBI negotiation techniques from Never Split the Difference. Help me apply these methods to improve my sales conversations, especially in high-stakes B2B deals. Use a real-world sales scenario — for example, negotiating pricing or contract terms with a skeptical decision-maker — and guide me through how to use calibrated questions ('How' and 'What'), tactical empathy, mirroring, labeling, and the 'accusation audit' to build trust and shift the conversation in my favor. Show me how to uncover hidden objections, slow the negotiation down to my advantage, and make the other person feel in control while guiding them toward my desired outcome. Include a sample dialogue, suggested phrases to use at each stage of the sales process, and how to handle a 'no' as a gateway to 'yes.' End with a one-page cheat sheet of Voss-style sales tactics and a preparation checklist I can use before every important sales call."
 usefulness: Advanced B2B sales training using proven FBI negotiation techniques.
 tags: ["persuasion", "writing"]

- prompt_id: interview_preparation_coach
 prompt: "Create winning answers for [role]. Show response structures, achievement stories, and confidence-building tools. Include powerful phrases and memory triggers. Generate a preparation score. Position: [Enter role]."
 usefulness: Comprehensive interview preparation with winning response structures.
 tags: ["interviewing", "research"]

---

## WRITING, CONTENT & COMMUNICATION PROMPTS

- prompt_id: essay_writer
 prompt: "I want you to act as an essay writer. You will need to research a given topic, formulate a thesis statement, and create a persuasive piece of work that is both informative and engaging. My first suggestion request is '[essay topic and requirements]'."
 usefulness: Creates well-structured, persuasive essays on various topics with proper research.
 tags: ["essay writing", "academic writing", "research", "persuasive writing", "content creation"]

- prompt_id: prompt_enhancer
 prompt: "Act as a Prompt Enhancer AI that takes user-input prompts and transforms them into more engaging, detailed, and thought-provoking questions. Describe the process you follow to enhance a prompt, the types of improvements you make, and share an example of how you'd turn a simple, one-sentence prompt into an enriched, multi-layered question that encourages deeper thinking and more insightful responses. Here's the prompt to enhance: '[original prompt]'."
 usefulness: Improves and enriches prompts for better AI interactions and deeper responses.
 tags: ["prompt engineering", "ai optimization", "prompt enhancement", "question design", "communication"]

- prompt_id: writing_improvement_engine
 prompt: "Transform my writing for [purpose]. Show structure improvements, impact words, and reader engagement tricks. Create before and after examples with explanations. Generate a quality score. Show: [Paste your text]."
 usefulness: Writing improvement with before/after examples and engagement tactics.
 tags: ["writing"]

 - prompt_id: natural_human_writing
  prompt: "You are a writing assistant trained to write in a clear, natural, and honest tone. Rewrite or generate text using these principles: Use simple language with short, plain sentences. Avoid AI phrases like 'dive into,' 'unleash,' or 'game-changing.' Be direct and concise. Write like people actually talk - it's fine to start with 'and' or 'but.' Skip marketing hype. Don't use dashes (-) in writing. Avoid lists with 'X and also Y' structure. No rhetorical questions like 'Have you ever wondered?' Don't start sentences with 'Basically,' 'Clearly,' or 'Interestingly.' No fake engagement phrases. Match the tone to feel human and authentic, not robotic or promotional."
  usefulness: Transforms AI-generated text to sound more natural and human-like.
  tags: ["writing style", "natural tone", "human-like", "authenticity", "communication"]

- prompt_id: writing_style_analyzer
  prompt: "Analyze the following writing sample for tone, sentence structure, humor, and emotional depth. Then write ONE paragraph about what you found: [Insert Writing Sample]. Next, write [content length] about [topic] based on the analyzed style. Don't copy verbatim, just use the same style, tone, sentence structure, and emotional depth."
  usefulness: Captures and replicates specific writing styles from examples.
  tags: ["writing style", "style analysis", "tone matching", "content creation", "voice replication"

 ---

## TRANSFORM PROMPTS

- prompt_id: document_to_sop
  prompt: "Here's a [document/URL] from [meeting/training/process]. Turn it into a detailed SOP for [specific workflow]. Include step-by-step instructions, responsibilities, and key checkpoints. Format it for team onboarding and reference."
  usefulness: Transforms recorded content into structured standard operating procedures.
  tags: ["documentation", "sop", "process", "onboarding", "workflow"]

---

## CAREER & HIRING PROMPTS

- prompt_id: job_search_optimization
  prompt: "I'm applying for a [role type] at [company/industry]. Here's my current resume and the job description. Provide detailed feedback on my resume, optimize it for this role, and suggest improvements to match the requirements."
  usefulness: Optimizes resumes and job applications for specific opportunities.
  tags: ["career", "job search", "resume", "optimization", "application"]

- prompt_id: job_interviewer
 prompt: "I want you to act as an interviewer. I will be the candidate and you will ask me the interview questions for the [Position] position. I want you to only reply as the interviewer. Do not write all the conversation at once. I want you to only do the interview with me. Ask me the questions and wait for my answers. Do not write explanations. Ask me the questions one by one like an interviewer does and wait for my answers. My first sentence is 'Hi'."
 usefulness: Simulates realistic job interviews for interview preparation and practice.
 tags: ["interview", "job search", "career", "practice", "hiring", "recruitment"]

- prompt_id: recruiter
 prompt: "I want you to act as a recruiter. I will provide some information about job openings, and it will be your job to come up with strategies for sourcing qualified applicants. This could include reaching out to potential candidates through social media, networking events or even attending career fairs in order to find the best people for each role. My first request is '[specific recruiting challenge or job opening details]'."
 usefulness: Provides recruitment strategies and candidate sourcing advice.
 tags: ["recruiting", "hiring", "talent acquisition", "sourcing", "hr"]

- prompt_id: career_counselor
 prompt: "I want you to act as a career counselor. I will provide you with an individual looking for guidance in their professional life, and your task is to help them determine what careers they are most suited for based on their skills, interests and experience. You should also conduct research into the various options available, explain the job market trends in different industries and advice on which qualifications would be beneficial for pursuing particular fields. My first request is '[career guidance scenario or individual's background]'."
 usefulness: Offers professional career guidance and industry insights.
 tags: ["career counseling", "career advice", "professional development", "job market", "skills assessment"]

- prompt_id: cover_letter_writer
 prompt: "I want to write a new cover letter for job applications. Please compose a cover letter describing my technical skills and experience. Here are my details: [years of experience], [previous roles], [tech stack/tools used], [career goals]. I wish to [specific career objective]. Can you write a professional cover letter for a job application based on this information?"
 usefulness: Creates personalized, professional cover letters for job applications.
 tags: ["cover letter", "job application", "professional writing", "career", "job search"]

---

## UX & DESIGN PROMPTS

- prompt_id: ux_ui_developer
 prompt: "I want you to act as a UX/UI developer. I will provide some details about the design of an app, website or other digital product, and it will be your job to come up with creative ways to improve its user experience. This could involve creating prototyping prototypes, testing different designs and providing feedback on what works best. My first request is '[specific design challenge or product details]'."
 usefulness: Provides expert UX/UI guidance and improvement suggestions for digital products.
 tags: ["ux", "ui", "user experience", "design", "prototyping", "usability"]

- prompt_id: midjourney_prompt_generator
 prompt: "I want you to act as a prompt generator for Midjourney's artificial intelligence program. Your job is to provide detailed and creative descriptions that will inspire unique and interesting images from the AI. Keep in mind that the AI is capable of understanding a wide range of language and can interpret abstract concepts, so feel free to be as imaginative and descriptive as possible. For example, you could describe a scene from a futuristic city, or a surreal landscape filled with strange creatures. The more detailed and imaginative your description, the more interesting the resulting image will be. Here is your first prompt: '[describe the image concept you want to generate]'."
 usefulness: Creates detailed, creative prompts for AI image generation tools.
 tags: ["image generation", "midjourney", "creative prompts", "ai art", "visual design"]

---

## SOFTWARE & IT PROMPTS

- prompt_id: it_architect
 prompt: "I want you to act as an IT Architect. I will provide some details about the functionality of an application or other digital product, and it will be your job to come up with ways to integrate it into the IT landscape. This could involve analyzing business requirements, performing a gap analysis and mapping the functionality of the new system to the existing IT landscape. Next steps are to create a solution design, a physical network blueprint, definition of interfaces for system integration and a blueprint for the deployment environment. My first request is '[specific system integration challenge]'."
 usefulness: Provides enterprise-level IT architecture guidance and system integration strategies.
 tags: ["it architecture", "system integration", "enterprise", "technical design", "infrastructure"]

- prompt_id: github_expert
 prompt: "I want you to act as a git and GitHub expert. I will provide you with an individual looking for guidance and advice on managing their git repository. They will ask questions related to GitHub codes and commands to smoothly manage their git repositories. My first request is '[specific git/GitHub question or challenge]'."
 usefulness: Offers expert guidance on Git version control and GitHub workflows.
 tags: ["git", "github", "version control", "development", "repository management", "coding"]

---

## EXPERT ASSISTANT PROMPTS

- prompt_id: instant_expert_assistant
  prompt: "From now on, act as my expert assistant with access to all your reasoning and knowledge. Always provide: detailed explanations with examples, step-by-step breakdowns when relevant, potential challenges and solutions, actionable next steps. Never give vague answers. If the question is broad, break it into parts. If I ask for help, act like a professional in that domain (teacher, coach, engineer, doctor, etc.). Push your reasoning to 100% of your capacity."
  usefulness: Unlocks maximum capability and detailed responses from AI assistants.
  tags: ["expert", "assistant", "detailed analysis", "professional guidance", "reasoning"]

- prompt_id: daily_clarity_assistant
  prompt: "Help me clarify what actually matters today. Ask me questions that should prompt a conversation about what I need to tackle over the next few hours and break down what's urgent and what can wait."
  usefulness: Provides daily prioritization and focus through guided questioning.
  tags: ["productivity", "daily planning", "prioritization", "focus", "clarity"]

---

## EDUCATION & LEARNING PROMPTS

- prompt_id: fill_blank_worksheets
 prompt: "I want you to act as a fill in the blank worksheets generator for students learning English as a second language. Your task is to create worksheets with a list of sentences, each with a blank space where a word is missing. The student's task is to fill in the blank with the correct word from a provided list of options. The sentences should be grammatically correct and appropriate for students at an intermediate level of English proficiency. Your worksheets should not include any explanations or additional instructions, just the list of sentences and word options. Topic: [subject/theme for the worksheet]."
 usefulness: Generates educational worksheets for ESL students with customizable difficulty levels.
 tags: ["education", "esl", "worksheets", "language learning", "english", "teaching"]

- prompt_id: ai_writing_tutor
 prompt: "I want you to act as an AI writing tutor. I will provide you with a student who needs help improving their writing and your task is to use artificial intelligence tools, such as natural language processing, to give the student feedback on how they can improve their composition. You should also use your rhetorical knowledge and experience about effective writing techniques in order to suggest ways that the student can better express their thoughts and ideas in written form. My first request is '[specific writing help needed]'."
 usefulness: Provides detailed writing feedback and improvement suggestions for students.
 tags: ["writing tutor", "education", "writing improvement", "feedback", "composition", "rhetoric"]

 - prompt_id: deep_dive_explainer
 prompt: "Break down [complex topic] like I'm 12, then gradually increase complexity over 5 levels until I reach expert understanding."
 usefulness: Builds layered understanding from novice to expert with clear, staged explanations.
 tags: ["learning", "progressive explanation", "self-study", "aprendizaje"]

 - prompt_id: mistake_prevention_system
 prompt: "List the 10 most common mistakes beginners make with [skill/topic]. For each, give me a simple check to avoid it."
 usefulness: Surfaces high-impact pitfalls and adds quick guardrails to prevent them.
 tags: ["learning", "error prevention", "skill building", "prevención de errores"]

- prompt_id: analogy_machine
 prompt: "Explain [difficult concept] using 3 different analogies from [sports/cooking/movies]. Make it impossible to forget."
 usefulness: Anchors abstract ideas to familiar domains to boost comprehension and recall.
 tags: ["learning", "analogy", "explanation", "analogías"]

- prompt_id: practice_problem_generator
 prompt: "Give me 5 progressively harder practice problems for [topic]. Include hints and detailed solutions."
 usefulness: Provides scaffolded practice with worked solutions to consolidate skills.
 tags: ["learning", "practice", "problem solving", "ejercicios"]

- prompt_id: real_world_connector
 prompt: "Show me 7 ways [concept I'm learning] applies to everyday situations. Use specific examples I can relate to."
 usefulness: Connects theory to practical, personal contexts to improve transfer.
 tags: ["learning", "real-world examples", "contextualization", "ejemplos"]

- prompt_id: knowledge_gap_hunter
 prompt: "Quiz me on [subject] with 10 questions. Based on my answers, identify exactly what I need to study next."
 usefulness: Diagnoses weak areas and outputs targeted next-study topics.
 tags: ["learning", "diagnostic quiz", "assessment", "diagnóstico"]

- prompt_id: simplification_master
 prompt: "Take this complex explanation [paste text] and rewrite it so a 10-year-old could understand it perfectly."
 usefulness: Transforms dense text into plain, accessible language without losing meaning.
 tags: ["learning", "simplify", "ELI5", "simplificar"]

- prompt_id: memory_palace_builder
 prompt: "Help me create a vivid story connecting these [facts/formulas/vocab words] so I never forget them."
 usefulness: Converts lists into memorable narratives using mnemonic imagery.
 tags: ["learning", "mnemonics", "memory", "palacio de la memoria"]

- prompt_id: progress_accelerator
 prompt: "I know [current knowledge]. Design 3 challenging projects that will push me to the next level in [skill/subject]."
 usefulness: Drives advancement via project-based practice with stretch goals.
 tags: ["learning", "project-based", "advanced practice", "proyectos"]

---

## PROJECT MANAGEMENT PROMPTS

- prompt_id: project_manager_prd
 prompt: "I want you to act as a Project Manager specializing in Product Requirements Documents. I will provide you with a specific subject, feature, or development initiative, and you will help me develop a comprehensive PRD using a structured format that includes: Subject, Introduction, Problem Statement, Goals and Objectives, User Stories, Technical Requirements, Benefits, KPIs, Development Risks, and Conclusion. My project topic is: '[project or feature description]'."
 usefulness: Creates comprehensive Product Requirements Documents following industry standards.
 tags: ["project management", "prd", "product requirements", "documentation", "planning", "stakeholder alignment"]

--- 

  ## MORE PROMPT TEMPLATES
- awesome-chatgpt-prompts: https://github.com/f/awesome-chatgpt-prompts?tab=readme-ov-file
- hero.page: https://hero.page/ai-prompts
- data science prompts: https://github.com/travistangvh/ChatGPT-Data-Science-Prompts
- chatgpt prompts: https://www.reddit.com/r/ChatGPT_Prompts/
- snackprompt.com: https://snackprompt.com/
- prompt search: https://www.ptsearch.info/tags/list/
- Promptbase | AI prompt marketplace: https://promptbase.com/
- The chatGPT prompt book: https://docs.google.com/presentation/d/17b_ocq-GL5lhV_bYSShzUgxL02mtWDoiw9xEroJ5m3Q/edit?slide=id.gc6f83aa91_0_79#slide=id.gc6f83aa91_0_79
- chatGPTPromptGenius Reddit: https://www.reddit.com/r/ChatGPTPromptGenius/