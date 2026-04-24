# TATAKAE — Landing Page Specification

> Gymwear brand for people who know what it is to struggle, fight, and overcome.

---

## 01. Brand Identity

**Brand Name:** TATAKAE
**Meaning:** Japanese for "fight / struggle" — drawn from Eren Jaeger's war cry in Attack on Titan
**Tagline:** 自由のために戦え — Fight for your freedom.
**Personality (per Jonas Schmedtmann's design framework):** Bold / Confident
**Audience:** Gym-goers who identify with adversity, struggle, and comeback — AOT familiarity is secondary, shared fighter's mindset is primary
**Emotional Journey:** Relatability → Shared Struggle → Upcoming Triumph

---

## 02. Color Palette

| Role           | Name           | Hex       |
| -------------- | -------------- | --------- |
| Primary        | Deep Black     | `#0D0D0D` |
| Primary Soft   | Soft Black     | `#1A1A1A` |
| Accent         | Aggressive Red | `#E50914` |
| Accent Hover   | Brighter Red   | `#FF2E2E` |
| Neutral Light  | Off White      | `#F5F5F5` |
| Neutral Mid    | Secondary Text | `#CCCCCC` |
| Neutral Muted  | Muted Text     | `#888888` |
| Optional Elite | Gold           | `#C9A227` |

**Gold usage rule:** Sparingly — one product only. Signals elite/premium. Never decorative.

---

## 03. Typography

| Role      | Font             | Weight  | Notes                                      |
| --------- | ---------------- | ------- | ------------------------------------------ |
| Headlines | Barlow Condensed | 700–800 | All-caps, tight letter-spacing, 50px–108px |
| Body / UI | Inter            | 400–600 | 14–18px, line-height 1.6–1.7               |

**Rules:**

- Max 2 typefaces — strict
- Headlines: `clamp()` for fluid scaling across breakpoints
- Body text: never under 400 weight, never fully black on dark bg — use `#CCCCCC` or `#888888`
- Short section labels: all-caps, 10–11px, 3–4px letter-spacing, red color
- No justified text

---

## 04. Design Rules (from Design Guidelines PDF)

- **No JavaScript** — every interaction solved in CSS only
- **Spacing system:** multiples of 16px throughout
- **Border-radius:** zero — sharp edges reinforce the brand's serious, disciplined personality
- **Shadows:** minimal use; red glow only on CTAs if needed
- **Dot-grid texture:** `radial-gradient` CSS pattern on dark sections for depth
- **Section contrast rhythm:** dark → dark-soft → light → red → near-black (footer)
- **Icons:** SVG only if used — no bitmap formats. One icon pack max, IonIcons preferably.
- **Images:** when added, real people preferred; overlay with dark gradient if text sits on top
- **Max line length:** 75 characters for body text

---

## 05. Page Sections

### 5.1 Header

- **Background:** `#0D0D0D` sticky, `1px #222` bottom border
- **Height:** 72px
- **Logo:** `TATAKAE` — Barlow Condensed 800, 30px. First `A` in red (`#E50914`) with red 2px underline bar beneath it
- **Nav links:** `Our Fight` (→ #about) · `The Gear` (→ #gear)
  - Style: Inter 500, 12px, 2px letter-spacing, uppercase, `#CCCCCC`
- **CTA Button:** `Shop Now` — red block, no border-radius, hover to `#FF2E2E`
- **Mobile behavior:** Nav links hidden on ≤768px. Logo + Shop Now button only.

---

### 5.2 Hero Section

- **Background:** `#0D0D0D` + CSS dot-grid texture + radial vignette overlay
- **Layout:** Full-screen centered, `min-height: 100vh`
- **Bottom fade:** gradient into next section

**Content:**

- Eyebrow: `TATAKAE GYMWEAR` — red, 11px, 4px letter-spacing, flanked by red lines
- Headline: `BUILT FOR THOSE / WHO FIGHT BACK` — "WHO FIGHT BACK" in red, Barlow 800, `clamp(64px, 10vw, 108px)`, line-height 0.95
- Subtext: _"The wall isn't in your way. **The wall is the way.** Gear built for people who already know what it costs to keep going."_ — `#888888`, 16–17px
- Primary CTA: `Shop the Collection` — red block button
- Secondary CTA: `Our Fight` — ghost outline button, `1px #333` border

**Scroll indicator:** CSS-only animated line (scaleY keyframe), no JS

---

### 5.3 Features Section

- **Background:** `#1A1A1A`
- **Padding:** 120px vertical
- **Borders:** `1px #1f1f1f` top and bottom

**Header:**

- Eyebrow: `WHAT WE STAND FOR`
- Title: `THE CODE WE TRAIN BY`

**Layout:** 4-column grid with vertical `1px #2a2a2a` dividers
→ 2-col at ≤900px → 1-col at ≤560px

**4 Pillars (in order):**

| #   | Title                       | Copy                                                                                               |
| --- | --------------------------- | -------------------------------------------------------------------------------------------------- |
| 01  | No **Comfort** Zone         | Designed for people who train past the point most stop. If you're comfortable, you're not growing. |
| 02  | Form Meets **Force**        | Technical fit engineered to move with you — not against you. Every cut has a reason.               |
| 03  | Discipline **is** the Brand | Every design choice is intentional. Nothing is decorative. We build what we believe in.            |
| 04  | Built to **Endure**         | Fabric that survives the grind, wash after wash. Built for the long game — just like you.          |

**Styling per pillar:**

- Ghost number (01–04): Barlow 800, 72px, transparent fill, `1px #2e2e2e` stroke
- Red 2px rule above title
- Red accent on one keyword per title
- Description: Inter 400, 14px, `#888888`

---

### 5.4 Products Grid

- **Background:** `#F5F5F5` (light section — intentional contrast break)
- **Padding:** 120px vertical

**Header:**

- Eyebrow: `THE ARSENAL`
- Title: `BUILT TO BE WORN` — dark (`#0D0D0D`)
- `View All →` link — right-aligned, underline style, hover to red

**4 Products:**

| Product           | Category    | Placeholder Price | Notes              |
| ----------------- | ----------- | ----------------- | ------------------ |
| The Grind Tights  | Compression | $74               | —                  |
| The Burden Hoodie | Outerwear   | $119              | Gold `ELITE` badge |
| The Push Shorts   | Shorts      | $59               | —                  |
| The Stripped Tank | Tank        | $44               | —                  |

**Card styling:**

- White card, no border-radius
- Image area: `aspect-ratio: 3/4`, dark CSS gradient placeholder (swap for real images)
- Gold `ELITE` badge: top-left, `#C9A227`, one product only
- `Shop` button: black → red on hover
- Grid: 4-col → 2-col at ≤900px

---

### 5.5 CTA Section

- **Background:** `#E50914` (full red)
- **Padding:** 120px vertical
- **Texture:** CSS dot-grid `rgba(0,0,0,0.12)` on red
- **Ghost element:** `戦え` in kanji — massive, `rgba(0,0,0,0.08)`, right-aligned behind content. CSS only. AOT easter egg.

**Content:**

- Label: `THE FINAL PUSH`
- Headline: `STOP WAITING. / START WEARING.` — white, Barlow 800, `clamp(52px, 9vw, 96px)`
- Subtext: _"You've already done the hard part — **you kept going.** The gear should match that."_
- CTA: `Shop the Collection` — white button, red text, hover to black

**Mobile:** Ghost kanji hidden on ≤600px. Button full-width.

---

### 5.6 Footer

- **Background:** `#080808`
- **Border:** `1px #1a1a1a` top

**Three columns (top row):**

**Brand (left):**

- Logo: same as header
- Tagline: `自由のために戦え` (Japanese, 15px, `#CCCCCC`) + `— Fight for your freedom.` (English, 12px, `#888888`)

**Navigate (center):**

- Home · Our Fight · The Gear · Shop Now

**Follow (right):**

- Instagram `@tatakae`
- TikTok `@tatakae`
- X `@tatakae`
- Hover: links turn red

**Bottom row:**

- Copyright: `© 2026 TATAKAE. All rights reserved.` — "TATAKAE" in red
- Legal: Privacy Policy · Terms of Use

**Responsive:** 3-col → 2-col (brand full-width) at ≤768px → 1-col at ≤480px

---

## 06. Responsive Breakpoints

| Breakpoint | Behaviour                                           |
| ---------- | --------------------------------------------------- |
| ≤ 768px    | Nav links hidden, header shows logo + Shop Now only |
| ≤ 900px    | Features: 4-col → 2-col. Products: 4-col → 2-col    |
| ≤ 600px    | Hero CTAs stack full-width. CTA ghost kanji hidden  |
| ≤ 560px    | Features → 1-col. Products stay 2-col               |
| ≤ 480px    | Footer → 1-col                                      |

---

## 07. Asset Placeholders (to replace)

| Location           | Asset Needed                                              |
| ------------------ | --------------------------------------------------------- |
| Product cards (×4) | Real product photography, `aspect-ratio: 3/4`, compressed |
| Hero section       | Optional: model/product image with dark overlay           |
| Social handles     | Real Instagram, TikTok, X URLs                            |
| Prices             | Real pricing per product                                  |
| Legal pages        | Privacy Policy + Terms of Use pages                       |

---

## 08. Files Delivered

| File                    | Contents                                 |
| ----------------------- | ---------------------------------------- |
| `tatakae-header.html`   | Header section only                      |
| `tatakae-hero.html`     | Header + Hero                            |
| `tatakae-features.html` | Header + Hero + Features                 |
| `tatakae-products.html` | Header + Hero + Features + Products      |
| `tatakae-cta.html`      | Header → CTA (all sections minus footer) |
| `tatakae-complete.html` | Full page — all 6 sections               |

---

_Spec compiled by Landing Page Architect session. No JavaScript used anywhere. All interactions CSS-only._
