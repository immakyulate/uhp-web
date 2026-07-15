# Design Spec: UHP Transformations Page

**Date:** 2026-07-15  
**Status:** Approved by User  
**Author:** Antigravity AI  

---

## 1. Objective
Build a dedicated results page (`transformations.html`) featuring real client case studies in a timeline journey grid format to build credibility and trust. Integrate navigation links into the headers and footers across all site files.

---

## 2. Page Architecture & Design System
The new page will be built as a standalone static file `transformations.html` in the project root. It will share the global assets and styling properties of the main project:
*   **Fonts:** `Barlow Condensed` (headers) and `Inter` (body/copy).
*   **Color Theme:** Dark backgrounds (`var(--bg)` / `#080808`), surface cards (`var(--surface)` / `#111111`), borders (`var(--border)` / `rgba(255,255,255,0.08)`), and brand gold accents (`var(--gold)` / `#c9a84c`).
*   **Responsive Layout:** Alternates to single-column stacking below `900px` screen width.

---

## 3. Transformations Page Layout (`transformations.html`)

### 3.1. Page Header & Hero Section
*   **Navigation Header:** Match the existing global navigation header containing UHP logo, links to Home (`index.html`), Programs (`services.html`), About (`about.html`), Journal (`blog.html`), Transformations (`transformations.html` - set as active), and Book a Call button.
*   **Hero Text:**
    *   Subtitle label: "Rigorous Results" (uppercase, Gold color)
    *   H1 Main Title: "Systematic Transformations"
    *   Lede Paragraph: "Every transformation is a case study in consistency. We systematise health and habit structures to ensure weight loss, peak focus, and lasting Company ROI."
*   **Scoreboard Card Grid (`.mock-board`):**
    *   Avg Fat Loss: `11kg`
    *   Improved Daily Focus: `94%`
    *   Habit Consistency: `91%`

### 3.2. Narrative Timelines (Timeline Journey Grid)
*   **Wrapper Grid (`.journey-item`):** Grid layout splitting profile card and timeline flow:
    *   Desktop: `grid-template-columns: 1fr 1.6fr; gap: 64px;`
    *   Mobile (<= 900px): `grid-template-columns: 1fr; gap: 32px;`
*   **Profile Card (`.journey-profile`):**
    *   Desktop: Sticky behavior (`position: sticky; top: 120px;`) so it stays visible while scrolling the timeline.
    *   Includes: Case Study indicator tag, client name, business role, testimonial quote block, and a small key results list (e.g. Initial vs current weight, compliance rates).
*   **Timeline Flow (`.timeline-flow`):**
    *   Vertical border line (`border-left: 2px solid var(--border)`).
    *   Timeline nodes (`.timeline-node`) styled with absolute positioned circle badges matching the custom pillar theme color.

---

## 4. Case Studies Data & Copy

### 4.1. Case Study 01: Marcus B.
*   **Theme Color:** `#eb6826` (Orange / Healthy Eating & Supplementation focused)
*   **Profile Info:**
    *   Name: Marcus B.
    *   Role: Founder · Technology Company
    *   Quote: "Down 13 kg in 14 weeks and my energy in back-to-back meetings is night and day. I used to crash by 2 pm; now I'm running my best sessions at the end of the day."
    *   Initial Weight: `98 kg`
    *   Current Weight: `85 kg`
    *   12-Wk Compliance: `93%`
*   **Timeline Journey:**
    *   **Week 0: The Friction:** Slipping physical leadership. Exhaustion by early afternoon, heavy decision fatigue on meal choices, and skipping meals entirely on client weeks.
    *   **Weeks 1–4: Anchors:** Low-fatigue breakfast structures. Implemented daily breakfast smoothie replacements and context-aware text checks with UHP Coach to audit travel meals.
    *   **Weeks 5–12: Result:** 13kg down & peak performance. Energy night and day. Daily fat loss stabilized with macro adjustments. Executive team noticed the shift in meetings.

### 4.2. Case Study 02: James S.
*   **Theme Color:** `#00a8b5` (Teal / Fitness & Coach focused)
*   **Profile Info:**
    *   Name: James S.
    *   Role: Owner · Marketing Agency
    *   Quote: "I've tried every approach. The difference here is the system fits around my week — it doesn't expect a version of me that doesn't exist."
    *   Initial Weight: `92.5 kg`
    *   Current Weight: `82 kg`
    *   12-Wk Compliance: `95%`
*   **Timeline Journey:**
    *   **Week 0: The Friction:** Routine clash & joint fatigue. Failed previous strict gym routines due to 10-hour days. Experienced persistent lower back and knee pain from sitting.
    *   **Weeks 1–4: Anchors:** Functional active movement. Began 30-minute joint-friendly strength training templates and daily step audits. Replaced heavy commercial gym goals.
    *   **Weeks 5–12: Result:** Sharp in boardroom & active with family. Fat loss goal reached. Completely resolved back pain through targeted mobility. Reclaimed high focus at work and presence with kids.

### 4.3. Case Study 03: Anika K.
*   **Theme Color:** `#79bc43` (Green / Supplementation & Travel focused)
*   **Profile Info:**
    *   Name: Anika K.
    *   Role: Executive Director · Investment Firm
    *   Quote: "I travel every second week. Every other coach I'd tried just told me to 'eat well' when I fly. UHP built specific protocols for airports, hotel rooms, and client dinners before I even asked."
    *   Initial Weight: `74 kg`
    *   Current Weight: `64 kg`
    *   12-Wk Compliance: `91%`
*   **Timeline Journey:**
    *   **Week 0: The Friction:** Airport & client dinners chaos. Frequent travel schedules disrupted regular eating. Airplane food, late dinners, and business dining caused poor recovery and weight gain.
    *   **Weeks 1–4: Anchors:** Done-for-you travel protocols. Customized low decision-fatigue travel checklists. Added on-the-go protein packs and pre-flight nutrient guidelines.
    *   **Weeks 5–12: Result:** 10kg fat loss & energy consistency. Reached target weight. Replaced airplane snacks with high-protein alternatives. Consistent energy levels regardless of travel time zones.

---

## 5. Site Navigation Integration

### 5.1. Global Header Navigation
Include the transformations link in the navigation menus (`index.html`, `about.html`, `services.html`, `blog.html`, `contact.html`):
```html
<nav class="nav-links">
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
  <a href="services.html">Programs</a>
  <a href="transformations.html">Transformations</a>
  <a href="blog.html">Journal</a>
  <a href="contact.html">Contact</a>
</nav>
```

### 5.2. Footer Integration
Add the transformations link to the footers in all HTML files:
```html
<div class="ft-col">
  <h6>Navigate</h6>
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
  <a href="services.html">Programs</a>
  <a href="transformations.html">Transformations</a>
  <a href="blog.html">Journal</a>
  <a href="contact.html">Contact</a>
</div>
```

---

## 6. Spec Self-Review
1. **Placeholder scan:** Exact metrics, weight details, and testimonial quotes are fully specified.
2. **Internal consistency:** Anchor IDs, filenames, and page titles align perfectly.
3. **Scope check:** Bounded exclusively to the new page creation and site navigation links updates.
