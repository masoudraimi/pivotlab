# PivotLab Design System

## 1. Visual Theme & Atmosphere

PivotLab's design language is warm, credible, and purposefully playful. It borrows from the Clay design system: a cream canvas with named swatch sections, bold compressed typography, and signature hover animations that give the interface a physical, craft-like quality. The goal is to feel like a trusted human organisation, not a generic edtech SaaS product.

Each major page section uses a distinct full-bleed swatch color as its "room", creating strong visual rhythm as users scroll. Color is not decorative — it encodes meaning: Ube (purple) signals tension and problem framing, Matcha (green) signals growth and enablement, Lemon (gold) signals financial warmth and access, Slushie (cyan) signals clarity and action.

**Key Characteristics:**
- Warm cream canvas (`#faf9f7`) with oat-toned borders (`#dad4c8`) — artisanal, not clinical
- Named swatch palette used for full-section backgrounds, not small accents
- Roobert font with 5 OpenType stylistic sets for headings — quirky geometric character
- Space Mono for stats, monospace labels, and quotation marks
- Playful hover animations: `rotateZ(-8deg)` + upward translate + hard offset shadow `rgb(0,0,0) -7px 7px`
- Generous border radius: 24px cards, 40px sections, 1584px pill buttons
- Mixed border styles: solid oat borders + dashed borders for secondary containers
- Multi-layer clay shadow: `rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset, rgba(0,0,0,0.05) 0px -0.5px 1px`

---

## 2. Color Palette

### Base

| Name | Hex | Role |
|------|-----|------|
| Cream | `#faf9f7` | Page background — non-negotiable warm canvas |
| Black | `#000000` | Primary text, headings, buttons |
| White | `#ffffff` | Card backgrounds, inverse text, button fills |
| Warm Silver | `#9f9b93` | Secondary/muted text, labels, footer copy |
| Warm Charcoal | `#55534e` | Body text, descriptions, tertiary content |
| Oat Border | `#dad4c8` | Primary border — warm, cream-toned structural lines |
| Oat Light | `#eee9df` | Secondary lighter border, dividers |

### Swatch Palette

**Matcha (Green)** — growth, enablement, success
| Stop | Hex | Use |
|------|-----|-----|
| 300 | `#84e7a5` | Light accent, highlight text on dark green, cost-total background |
| 600 | `#078a52` | Button hover, positive values, cost-total text |
| 800 | `#02492a` | Full section background (pillars section) |

**Slushie (Cyan)** — clarity, action, CTA
| Stop | Hex | Use |
|------|-----|-----|
| 500 | `#3bd3fd` | Accent text on dark cyan backgrounds, ticker dots |
| 800 | `#0089ad` | Full section background (CTA section) |

**Lemon (Gold)** — financial access, warmth, highlights
| Stop | Hex | Use |
|------|-----|-----|
| 400 | `#f8cc65` | Hero text highlight, badge background, button hover fill |
| 500 | `#fbbd41` | Nav logo dot, primary gold accent |
| 700 | `#d08a11` | Label text on Lemon backgrounds |

**Ube (Purple)** — problem framing, tension, urgency
| Stop | Hex | Use |
|------|-----|-----|
| 300 | `#c1b0ff` | Accent text on dark purple, stat numbers in problem section |
| 800 | `#43089f` | Button hover background (nav CTA) |
| 900 | `#32037d` | Full section background (problem section) |

**Pomegranate (Pink)**
| Stop | Hex | Use |
|------|-----|-----|
| 400 | `#fc7981` | Ticker dot accent only |

### Shadow System

| Name | Value | Use |
|------|-------|-----|
| Clay Shadow | `rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset, rgba(0,0,0,0.05) 0px -0.5px 1px` | Cards, stat blocks, partner tags |
| Hard Offset | `rgb(0,0,0) -7px 7px` | Button hover state — the signature interaction |

---

## 3. Typography

### Font Families

| Family | Use |
|--------|-----|
| `Roobert` (fallback: `Arial`) | All UI text — headings, body, buttons, labels |
| `Space Mono` | Stats, monospace accents, testimonial quote marks |

**Roobert license note:** Roobert is a commercial font. Purchase and self-host WOFF2 files for production. The fallback to Arial renders cleanly but loses the OpenType personality.

**OpenType Stylistic Sets:**
- Headings: `"ss01","ss03","ss10","ss11","ss12"` (all 5)
- Body/UI: `"ss03","ss10","ss11","ss12"` (4 sets, omit ss01)

### Type Scale

| Role | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|--------|-------------|----------------|-------|
| Display Hero | `clamp(52px, 6.5vw, 80px)` | 700 | 1.0 | -3px | Page H1 only |
| Section Heading | `clamp(36px, 4vw, 52px)` | 700 | 1.05 | -1.5px | H2 in all sections |
| Card Title | 22px | 700 | 1.1 | -0.4px | Step titles, pillar titles |
| Feature Title | 18px | 700 | 1.2 | -0.3px | Pillar titles, persona names |
| Body Large | 20px | 400 | 1.5 | normal | Hero subtitle |
| Body | 16px | 400 | 1.65 | normal | Step descriptions, card body |
| Body Small | 15px | 400 | 1.65 | normal | Testimonial text, fin options |
| Nav Link | 15px | 500 | 1.6 | normal | Navigation |
| Button Primary | 16px | 700 | 1.5 | -0.2px | All CTA buttons |
| Button Nav | 15px | 600 | 1.5 | -0.2px | Nav CTA |
| Caption | 14px | 400 | 1.5 | normal | Stat labels, cost items |
| Uppercase Label | 12px | 700 | 1.2 | 1.08px | Section wayfinding, `text-transform: uppercase` |
| Badge | 12px | 700 | 1.2 | 0.8px | Hero badges, uppercase |
| Mono Stat | 28px | 700 | 1.1 | normal | Hero stat numbers (Space Mono) |
| Mono Large | 48px | 700 | 1.0 | normal | Problem section stats (Space Mono) |
| Mono Quote | 36px | 400 | 1.0 | normal | Testimonial quotation mark (Space Mono) |

### Principles

- **Three weights only:** 700 headings, 500–600 UI/buttons, 400 body. Never use 300.
- **Aggressive display compression:** -3px at display scale creates billboard-like punch.
- **Uppercase labels with positive tracking:** 12px + 1.08px letter-spacing is the wayfinding system used consistently before every section heading.
- **Space Mono for numbers:** Any statistic, metric, or monospaced element uses Space Mono to signal precision and data credibility.

---

## 4. Component Styles

### Buttons

**Primary (Black Pill)**
```css
background: #000000;
color: #ffffff;
font-size: 16px;
font-weight: 700;
padding: 14px 28px;
border-radius: 1584px;
transition: background 0.15s, transform 0.2s, box-shadow 0.2s;

/* Hover */
background: #078a52; /* Matcha 600 */
transform: rotateZ(-8deg) translateY(-6px);
box-shadow: rgb(0,0,0) -7px 7px;
```

**Ghost (Outlined Pill)**
```css
background: transparent;
color: #000000;
border: 1px solid #dad4c8;
font-size: 16px;
font-weight: 700;
padding: 14px 28px;
border-radius: 1584px;

/* Hover */
background: #f8cc65; /* Lemon 400 */
border-color: #f8cc65;
transform: rotateZ(-8deg) translateY(-6px);
box-shadow: rgb(0,0,0) -7px 7px;
```

**White Pill (on dark sections)**
```css
background: #ffffff;
color: #000000;
font-size: 18px;
font-weight: 700;
padding: 16px 36px;
border-radius: 1584px;

/* Hover */
background: #f8cc65; /* Lemon 400 */
transform: rotateZ(-8deg) translateY(-8px);
box-shadow: rgb(0,0,0) -7px 7px;
```

**Nav CTA (Small Black Pill)**
```css
background: #000000;
color: #ffffff;
font-size: 15px;
font-weight: 600;
padding: 8px 20px;
border-radius: 1584px;

/* Hover */
background: #43089f; /* Ube 800 */
transform: rotateZ(-8deg) translateY(-4px);
box-shadow: rgb(0,0,0) -5px 5px;
```

**Rule:** Every button on this site uses the rotation + hard shadow hover. No subtle fades. No scale transforms. The physical tilt is the signature interaction.

### Cards

**Standard White Card**
```css
background: #ffffff;
border: 1px solid #dad4c8;
border-radius: 24px;
padding: 32px 28px;
box-shadow: rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset, rgba(0,0,0,0.05) 0px -0.5px 1px;
transition: transform 0.2s;

/* Hover */
transform: translateY(-4px);
```

**Dark Swatch Card (inside colored sections)**
```css
background: rgba(255,255,255,0.07);
border: 1px solid rgba(255,255,255,0.12);
border-radius: 24px;
padding: 32px 28px;

/* Hover */
background: rgba(255,255,255,0.12);
transform: translateY(-4px);
```

**Stat Block (hero stats)**
```css
background: #ffffff;
border: 1px solid #dad4c8;
border-radius: 24px; /* on outer container */
box-shadow: [clay shadow];
/* Individual blocks separated by: border-right: 1px solid #dad4c8 */
padding: 24px 28px;
```

### Badges & Labels

**Filled Badge (hero)**
```css
background: #f8cc65; /* Lemon 400 */
color: #000000;
font-size: 12px;
font-weight: 700;
letter-spacing: 0.8px;
text-transform: uppercase;
padding: 5px 14px;
border-radius: 11px;
```

**Outline Badge (hero)**
```css
border: 1px dashed #dad4c8;
color: #9f9b93;
font-size: 12px;
font-weight: 600;
letter-spacing: 0.8px;
text-transform: uppercase;
padding: 5px 14px;
border-radius: 11px;
```

**Chip (step tags)**
```css
background: #ffffff;
border: 1px solid #dad4c8;
color: #55534e;
font-size: 13px;
padding: 4px 12px;
border-radius: 1584px;
box-shadow: [clay shadow];
```

**Uppercase Section Label**
```css
font-size: 12px;
font-weight: 700;
letter-spacing: 1.08px;
text-transform: uppercase;
color: #9f9b93; /* or swatch-appropriate on dark sections */
display: block;
margin-bottom: 20px;
```

### Navigation

```css
position: fixed;
background: rgba(250,249,247,0.9);
backdrop-filter: blur(16px);
border-bottom: 1px solid #dad4c8;
height: 60px;
padding: 0 40px;
```

Logo dot: `8px circle, background: #fbbd41 (Lemon 500)`

### Footer

The footer uses a nested container pattern:
- Outer: `background: #ffffff`, `border-top: 1px solid #dad4c8`, `padding: 48px 40px`
- Inner: `background: #faf9f7`, `border: 1px solid #dad4c8`, `border-radius: 40px`, `padding: 56px 56px 40px`

This creates a "card inside a page" effect that gives the footer a contained, finished quality.

---

## 5. Page Section Architecture

Each section follows a consistent color-to-meaning mapping:

| Section | Background | Swatch Role |
|---------|-----------|-------------|
| Nav | Cream (frosted) | Neutral wayfinding |
| Hero | Cream `#faf9f7` | Open, inviting canvas |
| Ticker strip | Black `#000000` | Attention anchor |
| Problem | Ube 900 `#32037d` | Tension, urgency |
| How it works | White `#ffffff` | Clean, readable process |
| Pillars | Matcha 800 `#02492a` | Growth, enablement |
| Personas | White `#ffffff` | Human, personal |
| Partners | Cream with borders | Credibility, neutral |
| Financial | Lemon 500 `#fbbd41` | Warmth, access, optimism |
| Testimonials | White `#ffffff` | Trust, social proof |
| CTA | Slushie 800 `#0089ad` | Action, clarity, forward motion |
| Footer | White + Cream nested | Settled, complete |

**Rule:** Never use more than 2 swatch colors in the same section. Color encodes meaning, not decoration.

---

## 6. Layout & Spacing

### Spacing Scale (base 8px)
`4px, 8px, 10px, 12px, 14px, 16px, 18px, 20px, 24px, 28px, 32px, 36px, 40px, 48px, 56px, 64px, 80px, 96px`

### Container
- Max width: `1100px`, centered
- Side padding: `40px` desktop, `20px` mobile
- Colored full-bleed sections: `margin: 0 40px` on desktop, `margin: 0 16px` on mobile (creates a floating card effect)

### Border Radius Scale

| Name | Value | Use |
|------|-------|-----|
| Pill | `1584px` | All buttons, chips, tags |
| Badge | `11px` | Hero badges |
| Card | `24px` | All cards and inner containers |
| Section | `40px` | Full colored sections, footer inner |

### Grid System

| Layout | Columns | Gap |
|--------|---------|-----|
| Pillars | 3 col | 16px |
| Personas | 3 col | 16px |
| Testimonials | 3 col | 16px |
| Financial | 2 col | 56px |
| Hero stats | flex row | 0 (divided by borders) |
| Steps | 2 col (72px + 1fr) | 32px |

---

## 7. Motion & Interaction

### Button Hover (signature)
```css
transform: rotateZ(-8deg) translateY(-6px);
box-shadow: rgb(0,0,0) -7px 7px;
transition: transform 0.2s, box-shadow 0.2s, background 0.15s;
```
Adjust translate and shadow size by button size:
- Large CTA: `translateY(-8px)`, shadow `-7px 7px`
- Standard: `translateY(-6px)`, shadow `-7px 7px`
- Nav small: `translateY(-4px)`, shadow `-5px 5px`

### Card Hover
```css
transform: translateY(-4px);
transition: transform 0.2s;
```

### Page Load (hero)
Staggered `fadeUp` animation on hero elements:
```css
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}
/* Delays: eyebrow 0.1s, h1 0.2s, subtitle 0.3s, actions 0.4s, stats 0.5s */
```

### Ticker Strip
```css
animation: ticker 30s linear infinite;
@keyframes ticker {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}
/* Duplicate all items for seamless loop */
```

### Step Indicator
```css
/* Step pip dot on hover */
.step-item:hover .step-pip {
  background: #fbbd41; /* Lemon 500 */
  border-color: #fbbd41;
  transition: background 0.2s, border-color 0.2s;
}
```

---

## 8. Responsive Breakpoints

| Breakpoint | Width | Key Changes |
|------------|-------|-------------|
| Desktop | 960px+ | Full layout, 3-col grids, side margins on sections |
| Tablet/Mobile | < 960px | Nav links hidden, single column grids, reduced section padding, section margins 16px |

### Collapsing Rules
- Pillar, persona, testimonial grids: 3 col → 1 col
- Financial layout: 2 col → 1 col, gap 32px
- Colored sections: margin `0 40px` → `0 16px`
- Section padding: `80px 64px` → `56px 28px`
- Hero H1: `clamp(52px, 6.5vw, 80px)` scales naturally

---

## 9. Do's and Don'ts

### Do
- Use warm cream `#faf9f7` as the page background — never cool white
- Use swatch colors as full section backgrounds, not small accents
- Apply all 5 OpenType stylistic sets on headings: `"ss01","ss03","ss10","ss11","ss12"`
- Apply the rotation + hard shadow on every button hover
- Use oat borders `#dad4c8` everywhere — never neutral gray `#ccc` or `#ddd`
- Mix solid and dashed borders for visual variety
- Use 24px radius on cards, 40px on sections, 1584px on pills
- Use Space Mono for all stats and monospace moments
- Keep the uppercase label + 1.08px tracking as the section wayfinding system
- Map swatch color to section meaning (problem = ube, growth = matcha, financial = lemon, CTA = slushie)

### Don't
- Don't use cool gray backgrounds anywhere
- Don't use more than 2 swatch colors in the same section
- Don't use subtle hover effects — the rotation + hard shadow is non-negotiable
- Don't use standard blur-based box shadows — Clay uses hard offset and multi-layer inset only
- Don't use small border radius (under 12px) on feature cards
- Don't skip the OpenType stylistic sets — they define the typographic personality
- Don't use font weight 300 or 800 — strict three-tier system: 700, 500/600, 400
- Don't centre-align body text — left-aligned only

---

## 10. Quick Reference — CSS Variables

```css
:root {
  --cream: #faf9f7;
  --black: #000000;
  --white: #ffffff;
  --silver: #9f9b93;
  --charcoal: #55534e;
  --oat: #dad4c8;
  --oat-light: #eee9df;

  --matcha-300: #84e7a5;
  --matcha-600: #078a52;
  --matcha-800: #02492a;

  --slushie-500: #3bd3fd;
  --slushie-800: #0089ad;

  --lemon-400: #f8cc65;
  --lemon-500: #fbbd41;
  --lemon-700: #d08a11;

  --ube-300: #c1b0ff;
  --ube-800: #43089f;
  --ube-900: #32037d;

  --pom-400: #fc7981;

  --shadow-clay: rgba(0,0,0,0.1) 0px 1px 1px,
                 rgba(0,0,0,0.04) 0px -1px 1px inset,
                 rgba(0,0,0,0.05) 0px -0.5px 1px;

  --font: 'Roobert', 'Arial', sans-serif;
  --mono: 'Space Mono', monospace;
  --ot-heading: "ss01","ss03","ss10","ss11","ss12";
  --ot-body: "ss03","ss10","ss11","ss12";
}
```

---

## 11. Agent Prompt Guide

Use these prompts when asking an AI to generate new components or pages in the PivotLab system.

**New section on cream background:**
"Create a section on warm cream `#faf9f7`. Uppercase label at 12px, weight 700, letter-spacing 1.08px, color `#9f9b93`. H2 at clamp(36px,4vw,52px), weight 700, letter-spacing -1.5px, color `#000000`. White cards with `1px solid #dad4c8` border, 24px radius, clay shadow. Oat borders `#dad4c8` throughout."

**New colored swatch section:**
"Create a full-bleed section with [SWATCH] background, 40px border-radius, margin 0 40px. Uppercase label in light swatch text. H2 in white, weight 700, letter-spacing -1.5px. Semi-transparent cards: `rgba(255,255,255,0.07)` background, `rgba(255,255,255,0.12)` border, 24px radius."

**New button:**
"Button with black background, white text, 16px weight 700, padding 14px 28px, border-radius 1584px. Hover: background Matcha 600 `#078a52`, `transform: rotateZ(-8deg) translateY(-6px)`, `box-shadow: rgb(0,0,0) -7px 7px`."

**New card:**
"White card, `1px solid #dad4c8`, 24px radius, padding 32px 28px. Shadow: `rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset, rgba(0,0,0,0.05) 0px -0.5px 1px`. Hover: `transform: translateY(-4px)`."
