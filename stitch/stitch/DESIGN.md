# Design System Document: Haute Horlogerie Digital Excellence

## 1. Overview & Creative North Star: "The Digital Curator"
This design system is engineered to transform a standard e-commerce interface into a curated, gallery-like experience. The Creative North Star, **"The Digital Curator,"** dictates that every pixel must feel intentional, rare, and silent. 

We break the "template" look by moving away from rigid, boxed grids in favor of **Intentional Asymmetry**. Imagine a high-end editorial spread: large-scale typography may overlap cinematic imagery, and white space (or "dark space") is treated as a premium material itself. This system rejects the cluttered "buy now" mentality, replacing it with a "discover the heritage" journey.

---

## 2. Colors & Atmospheric Depth
Our palette is rooted in the "Deep Obsidian" of a luxury watch presentation box, accented by the "Metallic Gold" of movement gears.

### The Palette (Material Design Tokens)
*   **Primary (Gold):** `#F2CA50` (Interactive) / `primary_container`: `#D4AF37` (Heritage Gold)
*   **Surface (Obsidian):** `#131313` (Base) / `surface_container_lowest`: `#0E0E0E` (Deep Depth)
*   **Secondary (Royal Navy):** `secondary_container`: `#2A4386` (Subtle Depth)
*   **On-Surface (Luminous White):** `#E5E2E1`

### Signature Rules
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Contrast must be achieved through background shifts. For example, a `surface_container_low` section should sit against a `surface` background to define boundaries.
*   **Surface Hierarchy:** Use nested tiers to create physical depth. A product spotlight should live on a `surface_container_high` card, floating over a `surface_dim` background. 
*   **The "Glass & Gradient" Rule:** Use Glassmorphism for floating navigation and overlays. Use a backdrop-blur (20px+) with a 10% opacity `surface_variant` fill. 
*   **Signature Textures:** For primary CTAs, apply a subtle linear gradient from `primary` (#F2CA50) to `primary_container` (#D4AF37) at a 135-degree angle to mimic the sheen of polished 18k gold.

---

## 3. Typography: The Editorial Voice
Typography is our primary vehicle for conveying prestige. We mix architectural stability with cursive elegance.

*   **Display (Cinzel):** Used for "Monumental" moments. Use `display-lg` for collection titles. This font represents the stone-carved heritage of Jerusalem.
*   **Headline (Playfair Display Italic):** Used for "The Human Touch." Apply to `headline-md` for storytelling and philosophical quotes. It breaks the rigidity of the grid with its organic curves.
*   **Body & Labels (Heebo/Manrope):** Used for "Modern Clarity." All technical specifications and price points must use `body-md` or `label-md` for maximum legibility against dark backgrounds.
*   **Hierarchy Note:** Always pair a `display-lg` (Cinzel) title with a small `label-md` (Heebo) uppercase tagline above it (spaced at `spacing-3`) to create an authoritative, editorial look.

---

## 4. Elevation & Depth: Tonal Layering
In Haute Horlogerie, we do not use "drop shadows"; we use **Ambient Occlusion**.

*   **The Layering Principle:** Stack `surface_container` tiers. A `surface_container_lowest` inset area on a `surface` background creates a "carved out" look, perfect for technical spec sheets.
*   **Ambient Shadows:** When a card must float (e.g., a "Quick View"), use a shadow with a 40px blur, 0px spread, and 6% opacity, tinted with `on_secondary` (#0D2C6E) to create a "cool" obsidian glow rather than a muddy grey.
*   **The "Ghost Border":** For buttons or inputs, use a 1px border with `outline_variant` at 15% opacity. It should feel like a whisper, only visible when the light hits it.
*   **Glassmorphism:** Apply to the Header and Filter panels. Use `surface_container_highest` at 40% opacity with a `backdrop-filter: blur(12px)`.

---

## 5. Components: The Bespoke Toolkit

### Buttons (The "Jewel" Interaction)
*   **Primary:** Solid Gold Gradient (`primary` to `primary_container`). Sharp corners (`rounded-none` or `sm: 0.125rem`). Text in `on_primary` (Dark Obsidian).
*   **Secondary:** Ghost style. `outline_variant` border at 20% opacity. On hover, the border opacity increases to 100%.
*   **Micro-interaction:** On hover, buttons should have a subtle "shimmer" effect—a white linear gradient mask moving from left to right.

### Input Fields & Selectors
*   **The "Minimalist" Input:** No box. Only a bottom border using `outline_variant`. On focus, the border transitions to `primary` (Gold).
*   **Checkboxes/Radios:** Must be custom-styled. Use `primary_container` for the "checked" state. Avoid standard OS styling.

### Cards & Lists
*   **The "No-Divider" Rule:** Never use horizontal lines to separate list items. Use `spacing-8` (2.75rem) of vertical white space or a subtle background shift to `surface_container_low`.
*   **Product Cards:** Use `surface_container_lowest` for the image container to create a "shadowbox" effect for the watch photography.

### Additional Signature Components
*   **Cinematic Video Backgrounds:** Use low-contrast, slow-motion macro shots of watch movements behind `display-lg` typography. Apply a `surface_dim` overlay at 60% to ensure legibility.
*   **Scroll-Triggered Parallax:** Image elements should move at a 0.9x speed relative to text to create a sense of three-dimensional depth.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use extreme letter-spacing (0.1em to 0.2em) for `label-sm` text to increase the "luxury" feel.
*   **Do** allow images to bleed off the edge of the screen to break the "contained" feel of a website.
*   **Do** use `secondary_container` (Royal Navy) for deep background sections to prevent the site from looking purely monochromatic.

### Don't:
*   **Don't** use standard "Blue" for links. All interactions are `primary` (Gold) or `on_surface` (White).
*   **Don't** use rounded corners above `sm` (0.125rem) for main UI elements. Sharpness equates to precision engineering.
*   **Don't** crowd the interface. If a section feels "full," double the spacing using the `20` or `24` spacing tokens.
*   **Don't** use pure `#000000` black. Use `surface_container_lowest` (#0E0E0E) to maintain texture and depth.