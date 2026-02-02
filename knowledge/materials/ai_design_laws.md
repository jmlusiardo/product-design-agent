# Guide to 12 AI Design Laws

A practical framework for designing trustworthy, usable AI experiences. Each law addresses a core tension in human-AI interaction and provides actionable guidance for product teams.

**Source**: @felixleezd

---

## 1. Black Box Law

> If users don't understand AI, they won't trust it. Show reasoning behind AI outputs to build credibility and encourage trust, even with small transparency cues.

### How-to
Implement confidence scores, "show steps" buttons, or tooltips explaining recommendations directly in the UI.

### Examples

| Context | Implementation |
|---------|----------------|
| **E-commerce product search** | Display "Why these results?" link showing matched attributes (e.g., "Matches: blue, cotton, under $50") |
| **Credit score apps** | Break down score factors: "Payment history (35%), credit utilization (30%)..." with visual weights |
| **Content recommendation** | Netflix-style "Because you watched X" labels beneath suggested titles |
| **Medical diagnosis tools** | Show symptom-to-condition mapping: "High match: 3/4 symptoms align with condition Y" |
| **AI writing assistants** | Grammarly's explanation popups: "This suggestion improves clarity by reducing passive voice" |
| **Fraud detection alerts** | "Flagged because: unusual location + high amount + new merchant" breakdown |
| **Job matching platforms** | Skills match percentage with breakdown: "8/10 required skills, 3/5 preferred skills" |

---

## 2. Human-in-the-Loop Law

> AI is never 100% right. Design AI tools so humans make final decisions, using override buttons, editable suggestions, and undo options.

### How-to
Always provide options for users to accept, reject, or edit AI outputs and include an undo feature.

### Examples

| Context | Implementation |
|---------|----------------|
| **AI shopping assistant** | Present product recommendations as "suggestions" with thumbs up/down and "show different options" button |
| **Email autocomplete** | Tab to accept, keep typing to ignore, easy backspace to undo accepted suggestion |
| **Automated meeting scheduling** | AI proposes times; user confirms, edits, or requests alternatives before sending invite |
| **Photo editing (auto-enhance)** | Before/after slider, intensity controls, and one-tap "Reset to original" |
| **Document summarization** | Editable summary field with "Regenerate" and "Expand section" controls |
| **Chatbot escalation** | Visible "Talk to a human" option at any point; bot acknowledges its limits |
| **Inventory reordering** | AI suggests order quantities; buyer reviews, adjusts, and approves before submission |

---

## 3. Bias Mirror Law

> AI reflects the flaws in its training data. Audit datasets and stress-test for edge cases, adding correction and review checkpoints to mitigate bias.

### How-to
Schedule regular audits and set up feedback channels to review and correct biased outputs in production.

### Examples

| Context | Implementation |
|---------|----------------|
| **Search result ranking** | Regularly audit whether certain brands/categories are over-represented; A/B test ranking fairness |
| **Hiring tools** | Test with synthetic profiles varying only protected attributes; monitor demographic outcome distributions |
| **Loan approval systems** | Quarterly bias audits comparing approval rates across zip codes and demographics |
| **Image recognition** | Stress-test with diverse skin tones, lighting conditions, and cultural contexts |
| **Language models** | Red-team for stereotypes; implement content filters for known bias patterns |
| **Voice assistants** | Test accent recognition accuracy across regional dialects; track and improve failure cases |
| **Product recommendations** | Monitor whether "similar users" clustering reinforces echo chambers or filter bubbles |

---

## 4. Trust Gap Law

> People are skeptical when AI makes high-stakes decisions. Start with low-stakes outputs and build trust gradually, adding more proof and reliability in high-impact areas.

### How-to
Deploy AI first in safe, low-stakes situations and add context and disclaimers for high-stakes scenarios.

### Examples

| Context | Implementation |
|---------|----------------|
| **AI shopping assistant** | Start with "inspiration" queries (outfit ideas) before handling complex purchases (appliances, electronics) |
| **Healthcare AI** | Begin with appointment scheduling and symptom logging; escalate to triage only after trust is established |
| **Financial planning** | First show spending insights, then savings suggestions, then investment recommendations (progressive stakes) |
| **Autonomous vehicles** | Lane-keeping assist → adaptive cruise → highway autopilot → full self-driving (graduated autonomy) |
| **Legal document review** | AI highlights potential issues; lawyer reviews. Don't auto-submit legal filings. |
| **Customer service bots** | Handle FAQs and order status first; route complaints and refunds to humans initially |
| **Code generation** | Suggest autocompletions before generating entire functions; let users build confidence incrementally |

---

## 5. Explainability Law

> Clarity beats cleverness for AI outputs. Provide human-readable signals and direct explanations to ensure users understand why AI made a certain decision.

### How-to
Add tooltips ("Why this?") or a "show steps" button next to every major AI recommendation.

### Examples

| Context | Implementation |
|---------|----------------|
| **Product recommendations** | "Recommended because: similar shoppers bought this + matches your size preference + highly rated" |
| **Spam filters** | "Marked as spam: sender not in contacts + contains suspicious link + matches known phishing pattern" |
| **Dynamic pricing** | "Price reflects: current demand (high) + limited inventory + seasonal factor" |
| **Route optimization** | "This route chosen: 12 min faster due to traffic on alternate + avoids toll roads (your preference)" |
| **Content moderation** | "Removed because: violates community guideline #3 (hate speech) - specific phrase flagged" |
| **Insurance quotes** | Breakdown showing which factors (age, location, vehicle, history) contributed to premium calculation |
| **Search ranking** | "Top result because: exact phrase match + high purchase rate + strong reviews in your size" |

---

## 6. Co-pilot Principle

> AI is most effective as a collaborator. Frame AI as an assistant, allowing users to edit and iterate outputs collaboratively without handing over full control.

### How-to
Present AI-generated outputs as draft suggestions users can easily edit or improve.

### Examples

| Context | Implementation |
|---------|----------------|
| **AI writing tools** | Generate draft → user edits → "Improve this section" → iterate together |
| **Design tools (Figma AI)** | AI suggests layout; designer adjusts, then asks for variations on specific elements |
| **Data analysis** | AI generates initial charts and insights; analyst refines queries and visualization choices |
| **Meeting notes** | AI drafts summary; organizer edits key points and action items before sharing |
| **Product descriptions** | AI writes first draft with placeholders; merchandiser customizes voice and adds specifics |
| **Code review** | AI flags potential issues and suggests fixes; developer accepts, modifies, or dismisses each |
| **Email replies** | AI drafts response options; user selects, edits tone, adds personal touches |

---

## 7. Confidence Law

> Overconfident AI undermines trust. Teach AI to hedge and show probabilities so users see uncertainty, making mistakes feel safer and less damaging.

### How-to
Display probability ranges and use language like "It looks like..." for all uncertain results.

### Examples

| Context | Implementation |
|---------|----------------|
| **Product search intent** | "I think you're looking for running shoes (85% confident). Not quite right? Tell me more." |
| **Weather apps** | "70% chance of rain" with hourly probability graph, not just "It will rain" |
| **Medical symptom checkers** | "Possible conditions: Cold (likely), Flu (possible), COVID (less likely) - consult a doctor to confirm" |
| **Object recognition** | "This appears to be a Golden Retriever (92%)" vs. asserting breed as fact |
| **Translation tools** | Flag ambiguous phrases: "This could mean X or Y depending on context" |
| **Sentiment analysis** | "Sentiment: Likely negative (68%) - contains mixed signals" with highlighted phrases |
| **Sales forecasting** | Show prediction ranges: "Q4 revenue: $2.1M - $2.6M (80% confidence interval)" |

---

## 8. Context Window Law

> AI depends on the quality of provided context. Design structured prompts and pre-filled examples so the user gives clear input, enabling more useful AI results.

### How-to
Create templates, dropdowns, or starter prompts to guide user input for optimal AI output.

### Examples

| Context | Implementation |
|---------|----------------|
| **AI shopping assistant** | Guided questions: "What's the occasion? → Who's it for? → Budget range?" before free-form search |
| **AI image generation** | Style presets + structured fields (subject, style, mood, colors) alongside free prompt |
| **Customer support bots** | Pre-conversation form: order number, issue category, preferred resolution |
| **Resume builders** | Structured fields (role, company, dates, achievements) that feed into AI-generated descriptions |
| **Code generation** | Language selector + framework dropdown + example input/output before generating |
| **Meeting schedulers** | Duration, participant list, urgency level, and preferences collected before AI suggests times |
| **Product quizzes** | Progressive disclosure: broad preference → specific needs → constraints → personalized results |

---

## 9. Friction vs. Magic Law

> Some friction increases user trust in AI. Allow lightweight user interactions and confirmation steps; remove excessive friction but avoid making the process too effortless.

### How-to
Add quick preference questions or confirmation steps before generating important outputs.

### Examples

| Context | Implementation |
|---------|----------------|
| **One-click purchases** | Confirmation screen showing items, total, address before completing AI-suggested reorder |
| **Auto-reply suggestions** | Single tap to select, but require tap (not auto-send) for outgoing messages |
| **Smart home automation** | "Turning off all lights in 10 seconds" with cancel option vs. instant execution |
| **Document formatting** | AI applies template; shows preview with "Apply" / "Adjust" options before finalizing |
| **Subscription management** | AI suggests plan changes; requires explicit confirmation before billing changes |
| **Portfolio rebalancing** | AI recommends trades; investor reviews impact summary and confirms batch |
| **Calendar rescheduling** | AI proposes new times; user confirms before invites are sent to attendees |

---

## 10. Feedback Loop Law

> AI needs feedback to improve. Integrate visible feedback options next to outputs so users can quickly adjust and help refine future AI performance.

### How-to
Embed thumbs up/down buttons and fast correction tools right next to every AI output.

### Examples

| Context | Implementation |
|---------|----------------|
| **Search results** | "Was this helpful?" + "Hide results like this" on each result card |
| **Chatbot responses** | Thumbs up/down after each message + "This didn't answer my question" escalation |
| **Product recommendations** | "Not interested" / "More like this" buttons; "Why am I seeing this?" with correction option |
| **Voice transcription** | Inline correction interface that improves speaker-specific model over time |
| **Auto-categorization** | Easy re-categorize dropdown when AI assigns wrong label to expense, email, or file |
| **Content moderation** | Appeal button with structured feedback form when AI incorrectly flags content |
| **Predictive text** | Long-press to report bad suggestion; track acceptance rate to tune model |

---

## 11. Anthropomorphism Trap

> Don't make AI too human or too robotic. Balance friendly language and warmth with clear boundaries; frame AI as a capable teammate, not a perfect person.

### How-to
Use relatable language but set clear expectations that the AI is not human or infallible.

### Examples

| Context | Implementation |
|---------|----------------|
| **Chatbot identity** | "I'm an AI assistant. I can help with X, Y, Z—but I might make mistakes." |
| **Error messaging** | "I'm not sure I understood that correctly" (warm) vs. "Error: invalid input" (robotic) |
| **Personality balance** | Friendly but not overly casual: "Here's what I found" vs. "OMG you're gonna LOVE this!" |
| **Capability framing** | "I can search products and answer questions, but I can't process returns—let me connect you with someone who can" |
| **Emotional boundaries** | Acknowledge user frustration without pretending to feel emotions: "That sounds frustrating. Let me try a different approach." |
| **Name and avatar** | Use clearly non-human identifiers (abstract icon, functional name) rather than human names/photos |
| **Limitation transparency** | "I work best with specific questions. For complex issues, a specialist might help more." |

---

## 12. AI Trust Decay Law

> One AI mistake can break user trust permanently. Build in fail-safes, clear disclaimers, and recovery paths to gracefully handle errors and retain user confidence.

### How-to
Set up quick error recovery options and provide disclaimers, apologizing and correcting mistakes when they happen.

### Examples

| Context | Implementation |
|---------|----------------|
| **Search failures** | "I couldn't find exactly what you described. Here are close alternatives—or try rephrasing?" |
| **Wrong recommendations** | Immediate "Not what you wanted? Tell me what's wrong" with quick correction flow |
| **Chatbot confusion** | "I think I misunderstood. Let me try again—or would you like to talk to a person?" |
| **Proactive disclaimers** | "I'm still learning about [topic]. Double-check important details." |
| **Graceful degradation** | When AI fails, fall back to traditional UI (filters, manual search) seamlessly |
| **Error acknowledgment** | "Sorry, that recommendation didn't match. I've noted your feedback to improve." |
| **Recovery shortcuts** | "Undo" prominent after any AI action; "Start over" option always visible |

---

## Quick Reference Matrix

| Law | Core Tension | Key Question |
|-----|--------------|--------------|
| Black Box | Opacity vs. Trust | Can users see *why*? |
| Human-in-the-Loop | Automation vs. Control | Can users override? |
| Bias Mirror | Data vs. Fairness | Who's being excluded? |
| Trust Gap | Capability vs. Acceptance | What stakes are appropriate? |
| Explainability | Complexity vs. Clarity | Is reasoning visible? |
| Co-pilot | AI agency vs. User agency | Who's in the driver's seat? |
| Confidence | Precision vs. Honesty | Are uncertainties shown? |
| Context Window | Input quality vs. Output quality | Is the user guided to give good input? |
| Friction vs. Magic | Speed vs. Trust | Is there appropriate confirmation? |
| Feedback Loop | Static vs. Improving | Can users teach the AI? |
| Anthropomorphism | Warmth vs. Clarity | Are expectations realistic? |
| Trust Decay | Mistakes vs. Recovery | Can errors be forgiven? |

---

## Application Checklist

Use this when designing or auditing AI features:

- [ ] **Transparency**: Users can see reasoning behind AI decisions
- [ ] **Control**: Override, edit, and undo options exist
- [ ] **Fairness**: Bias audits scheduled; edge cases tested
- [ ] **Graduated trust**: AI deployed in low-stakes contexts first
- [ ] **Explainability**: "Why this?" available for key outputs
- [ ] **Collaboration**: AI framed as assistant, not authority
- [ ] **Uncertainty**: Confidence levels communicated honestly
- [ ] **Input guidance**: Structured prompts help users provide context
- [ ] **Appropriate friction**: Confirmations for consequential actions
- [ ] **Feedback capture**: Easy correction and rating mechanisms
- [ ] **Identity clarity**: AI presented as capable tool, not human
- [ ] **Error recovery**: Graceful failures with clear recovery paths

---

## Further Reading

- Nielsen Norman Group: [AI UX Guidelines](https://www.nngroup.com/)
- Google PAIR: [People + AI Guidebook](https://pair.withgoogle.com/)
- Microsoft: [HAX Toolkit](https://www.microsoft.com/en-us/haxtoolkit/)
- Apple: [Human Interface Guidelines - Machine Learning](https://developer.apple.com/design/human-interface-guidelines/machine-learning)