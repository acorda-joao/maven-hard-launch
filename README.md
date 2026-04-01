# Maven Hard Launch — Landing Page Prototypes

Two high-fidelity interactive prototypes for Maven's "Learn from Humans" campaign landing page.

## The Project

Maven is launching a major campaign to drive 100K student leads. The funnel:
```
Video ("Learn from humans") → Landing Page → Email Capture → Personalized Skills Report
```

The landing page is the bridge between the video and the report. It needs to:
1. **Clear value prop** — What do I get for my email?
2. **Show instructors** — Real faces, real credentials
3. **Show categories** — "This covers MY field"
4. **Convert** — Email capture, prominent and frictionless

## Two Prototypes to Build

### Option A: The Human Wall (`option-a/`)

**Conversion logic:** Belonging + breadth. You see the people, you're impressed, you want in.

**Layout (desktop 1440px):**
- **Nav bar:** Logo left, 7 role pills right (Product, Engineering, Design, Marketing, Sales, Leadership, Founders)
- **Split layout:** Left 420px for copy stack, right fills with staggered face grid
- **Left side (top to bottom):**
  - "Learn" (white)
  - "[Role Name]" (brand-light blue #7CBEFF) — rotates when pills change
  - "from humans." (white)
  - Skill tags row (6 tags showing skills within the active role)
  - Supporting copy: "The irreplaceable skills of 2026 — taught by the experts who've mastered them."
  - Email input + "Get your report" button
- **Right side:**
  - 4-column staggered grid of instructor photo cards
  - Each card: photo background, name + skill label at bottom
  - Columns offset vertically (-20px, +30px, -10px, +20px) for visual energy
  - Cards overflow viewport top/bottom (implies "there are more")
  - When role pill changes: all faces swap to that role's instructors, skill tags update

**Interaction:**
- Role pills are clickable — switching roles changes: hero text, skill tags, instructor grid
- Auto-rotation every 5 seconds through all roles
- Pause on interaction, resume after 12 seconds
- Photo transitions: ideally use dither/pixel dissolve effect (Maven brand element)

**Key UX detail:** The category pills act as a horizontal organizer. When "Product" is active, all content is Product. Click "Engineering" — hero says "Learn Engineering from humans", skill tags show Engineering skills, faces swap to Engineering instructors.

### Option B: The Curtain (`option-b-photo/` and `option-b-grid/`)

**Conversion logic:** Curiosity + value. The report is the prize, the faces are proof.

**Two sub-versions with the same layout but different backgrounds:**

**option-b-photo:** Instructor photos as a faded grid behind the centered content (opacity ~0.15-0.2). The faces create subconscious human presence without competing with the text.

**option-b-grid:** Maven's architectural grid pattern as the background, with color gradients (radial glows in lapis blues). Inspired by the expert pages hero section. Cleaner, brand-forward.

**Layout (both versions, desktop 1440px):**
- **Nav bar:** Logo left, "LEARN FROM HUMANS" tagline right
- **Centered stack (top to bottom):**
  - "The irreplaceable skills" (white, headline-xl)
  - "of 2026" (brand-light blue, headline-xl)
  - Supporting copy: "The skills reshaping your career. The experts who teach them. Your personalized report, built by Maven."
  - Email input + "Get your report" button
  - 7 role pills (centered row)
- **Below the fold (scrollable):**
  - Full-width instructor face strip (5-7 cards per row, with name + skill label)
  - Report preview section: race chart bars + skill map circle (faded, teaser)

## Content & Data

### Roles (what rotates in the hero)
7 roles: Product, Engineering, Design, Marketing, Sales, Leadership, Founders

### Data files (`data/`)
- `pm-skills-taxonomy.json` — Skills with experts, lightning lessons, courses per skill
- `pm-experts.json` — 10 featured experts with name, credential, tag, bio
- `pm-race-data.json` — 5-year skill trend data (for race chart visualization)
- `reimbursement-data.json` — Reimbursement rates by function/seniority

### PM Role Content (fully built — use as prototype content)

**10 Featured Instructors:**
| Name | Skill | Credential |
|------|-------|-----------|
| Shreyas Doshi | Product Sense | $7.2M GMV, Ex-Stripe |
| Hamel Husain | AI Evals | $5.1M GMV |
| Product Faculty | AI PM | $4.3M GMV, 68K learners |
| Marily Nika | AI Products | Google Gen AI PM Lead |
| Aishwarya Reganti | Agentic AI | $1.9M GMV, 96K learners |
| Mahesh Yadav | Product Sense | 172K learners |
| Ethan Evans | Executive Influence | Ex-Amazon VP, $1.1M GMV |
| Wes Kao | Exec Communication | Maven Co-founder, $1.2M GMV |
| Colin Matthews | Vibe Coding | $727K GMV |
| Ronny Kohavi | AI Evals | A/B Testing pioneer, $463K GMV |

**PM Skills (shown as tags):**
Product Sense, AI Product Management, Agentic AI, Executive Communication, Vibe Coding, AI Evals, Stakeholder Management, User Research, Data Analysis, Go-to-Market

### Instructor Images (`images/`)
37 photos available. Key ones for PM prototype:
- `shreyas-doshi.png`, `hamel-husain.jpg`, `marily-nika.jpg`
- `ethan-evans.jpg`, `colin-matthews.png`, `aishwarya-reganti.jpg`
- `mahesh-yadav.png`, `ronny-kohavi.jpg`, `annie-duke.jpg`
- `dave-kline.jpg`, `jason-liu.png`, `jess-goldberg.jpg`

## Copy

### Option A hero:
```
Learn
[Product Management]     ← rotates per role, color: #7CBEFF
from humans.
```

### Option A supporting:
```
The irreplaceable skills of 2026 — taught by the experts who've mastered them.
```

### Option B hero:
```
The irreplaceable skills
of 2026                  ← color: #7CBEFF
```

### Option B supporting:
```
The skills reshaping your career. The experts who teach them.
Your personalized report, built by Maven.
```

### CTA button: `Get your report`
### Email placeholder: `Enter your email`

## Design System

### Fonts
- **Headlines:** STK Bureau Serif, weight 300 (Light)
- **Body/UI:** STK Bureau Sans, weights 400/500/600

### Colors
| Token | Hex | Usage |
|-------|-----|-------|
| lapis-900 | #080c28 | Page background |
| lapis-800 | #101b57 | Grid pattern, card backgrounds |
| lapis-500 | #1e51ca | Primary blue, active states |
| lapis-400 | #2465e8 | Accent blue |
| brand-light | #7CBEFF | CTA button, hero accent text |
| lapis-100 | #b2d3fa | Light text accents |
| brand-highlight | #CDFF92 | Green accent (sparingly) |

### Grid Pattern
CSS background pattern with 90px cells, color #101b57 at 40% opacity. See `shared/styles.css` `.grid-pattern` class.

### Gradients (from expert pages)
- **Fade down:** Multi-stop linear gradient for grid fade-out
- **Glow top:** Radial gradient, rgba(28,54,141,0.4) center
- **Glow bottom:** Radial gradient, rgba(28,54,141,0.35) center
See `shared/styles.css` for exact values.

## Technical Approach

- **Pure HTML/CSS/JS** — No build step, no framework
- **Single HTML file per prototype** — self-contained, easy to share
- **Link to `shared/styles.css`** for design tokens
- **Load data from `data/*.json`** via fetch
- **Deploy to GitHub Pages** — each option as a separate route

### File structure per prototype:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Maven — Learn from Humans</title>
  <link rel="stylesheet" href="../shared/styles.css">
  <style>/* Prototype-specific styles */</style>
</head>
<body>
  <!-- Prototype content -->
  <script>/* Interaction logic + data loading */</script>
</body>
</html>
```

## Reference

- Paper wireframes: See `reference/wireframes.md`
- Session documentation: See project vault at `Maven/Hard Launch/6. Session - Strategic Redesign & Layout Decisions.md`
- Expert pages (design reference): https://maven-expert-pages.vercel.app/experts/joao-ventura
- Experts report (data source): https://github.com/rqcai200/experts-report
