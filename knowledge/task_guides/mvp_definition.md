# Build the Right Thing, Right Now: A Practical Guide to POC, Prototype, MVP, MVE/MUE, MLP & MAP

> **Executive Summary** — This guide helps product teams pick the *right* build artifact for their stage: **POC**, **Prototype**, **MVP**, **MUE/MVE**, **MLP**, or **MAP**. It explains when to use each, the minimum bar for quality and experience, and concrete best practices and checklists. Use it alongside your discovery work and **defer prioritization details to `prioritization.md`**.

## Overview & Objectives
- **Purpose:** Provide a clear decision path to choose between POC, Prototype, MVP, MUE/MVE, MLP, and MAP; define minimum quality bars and practices for each.
- **Scope:** Early to mid-stage product efforts (0→1 features/products); excludes detailed prioritization frameworks (see `prioritization.md`).
- **Audience:** Founders, PMs, Designers, Tech Leads.
- **Success Criteria / KPIs:** Faster cycle times to validated learning; improved activation/retention through a defined **minimum experience**; fewer misfired builds.

## Concept Map (Quick Definitions)
- **POC (Proof of Concept):** Narrow, internal test to **de-risk feasibility** of a technology/approach. Go/No-Go outcome. (Verma)
- **Prototype:** Visual/interactive model to **test UX & flows** before full build; can be low→high fidelity. (Verma)
- **MVP (Minimum Viable Product):** Working product with **core functionality** to validate problem–solution fit with real users. (Pessan; Userpilot)
- **MUE / MUP (Minimum Usable Experience/Product):** **Do few things well** with consistent quality—avoid using “minimum” as an excuse for poor UX; uphold a baseline bar. (Notion)
- **MVE (Minimum Viable Experience):** **360° experience** (find/try/buy/use/support) that meets expectations from day one; complements MVP. (Userpilot; Product School; Moatazsamy)
- **MLP (Minimum Lovable Product):** MVP + touches that spark **delight/love** to seed loyalty. (Userpilot)
- **MAP (Minimum Awesome Product):** In competitive spaces, launch with **well-designed, polished** experience meeting modern expectations. (Productea)

---

## Preparation
- **Research & Planning:**
  - Validate **problem & audience** before building anything. Consider Lean/Problem interviews and offer tests. (YouTube ref)
  - Decide **unknowns to retire** (feasibility vs usability vs market).
  - Define **“minimum”** per brand/context—startups vs established brands have different bars. (Product School; Userpilot)
- **Checklist**
  - - [ ] Problem & segment validated (interviews/signals/offer tests)
  - - [ ] Primary unknown classified: **Feasibility**, **Experience**, or **Market fit**
  - - [ ] Success metrics/hypotheses defined (per artifact below)
  - - [ ] Non-goals list created (“what we won’t do now”) (Notion)
  - - [ ] Baseline **experience bar** agreed (MUE/MVE checklist ready)
  - - [ ] Prioritization mechanics → **see `prioritization.md`**

---

## Choosing What to Build (Decision Flow)
1) **Is core feasibility unknown?**  
   → **POC** (smallest tech experiment to prove it can work). (Verma)

2) **Is usability/interaction unclear but tech is feasible?**  
   → **Prototype** (low/high-fidelity to test tasks & flows). (Verma)

3) **Do you need market signal on core value with real users?**  
   → **MVP** (ship core value). Layer a **minimum experience** (MUE/MVE). (Pessan; Userpilot)

4) **Crowded competitive space or high expectation baseline?**  
   → Raise bar to **MLP/MAP** (polish & delighters at launch). (Productea; Userpilot)

5) **Regardless of path:**  
   - Maintain **MUE** (usability baseline) and **MVE** (end-to-end basics: find/try/buy/support). (Notion; ProductPlan)

> **Anti-pattern:** Don’t “start with an MVP” by default—start with **problem/offer tests** and pick the smallest artifact that retires your riskiest unknown. (YouTube ref)

---

## Main Flow / Process (Time-Boxed)
### 1) Align on Risk & Artifact (30–60 min)
- Clarify primary unknown; pick **POC/Prototype/MVP** and **MUE/MVE** bar.
- Set hypotheses & decision criteria (Go/No-Go, success metric).

### 2) Scope the Artifact (60–120 min)
- Write **non-goals**; define smallest slice to learn.
- Map **user journey** touchpoints you’ll cover to hit **MVE** basics.

### 3) Build & Test (1–3 sprints; time varies by artifact)
- **POC:** isolate tech spike; collect perf/feasibility data.
- **Prototype:** recruit target users; run task-based tests.
- **MVP (+MUE/MVE):** ship to early adopters; ensure onboarding/support basics.

### 4) Measure & Decide (30–60 min per cycle)
- Review metrics (see per-artifact sections).
- Decide **iterate / escalate / pivot / stop**.

---

## Best Practices by Artifact

### POC (Proof of Concept)
- **Use when:** Feasibility is the main risk. (Verma)
- **Scope:** One core hypothesis (e.g., latency <X ms; model accuracy >Y%).
- **Success Metric:** **Go/No-Go** on feasibility; documented constraints.
- **Do:**
  - - [ ] Isolate the riskiest assumption in a sandbox.
  - - [ ] Keep throwaway code; optimize later.
  - - [ ] Capture limits (scale, cost, ops).
- **Avoid:** Feature creep; user-facing polish (not needed yet).

### Prototype
- **Use when:** UX, flows, or IA are uncertain. (Verma)
- **Fidelity:** Start low (paper/wireframe) → high (clickable) as needed.
- **Success Metric:** Task success, errors, qualitative insights.
- **Do:**
  - - [ ] Define 3–5 critical tasks to test.
  - - [ ] Recruit representative users; think-aloud sessions.
  - - [ ] Capture **UMUX/SUS** or simple post-task ratings for perceived usability.  
- **Avoid:** Building full backend; over-investing before signals.

### MVP (Minimum Viable Product)
- **Use when:** Need **real-user** validation of core value. (Pessan; Userpilot)
- **Success Metric:** Activation %, retention proxy, learning velocity.
- **Do:**
  - - [ ] Ship **one clear value path** end-to-end.
  - - [ ] Define activation event & **time-to-value (TTV)** target. (Userpilot)
  - - [ ] Instrument feedback loops (qual + quant).
  - - [ ] Pair with **MUE/MVE** baseline (below).
- **Avoid:** Over-stuffing features; conflating MVP with “low quality”.

### MUE / MVE (Baseline Experience for Anything User-Facing)
- **Use when:** Always, once users touch it. (Notion; Userpilot; ProductPlan)
- **Scope:** 360° basics — **Find → Try → Buy/Onboard → Use → Get Help**.
- **Success Metrics:** **TTV**, **CES (effort)**, **NPS**, early **retention**. (Userpilot)
- **Do:**
  - - [ ] **Do few things well**; consistent quality across shipped features. (Notion)
  - - [ ] Minimum viable onboarding (guided activation, tooltips/walkthroughs). (Userpilot)
  - - [ ] Make support easy (help email/chat, basic docs). (ProductPlan)
  - - [ ] Set expectations in marketing/UX copy (no surprises).
- **Avoid:** Using “minimum” as a reason for janky flows or confusing UI.

### MLP (Minimum Lovable Product)
- **Use when:** You need an emotional hook early (brand/loyalty leverage).
- **Scope:** Add small **delighters** without bloating scope. (Userpilot)
- **Success Metric:** Qual signals (love/word-of-mouth), uplift in activation/retention.

### MAP (Minimum Awesome Product)
- **Use when:** Competing against polished incumbents—users expect more. (Productea)
- **Scope:** Less features, **well designed & performant**; matches modern patterns.
- **Success Metric:** Early conversion/retention in competitive comps; “quality” feedback.

---

## Templates / Canvases / Frameworks

### 1) POC One-Pager
- **Hypothesis:** _e.g., “We can generate summaries <500ms @P95.”_
- **Method:** dataset/stub, environment, constraints.
- **Exit Criteria:** Go/No-Go thresholds; follow-up risks.

### 2) Prototype Test Plan
- **Users:** segment, N=5–8.
- **Tasks:** 3–5 critical tasks; success criteria.
- **Measures:** errors, completion time, UMUX/SUS quick survey; notes.

### 3) MVP Experiment Canvas (summary)
- **Problem & Segment**, **Value Path**, **Hypotheses**, **Activation Event**, **Metrics**, **Risks/Non-goals**, **Rollout & Feedback**.  
  _Tip:_ Use an MVP canvas (see References) and pair with a simple launch checklist.

### 4) MUE/MVE Baseline Checklist
- - [ ] **Find/Try:** landing page clarity; simple signup; privacy basics
- - [ ] **Onboard:** first-run guidance; sample data/demo; TTV target
- - [ ] **Use:** empty-state guidance; helpful errors; accessible basics
- - [ ] **Help:** visible help entry; contact within 1 click; basic FAQ
- - [ ] **Feedback:** in-app survey/NPS; issue capture
- - [ ] **Consistency:** terminology, tone, and UI patterns align

---

## Aftermath / Follow-ups
- **POC → Prototype?** If feasible, resolve UX unknowns next.
- **Prototype → MVP?** When tasks succeed and desirability is clear.
- **MVP → MLP/MAP?** When market validates value and competition raises experience bar.
- **Experience Debt Log:** Track MUE/MVE gaps to close each sprint.
- **Prioritization:** For trade-offs and sequencing, **see `prioritization.md`**.

---

## Best Practices & Pitfalls
- **Do:**
  - Treat **MUE/MVE** as a non-negotiable bar once users touch it.
  - Keep artifacts **small & purpose-built**; retire the riskiest unknown.
  - Maintain **non-goals** to protect scope.
  - Instrument **activation, TTV, CES, NPS, retention** early.
- **Avoid:**
  - Equating MVP with **low quality**.
  - Shipping to users without **onboarding/support basics**.
  - Skipping problem validation—**don’t start by building an MVP**.

---

## Tools & Resources
- **MVE/MUE:** Onboarding tooltips/walkthroughs, lightweight help center, NPS/CES surveys.
- **Discovery:** Interview scripts, offer/landing tests, analytics for **activation/TTV**.
- **Canvases:** MVP Experiment Canvas; Lean-style one-pagers for POC/Prototype.

---

## FAQ / Quick Answers
- **POC vs Prototype?** POC proves **feasibility**; Prototype tests **usability/UX**. (Verma)
- **MVP vs MVE?** MVP = **product** with core value; MVE = **experience** baseline across the journey; they should be built in tandem. (Userpilot; Product School)
- **When MLP/MAP?** When experience differentiation is needed at launch (crowded markets, high expectations). (Productea; Userpilot)
- **What’s “minimum” here?** Contextual—brand maturity and market norms set the bar. (Product School)

---

## References
- MVP, POC, or Prototype — Rohit Verma (Medium): https://rohitverma141.medium.com/mvp-poc-or-prototype-which-one-should-you-choose-for-your-next-product-0997b88e428b
- El MVP ha muerto, larga vida al MAP — Productea (Medium): https://medium.com/productea/el-mvp-ha-muerto-larga-vida-al-map-596987f37de4
- Unveiling the Power of MVE — Moatazsamy (Medium): https://medium.com/@moatazsamy122/unveiling-the-power-of-minimum-viable-experience-mve-657b8a153532
- Minimum Viable Experience (MVE): What PMs Should Know — Userpilot: https://userpilot.com/blog/minimum-viable-experience-mve/
- MVP or MVE: Decoding the Right Approach — Julio Pessan (Medium): https://medium.com/@julio.pessan.pessan/mvp-or-mve-decoding-the-right-approach-for-startups-a20b884d804d
- Don’t Start With an MVP (Minimum Viable Product) — YouTube: https://www.youtube.com/watch?v=VBr0TI67qwk