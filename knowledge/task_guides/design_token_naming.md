# Design Token Naming Guide

## Executive Summary

Design token naming is a systematic approach to creating consistent, scalable vocabularies for design systems. Effective naming conventions enable clear communication between designers and developers, reduce confusion, and support long-term system evolution. This guide provides frameworks, taxonomies, and practical examples for naming tokens across different categories.

## Prerequisites

- Basic understanding of design tokens and design systems
- Familiarity with your team's technical implementation (CSS variables, JSON, etc.)
- Access to existing design system documentation
- Alignment on naming conventions across design and development teams

## Quickstart

### The Universal Token Naming Pattern
[namespace]-[category]-[concept]-[property]-[variant]-[state]-[scale]-[mode]

**Example:**
`ds-color-action-background-primary-hover-on-dark`

### Core Principles
- **Logical**: Names should clearly describe the token's purpose
- **Scalable**: Allow for future additions without breaking existing patterns
- **Simple**: Keep names concise and understandable
- **Standardized**: Use industry-standard terminology when possible

## Token Taxonomy Framework

### Base Levels (Required)

#### Category
The fundamental type of visual property:
- `color` - All color-related tokens
- `font` (or `typography`) - Text styling properties
- `space` (or `spacing`) - Spatial measurements
- `size` (or `sizing`) - Dimensional properties
- `radius` - Border radius values
- `elevation` (or `shadow`) - Shadow and layering effects
- `time` (or `duration`) - Animation timing
- `breakpoint` - Responsive breakpoints

#### Concept
Groups tokens by semantic meaning within a category:

**Color Concepts:**
- `action` - Interactive elements (buttons, links)
- `feedback` - Status communication (success, error, warning)
- `content` - Text and content colors
- `surface` - Background and container colors
- `border` - Boundary and separator colors

**Spacing Concepts:**
- `inset` - Internal spacing (padding)
- `stack` - Vertical spacing between elements
- `inline` - Horizontal spacing between elements
- `layout` - Structural spacing (margins, gaps)

#### Property
Specific attribute being styled:

**Color Properties:**
- `background`, `text`, `border`, `fill`, `stroke`

**Typography Properties:**
- `size`, `weight`, `line-height`, `letter-spacing`, `family`

**Spacing Properties:**
- `top`, `right`, `bottom`, `left`, `x`, `y`, `all`

### Modifier Levels (Optional)

#### Variant
Distinguishes different intensities or types:
- `primary`, `secondary`, `tertiary`
- `accent`, `neutral`, `inverse`
- `subtle`, `strong`, `stronger`

#### State
Interactive and contextual states:
- `default`, `hover`, `focus`, `active`, `pressed`
- `disabled`, `loading`, `selected`
- `error`, `success`, `warning`, `info`

#### Scale
Size or intensity variations:

**Numeric scales:** `100`, `200`, `300`, `400`, `500`
**T-shirt sizes:** `xs`, `sm`, `md`, `lg`, `xl`, `2xl`
**Semantic sizes:** `small`, `medium`, `large`

#### Mode
Theme or context variations:
- `light`, `dark`
- `high-contrast`, `reduced-motion`

### Object Levels (Component-specific)

#### Component
- `button`, `input`, `card`, `modal`, `navbar`

#### Element
- `header`, `body`, `footer`, `icon`, `label`

### Namespace Levels

#### System
- `ds` (design system), `brand`, `product-name`

#### Theme
- `light`, `dark`, `ocean`, `forest`

## Practical Examples by Category

### Color Tokens

#### Basic Color Structure

**System colors (primitives)**
```css
ds-color-blue-100: #E3F2FD
ds-color-blue-500: #2196F3
ds-color-blue-900: #0D47A1
```
**Semantic colors**
```css
ds-color-action-background-primary: var(--ds-color-blue-500)
ds-color-action-text-primary: #FFFFFF
ds-color-feedback-background-success: #4CAF50
ds-color-content-text-primary: #212121
ds-color-surface-background-default: #FFFFFF
```
#### Advanced Color Examples

**Interactive states**
```css
ds-color-action-background-primary-hover: #1976D2
ds-color-action-background-primary-focus: #1565C0
ds-color-action-background-primary-disabled: #BBDEFB
```
**Mode variations**
```css
ds-color-content-text-primary-on-light: #212121
ds-color-content-text-primary-on-dark: #FFFFFF
```
**Component-specific**
```css
ds-color-button-background-primary: var(--ds-color-action-background-primary)
ds-color-input-border-default: #E0E0E0
ds-color-card-background-elevated: #FFFFFF
```
### Typography Tokens

#### Font Family Structure
```css
ds-font-family-primary: "Inter", system-ui, sans-serif
ds-font-family-secondary: "Roboto Mono", monospace
ds-font-family-brand: "Custom Brand Font", serif
```
#### Font Size Scales

**T-shirt sizing**
```css
ds-font-size-xs: 0.75rem    # 12px
ds-font-size-sm: 0.875rem   # 14px
ds-font-size-md: 1rem       # 16px
ds-font-size-lg: 1.125rem   # 18px
ds-font-size-xl: 1.25rem    # 20px
ds-font-size-2xl: 1.5rem    # 24px
```
**Semantic sizing**
```css
ds-font-size-body-small: var(--ds-font-size-sm)
ds-font-size-body-default: var(--ds-font-size-md)
ds-font-size-heading-1: var(--ds-font-size-2xl)
ds-font-size-heading-2: var(--ds-font-size-xl)
```
#### Font Weight Examples
```css
ds-font-weight-light: 300
ds-font-weight-regular: 400
ds-font-weight-medium: 500
ds-font-weight-semibold: 600
ds-font-weight-bold: 700
```
**Semantic weights**
```css
ds-font-weight-body: var(--ds-font-weight-regular)
ds-font-weight-heading: var(--ds-font-weight-semibold)
ds-font-weight-emphasis: var(--ds-font-weight-bold)
```
### Spacing Tokens

#### Base Spacing Scale

**Multiplier-based system (base: 4px)**
```css
ds-space-0: 0
ds-space-1: 0.25rem   # 4px
ds-space-2: 0.5rem    # 8px
ds-space-3: 0.75rem   # 12px
ds-space-4: 1rem      # 16px
ds-space-5: 1.25rem   # 20px
ds-space-6: 1.5rem    # 24px
ds-space-8: 2rem      # 32px
ds-space-10: 2.5rem   # 40px
ds-space-12: 3rem     # 48px
ds-space-16: 4rem     # 64px
```
#### Semantic Spacing

**Component spacing**
```css
ds-space-inset-xs: var(--ds-space-2)    # 8px
ds-space-inset-sm: var(--ds-space-3)    # 12px
ds-space-inset-md: var(--ds-space-4)    # 16px
ds-space-inset-lg: var(--ds-space-6)    # 24px
```
**Layout spacing**
```css
ds-space-stack-xs: var(--ds-space-2)    # 8px
ds-space-stack-sm: var(--ds-space-4)    # 16px
ds-space-stack-md: var(--ds-space-6)    # 24px
ds-space-stack-lg: var(--ds-space-8)    # 32px
```
**Responsive spacing**
```css
ds-space-section-mobile: var(--ds-space-8)   # 32px
ds-space-section-tablet: var(--ds-space-12)  # 48px
ds-space-section-desktop: var(--ds-space-16) # 64px
```
### Border Radius Tokens

**Radius Scale**
```css
ds-radius-none: 0
ds-radius-xs: 0.125rem    # 2px
ds-radius-sm: 0.25rem     # 4px
ds-radius-md: 0.375rem    # 6px
ds-radius-lg: 0.5rem      # 8px
ds-radius-xl: 0.75rem     # 12px
ds-radius-2xl: 1rem       # 16px
ds-radius-full: 9999px    # circular
```
**Semantic Radius**
```css
ds-radius-button-small: var(--ds-radius-sm)
ds-radius-button-default: var(--ds-radius-md)
ds-radius-card: var(--ds-radius-lg)
ds-radius-modal: var(--ds-radius-xl)
ds-radius-avatar: var(--ds-radius-full)
```
### Elevation (Shadow) Tokens

**Shadow Levels**
```css
ds-elevation-0: none
ds-elevation-1: 0 1px 2px rgba(0, 0, 0, 0.05)
ds-elevation-2: 0 1px 3px rgba(0, 0, 0, 0.1), 0 1px 2px rgba(0, 0, 0, 0.06)
ds-elevation-3: 0 4px 6px rgba(0, 0, 0, 0.07), 0 2px 4px rgba(0, 0, 0, 0.06)
ds-elevation-4: 0 10px 15px rgba(0, 0, 0, 0.1), 0 4px 6px rgba(0, 0, 0, 0.05)
ds-elevation-5: 0 20px 25px rgba(0, 0, 0, 0.1), 0 10px 10px rgba(0, 0, 0, 0.04)
ds-elevation-6: 0 25px 50px rgba(0, 0, 0, 0.25)
```
**Semantic Elevation**
```css
ds-elevation-card: var(--ds-elevation-1)
ds-elevation-dropdown: var(--ds-elevation-3)
ds-elevation-modal: var(--ds-elevation-5)
ds-elevation-tooltip: var(--ds-elevation-2)
```
## Component-Specific Token Patterns

### Button Token Example

**Button backgrounds**
```css
ds-button-background-primary: var(--ds-color-action-background-primary)
ds-button-background-primary-hover: var(--ds-color-action-background-primary-hover)
ds-button-background-secondary: transparent
ds-button-background-tertiary: var(--ds-color-surface-background-subtle)
```
**Button text**
```css
ds-button-text-primary: var(--ds-color-action-text-primary)
ds-button-text-secondary: var(--ds-color-action-text-secondary)
```
**Button spacing**
```css
ds-button-inset-sm: var(--ds-space-2) var(--ds-space-3)
ds-button-inset-md: var(--ds-space-3) var(--ds-space-4)
ds-button-inset-lg: var(--ds-space-4) var(--ds-space-6)
```
**Button radius**
```css
ds-button-radius: var(--ds-radius-md)
```
## Implementation Strategies

### CSS Custom Properties
```css
:root {
  /* Base tokens */
  --ds-color-blue-500: #2196F3;
  --ds-space-4: 1rem;
  
  /* Semantic tokens */
  --ds-color-action-background-primary: var(--ds-color-blue-500);
  --ds-button-inset-md: var(--ds-space-3) var(--ds-space-4);
}

{
  "color": {
    "action": {
      "background": {
        "primary": {
          "value": "#2196F3",
          "type": "color"
        }
      }
    }
  }
}
```

## Troubleshooting

### Common Naming Issues
Problem: Token names are too long
Solution: Use abbreviated forms consistently (e.g., bg for background, txt for text)
Problem: Inconsistent casing across tools
Solution: Establish casing standards (kebab-case for CSS, camelCase for JavaScript)
Problem: Semantic tokens map to wrong primitive values
Solution: Create clear mapping documentation and review processes
Problem: Missing tokens for edge cases
Solution: Establish token request process and regular audits

### Migration Strategies
1. Audit existing tokens for naming inconsistencies
2. Create mapping table from old names to new names
3. Implement aliases for backward compatibility
4. Update design tools (Figma variables, etc.)
5. Update code references gradually
6. Remove deprecated tokens after migration period

### Validation Checklist
[] Names follow established taxonomy structure
[] All required base levels are present
[] Semantic meaning is clear from the name
[] Names are consistent across design and code
[] Future scaling is considered
[] Team consensus on naming conventions
[] Documentation is updated
[] Implementation is tested across tools

## Examples

### Complete Button Component Token Set
```markdown
# Base colors
ds-color-blue-500: #2196F3
ds-color-blue-600: #1976D2
ds-color-white: #FFFFFF

# Semantic colors
ds-color-action-background-primary: var(--ds-color-blue-500)
ds-color-action-background-primary-hover: var(--ds-color-blue-600)
ds-color-action-text-primary: var(--ds-color-white)

# Typography
ds-font-weight-medium: 500
ds-font-size-md: 1rem

# Spacing
ds-space-3: 0.75rem
ds-space-4: 1rem

# Radius
ds-radius-md: 0.375rem

# Component tokens
ds-button-background-primary: var(--ds-color-action-background-primary)
ds-button-background-primary-hover: var(--ds-color-action-background-primary-hover)
ds-button-text-primary: var(--ds-color-action-text-primary)
ds-button-font-weight: var(--ds-font-weight-medium)
ds-button-font-size: var(--ds-font-size-md)
ds-button-inset: var(--ds-space-3) var(--ds-space-4)
ds-button-radius: var(--ds-radius-md)
```
## FAQ
Q: Should I use color names (blue, red) or semantic names (primary, success)?
A: Use semantic names for tokens that will be consumed by components. Use color names only for primitive/base tokens that map to semantic ones.
Q: How detailed should component-specific tokens be?
A: Create component tokens only when the same semantic token isn't sufficient. Start with semantic tokens and add component-specific ones as needed.
Q: How do I handle responsive design tokens?
A: Use scale modifiers or breakpoint-specific tokens. Consider both approach based on your team's needs.
Q: Should abbreviations be used in token names?
A: Use abbreviations sparingly and only when they're widely understood. Prioritize clarity over brevity.

## References
- Nathan Curtis - "Naming Tokens in Design Systems" (EightShapes): https://medium.com/eightshapes-llc/naming-tokens-in-design-systems-9e86c7444676
- Nate Baldwin - "Creating a flexible design token taxonomy for Intuit's Design System": https://medium.com/@NateBaldwin/creating-a-flexible-design-token-taxonomy-for-intuits-design-system-81c8ff55c59b
- Ardena - "Naming conventions for design systems" (Backlight): https://backlight.dev/blog/naming-conventions-for-design-systems/
- Design tokens, from Adobe Spectrum: https://spectrum.adobe.com/page/design-tokens/
- Naming conventions, from goodpractices.design: https://goodpractices.design/guidelines/naming