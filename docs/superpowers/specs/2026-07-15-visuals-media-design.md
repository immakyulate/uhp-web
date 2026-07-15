# Design Spec: UHP Visuals & Media Integration

**Date:** 2026-07-15  
**Status:** Approved by User  
**Author:** Antigravity AI  

---

## 1. Objective
Enhance the visual experience and scannability of the UHP website by:
1. **Dynamic Immersive Transition (Homepage):** Transition the homepage scrolling storyteller block background to a high-contrast active lifestyle photo specifically during Slide 3 (Routine Friction) where the new active movement copy resides.
2. **Scannable Iconography (Programs Page):** Replacing standard feature bullet checkmarks on `services.html` with unique custom SVG icons tailored to each bullet point's meaning, colored dynamically via CSS variables.

---

## 2. Homepage Slide 3 Background Transition

### 2.1. HTML Structure
Add a second background image layer in `index.html` within the `#story-sticky` block:
```html
<!-- Immersive Background Image Layers -->
<div id="story-bg-img"></div>
<div id="story-bg-img-active" style="background-image: url('assets/active_lifestyle.jpg');"></div>
```

### 2.2. CSS Styling
Define styles for the active background layer in the `<style>` block:
```css
#story-bg-img-active {
  position: absolute;
  inset: 0;
  z-index: 0;
  background-size: cover;
  background-position: center;
  opacity: 0;
  transition: opacity 0.6s ease, transform 0.6s ease;
  transform: scale(1.02);
}
```

### 2.3. JS Scroll Logic Update
Modify the scroll storyteller JS scrub handler:
* When `cardIndex === 2` (Slide 3: Routine Friction):
  * Set `bgImg.style.opacity = '0'` and `bgImg.style.transform = 'scale(0.98)'`.
  * Set `bgActiveImg.style.opacity = '0.45'` (making the active lifestyle photo beautifully visible behind the text) and `bgActiveImg.style.transform = 'scale(1.0)'`.
* When `cardIndex` is anything else (Slides 1, 2, 4, 5):
  * Set `bgImg` opacity to its respective values (`0.04`, `0.78`, `0.15`).
  * Set `bgActiveImg.style.opacity = '0'` and `bgActiveImg.style.transform = 'scale(1.02)'`.

---

## 3. Programs Page Bullet-Level Iconography (`services.html`)
Replace the standard checkmark SVGs inside the `.pf-item` list elements with custom scannable SVG icons inside `.pf-check`. 

Style `.pf-check` to remove background-color restrictions, allowing the icons to render cleanly in their respective theme colors (`var(--pillar-color)`):
```css
.pf-check { 
  background: transparent !important; 
  border: 1px solid var(--pillar-color) !important;
  color: var(--pillar-color) !important;
}
.pf-check svg { 
  stroke: var(--pillar-color) !important; 
}
```

### 3.1. SVGs Map by Bullet Point

#### Pillar 1: Healthy Eating (id="nutrition")
*   **Bullet 1 (Daily Meal Structures):** Fork/Knife Plate SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2v20M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>`
*   **Bullet 2 (Dining out / travel):** Wine Glass SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 22H2M6 2h12v11c0 3.3-2.7 6-6 6s-6-2.7-6-6V2zM12 19v3"/></svg>`
*   **Bullet 3 (Decision anchors):** Calendar Check SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/><path d="m9 16 2 2 4-4"/></svg>`
*   **Bullet 4 (Caloric adjustments):** Gauge/Dial SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2a10 10 0 0 1 10 10c0 2.22-.73 4.27-1.96 5.92L18.5 16.4a6 6 0 1 0-13 0l-1.54 1.52A9.97 9.97 0 0 1 2 12 10 10 0 0 1 12 2z"/><path d="m12 8-2 4h4z"/></svg>`

#### Pillar 2: Fitness Plan (id="fitness")
*   **Bullet 1 (Daily Step Protocols):** Footprints/Shoe SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 17h18M6 10v4M10 7v7M14 5v9M18 10v4"/><rect x="2" y="14" width="20" height="4" rx="1"/></svg>`
*   **Bullet 2 (Strength training):** Dumbbell SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6.5 6.5h11M18 3v7M6 3v7M3 6.5h3M18 6.5h3"/></svg>`
*   **Bullet 3 (Active family integration):** Heart/Family SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5l7 7Z"/></svg>`
*   **Bullet 4 (Travel workouts):** Luggage SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="7" width="18" height="14" rx="2"/><path d="M8 7V3h8v4"/></svg>`

#### Pillar 3: Supplementation (id="supplements")
*   **Bullet 1 (Smoothies/Shakes):** Shaker Bottle SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3h12l-2 15H8L6 3z"/><path d="M9 3v3M15 3v3M8 18h8M12 18v3"/></svg>`
*   **Bullet 2 (Energy teas):** Mug/Tea SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 8h1a4 4 0 0 1 0 8h-1M2 8h16v9a4 4 0 0 1-4 4H6a4 4 0 0 1-4-4V8z"/><path d="M6 1v3M10 1v3M14 1v3"/></svg>`
*   **Bullet 3 (Protein & digestive aloe):** Drop SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22a7 7 0 0 0 7-7c0-4.3-7-13-7-13S5 10.7 5 15a7 7 0 0 0 7 7z"/></svg>`
*   **Bullet 4 (Monthly Shipping):** Box/Delivery SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="1" y="3" width="15" height="13"/><polygon points="16 8 20 8 23 11 23 16 16 16"/><circle cx="5.5" cy="18.5" r="2.5"/><circle cx="18.5" cy="18.5" r="2.5"/></svg>`

#### Pillar 4: Personal Coach (id="accountability")
*   **Bullet 1 (AI Assistant check-in):** Chat Message SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>`
*   **Bullet 2 (Real-time dinner/menu advice):** Book Open/Menu SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2zM22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg>`
*   **Bullet 3 (1:1 sessions & audits):** User Check SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="m16 11 2 2 4-4"/></svg>`
*   **Bullet 4 (Continuous adjustments):** Target SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><circle cx="12" cy="12" r="6"/><circle cx="12" cy="12" r="2"/></svg>`

#### Pillar 5: Community Support (id="community")
*   **Bullet 1 (Peer network):** Users SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75"/></svg>`
*   **Bullet 2 (Shared dashboards):** Trophy SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 9H4.5a2.5 2.5 0 0 1 0-5H6M18 9h1.5a2.5 2.5 0 0 0 0-5H18M4 22h16M10 14.66V17c0 .55-.45 1-1 1H4v2h16v-2h-5c-.55 0-1-.45-1-1v-2.34M12 2a5 5 0 0 0-5 5v3c0 2.76 2.24 5 5 5s5-2.24 5-5V7a5 5 0 0 0-5-5z"/></svg>`
*   **Bullet 3 (Weekly group coaching):** Megaphone SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M11 5 6 9H2v6h4l5 4V5zM23 9s-2.33 1.5-2.33 3 2.33 3 2.33 3M19 10s-1 1-1 2 1 2 1 2"/></svg>`
*   **Bullet 4 (Unified metrics tracking):** Line Chart SVG
    `<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 3v18h18M18.7 8l-5.1 5.2-2.8-2.7L7 14.3"/></svg>`

---

## 4. Spec Self-Review
1. **Placeholder scan:** SVGs are specified down to their exact inline XML strings. Transition behaviors are mapped with exact numeric target values.
2. **Internal consistency:** Colors and anchors match the newly established Five Pillars mapping.
3. **Scope check:** Bounded exclusively to media/asset transitions and iconography updates.
