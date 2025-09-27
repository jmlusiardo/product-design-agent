# Content Testing / Pruebas de Contenido

## Executive Summary

Content testing evaluates how users understand, navigate, and derive value from digital content. This specialized UX research method uses techniques like banana testing (replacing text with "Banana" to test hierarchy), highlighting exercises (marking valuable vs. confusing content), and comprehension assessments to ensure content clarity, effectiveness, and user-centered design.

**Key Benefits:**
- Validates content before development investment
- Identifies comprehension gaps and hierarchy issues  
- Tests content value and emotional impact
- Supports evidence-based content design decisions
- Reduces user confusion and abandonment

**Core Methods:** Banana testing, content value highlighting, cloze testing, 5-second impression tests, preference testing.

## Prerequisites

**Required Skills:**
- Basic UX research methodology
- Content analysis capabilities
- User interview and observation techniques
- Digital highlighting/annotation tools proficiency

**Required Knowledge:**
- Understanding of information hierarchy principles
- Content design fundamentals
- User mental models and perception psychology
- Basic statistical analysis for quantitative results

**Tools Needed:**
- Highlighting tools (digital: Figma, Miro, Google Docs; physical: colored markers)
- Content testing platforms (Maze, UXtweak, UserTesting)

## Quickstart

### 5-Minute Banana Test Setup
1. **Select content:** Choose 1-2 key screens or content sections
2. **Create banana version:** Replace all meaningful text with "Banana" (keep navigation/structure)
3. **Prepare questions:** "What do you think this 'Banana' does?" for each element
4. **Test with 3-5 users:** Remote or in-person, 10-15 minutes each
5. **Analyze patterns:** Note consistent interpretations vs. confusion points

### Quick Highlighting Exercise
1. **Choose content:** 1-2 paragraphs of existing copy
2. **Set up highlighting:** Green = helpful/clear, Red = confusing/unnecessary
3. **Brief participants:** "Highlight text that helps you vs. creates confusion"
4. **Collect results:** Overlay all participant highlights to see patterns
5. **Identify actions:** Revise consistently red-highlighted content

## Core Content Testing Methods

### Banana Testing (Hierarchy & Mental Model Validation)

**Purpose:** Test if users understand content hierarchy and functionality when stripped of semantic meaning.

**Process:**
1. **Content preparation:** Replace all meaningful text with "Banana" while preserving:
   - Visual hierarchy (headings, subheadings, body text)
   - Interactive elements (buttons, links, forms)
   - Layout and spacing
   - Icons and visual indicators

2. **Session structure:**
   - Show banana version for 30-60 seconds
   - Ask: "What do you think each 'Banana' represents?"
   - For interactive elements: "What would happen if you clicked this Banana?"
   - Follow up: "How confident are you in that interpretation?"

3. **Analysis:**
   - **High comprehension:** Consistent interpretations across participants
   - **Medium comprehension:** Some variation but generally correct understanding
   - **Low comprehension:** Confused or incorrect interpretations
   - **Action items:** Redesign low-comprehension elements

**Best Practices:**
- Test early wireframes and established interfaces
- Focus on 5-7 key elements per session
- Use with navigation, CTAs, and complex workflows
- Combine with standard usability testing for complete picture

### Content Value Testing (Highlighting Method)

**Purpose:** Identify which content builds confidence, provides value, or creates confusion.

**Setup Options:**
- **Digital:** Google Docs, Figma comments, Miro boards
- **Physical:** Printed content with colored highlighters
- **Tools:** UXtweak, Maze highlighting features

**Color Coding Systems:**

**Standard Confidence Scale:**
- Green: "Increases my confidence/helpful"
- Red: "Decreases my confidence/confusing" 
- Yellow: "Neutral/unsure"

**Value Assessment Scale:**
- Green: "Valuable information I need"
- Orange: "Somewhat useful"
- Red: "Unnecessary/doesn't help me"

**Emotional Response Scale:**
- Green: "Makes me feel positive/trusting"
- Yellow: "Neutral feeling"
- Red: "Makes me feel worried/uncertain"

**Process:**
1. **Content selection:** Choose 1-3 coherent content sections (onboarding flows, product descriptions, help content)
2. **Participant briefing:** Explain highlighting system and provide realistic use case scenario
3. **First read:** Allow participants to read without highlighting
4. **Highlighting phase:** Ask them to highlight according to chosen scale
5. **Follow-up questions:** "Why did you highlight this section green/red?"

**Analysis:**
- **Dark green overlays:** Keep and potentially expand successful content
- **Dark red overlays:** Priority candidates for revision or removal
- **Mixed responses:** Investigate with follow-up interviews
- **Uncolored content:** May be skipped or ignored by users

### Comprehension Testing Methods

#### Cloze Testing
**Purpose:** Measure reading comprehension and content clarity.

**Process:**
1. Select content passage (50-100 words)
2. Remove every 5th-7th word, replace with blank lines
3. Ask participants to fill in missing words
4. Score: Correct/similar words indicate good comprehension

**Scoring:**
- 85%+ correct: Content at appropriate reading level
- 70-84% correct: May need simplification
- Below 70%: Requires significant revision

#### 5-Second Impression Test
**Purpose:** Test immediate comprehension and first impressions.

**Process:**
1. Show content for exactly 5 seconds
2. Remove from view
3. Ask: "What was this content about?" "What would you do next?" "How did it make you feel?"
4. Analyze which elements were retained vs. missed

#### Preference Testing
**Purpose:** Compare content variations or competitor approaches.

**Process:**
1. Present 2-3 content variations side by side
2. Ask users to choose preferred option
3. Follow up: "What made you choose this version?"
4. Test tone, clarity, length, and structure variations

## Content-Specific Research Considerations

### Participant Recruiting Adaptations
**Critical Principle:** Content effectiveness depends heavily on audience knowledge and context.

**Content Domain Matching:** For specialized content (medical, technical, financial), recruit participants with genuine experience rather than proxy users. See [ux-research-planning](./ux-research-planning.md) for detailed recruiting strategies.

### Session Adaptations
**Content-Specific Facilitation:** Beyond standard session practices covered in [user-interviews](./user-interviews.md):
- Allow natural reading pace vs. rushed scanning
- Test content in realistic context (mobile vs. desktop)
- Consider reading order and visual attention patterns
- Note when participants re-read sections (comprehension difficulty indicator)

## Analysis and Reporting

### Content-Specific Analysis Methods
**Highlighting Heat Maps:**
- Overlay all participant highlighting responses
- Calculate percentage agreement on positive/negative sections
- Create visual heat maps showing content value distribution

**Comprehension Scoring:**
- Banana test: % participants correctly identifying element function
- Cloze test: % correct word completion
- 5-second test: % recalling key information

**Content Testing Report Structure:**
1. **Executive Summary:** Key findings and recommendations
2. **Methodology:** Which tests used, sample size, recruitment approach
3. **Content Heat Maps:** Visual representation of highlighting results
4. **Comprehension Analysis:** Banana test and cloze test results
5. **Specific Recommendations:** Content to keep, revise, or remove
6. **Appendix:** Raw participant responses and detailed scores

For general analysis techniques, see [usability-testing](./usability-testing.md) and [ux-research-planning](./ux-research-planning.md).

**Content-Specific Recommendations Format:**
- **Keep:** Content with 80%+ positive highlighting
- **Revise:** Content with mixed responses or comprehension issues
- **Remove:** Content with 60%+ negative highlighting
- **Add:** Information gaps identified through user questions

## Common Pitfalls and Solutions

### Content Testing Specific Pitfalls

**Problem:** Testing too much content at once
**Solution:** Focus on 1-3 key content sections per session

**Problem:** Testing content before defining user needs
**Solution:** Complete [user-interviews](./user-interviews.md) and needs assessment first

**Problem:** Focusing only on comprehension, ignoring emotional response
**Solution:** Include confidence and emotional impact in testing framework

## Tools and Resources

### Content Testing Specific Tools
- **Maze:** Dedicated content testing and highlighting features
- **UXtweak:** Content testing toolkit with heat maps
- **UserTesting:** Content-focused research templates
- **Google Docs:** Built-in commenting and highlighting for simple tests

For general UX research tools, see [ux-research-planning](./ux-research-planning.md).

## Examples and Case Studies

### Example 1: E-commerce Product Description Testing
**Context:** Online furniture retailer with high bounce rates on product pages

**Method:** Highlighting test with confidence scale
- Green: "Helps me decide to purchase"
- Red: "Creates doubt or confusion"

**Key Findings:**
- Technical specifications (green): Users wanted detailed measurements
- Marketing copy (red): "Luxurious" and "premium" created skepticism
- Shipping information (mixed): Clear delivery times helped, shipping costs hurt

**Actions:**
- Moved technical specs higher on page
- Replaced marketing adjectives with specific benefits
- Restructured shipping information for clarity

### Example 2: Healthcare Onboarding Flow
**Context:** Medical app with low completion rates for initial setup

**Method:** Banana testing + follow-up interviews

**Key Findings:**
- Privacy policy link (confusion): Users thought clicking would start lengthy legal process
- Progress indicators (success): Clear understanding of steps remaining
- Medical terminology (confusion): Users couldn't predict what information was needed

**Actions:**
- Changed "Privacy Policy" to "How we protect your data (2 min read)"
- Kept existing progress indicators
- Added preview questions: "We'll ask about your current medications"

### Example 3: SaaS Feature Explanation
**Context:** Project management tool with low feature adoption

**Method:** 5-second test + cloze testing

**Key Findings:**
- Users missed key benefits in 5-second exposure
- Cloze test revealed terminology mismatches with user language
- Feature names didn't match user mental models

**Actions:**
- Restructured content with benefit-first hierarchy
- Replaced internal terminology with user language from interviews
- Added visual examples alongside text descriptions

## Cross-references

**Essential Prerequisites:**
- [ux-research-planning](./ux-research-planning.md) - Study design, participant recruiting, sample size calculations
- [user-interviews](./user-interviews.md) - Session facilitation, participant recruiting, interviewing techniques
- [usability-testing](./usability-testing.md) - Moderated vs unmoderated testing, session setup, general analysis methods

**Related Methods:**
- [ux-writing](./ux-writing.md) - Content creation principles, tone and voice guidelines
- [information-architecture](./information-architecture.md) - Content organization and hierarchy principles
- [a-b-testing](./a-b-testing.md) - Quantitative content performance testing
- [card-sorting](./card-sorting.md) - Content organization and categorization testing

**Follow-up Tasks:**
- [design-system](./design-system.md) - Implementing content standards and guidelines
- [accessibility-testing](./accessibility-testing.md) - Content accessibility evaluation

## References
1. Smashing Magazine: How To Test And Measure Content In UX - https://www.smashingmagazine.com/2025/02/how-to-test-and-measure-content-in-ux/
2. Smart Interface Design Patterns: Content Testing Methods - https://smart-interface-design-patterns.com/articles/content-testing/
3. Nielsen Norman Group: Testing Content with Users - https://www.nngroup.com/articles/testing-content-websites/
4. Dscout: 3 Effective Methods for Content Tests - https://www.dscout.com/people-nerds/content-testing
5. UX Content Collective: Content testing and measurement for UX - https://uxcontent.com/content-testing-measurement-ux/
6. GOV.UK User Research: A simple technique for evaluating content - https://userresearch.blog.gov.uk/2014/09/02/a-simple-technique-for-evaluating-content/
7. UserTesting: Content Testing & Measurement - https://www.usertesting.com/blog/content-testing-and-measurement
8. Maze: Content Testing For UX - https://maze.co/guides/content-testing/
9. UXtweak: Content Testing Methods - https://www.uxtweak.com/content-testing/methods/
10. Dovetail: Content Testing Guide - https://dovetail.com/ux/what-is-content-testing/
11. UXtweak: Content Testing Guide - https://www.uxtweak.com/content-testing/