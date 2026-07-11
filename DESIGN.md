---
version: alpha
name: "UHP Dark Athletic"
description: "The Ultimate Health Project is a dark-first health and nutrition coaching brand site targeting busy professionals. The design is built on a near-black (#000000) canvas with warm off-white (#f0f0ee) body text, a muted warm-beige palette, and a single gold accent (#c9a84c) used for CTAs and brand highlights. Typography is the defining feature: massive Barlow Condensed Black headlines (up to 102px) create aggressive impact, while Inter handles all body and UI copy. The overall aesthetic is high-contrast, athletic, and editorial. closer to a premium fitness brand than a clinical health site."
colors:
  gold-primary: "#c9a84c"
  background-base: "#000000"
  surface-raised: "#111111"
  surface-secondary: "#080808"
  text-dim: "#444440"
  text-muted: "#777770"
  text-primary: "#f0f0ee"
  text-white: "#ffffff"
  beige-accent: "#c4c0b7"
  border-subtle: "#ffffff"
typography:
  hero-display-xl:
    fontFamily: "Barlow Condensed"
    fontSize: "102.4px"
    fontWeight: "900"
    lineHeight: "92.16px"
    letterSpacing: "-2.048px"
  hero-display-l:
    fontFamily: "Barlow Condensed"
    fontSize: "83.2px"
    fontWeight: "900"
    lineHeight: "74.88px"
    letterSpacing: "-2.08px"
  section-headline:
    fontFamily: "Barlow Condensed"
    fontSize: "64px"
    fontWeight: "900"
    lineHeight: "58.88px"
    letterSpacing: "-1.28px"
  section-headline-alt:
    fontFamily: "Barlow Condensed"
    fontSize: "62px"
    fontWeight: "900"
    lineHeight: "57.66px"
    letterSpacing: "-1.24px"
  card-headline:
    fontFamily: "Barlow Condensed"
    fontSize: "52px"
    fontWeight: "900"
    lineHeight: "62.4px"
    letterSpacing: "2.08px"
  display-inter:
    fontFamily: "Inter"
    fontSize: "61.44px"
    fontWeight: "900"
    lineHeight: "61.44px"
    letterSpacing: "-1.8432px"
  subheading-inter:
    fontFamily: "Inter"
    fontSize: "26px"
    fontWeight: "900"
  label-caps:
    fontFamily: "Inter"
    fontSize: "13px"
    fontWeight: "700"
    letterSpacing: "2.34px"
  label-caps-small:
    fontFamily: "Inter"
    fontSize: "11px"
    fontWeight: "700"
    letterSpacing: "2.42px"
  nav-label:
    fontFamily: "Barlow Condensed"
    fontSize: "12.5px"
    fontWeight: "700"
    letterSpacing: "1px"
  body-regular:
    fontFamily: "Inter"
    fontSize: "16px"
    fontWeight: "400"
  body-small:
    fontFamily: "Inter"
    fontSize: "14px"
    fontWeight: "400"
    lineHeight: "23.8px"
rounded:
  radius-sharp: "1px"
spacing:
  space-1: "4px"
  space-2: "8px"
  space-3: "12px"
  space-4: "16px"
  space-5: "20px"
  space-6: "24px"
  space-7: "28px"
  space-8: "32px"
  space-9: "36px"
  space-10: "40px"
  space-13: "52px"
  space-32: "128px"
---

## Overview

The Ultimate Health Project is a dark-first health and nutrition coaching brand site targeting busy professionals. The design is built on a near-black (#000000) canvas with warm off-white (#f0f0ee) body text, a muted warm-beige palette, and a single gold accent (#c9a84c) used for CTAs and brand highlights. Typography is the defining feature: massive Barlow Condensed Black headlines (up to 102px) create aggressive impact, while Inter handles all body and UI copy. The overall aesthetic is high-contrast, athletic, and editorial. closer to a premium fitness brand than a clinical health site.

**Signature traits:**
- Dual typeface system: Pairs Barlow Condensed and Inter across the type hierarchy.
- Tight geometric corners: Near-square geometry with corner radii capped around 1px.

## Colors

The palette uses 10 validated color tokens across 1 theme profile. Semantic roles stay attached to observed usage so generation agents can choose accents without inventing new color meaning.

**Semantic naming:**
- **surface-background** maps to `background-base`: Role "background" is grounded by usage context "Primary page and section background; hero, nav, footer surfaces".
- **action-text** maps to `text-primary`: Role "text" is grounded by usage context "Primary body text, nav links, hero subtext, general foreground".
- **content-text** maps to `text-muted`: Role "text" is grounded by usage context "Secondary/supporting body copy, captions, metadata".
- **border-border** maps to `beige-accent`: Role "border" is grounded by usage context "Dividers, subtle borders, decorative rule lines, secondary accents".

### Primary Brand
- **Gold Primary** (#c9a84c): CTA button backgrounds (Book Free Call), brand highlight, key accent. Role: primary.

### Text Scale
- **Text Dim** (#444440): Tertiary text, disabled states, low-emphasis labels. Role: text.
- **Text Muted** (#777770): Secondary/supporting body copy, captions, metadata. Role: text.
- **Text Primary** (#f0f0ee): Primary body text, nav links, hero subtext, general foreground. Role: text.
- **Text White** (#ffffff): Hero headlines, high-emphasis headings, button text on dark. Role: text.

### Interactive
- **Beige Accent** (#c4c0b7): Dividers, subtle borders, decorative rule lines, secondary accents. Role: border.
- **Border Subtle** (#ffffff): Hairline borders at 7% opacity (rgba(255,255,255,.07)). Role: border.

### Surface & Shadows
- **Background Base** (#000000): Primary page and section background; hero, nav, footer surfaces. Role: background.
- **Surface Raised** (#111111): Slightly elevated card and section surfaces. Role: background.
- **Surface Secondary** (#080808): Secondary background layer, subtle section separation. Role: background.

## Typography

Typography uses Barlow Condensed, Inter across extracted hierarchy roles. Keep hierarchy mapped to these token rows before adding decorative type styles.

Mixes Barlow Condensed and Inter for visual contrast. Weight range spans bold, regular, semi-bold. Sizes range from 11px to 102.4px.

### Font Roles
- **Headline Font**: Barlow Condensed
- **Body Font**: Barlow Condensed

### Type Scale Evidence
| Role | Font | Size | Weight | Line Height | Letter Spacing | Stack / Features | Notes |
|------|------|------|--------|-------------|----------------|------------------|-------|
| Largest hero headline — full-bleed impact statement | Barlow Condensed | 102.4px | 900 | 92.16px | -2.048px | Barlow Condensed, Arial Narrow, sans-serif | Extracted token |
| Secondary hero headline size | Barlow Condensed | 83.2px | 900 | 74.88px | -2.08px | Barlow Condensed, Arial Narrow, sans-serif | Extracted token |
| Section-level headings | Barlow Condensed | 64px | 900 | 58.88px | -1.28px | Barlow Condensed, Arial Narrow, sans-serif | Extracted token |
| Alternate section heading size | Barlow Condensed | 62px | 900 | 57.66px | -1.24px | Barlow Condensed, Arial Narrow, sans-serif | Extracted token |
| Card and feature block headings | Barlow Condensed | 52px | 900 | 62.4px | 2.08px | Barlow Condensed, Arial Narrow, sans-serif | Extracted token |
| Large Inter-based display numbers or stats | Inter | 61.44px | 900 | 61.44px | -1.8432px | Inter, system-ui, sans-serif | Extracted token |
| Sub-section headings in Inter | Inter | 26px | 900 | normal | normal | Inter, system-ui, sans-serif | Extracted token |
| Uppercase tracking labels, eyebrow text, category tags | Inter | 13px | 700 | normal | 2.34px | Inter, system-ui, sans-serif | Extracted token |
| Small uppercase tracking labels, scroll cues | Inter | 11px | 700 | normal | 2.42px | Inter, system-ui, sans-serif | Extracted token |
| Navigation items and UI labels in condensed font | Barlow Condensed | 12.5px | 700 | normal | 1px | Barlow Condensed, Arial Narrow, sans-serif | Extracted token |
| Primary body copy, paragraphs, general UI text | Inter | 16px | 400 | normal | normal | Inter, system-ui, sans-serif | Extracted token |
| Secondary body copy, descriptions, supporting text | Inter | 14px | 400 | 23.8px | normal | Inter, system-ui, sans-serif | Extracted token |

## Layout

Responsive system uses 2 breakpoint tier(s): mobile, desktop.

This system uses a 4px base grid with scale values 4, 8, 12, 16, 20, 24, 28, 32, 36, 40, 52, 128.

### Responsive Strategy
- **mobile (<= 1024px)**: Constrain layout for small viewports and prioritize vertical stacking.
- **desktop (Unknown)**: Expand layout density and horizontal composition for wide viewports.

### Spacing System
| Token | Value | Px | Notes |
|------|-------|----|-------|
| space-1 | 4px | 4 | Extracted spacing token |
| space-2 | 8px | 8 | Extracted spacing token |
| space-3 | 12px | 12 | Extracted spacing token |
| space-4 | 16px | 16 | Extracted spacing token |
| space-5 | 20px | 20 | Extracted spacing token |
| space-6 | 24px | 24 | Extracted spacing token |
| space-7 | 28px | 28 | Extracted spacing token |
| space-8 | 32px | 32 | Extracted spacing token |
| space-9 | 36px | 36 | Extracted spacing token |
| space-10 | 40px | 40 | Extracted spacing token |
| space-13 | 52px | 52 | Extracted spacing token |
| space-32 | 128px | 128 | Extracted spacing token |

## Elevation & Depth

Keep depth flat unless validated shadow or interaction evidence appears in the extraction payload. Do not invent shadows beyond this evidence boundary.

### Shadow Evidence
| Shadow Token | Layers | Details |
|--------------|--------|---------|
| n/a | 0 | No validated shadow payload |

### Interaction Signals
| Theme | Signal | Evidence |
|-------|--------|----------|
| Light | backdrop-filter | blur(12px) |
| Light | outline-color | rgb(240, 240, 238) ; rgb(119, 119, 112) ; rgb(255, 255, 255) |
| Light | outline-width | 3px |
| Light | outline-offset | 0px |
| Light | transform | matrix(1, 0, 0, 1, 0, 36) ; matrix(1, 0, 0, 0, 0, 0) ; matrix(1, 0, 0, 1, -133.1, 0) |

## Shapes

Shape language maps directly to rounded tokens. Keep component corners consistent with the role mapping below before introducing bespoke geometry.

### Radius Roles
| Token | Value | Px | Role Mapping |
|------|-------|----|--------------|
| radius-sharp | 1px | 1 | Hairline corner |

### Geometry Evidence
| Radius Token | Shape | Units |
|--------------|-------|-------|
| radius-sharp | 1px | px |

## Components

(none detected)

## Do's and Don'ts

Guardrails protect Dual typeface system, Tight geometric corners without adding unsupported visual claims.

| Do | Don't |
|----|---------|
| Do maintain consistent spacing using the base grid | Don't make unsupported claims about absent visual features |
| Do maintain WCAG AA contrast ratios (4.5:1 for normal text) | Don't mix rounded and sharp corners in the same view |
| Do use the primary color only for the single most important action per screen |  |
| Do verify evidence before writing new design-system guidance |  |

## Responsive Evidence

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <= 600px | (max-width: 600px) |
| Breakpoint 2 | <= 768px | (max-width: 768px) |
| Breakpoint 3 | <= 900px | (max-width: 900px) |
| Breakpoint 4 | <= 1000px | (max-width: 1000px) |
| Breakpoint 5 | <= 1024px | (max-width: 1024px) |
| Breakpoint 6 | Unknown | (prefers-reduced-motion: reduce) |

## Agent Prompt Guide

### Example Component Prompts
- Create button component using validated primary color role and spacing tokens.
- Create card component with mapped radius role and evidence-backed elevation.
- Create form input component using inferred typography hierarchy and border roles.

### Iteration Guide
1. Start with extracted palette and typography roles only.
2. Map spacing and radius directly from token tables before visual polish.
3. Apply component patterns one section at a time and compare against source intent.
4. Keep elevation claims tied to explicit evidence in output.
5. Iterate with smallest diffs and re-check section hierarchy after each change.
