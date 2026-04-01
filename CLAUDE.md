# Maven Hard Launch Prototypes

Read `README.md` first — it contains the complete build brief with layout specs, copy, data references, and design tokens.

## Quick Reference

- **Fonts:** `fonts/` — STK Bureau Serif (Light 300, Book 400) + STK Bureau Sans (Book 400, Medium 500, SemiBold 600)
- **Colors:** See `shared/styles.css` — lapis palette, all CSS custom properties
- **Data:** `data/` — JSON files with skills taxonomy, experts, race chart data
- **Images:** `images/` — 37 instructor photos (JPG/PNG)
- **Design reference:** https://maven-expert-pages.vercel.app/experts/joao-ventura

## Build Rules

- Pure HTML/CSS/JS — no build step, no framework
- Single HTML file per prototype, linking to `shared/styles.css`
- Load data via fetch from `data/` directory
- All instructor cards must show: photo, name, skill label
- Hero headline font: STK Bureau Serif, weight 300, with `font-feature-settings: 'ss01' 1`
- Background: always #080c28 (lapis-900)
- CTA button: always #7CBEFF (brand-light) with #080c28 text
- Grid pattern: 90px cells, color #101b57

## The Two Prototypes

1. **Option A** (`option-a/index.html`): Split layout, face wall right, role rotation drives content changes
2. **Option B** (`option-b-photo/index.html`): Centered layout, faded instructor photo grid as background
3. **Option B** (`option-b-grid/index.html`): Centered layout, Maven grid pattern as background with gradients

See README.md for detailed layout specs and interaction requirements.
