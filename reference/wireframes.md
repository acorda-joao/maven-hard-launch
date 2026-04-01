# Wireframe Specifications

Layout specs extracted from Paper explorations (file: "hard launch", pages: "Refinament" and "Improvment").

## Option A — The Human Wall (A3v2)

### Desktop (1440 x 900)
```
┌─────────────────────────────────────────────────────────────────┐
│ [Logo]                    [Product] [Eng] [Design] [Mkt] [...] │  ← 24px padding, pills right
│                                                                 │
│                     ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐        │
│                     │      │ │      │ │      │ │      │        │  ← 4 cols, staggered vertically
│  Learn              │ Face │ │      │ │ Face │ │ Face │        │     offsets: -20, +30, -10, +20
│  [Product           │      │ │ Face │ │      │ │      │        │
│   Management]       ├──────┤ │      │ ├──────┤ ├──────┤        │
│  from humans.       │      │ ├──────┤ │      │ │      │        │
│                     │ Face │ │      │ │ Face │ │ Face │        │
│  [tag] [tag] [tag]  │      │ │ Face │ │      │ │      │        │
│  [tag] [tag] [tag]  ├──────┤ │      │ ├──────┤ ├──────┤        │
│                     │      │ ├──────┤ │      │ │      │        │
│  Value prop text    │      │ │      │ │      │ │ Face │        │
│                     │      │ │      │ │      │ │      │        │
│  [email] [CTA]      └──────┘ └──────┘ └──────┘ └──────┘        │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Dimensions
- Left column: 420px width, padded 56px from left
- Right column: flex fills remaining space
- Gap between left and right: 40px
- Face grid: 4 columns, 10px gap between cards
- Card aspect ratio: 3:4
- Card border radius: 6px
- Nav padding: 24px vertical, 56px horizontal
- Pill gap: 5px

### Typography (left side)
- "Learn" / "from humans.": headline-lg (56px), weight 300, white
- "[Role]": headline-lg (56px), weight 300, #7CBEFF
- Skill tags: 11px, pill-style with light blue border
- Value prop: 16px, rgba(255,255,255,0.4)
- Tag gap: 6px, wrapping

## Option B — The Curtain

### Desktop (1440 x 900) — Above the fold
```
┌─────────────────────────────────────────────────────────────────┐
│ [Logo]                                    LEARN FROM HUMANS     │
│                                                                 │
│                                                                 │
│              The irreplaceable skills                           │  ← headline-xl, centered
│                    of 2026                                      │  ← #7CBEFF
│                                                                 │
│         The skills reshaping your career.                       │  ← 16px, centered, muted
│         The experts who teach them.                             │
│         Your personalized report, built by Maven.               │
│                                                                 │
│              [email input] [Get your report]                    │  ← centered
│                                                                 │
│       [Product] [Eng] [Design] [Mkt] [Sales] [Lead] [Found]    │  ← pills, centered
│                                                                 │
│  ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌────┐ │
│  │ Face │ │ Face │ │ Face │ │ Face │ │ Face │ │ Face │ │Face│ │  ← face strip, 7 cards
│  │      │ │      │ │      │ │      │ │      │ │      │ │    │ │     with name + skill
│  └──────┘ └──────┘ └──────┘ └──────┘ └──────┘ └──────┘ └────┘ │
└─────────────────────────────────────────────────────────────────┘
```

### Below the fold (scroll)
```
┌─────────────────────────────────────────────────────────────────┐
│                    Report Preview (faded)                        │
│                                                                 │
│  THE SKILLS RACE — 2026           ┌─────────────────────┐       │
│  AI Product Mgmt  ████████████    │    ○ ○              │       │
│  Vibe Coding      ██████████      │   ○   ○  Skill Map  │       │
│  Product Sense    ████████        │    ○ ○              │       │
│  Agentic AI       ██████          └─────────────────────┘       │
│  Exec Comms       ████                                          │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Background treatments
**B-photo:** Grid of instructor photos, heavily faded (opacity 0.12-0.18), desaturated, as CSS background
**B-grid:** Maven grid pattern (90px cells, #101b57) with radial gradient glows:
- Top center: rgba(28,54,141,0.4) ellipse
- Bottom center: rgba(28,54,141,0.35) ellipse

### Dimensions
- Max content width: centered, ~900px for text content
- Face strip: full width minus 56px padding each side
- Face cards: equal width, 8px gap, min-height 140px, border-radius 8px
- Report preview: full width minus 56px padding, opacity 0.5, border-radius 12px
- Headline: 76px on desktop, 48px on mobile
- Pill row gap: 5px
- Vertical spacing between sections: 16-20px
