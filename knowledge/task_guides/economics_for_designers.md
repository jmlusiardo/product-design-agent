# Economics for Designers

A retrieval-friendly guide to applying economic and behavioral principles in product and UX design.

---

## Economic Fundamentals (from the attached "Economic Fundamentals" file)

### Economies of Scale
- **Definition**: When production volume increases, the cost per unit decreases. In software, more customers mean feature costs are spread, reducing per-customer cost.
- **Design Insight**: Build reusable components and scalable systems—every new feature or asset should benefit multiple contexts.
- **Risk**: Assuming scale always helps—coordination overhead can reverse the benefit.

### Diseconomies of Scale
- **Definition**: When a company gets too big, costs rise due to coordination/management complexity.
- **Design Insight**: Overly complex design systems or bloated workflows slow down delivery.
- **Metric**: Design cycle time per feature vs. team size.

### Opportunity Costs
- **Definition**: The value of the next-best alternative forgone when making a choice.
- **Design Insight**: Every added field, flow, or experiment means not doing something else. Ask “what are we not building if we build this?”
- **Metric**: % of roadmap tied to high-value outcomes.

### Time Value of Money (TVoM)
- **Definition**: Money (and value) today is worth more than tomorrow because it can generate returns sooner.
- **Design Insight**: Reduce time-to-value in onboarding and flows. Bring forward the “aha” moment.
- **Metric**: Time-to-first-value, week-1 retention.

### Law of Supply and Demand
- **Definition**: Price adjusts based on scarcity vs. demand.
- **Design Insight**: Scarcity cues (limited stock, waitlists) influence user behavior, but must remain credible.
- **Risk**: Manipulative scarcity (fake counters) erodes trust.

### Zero Marginal Cost of Production
- **Definition**: Once a digital product is made, extra copies cost nearly nothing.
- **Design Insight**: Favor self-serve scaling: templates, automations, or generative tools.
- **Metric**: Active usage growth vs. marginal delivery cost.

### Economies of Scope
- **Definition**: Cheaper to produce multiple related things together (shared infra, shared tools).
- **Design Insight**: Use shared design tokens, UI kits, or frameworks across products.
- **Metric**: % component/library reuse.

### Network Effects
- **Definition**: Product value increases as more people use it.
- **Design Insight**: Design invitation loops, reciprocity features, and interoperability.
- **Metric**: Invite rate, cross-side matches, K-factor.

### Veblen Goods
- **Definition**: Higher price increases demand when used as a status signal.
- **Design Insight**: Premium design should feel premium—craft, exclusivity, responsiveness.
- **Risk**: Price signaling without quality backfires.

### The Invisible Hand
- **Definition**: Markets self-regulate as users select better solutions, poor ones drop out.
- **Design Insight**: Shorten feedback loops so user preference shapes product evolution quickly.
- **Metric**: Iteration speed, user adoption vs. churn.

---

## Behavioral Economics & Choice Architecture (from Bridgeable, Bootcamp, UX Planet)

Behavioral economics explains how people actually make decisions—not as rational optimizers, but as humans relying on shortcuts, context, and emotions. For designers, the lesson is: **how you frame, structure, and time information matters as much as the content itself.**

### Choice Architecture (6 Basics)

1. **Incentives**  
   - **Principle**: People respond to perceived costs/benefits, not just logical ones.  
   - **Design Examples**:  
     - Duolingo shows “streaks” (loss aversion + progress incentives).  
     - Free shipping above a threshold nudges larger baskets.  
   - **Tip**: Always check whether the incentive aligns with long-term outcomes (avoid vanity incentives like empty “points” that lose value).  

2. **Understand Mappings**  
   - **Principle**: People struggle to translate abstract values (calories, kilobytes, APR) into real meaning.  
   - **Design Examples**:  
     - Health apps show “walking 30 min” instead of “burn 200 kcal.”  
     - Netflix highlights “hours saved” by skipping intros.  
   - **Tip**: Convert technical metrics into **intuitive, human-friendly frames.**  

3. **Defaults**  
   - **Principle**: Most people stick with the pre-selected option (status quo bias).  
   - **Design Examples**:  
     - Opt-out organ donation increases participation vs opt-in systems.  
     - Privacy settings: Apple defaults to “Ask App Not to Track.”  
   - **Tip**: Use defaults to protect users (privacy, safety, error prevention), not to exploit them.  

4. **Give Feedback**  
   - **Principle**: People need to understand the effect of their actions.  
   - **Design Examples**:  
     - Real-time error validation in forms (“invalid email format”).  
     - Progressive goal trackers (LinkedIn profile completeness).  
   - **Tip**: Feedback should be **immediate, specific, and actionable.**  

5. **Expect Error**  
   - **Principle**: Humans make mistakes—systems should anticipate and allow recovery.  
   - **Design Examples**:  
     - Gmail attachment reminder if you mention “attached” but forgot the file.  
     - Undo in Google Docs, or “recently deleted” in iOS photos.  
   - **Tip**: Never design flows that punish users irreversibly for predictable mistakes.  

6. **Structure Complex Choices**  
   - **Principle**: Too many options cause decision paralysis; how you group or stage them matters.  
   - **Design Examples**:  
     - Insurance websites showing 3 simplified tiers (Basic, Plus, Premium).  
     - Netflix categories (Action, Comedy, Trending) instead of one long list.  
   - **Tip**: Limit comparisons to a few meaningful attributes; chunk information into digestible steps.  

### Defaults

- **What**: People prefer not to change pre-set options.  
- **Examples in Design**:  
  - Gmail automatically saves drafts (no effort needed).  
  - Default notification toggles in apps—if respectful, they ensure users don’t miss important alerts.  
- **Designer Move**:  
  - Pick defaults that reduce harm (opt-in encryption, muted marketing).  
  - Always make opt-out **clear and accessible**.  

### Anchoring

- **What**: Initial numbers or references bias subsequent decisions.  
- **Examples in Design**:  
  - E-commerce showing a crossed-out “original price” makes discounts seem larger.  
  - Subscription services presenting the “Most Popular” plan first as anchor.  
- **Designer Move**:  
  - Provide **honest anchors** (median price, realistic delivery windows).  
  - Avoid inflated anchors (fake “was $199, now $49”), which erode trust.  

### Friction Costs

- **What**: Small barriers deter or delay action; but intentional friction can protect users.  
- **Examples in Design**:  
  - One-click checkout removes friction, boosting conversions.  
  - Adding password confirmation before deleting an account is *good friction*.  
- **Designer Move**:  
  - Audit flows for **unnecessary friction** (redundant fields, unclear CTAs).  
  - Add friction selectively where irreversible harm is possible (data deletion, financial transactions).  

### Social Proof

- **What**: People rely on others’ behavior when uncertain.  
- **Examples in Design**:  
  - “Join 5 million users already saving money with this app.”  
  - Ratings & reviews on Amazon; “friends who use this app” on Spotify.  
- **Designer Move**:  
  - Frame usage stats in ways that encourage adoption (“82% of similar users…”).  
  - Beware “boomerang effect”: showing low numbers can discourage (“Only 3 people signed up”).  

### Ostrich Effect

- **What**: Users avoid negative or stressful information.  
- **Examples in Design**:  
  - Finance apps: users may avoid opening them when markets are down.  
  - Fitness apps: people stop logging when they break their diet.  
- **Designer Move**:  
  - Provide **gentle nudges** instead of guilt (“Ready to get back on track?”).  
  - Offer positive framing: progress compared to their *own* past, not an unrealistic ideal.  

### Two Types of Thinking (System 1 vs. System 2)

- **System 1 (fast, intuitive)**  
  - Example: one-tap “like” button; swipe to archive email.  
  - Design for: low-stakes, frequent interactions → simple, immediate.  

- **System 2 (slow, reflective)**  
  - Example: comparing health insurance plans, confirming large purchases.  
  - Design for: high-stakes decisions → structured options, transparent trade-offs, deliberate pacing.  

- **Designer Move**: Match flow to the system:  
  - **Encourage System 1** for repeatable, simple tasks.  
  - **Trigger System 2** for important or costly decisions (with explanations, comparisons, confirmations).  

### CREATE Model (Decision Process)

1. **Cue** – the trigger: timely reminders (e.g., Headspace sends meditation nudges at chosen time).  
2. **Reaction** – emotional resonance: friendly copy, relatable visuals.  
3. **Evaluation** – clear framing: show pros/cons side by side.  
4. **Ability** – ensure action is feasible: reduce requirements (auto-fill, integrations).  
5. **Timing** – align with urgency/decay: limited-time offers, contextual prompts.  
6. **Experience** – close loop: confirmations, progress dashboards, “celebratory” micro-interactions.  

**Designer Move**: Use CREATE as a checklist in usability testing—map breakdowns to the specific stage (e.g., wrong cue, poor feedback, timing mismatch).  

---

## Suggested Titles
- **“Economics for Designers: Fundamentals & Behavioral Playbook”**  
- **“Design x Economics: How Value, Incentives & Behavior Interact”**

---

## #references
- Anderson, J. [The Economics of Good Design](https://medium.com/design-bootcamp/the-economics-of-good-design-2eea6de51d34)  
- Bridgeable. [The Top 5 Behavioural Economics Principles for Designers](https://www.bridgeable.com/ideas/the-top-5-behavioural-economics-principles-for-designers/)  
- Dulenko, V. [Design, Economics and Two Types of Thinking](https://uxplanet.org/design-economics-and-two-types-of-thinking-73cccaaf7a1b)