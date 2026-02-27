# Task Router Index

> **Usage**: Extract lowercase nouns/verbs from the normalized query. Match against signals below (AND logic for multi-word clusters). Stem matching supported (e.g., "prioritize" matches `prioritiz`).

## Signal Map
```
# ── ONBOARDING ──────────────────────────────────────────
how + does + this + work          → agent_onboarding_guide
what + can + you + do             → agent_onboarding_guide
help + getting + started          → agent_onboarding_guide
onboarding + agent                → agent_onboarding_guide
onboarding + designer             → onboarding_designers
onboarding + lead                 → onboarding_design_leads

# ── DISCOVERY ───────────────────────────────────────────
journey + map                     → journey_mapping
journey + current + state         → journey_mapping
empathy + map                     → empathy_mapping
mental + model                    → mental_modeling
critical + path                   → critical_path
problem + statement               → writing_statements
user + stor                       → writing_statements
job + stor                        → writing_statements
how + might + we                  → writing_statements
hypothesis                        → writing_statements
assumption + defin                → define_assumptions
assumption + valid                → define_assumptions
design + pitch                    → design_pitch
event + storm                     → event_storming_workshop
event + storming + workshop       → event_storming_workshop
domain + event                    → event_storming_workshop
initiative + canvas               → initiative_canvas
story + map                       → user_story_mapping
story + mapping                   → user_story_mapping
map + user + stor                 → user_story_mapping
backlog + map                     → user_story_mapping
visualize + backlog               → user_story_mapping

# ── USER RESEARCH ───────────────────────────────────────
persona + create                  → user_personas
persona + develop                 → user_personas
persona + valid                   → user_personas
interview + user                  → user_interviews
interview + stakeholder           → stakeholder_interviews
survey + design                   → survey_design
survey + create                   → survey_design
questionnaire                     → survey_design
card + sort                       → card_sorting
tree + test                       → tree_testing
usability + test + plan           → usability_test_planning
usability + test + moderate       → usability_test_moderation
usability + test + facilitat      → usability_test_moderation
usability + test + report         → usability_test_reporting
usability + test + finding        → usability_test_reporting
usability + test                  → usability_test_planning
test + prototype                  → usability_test_planning
test + user                       → usability_test_planning
audit + ux                        → ux_audit
audit + heuristic                 → heuristic_evaluation
heuristic + evaluat               → heuristic_evaluation
affinity + diagram                → affinity_diagramming
contextual + inquiry              → contextual_inquiry
field + study                     → contextual_inquiry
# NOTE: content_testing signal removed — no backing task in tasks.yaml (TODO: add task or restore signal)
research + no + user              → ux_research_without_users
research + without + user         → ux_research_without_users
first + click                     → first_click_testing
funnel + analysis                 → funnel_analysis
ab + test                         → ab_testing
a/b + test                        → ab_testing
data + analysis                   → data_analysis
analytics + review                → data_analysis
conversion + optimiz              → conversion_optimization
cognitive + bias                  → cognitive_biases
recruit + user                    → recruiting_users
recruit + participant             → recruiting_users

# ── STRATEGY ────────────────────────────────────────────
business + model                  → business_model
mvp + defin                       → mvp_definition
minimum + viable                  → mvp_definition
prioritiz                         → prioritization
value + proposition               → value_proposition
okr                               → okrs
kpi + metric                      → kpi_metrics
kpi + defin                       → kpi_metrics
roadmap                           → product_roadmap
competitive + analysis            → competitive_analysis
competitor + analysis             → competitive_analysis
brainstorm                        → brainstorming
ideat                             → brainstorming
product + requirement             → product_requirements_document
prd                               → product_requirements_document
project + plan                    → project_planning
agile + ux                        → agile_lean_ux_frameworks
lean + ux                         → agile_lean_ux_frameworks
sprint + ux                       → agile_lean_ux_frameworks
ux + agile                        → agile_lean_ux_frameworks
lean + canvas                     → agile_lean_ux_frameworks

# ── PROJECT FRAMING ─────────────────────────────────────
kickoff + meeting                 → kickoff_meeting
project + kickoff                 → kickoff_meeting
kickoff + facilitat               → kickoff_meeting
project + type                    → project_type_strategy
project + strateg                 → project_type_strategy
ux + strateg + project            → project_type_strategy
design + approach + select        → project_type_strategy

# ── DESIGN & PROTOTYPING ───────────────────────────────
wireframe                         → wireframing
prototype + prompt                → prototype_prompt_creation
prototype + spec                  → prototype_prompt_creation
prototype + creat                 → prototype_prompt_creation
design + system + audit           → design_system_audit
design + token                    → design_token_naming
color + palette                   → color_palette_generation
icon + design                     → creating_icons
icon + creat                      → creating_icons
icon + rule                       → creating_icons
icon + principl                   → creating_icons
icon + family                     → icon_family_specification
icon + json                       → icon_family_specification
icon + spec                       → icon_family_specification
icon + typeface                   → matching_icons_typefaces
icon + font + match               → matching_icons_typefaces
icon + typograph                  → matching_icons_typefaces
typeface + icon + pair            → matching_icons_typefaces
token + audit                     → token_audit
token + lint                      → token_audit
token + consist                   → token_audit
token + health                    → token_audit
responsive + design               → responsive_design
interaction + design              → interaction_design
micro + interaction               → micro_interactions
component + document              → component_documentation
component + spec                  → component_documentation
accessibility + audit             → accessibility_audit
accessibility + review            → accessibility_audit
wcag                              → accessibility_audit
a11y + audit                      → accessibility_audit
a11y + check                      → accessibility_audit
wcag + complian                   → accessibility_audit
screen + reader + test            → accessibility_audit
keyboard + navig + check          → accessibility_audit
contrast + check                  → accessibility_audit
is + this + accessibl             → accessibility_audit
inclus + design + audit           → accessibility_audit
disabilit + review                → accessibility_audit
accesib + audit                   → accessibility_audit
decision + tree                   → ui_component_decision_tree
component + select                → ui_component_decision_tree
which + component                 → ui_component_decision_tree
ui + component + when             → ui_component_decision_tree
radio + checkbox + dropdown       → ui_component_decision_tree
modal + drawer + dialog           → ui_component_decision_tree
toast + banner + alert            → ui_component_decision_tree
loading + pattern                 → ui_component_decision_tree
button + hierarch                 → ui_component_decision_tree

# ── CONTENT & UX WRITING ───────────────────────────────
content + audit                   → content_audit
content + inventory               → content_inventory
content + catalog                 → content_inventory
writing + task                    → writing_tasks
ux + writing + review             → ux_writing_review
tone + voice + review             → ux_writing_review
microcopy + optimiz               → microcopy_optimization
error + message + writ            → microcopy_optimization
empty + state + copy              → microcopy_optimization
cta + copy                        → microcopy_optimization

# ── AI & PROMPTING ──────────────────────────────────────
writing + prompt                  → writing_prompts
prompt + engineer                 → writing_prompts
prompt + minif                    → prompt_minification
prompt + compress                 → prompt_minification
vibe + cod                        → snowball_vibe_coding
snowball + cod                    → snowball_vibe_coding
style + spec + json               → style_spec_json_builder
extract + style                   → style_spec_json_builder
image + style + analysis          → style_spec_json_builder
ai + image + prompt               → writing_ai_image_prompts
image + generat + prompt          → writing_ai_image_prompts

# ── COLLABORATION ───────────────────────────────────────
stakeholder + manage              → stakeholder_management
stakeholder + map                 → stakeholder_management
conflict + resolv                 → conflict_resolution
difficult + conversation          → conflict_resolution
meeting + facilitat               → meeting_facilitation
meeting + design                  → meeting_facilitation
workshop + design                 → workshop_design
workshop + facilitat              → workshop_design
design + critique                 → design_critique
design + review                   → design_critique
executive + present               → executive_presentation
present + leadership              → executive_presentation
exec + deck                       → executive_presentation
present + c-suite                 → executive_presentation
executive + summary               → executive_summary
exec + update                     → executive_summary
status + update + exec            → executive_summary
one + page + summary              → executive_summary

# ── LEADERSHIP ──────────────────────────────────────────
team + manage                     → team_management
team + structur                   → team_management
ux + culture                      → boost_ux_culture
ux + maturity                     → boost_ux_culture
hiring + designer                 → hiring_designers
recruit + designer                → hiring_designers
interview + design + candidat     → hiring_designers
b2b + design                      → b2b_design
enterprise + ux                   → b2b_design

# ── DESIGN SYSTEMS & VISUAL  ────────────────────────────
handoff + spec                    → design_handoff_spec
handoff + document                → design_handoff_spec
dev + spec                        → design_handoff_spec
developer + documentation         → design_handoff_spec
design + spec + engineer          → design_handoff_spec
prepare + implement               → design_handoff_spec
ready + development               → design_handoff_spec
what + give + developer           → design_handoff_spec
design + debt                     → design_debt_registry
ux + debt                         → design_debt_registry
debt + registr                    → design_debt_registry
debt + backlog                    → design_debt_registry
design + inconsistenc             → design_debt_registry
design + cleanup                  → design_debt_registry
legacy + design                   → design_debt_registry
design + system + drift           → design_debt_registry
design + system + health          → design_debt_registry
token + misuse                    → design_debt_registry
accessibility + debt              → design_debt_registry
design + remediat                 → design_debt_registry
```

## Disambiguation Rules

When signal clusters match 2+ tasks, apply these tiebreakers:

| Ambiguous signal | Default task | If query also contains... | Route to instead |
|---|---|---|---|
| `usability + test` | `usability_test_planning` | moderate, facilitate, session | `usability_test_moderation` |
| | | report, findings, analysis, results | `usability_test_reporting` |
| `audit` | `ux_audit` | heuristic, nielsen | `heuristic_evaluation` |
| | | design + system | `design_system_audit` |
| | | accessibility, wcag | `accessibility_audit` |
| | | content | `content_audit` |
| | | token, naming | `token_audit` |
| `onboarding` | `agent_onboarding_guide` | designer, new + hire | `onboarding_designers` |
| | | lead, manager | `onboarding_design_leads` |
| `research + user` | `user_interviews` | no + access, without | `ux_research_without_users` |
| | | survey, questionnaire | `survey_design` |
| | | observe, field, context | `contextual_inquiry` |
| `icon` | `creating_icons` | json, spec, family, system | `icon_family_specification` |
| | | typeface, font, typograph | `matching_icons_typefaces` |
| `prototype` | `prototype_prompt_creation` | test, usability | `usability_test_planning` |
| `writing` | `writing_tasks` | prompt, ai | `writing_prompts` |
| | | statement, problem, hypothesis | `writing_statements` |
| | | ux, microcopy, interface | `ux_writing_review` |
| `content` | `content_audit` | inventory, catalog | `content_inventory` |
| `executive` | `executive_presentation` | summary, update, status | `executive_summary` |
| `agile` | `agile_lean_ux_frameworks` | kickoff, charter | `kickoff_meeting` |
| `project` | `project_planning` | type, classify, approach | `project_type_strategy` |
| | | kickoff, start, launch | `kickoff_meeting` |
| `user + stor` | `writing_statements` | map, mapping, backlog | `user_story_mapping` |
| `debt` | `design_debt_registry` | token, naming | `token_audit` |
| | | ux, heuristic | `ux_audit` |