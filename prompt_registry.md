# Prompt Registry

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
  prompt: "Research current design trends in [industry/category] and identify what’s working and what’s outdated. Provide examples and explain why."
  usefulness: Keeps designs modern and aligned with industry shifts.
  tags: ["research", "design trends", "tendencias de diseño"]

- prompt_id: competitor_analysis
  prompt: "Conduct a competitive analysis of [competitor names] focusing on their UX/UI approach to [specific feature]. What are their strengths and weaknesses?"
  usefulness: Benchmarks design strategies against competitors.
  tags: ["research", "competitive analysis", "benchmarking"]

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