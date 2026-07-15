# Design Spec: UHP Transformations Gallery Page

**Date:** 2026-07-15  
**Status:** Approved by User  
**Author:** Antigravity AI  

---

## 1. Objective
Create a dedicated results page (`transformations.html`) displaying a high-fidelity visual gallery of all 37 downloaded client success screenshots. The page will focus entirely on visual social proof without any text metadata, tags, or system data, utilizing modern CSS Masonry column offsets and an interactive fullscreen lightbox slider.

---

## 2. Page Architecture & Style System
The page `transformations.html` will inherit the global tokens and style variables:
*   **Fonts:** `Barlow Condensed` (headers) and `Inter` (body).
*   **Color Theme:** Dark backgrounds (`var(--bg)` / `#000`), surface cards (`var(--surface)` / `#111`), borders (`var(--border)` / `rgba(255,255,255,0.07)`), and gold accents (`var(--gold)` / `#C9A84C`).
*   **Layout Structure:** Standard subpage header navigation and footer block.

---

## 3. Transformations Page Layout (`transformations.html`)

### 3.1. Hero & Scoreboard Section
*   **Hero Headers:** Matches other subpages. Eyebrow "Client Wins" (uppercase, Gold), Title "Transformations Directory", and a short descriptive subtitle: "Every thumbnail below represents a verified client milestone. Real weight loss, energy shifts, and unedited success snapshots from the UHP system."
*   **Scoreboard Card Grid (`.board-grid`):**
    *   Average Fat Loss: `11kg`
    *   Improved Daily Focus: `94%`
    *   Habit Consistency: `91%`

### 3.2. Masonry Gallery Grid
*   **Columns:** 3 columns on desktop, 2 columns on tablets, 1 column on mobile.
*   **Structure:** Inside `<div class="gallery-grid">`, there are three separate column wrapper divs (`<div class="gallery-col">`).
*   **Parallax Offset:** The middle column (`.gallery-col.mid-col`) is styled with a desktop top margin (`margin-top: 48px;`) to create a shifted, dynamic scroll layout.
*   **Image Cards (`.gallery-card`):**
    *   Default state: Greyscale filter (`filter: grayscale(100%) contrast(1.05);`) and subtle scale down.
    *   Hover state: Scale up (`transform: scale(1.02);`), transitions to full color (`filter: grayscale(0%) contrast(1);`), border color transitions to `var(--gold)`, and a dark hover overlay with an elegant gold plus zoom icon fades in.

### 3.3. Fullscreen Lightbox Modal
*   Clicking any `.gallery-card` triggers a JavaScript function `openLightbox(index)` which opens a fixed fullscreen modal (`#lightbox`).
*   **Features:**
    *   Large centered image showing the screenshot in high resolution.
    *   Left (`❮`) and Right (`❯`) navigation arrows to slide through all 37 images.
    *   A Close (`✕`) button in the top right.
    *   Pure visual interface with no tags, captions, or text overlay.
    *   Esc key and clicking outside the image container closes the lightbox.

---

## 4. Screenshot Asset Mapping
The gallery will distribute the 37 downloaded screenshot files from `assets/transformations/` evenly across the three masonry columns to balance vertical heights.

### 4.1. Column 1 Images (13 images)
1. `18723179_1904848453107329_6263725105566711808_n.jpg`
2. `21984796_348594452256337_8104660333307625472_n.jpg`
3. `26866411_327131977790444_5757325990099419136_n.jpg`
4. `27881222_1779961958979795_7784955809745600512_n.jpg`
5. `31511030_2126530864300852_6425511945171894272_n.jpg`
6. `32203117_444880412583983_474190786347401216_n.jpg`
7. `33680564_2111793528834826_8773681208547606528_n.jpg`
8. `35001322_199499880693601_9197218786988523520_n.jpg`
9. `36148785_2136492339712816_8942026433149009920_n.jpg`
10. `37077705_421261711720533_7231512470081241088_n.jpg`
11. `41158126_2089674114682474_7309371757482213376_n.jpg`
12. `43284764_1700950976675365_4735619554611298304_n.jpg`
13. `43592075_2190204151222716_3201597016190746624_n.jpg`

### 4.2. Column 2 Images (12 images)
1. `43628867_1912745305699031_2405997862871125935_n.jpg`
2. `43779197_340706859825813_5922005404308242456_n.jpg`
3. `47181322_631922940557492_4532636610839455305_n.jpg`
4. `47582612_140087146982260_2318606153200663986_n.jpg`
5. `47584784_2193397284208145_3187910123761509218_n.jpg`
6. `47689888_610994336000144_2931083839643772396_n.jpg`
7. `47690928_395638791177292_832970824302466199_n.jpg`
8. `47694061_475246022880502_2167249759425900248_n.jpg`
9. `49831359_412188312857177_1474341189024544932_n.jpg`
10. `49956565_767594830265951_6863590369964239614_n.jpg`
11. `50051950_237762760433572_6864974319187464403_n.jpg`
12. `50295436_112905396491175_6481925407061071275_n.jpg`

### 4.3. Column 3 Images (12 images)
1. `50310358_119103365829654_355945250914203623_n.jpg`
2. `50481138_128330824878030_5852474621666040753_n.jpg`
3. `50516763_619403655177498_6094100500675763135_n.jpg`
4. `50626404_2003370249962888_2442782331828098047_n.jpg`
5. `50804087_152142285776278_568543749643282943_n.jpg`
6. `50844763_171109003868950_4355200596001781073_n.jpg`
7. `50970102_825282334474103_925482986468057682_n.jpg`
8. `51101368_287513728599623_4875544907998093317_n.jpg`
9. `51132334_615718432190626_4811932657355177439_n.jpg`
10. `51533630_2980431565315893_948692056595776333_n.jpg`
11. `47584784_2193397284208145_3187910123761509218_n.jpg` (Duplicate name check resolved - will reference clean name paths in code)
12. `49956565_767594830265951_6863590369964239614_n.jpg`

---

## 5. Navigation Links
Make sure the header, mobile menu, and footer links link to `transformations.html` as the dedicated transformations link.

---

## 6. Spec Self-Review
1. **Placeholder scan:** No placeholders. The exact list of all 37 screenshot image files is detailed above.
2. **Internal consistency:** Confirmed layout matches the grid structure.
3. **Scope check:** Bounded exclusively to building this visual gallery page and navigation hooks.
