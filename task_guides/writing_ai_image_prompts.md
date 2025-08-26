# RAG Guide: Writing Prompts for AI Image Generators  
**Scope:** Comprehensive, transcript-grounded reference for crafting effective prompts for text-to-image models.  
**Primary Source:** YouTube video “How to Write Great Prompts for AI Image Generators” (Learn with Shopify).  
**Models Mentioned:** Midjourney (Discord + website), DALL·E 3, Stable Diffusion, Google Gemini & ChatGPT (to *help write* prompts).

---

## 1) Purpose & Principles

- **Prompt engineering = crafting inputs that produce optimal results.** A simple prompt “gets you cake”; a well-engineered prompt gets you a higher-quality “homemade cake.”  
- **AI won’t ask clarifying questions.** If you don’t specify it, you’ll likely get a flat, generic image.  
- **Be specific *and* concise.** Overly long, tangled prompts can confuse generators.  
- **Think intention first.** What is the image for? What do you want the audience to feel?

---

## 2) Quick Checklist (Pre-Prompt)

1. **Intention** → Use case + desired feeling (e.g., “camping website; evoke peace/serenity/longing to be there”).  
2. **Subject** → Who/what (breed/type/age/texture/attitude, but only what’s relevant).  
3. **Action** → Make the subject *active* or interacting with the scene (even if still).  
4. **Lighting** → Mood/atmosphere/texture/focus (e.g., golden hour, campfire glow, backlit, soft/harsh).  
5. **Lens** → Wide-angle, fisheye, or a specific lens model; it *changes the image dramatically*.  
6. **Angle** → Camera position (low/heroic vs eye-level/natural).  
7. **Style & Medium** → Cinematic/hyper-real/animated/comic; digital image vs oil painting.  
8. **References** → Public-domain or owned images; avoid living artists (ethics + DALL·E 3 may decline).  
9. **Aspect Ratio & Resolution** → Fit the destination; avoid upscaling blur surprises.  
10. **Generator Settings** → Negative prompts; weight/prompt strength/adherence; seed number.  
11. **Natural-Language Enhancers** → Dashes and brackets to emphasize, separate, and clarify.

---

## 3) Field Guide (RAG Schema)

> Use these canonical fields so your agent can assemble, critique, or expand prompts consistently.

- **`intention`**: Purpose & emotional goal (e.g., “camping e-commerce hero; calm, serene, inviting”).  
- **`subject`**: Primary entity with key traits (e.g., “middle-aged scruffy golden retriever”).  
- **`action`**: Subject’s interaction with scene (e.g., “lying lazily by a calm lake, watching birds”).  
- **`environment`**: Setting & props (e.g., “smoldering campfire; green camping tent in foreground”).  
- **`lighting`**: Time, source, quality (e.g., “golden hour; warm campfire glow across fur; backlit/soft focus”).  
- **`lens`**: Focal feel (e.g., “wide-angle lens”; specific cinema lens permitted).  
- **`angle`**: Camera placement (e.g., “eye-level for natural perspective”).  
- **`style_medium`**: Aesthetic & medium (e.g., “hyperrealistic; cinematic; oil painting vs digital”).  
- **`references`**: Public-domain/owned image URLs (avoid living artists; DALL·E 3 may refuse).  
- **`aspect_ratio`**: Target frame (e.g., “16x9 / 16:9” for web hero).  
- **`resolution`**: Target quality; note that first passes may be low-res (upscale later).  
- **`negative_prompts`**: What to *avoid* (e.g., “cold, ominous, depressing”).  
- **`weights_or_strength`**: Prompt adherence setting (start slightly below ~¾ as a rule of thumb).  
- **`seed`**: Reproduce/adjust subtle randomness for small tweaks.  
- **`nl_enhancers`**: Dashes/brackets for emphasis, separation, or weighting hints.  
- **`generator_params`**: Model-specific flags (e.g., Midjourney `--no`, `--chaos`, out/zoom features).  
- **`notes`**: Constraints & ethics (e.g., commercial use; copyright comfort zone).

---

## 4) How to Build the Prompt (Step-by-Step)

### 4.1 Intention → Feeling
- Define **what** the image is for and **what viewers should feel** (e.g., *peaceful, serene, longing to join*).  
- This combats the most common failure: **lack of specificity**.

### 4.2 Subject → Action → Environment
- Upgrade “a dog” → **specific breed/age/texture** but stay concise (e.g., “middle-aged golden retriever”).  
- Make the subject **active** (e.g., “lying lazily by a calm lake, watching birds”).  
- Add **environment** elements that support intention (e.g., “smoldering campfire; green tent in foreground”).

### 4.3 Lighting (critical)
- Lighting **transforms** mood, texture, warmth, and focus.  
- Name **time** (golden hour, sunset), **sources** (campfire), **qualities** (warm glow, backlit, soft vs harsh).

### 4.4 Lens & Angle
- **Lens** shifts composition and feel (e.g., wide-angle for landscape; fisheye for distortion; even named cinema lenses are valid).  
- **Angle** sets power and intimacy (low = heroic; eye-level = natural, “it’s your campsite”).

### 4.5 Style, Medium & References
- Choose *cinematic/hyperreal/animated/comic*, plus *digital vs oil painting*, etc.  
- **References:** Use **public-domain** or **owned** images; Stable Diffusion supports image-as-reference; **DALL·E 3 may decline references to living artists**. Ethically avoid living-artist name prompts if using commercially.

### 4.6 Aspect Ratio & Resolution
- Set the **frame** (e.g., web hero often 16×9).  
- First pass in some tools is **lower resolution** → choose a candidate → **upscale**.  
- Some tools can **expand** (wider) or **shrink** (crop/focus tighter) after generation.

### 4.7 Generator Features to Exploit
- **Negative prompts:** Tell the model what *not* to do.  
  - Stable Diffusion: dedicated field.  
  - Midjourney: `--no <terms>` (e.g., `--no cold, ominous, depressing`).  
- **Weight / Prompt Strength / Adherence:** Start a bit **below ~¾** to give AI room while staying on brief.  
- **Seed:** A numeric handle on randomness; great for **small iterative tweaks** without changing everything.

### 4.8 Natural-Language Enhancers (Dashes & Brackets)
- Use **dashes** to clearly separate elements (subject | lighting | lens | angle | style | AR).  
- Use **brackets** around terms to **emphasize** qualities (e.g., `[whimsical] lake`, `[serene] atmosphere`).  
- Don’t overload brackets—too many priorities can confuse the model.

---

## 5) Prompt Blueprints (Transcript-Faithful)

> These patterns reflect exactly the building blocks shown in the source material.

### 5.1 Baseline (“Box-Cake”) Prompt
a dog sitting by (or near) a lake

### 5.2 Upgraded (“Homemade-Cake”) Prompt
a middle-aged golden retriever lying by a calm lake, watching birds fly across the sunset at golden hour — a smoldering campfire to the left casting a warm glow across his fur — a green camping tent in the foreground — hyperrealistic — wide-angle — eye-level perspective — AR 16x9

### 5.3 Add Negative Prompt (Same Scene)
… — a [serene], [whimsical] lake — AR 16x9

### 5.5 Chaos/Style Variations (Midjourney-style idea)
- Replace or pair parameters like:
–chaos   (you can also try terms like “weird”, “stylized”, “creepy”, or “raw” as alternatives)
–chaos … –weird …
> Combining such levers can push exploration (“dive deep down the rabbit hole”).

---

## 6) Use AI Assistants to *Engineer* Your Prompt

> The video demonstrates asking ChatGPT / Gemini to *be* your prompt engineer. Start from your “box-cake” prompt, specify your needs, and ask for 3 variations with AR included.

**Template (fill the brackets):**
You will act as my professional prompt engineer for the AI image generator [Midjourney / DALL·E 3 / Stable Diffusion].
I’m creating an image for my [business website / Instagram page], and I need an image that captures [beauty / peace / calm / …].
Here is the initial prompt: “[your baseline prompt here]”.
Please provide three variations. Each should be high-resolution, realistic, and set in a [wide-angle lens OR your preference].
Include the aspect ratio [e.g., 16x9] in each response.

- The demo compares outputs from ChatGPT and Gemini and shows both can help **expand** simple prompts into richer, on-brief variants.

---

## 7) Model Notes (As Stated)

- **Midjourney**
  - Available via **Discord** and **website**.  
  - Stores all outputs on a **personal web page** with reference codes and prompts (easy to look up what worked).  
  - First variation is **smaller resolution**; **upscale** the one you like.  
  - Can **expand** to widen the view or **shrink** to focus on a subject.  
  - **Negative prompts** via `--no`.  
  - Parameters like **chaos** (and similar words like “weird”, “stylized”, “creepy”, “raw”) influence exploration.

- **Stable Diffusion**
  - Has a **separate field for negative prompts**.  
  - Allows **uploading a photo as a reference** along with your prompt (ensure it’s public-domain or yours).

- **DALL·E 3**
  - May **decline references** to **living artists**.  
  - General ethical advice: if using images commercially, **avoid living-artist look-alikes**.

---

## 8) Reference Mining Without Burning Credits
- The video recommends using a site that shows **unlimited image results and the prompts** used, so you can study **lighting, texture, style** terms and **copy prompts** to try in your own generator.  
- You can **hover to see prompts**, click terms to open galleries for a specific **lighting/texture/style** concept, and **copy** prompts across tools (results won’t be identical but can get you closer faster).

---

## 9) Troubleshooting & Iteration

- **Flat images**: You likely skipped intention, lighting, or action (no story).  
- **Too literal**: Add **mood** via lighting; specify **lens/angle** for composition; bracket key adjectives.  
- **Off-brief details**: Add **negative prompts**; raise prompt **adherence/strength** modestly.  
- **Good but not quite**: Keep the **seed** and nudge fields (lighting variant, angle, or one prop).  
- **Overcomplication**: Trim adjectives; keep only the **most accurate** descriptors.

---

## 10) Minimal Working Patterns (Copy/Paste)

**A) Structured Scaffold**
[intention] — [subject] — [action] — [environment] — [lighting] — [lens] — [angle] — [style/medium] — [AR/resolution] [negatives/weights/seed as needed]

**B) Camping Website Hero (Transcript Build)**
a middle-aged golden retriever lying by a calm lake, watching birds fly across the sunset at golden hour — a smoldering campfire to the left casting a warm glow across his fur — a green camping tent in the foreground — hyperrealistic — wide-angle — eye-level perspective — AR 16x9

**C) Same + Negatives**
… — AR 16x9 –no cold, ominous, depressing

**D) Ask AI to Engineer Variations**
You will act as my professional prompt engineer for [Midjourney / DALL·E 3 / Stable Diffusion].
Goal: [business website / Instagram], feelings: [peace, calm, beauty].
Initial prompt: “[your baseline prompt]”.
Return 3 improved prompts with [wide-angle], high-resolution, and include aspect ratio [16x9].
---

## 11) Ethics & Copyright (As Stated)
- Prefer **public-domain** or **owned** images for references.  
- Avoid explicitly prompting in the style of **living artists**, especially for commercial use (aligns with DALL·E 3 behavior and general ethical guidance).

---

## References
- YouTube — “How to Write Great Prompts for AI Image Generators”: https://www.youtube.com/watch?v=6RAStep_3OI