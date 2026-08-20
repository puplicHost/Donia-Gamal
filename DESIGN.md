---
name: Aureate Portfolio
colors:
  surface: '#fbf9f8'
  surface-dim: '#dbdad9'
  surface-bright: '#fbf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f5f3f3'
  surface-container: '#efeded'
  surface-container-high: '#e9e8e7'
  surface-container-highest: '#e4e2e2'
  on-surface: '#1b1c1c'
  on-surface-variant: '#444748'
  inverse-surface: '#303031'
  inverse-on-surface: '#f2f0f0'
  outline: '#747878'
  outline-variant: '#c4c7c7'
  surface-tint: '#5f5e5e'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#1c1b1b'
  on-primary-container: '#858383'
  inverse-primary: '#c8c6c5'
  secondary: '#5e5e5b'
  on-secondary: '#ffffff'
  secondary-container: '#e1dfdb'
  on-secondary-container: '#63635f'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#281800'
  on-tertiary-container: '#a07e4a'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e5e2e1'
  primary-fixed-dim: '#c8c6c5'
  on-primary-fixed: '#1c1b1b'
  on-primary-fixed-variant: '#474746'
  secondary-fixed: '#e4e2dd'
  secondary-fixed-dim: '#c8c6c2'
  on-secondary-fixed: '#1b1c19'
  on-secondary-fixed-variant: '#474744'
  tertiary-fixed: '#ffdeae'
  tertiary-fixed-dim: '#e8c086'
  on-tertiary-fixed: '#281800'
  on-tertiary-fixed-variant: '#5d4213'
  background: '#fbf9f8'
  on-background: '#1b1c1c'
  surface-variant: '#e4e2e2'
typography:
  display-hero:
    fontFamily: Playfair Display
    fontSize: 84px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Playfair Display
    fontSize: 48px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Playfair Display
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
  section-title:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '700'
    lineHeight: '1.5'
    letterSpacing: 0.15em
  project-title:
    fontFamily: Playfair Display
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.4'
  body-main:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.7'
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  metadata:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: 0.05em
  label-button:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1'
    letterSpacing: 0.02em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 8px
  container-max: 1440px
  gutter: 32px
  margin-mobile: 24px
  margin-desktop: 64px
  section-gap: 128px
---

## Brand & Style
The design system embodies a **Luxury Editorial** aesthetic tailored for high-end marketing professionals. It prioritizes clarity, authority, and "the luxury of space." The design narrative focuses on a "Digital Gallery" approach where the professional's work is treated as a high-value asset.

The style is a synthesis of **Minimalism** and **High-Contrast Editorial**. It avoids digital-native trends like glassmorphism or neomorphism in favor of traditional print-inspired elements: stark layouts, 1px hairlines, and precise typographic scales. The emotional response is one of calm confidence, meticulousness, and established prestige.

## Colors
The palette is rooted in a "Paper and Ink" philosophy to ground the digital experience in tactile luxury.

- **Primary Background (#F9F7F2):** A warm Ivory that reduces eye strain and feels more premium than pure white.
- **Primary Text (#1A1A1A):** Deep Charcoal for maximum legibility and high-contrast impact against the ivory.
- **Secondary Text (#666666):** Used for metadata, captions, and secondary information to maintain hierarchy.
- **Accent (#B08D57):** A Deep Ochre used sparingly for calls to action, active states, and specific highlights to guide the user's eye without overwhelming the content.
- **Border/Divider (#D1CEC8):** A subtle tint of the background color used for 1px structural lines.

## Typography
The typography system relies on a high-contrast pairing between the expressive **Playfair Display** (Serif) and the functional **Plus Jakarta Sans** (Sans-serif). 

Use the Serif for large storytelling moments and headlines. Use the Sans-serif for navigation, long-form body copy, and technical details. Note the use of wide letter-spacing and uppercase transformations for `section-title` to create an architectural, labeled feel for the layout sections.

## Layout & Spacing
This design system utilizes an **Asymmetric Fixed Grid** model. On desktop, use a 12-column grid with generous 64px outer margins. Key content should often start on column 3 or 4, leaving "white space" on the left to emphasize the editorial nature of the work.

Vertical rhythm is critical. Use `section-gap` (128px) to separate major portfolio pieces, allowing each project to breathe. Avoid overcrowding elements; if in doubt, increase padding. On mobile, transition to a 4-column fluid grid with 24px margins, maintaining the vertical spacing to preserve the premium feel.

## Elevation & Depth
In this design system, depth is achieved through **Tonal Layers** and **1px Outlines**, never through shadows.

- **Level 0 (Base):** #F9F7F2 (The "Paper").
- **Level 1 (Interactions):** Elements like cards or images use a subtle 1px border (#D1CEC8) to define their boundaries.
- **Interaction Depth:** When an element is hovered (like a project card), it does not lift with a shadow. Instead, the border color may darken to #1A1A1A or the background of the card may shift slightly to a very light gray.
- **Layering:** Overlapping elements (e.g., text slightly overhanging an image) should be used to create a sense of physical editorial layout.

## Shapes
The shape language is **Soft (0.25rem)**, bordering on sharp. This provides a precision-engineered look that feels more modern and professional than fully rounded or pill-shaped designs.

- **Small elements (Checkboxes, small buttons):** 4px radius.
- **Medium elements (Cards, input fields):** 4px radius.
- **Large elements (Images, containers):** 4px or sharp (0px) depending on the content density.

## Components

### Buttons
- **Primary:** Solid #1A1A1A background with #F9F7F2 text. No border. Hover state shifts background to #B08D57.
- **Secondary:** Transparent background with 1px #1A1A1A border. Text is #1A1A1A.
- **Ghost/Tertiary:** No background or border. Text is #1A1A1A with an underline that expands or changes color on hover.

### Cards (Project Showcase)
- Minimalist approach: The image takes priority.
- 1px border (#D1CEC8).
- Typography is placed outside the image frame for an editorial gallery feel.
- Metadata (Year, Role) is styled with `metadata` tokens in #666666.

### Input Fields
- Underline-only style or very subtle 1px border.
- Background remains #F9F7F2 or a slightly darker tint.
- Focus state: The bottom border thickens or changes to #B08D57.

### Lists & Dividers
- Use horizontal 1px rules (#D1CEC8) to separate list items.
- Ensure large padding (24px - 32px) between list items to maintain the luxury of space.

### Chips/Tags
- Rectangular with 4px radius.
- Light gray background (#EBE9E4) with #666666 text. Use `metadata` font style.