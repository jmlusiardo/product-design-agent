# Task Registry

## ONBOARDING

tasks:
  - task_id: "onboarding_design_leads"
    triggers: ["onboarding design lead", "new design lead", "design lead first days", "design leadership onboarding"]
    task_guide: 
      - "onboarding_design_leads.md"

  - task_id: "onboarding_designers"
    triggers: ["onboarding designer", "new designer", "designer first days", "designer onboarding"]
    task_guide: 
      - "onboarding_designers.md"

## PROJECT FRAMING

tasks:
  - task_id: "kickoff_meeting"
    triggers: ["kickoff meeting", "project kickoff", "reunión de inicio", "kick off"]
    task_guide: 
      - "kickoff_meeting.md"

  - task_id: "initiative_canvas"
    triggers: ["initiative canvas", "product initiative canvas", "canvas iniciativa", "product canvas", "initiative planning", "strategic canvas", "product strategy canvas"]
    task_guide: 
      - "initiative_canvas.md"

  - task_id: "project_type_strategy"
    triggers: ["project type", "design strategy", "UX strategy", "tipo de proyecto", "estrategia de diseño"]
    task_guide: 
      - "project_type_strategy.md"

## DISCOVERY

tasks:
  - task_id: "writing_statements"
    triggers: ["user stories", "job stories", "hypotheses", "how might we", "key insight", "historias de usuario"]
    task_guide: 
      - "writing_statements.md"

  - task_id: "user_personas"
    triggers: ["user persona", "personas", "user profiles", "perfiles de usuario"]
    task_guide: 
      - "user_personas.md"

  - task_id: "journey_mapping"
    triggers: ["journey map", "customer journey", "event storming", "mapa de viaje"]
    task_guide: 
      - "journey_mapping.md"

## USER RESEARCH

tasks:
  - task_id: "ux_research_without_users"
   triggers: ["ux research without users", "research without user access", "proxy research", "indirect user research", "no access to users", "can't talk to users", "limited user access", "alternative research methods", "research constraints", "user access blocked", "stakeholder research", "secondary research methods", "forum research", "review analysis", "analytics research", "customer facing teams", "support team insights", "sales team feedback", "investigación sin usuarios", "investigación indirecta", "métodos de investigación alternativos", "sin acceso a usuarios", "equipos de cara al cliente", "análisis de reseñas", "investigación de foros", "datos analíticos para ux"]
   task_guide:
     - "ux_research_without_users.md"

  - task_id: "evaluation_type"
    triggers: ["evaluation definition", "define evaluation", "define evaluation type", "evaluation type", "evaluation plan", "research evaluation", "choose evaluation method", "method selection", "formative evaluation", "summative evaluation", "investigative evaluation", "lab vs field", "comparators", "benchmarking", "sampling plan", "tasks and activities", "measures and analysis", "contingency table", "repeated measures anova", "definición de evaluación", "definir evaluación", "definir tipo de evaluación", "plan de evaluación", "evaluación formativa", "evaluación sumativa", "evaluación investigativa", "selección de método de evaluación", "qué evaluación necesitamos", "tipo de evaluación"]
    task_guide: 
     - "evaluation_type.md"

- task_id: "usability_test_recruiting"
  triggers: ["recruit users", "user recruitment", "recruit participants", "recruiting for usability test", "participant recruitment", "user recruiting", "find test participants", "reclutar usuarios", "reclutamiento de usuarios", "encontrar participantes", "recruiting participants", "usability test participants", "user testing recruitment", "participant sourcing", "test user recruitment", "research participants", "recruiting for research", "user research recruiting", "finding users for testing", "participant screening", "user screening"]
  task_guide: 
    - "recruiting_users.md"
    - "usability_testing.md"
    - "data_information_knowledge.md"
  materials:
    - "cognitive_biases.md"
  
- task_id: "usability_test_planning"
  triggers: ["test plan", "usability test plan", "create test plan", "planning usability test", "usability testing planning", "test planning", "user testing plan", "plan de prueba", "planificar prueba de usabilidad", "planificación de test", "diseñar test de usabilidad", "test design", "usability study plan", "user research plan", "testing strategy", "test preparation", "preparar prueba de usabilidad"]
  task_guide: 
    - "test_plan.md"
    - "recruiting_users.md"
    - "usability_testing.md"
    - "data_information_knowledge.md"
  materials:
    - "cognitive_biases.md"
    - "product_metrics_list.csv"

- task_id: "usability_test_moderation"
  triggers: ["moderate usability test", "facilitate usability test", "run usability test", "conducting usability test", "usability test facilitation", "test moderation", "user testing moderation", "moderar prueba de usabilidad", "facilitar test", "conducir prueba", "ejecutar test de usabilidad", "test facilitation", "usability session", "user testing session", "running user tests", "test execution", "usability testing execution", "moderating sessions", "facilitating sessions"]
  task_guide: 
    - "moderating_usability_test.md"
    - "usability_testing.md"
    - "data_information_knowledge.md"
  materials:
    - "cognitive_biases.md"

- task_id: "usability_test_reporting"
  triggers: ["usability test results", "report usability test", "usability testing report", "test results reporting", "user testing results", "analyze usability test", "usability findings", "test analysis", "reportar resultados", "análisis de prueba", "resultados de test", "informe de usabilidad", "usability insights", "test insights", "user testing insights", "testing outcomes", "usability data analysis", "test findings", "research findings", "usability research results"]
  task_guide: 
    - "reporting_test_results.md"
    - "data_information_knowledge.md"
    - "usability_testing.md"
  materials:
    - "cognitive_biases.md"
    - "product_metrics_list.csv"

 - task_id: "measure_ux"
    triggers: ["measure UX", "user experience metrics", "HEART framework", "medir experiencia"]
    notion_pages:
      - page_id: "0c88c4f1-9cdf-405e-a9ae-fe1bad8c97d2"
        title: "HEART Framework"

  - task_id: "ux_audit"
    triggers: [
      "heuristic evaluation", "heuristics review", "expert review", "expert ux review", "usability audit", "ux audit", "nng", "nielsen heuristics", "jakob nielsen", "10 heuristics", "usability heuristics", "evaluación heurística", "evaluacion heuristica", "revisión experta", "revision experta", "auditoría de usabilidad", "auditoria de usabilidad", "heurísticas de nielsen", "heuristicas de nielsen", "inspección de usabilidad", "inspeccion de usabilidad", "taller de evaluación heurística", "taller evaluacion heuristica", "heuristic workshop"]
    task_guide:
      - "ux-audit-expert-review.md"
      - "heuristic_evaluation.md"
      - "data_information_knowledge.md"

## STRATEGY

tasks:  
  - task_id: "mvp_definition"
    triggers: ["mvp", "minimum viable product", "minimum usable experience", "mue",","mve","experiencia minima usable", "experiencia minima viable", "experiencia minima deseable", "MLP", "minimum lovable product", "prototype", "poc", "proof of concept", "prueba de concepto", "choose what to build", "choosing what to build", "elegir que construir", "eligiendo que producto construir"]
    task_guide: 
     - "mvp_definition.md"

  - task_id: "brainstorming"
    triggers: ["brainstorming", "ideation", "lluvia de ideas", "brainstorm", "product design workshop", "ideation workshop", "lluvia de ideas", "six thinking hats", "decision log", "crazy 8s", "crazy eights"]
    task_guide: 
     - "brainstorming.md"
  
  - task_id: "event_storming_workshop"
    triggers: ["event storming workshop", "workshop event storming", "taller event storming"]
    task_guide: 
     - "journey_mapping.md"

  - task_id: "project_planning"
    triggers: ["project planning", "project plan", "planificación de proyecto"]
    task_guide: 
     - "project_planning.md"

  - task_id: "prioritization"
    triggers: ["prioritization", "prioritize", "priorización", "effort impact", "effort value, "kano", "right idea","right initative","right project"]
    task_guide: 
     - "prioritization.md"

  - task_id: "kpi_metrics"
    triggers: ["KPI tree", "business objectives", "design metrics", "product metrics", "métricas"]
    task_guide: 
     - "design_kpis.md"
    materials:
     - "product_metrics_list.csv"

  - task_id: "business_model"
    triggers: ["business model canvas", "BMC", "modelo de negocio"]
    task_guide: 
     - "business_model.md"

  - task_id: "value_proposition"
    triggers: ["value proposition", "value proposition canvas", "propuesta de valor","market fit","fit de mercado"]
    task_guide: 
     - "value_proposition.md"

  - task_id: "design_pitch"
    triggers: ["create pitch", "pitch deck", "presentation pitch"]
    task_guide: 
     - "design_pitch.md"
  - task_id: "agile_lean_ux_frameworks"
    triggers: [ "agile ux", "lean ux", "agile user experience", "lean user experience", "ux in agile", "ux in lean", "integrating ux in agile", "ux en agile", "ux en lean", "frameworks de ux", "agile vs lean ux", "user research in agile", "discovery sprint", "design studios agile", "mvp in lean ux", "build measure learn", "prototyping in agile", "ux backlog", "ux retrospectives", "ux debt", "minimum usable product", "mue", "mup", "mvp vs mue", "ux scorecard"]
    task_guide:
      - "agile_lean_ux_frameworks.md"


## DESIGN SYSTEMS

tasks:
  - task_id: "component_documentation"
    triggers: ["component documentation", "document components", "design system documentation", "component guidelines", "component specs", "component guide", "UI component docs", "design component documentation", "component library documentation", "documentar componentes", "documentación de componentes", "guías de componentes", "especificaciones de componentes", "sistema de diseño documentación", "librería de componentes", "component writing", "component content", "component standards", "component template", "wise design components", "storybook documentation", "figma component specs", "component usage guidelines", "component anatomy", "component variants", "component states", "component accessibility", "component implementation", "component best practices", "atomic design documentation", "design tokens documentation", "ui kit documentation", "pattern library documentation", "style guide components"]
    task_guide: 
      - "component_documentation.md"

## VISUAL

tasks:
  - task_id: "writing_ai_image_prompts"
    triggers: ["ai image prompts","generar imagen","generate image","crear imagen","create image","prompt de imagen","crea una imagen","create an image","make an image","make image","hacer imagen"]
    task_guide:
      - "writing_ai_image_prompts.md"
    materials:
      - "prompt_templates_registry.md"

## LEADERSHIP

tasks:
  - task_id: "team_management"
    triggers: ["managing teams", "UX team management", "design team leadership", "liderazgo de equipos","manage product design team"]
    task_guide: 
     - "team_management.md"

  - task_id: "boost_ux_culture"
    triggers: ["UX culture", "UX maturity", "boost UX", "cultura UX", "impulsar UX","evangelizar ux","evangelize design","evangelize ux"]
    task_guide: 
     - "boost_ux_culture.md"

  - task_id: "hiring_designers"
    triggers: ["hiring designers", "recruit designers", "build design team", "contratar diseñadores", "crear equipo de diseño", "armar equipo de diseño", "construir equipo ux"]
    task_guide: 
     - "hiring_designers.md"
     - "creating_design_teams.md"

## COLLABORATION

tasks:
  - task_id: "conflict_resolution"
    triggers: ["conflict resolution", "resolve conflicts", "disagreements", "resolución de conflictos", "argumenting", "argument", "argumentation", "argumentacion de decisiones"]
    task_guide: 
     - "difficult_conversations.md"

  - task_id: "stakeholder_management"
    triggers: ["stakeholder management", "managing stakeholders", "BA collaboration", "manejo de stakeholders"]
    task_guide: 
     - "stakeholder_management.md"

  - task_id: "meeting_facilitation"
    triggers: ["meeting facilitation", "better meetings", "moderate meetings", "reuniones"]
    task_guide:_ 
     - "meeting_facilitation.md"

  - task_id: "design_critique"
    triggers: ["design critique", "design review", "critique session", "crítica de diseño"]
    task_guide:_ 
     - "design_critique.md"

  - task_id: "executive_presentation"
    triggers: ["presentar a ejecutivos", "presentacion a ejecutivos", "executive presentation", "executive showoff", "executive rundown", "present to upper-level management"]
    task_guide:_ 
     - "executive_presentation.md"

  - task_id: "executive_summary"
    triggers: ["executive summary", "status updates", "comunicación de actualizaciones", "resumen para ejecutivos"]
    task_guide:_ 
     - "executive_summary.md"

## PROMPTS AND VIBE CODING

tasks:
  - task_id: "prompt_minification"
    triggers: ["prompt minification", "minify prompts", "compress prompts", "optimize prompts", "shorten prompts", "prompt optimization", "reduce prompt length", "prompt compression", "minimal prompts", "concise prompts", "prompt engineering optimization", "minificar prompts", "optimizar prompts", "comprimir prompts", "prompts cortos", "prompts mínimos"]
    task_guide: 
      - "prompt_minification.md"

  - task_id: "writing_prompts"
    triggers: ["prompt engineering", "write prompts", "create prompts", "prompt creation", "chatgpt prompts", "ai prompts", "better prompts", "effective prompts", "prompt writing", "prompt best practices", "prompt optimization", "prompt formula", "6 step prompts", "prompt structure", "prompt guidelines", "how to prompt", "prompting techniques", "prompt methods", "prompt framework", "ingeniería de prompts", "escribir prompts", "crear prompts", "prompts efectivos", "mejores prompts", "fórmula de prompts", "estructura de prompts", "técnicas de prompts", "ai communication", "llm prompts", "claude prompts", "gpt prompts", "prompt design, "prompt strategy", "conversational ai", "ai instructions"]
    task_guide:
      - "writing_prompts.md"
    materials:
      - "prompt_templates_registry.md"

  - task_id: "snowball_vibe_coding"
    triggers: ["snowball vibe coding", "vibe coding", "ai prototyping", "python ai prototype", "ai prototype for ux", "llm assisted coding", "rapid ai prototyping", "ux designers coding", "ai driven prototypes", "functional ai  mockups", "code with llm", "python for designers", "ai product prototyping", "snowball methodology", "customer validation with code", "working ai demos"]
    task_guide: 
      - "snowball_vibe_coding.md"

## CONTENT

tasks:
- task_id: "content_audit"
    triggers: ["revisar contenido", "review content", "revisa este contenido", "review this content", "auditar contenido", "audit content", "revisar texto", "revisa este texto", "review this text", "review this message", "audit this message", "audita este mensaje"]
    task_guide: 
      - "content_audit.md"

## GENERAL PRODUCT DESIGN KNOWLEDGE

tasks:
 - task_id: "cognitive_biases"
  triggers: ["bias", "cognitive bias", "cognitive biases", "sesgo cognitivo", "sesgos cognitivos", "anchoring", "anchoring bias", "sesgo de anclaje", "availability heuristic", "availability bias", "heurística de disponibilidad", "sesgo de disponibilidad", "representativeness heuristic", "heurística de representatividad", "affect heuristic", "heurística del afecto", "confirmation bias", "sesgo de confirmación", "belief bias", "sesgo de creencia", "selection bias", "sesgo de selección", "sampling bias", "sesgo de muestreo", "survivorship bias", "sesgo de supervivencia", "base rate neglect", "base rate fallacy", "negligencia de la tasa base", "falacia de la tasa base", "conjunction fallacy", "falacia de la conjunción", "gambler's fallacy", "falacia del jugador", "hot hand fallacy", "falacia de la mano caliente", "law of small numbers", "ley de los números pequeños", "regression to the mean", "regresión a la media", "hindsight bias", "sesgo retrospectivo", "sesgo a posteriori", "outcome bias", "sesgo del resultado", "overconfidence effect", "exceso de confianza", "efecto de exceso de confianza", "optimism bias", "sesgo de optimismo", "pessimism bias", "sesgo de pesimismo", "planning fallacy", "falacia de planificación", "present bias", "sesgo del presente", "hyperbolic discounting", "descuento hiperbólico", "projection bias", "sesgo de proyección", "empathy gap", "brecha de empatía", "loss aversion", "aversión a la pérdida", "endowment effect", "efecto dotación", "status quo bias", "sesgo del statu quo", "sunk cost fallacy", "falacia del costo hundido", "escalation of commitment", "escalada de compromiso", "default effect", "efecto por defecto", "default bias", "sesgo del predeterminado", "framing effect", "efecto marco", "efecto de encuadre", "decoy effect", "attraction effect", "efecto señuelo", "dominancia asimétrica", "asimetría de dominancia", "compromise effect", "efecto compromiso", "scarcity effect", "heuristic of scarcity", "efecto de escasez", "ambiguity effect", "aversión a la ambigüedad", "efecto de ambigüedad", "zero-risk bias", "sesgo de riesgo cero", "risk compensation", "efecto Peltzman", "compensación de riesgo", "halo effect", "efecto halo", "horn effect", "efecto diablo"]
  materials: 
     - "cognitive_biases.md"

  - task_id: "b2b_design"
    triggers: ["B2B design", "designing for B2B", "enterprise design", "diseño B2B"]
    task_guide:_ 
     - "b2b_design.md"

 - task_id: "economics_for_designers"
    triggers: ["economics", "economy", "economic fundamentals", "fundamentos económicos", "value creation", "creación de valor", "incentives", "incentivos", "opportunity cost", "costo de oportunidad", "time value of money", "valor temporal del dinero", "law of supply and demand", "ley de oferta y demanda", "zero marginal cost", "costo marginal cero", "network effects", "efectos de red", "economies of scale", "economías de escala", "diseconomies of scale", "deseconomías de escala", "economies of scope", "economías de alcance", "veblen goods", "bienes veblen", "invisible hand", "mano invisible", "behavioral economics", "economía conductual", "choice architecture", "arquitectura de elección", "nudge", "empujón", "default", "defaults", "status quo bias", "sesgo del statu quo", "default effect", "efecto por defecto", "anchoring", "anchoring bias", "sesgo de anclaje", "friction costs", "costes de fricción", "friction", "fricción", "good friction", "fricción positiva", "social proof", "prueba social", "ostrich effect", "efecto avestruz", "two systems of thinking", "system 1", "system 2", "dos sistemas de pensamiento", "fast thinking", "pensamiento rápido", "slow thinking", "pensamiento lento", "create model", "modelo CREATE", "cue", "señal", "reaction", "reacción", "evaluation", "evaluación", "ability", "habilidad", "timing", "tiempo", "experience", "experiencia", "loss aversion", "aversión a la pérdida", "progress incentives", "incentivos de progreso", "reward design", "diseño de recompensas", "scarcity effect", "efecto de escasez", "scarcity heuristic", "heurística de escasez", "framing effect", "efecto de encuadre", "efecto marco", "decoy effect", "efecto señuelo", "attraction effect", "efecto de atracción", "compromise effect", "efecto compromiso"]
    task_guide:_ 
     - "economics_for_designers.md"