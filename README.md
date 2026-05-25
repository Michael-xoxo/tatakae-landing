# 戦え — TATAKAE

> **Built for those who fight back.**

A responsive, production-ready gymwear landing page built in pure HTML and CSS. No JavaScript. No frameworks. No dependencies beyond a Google Fonts import.

---

## Overview

TATAKAE is a gymwear brand built on a fighter's mindset. This landing page is the brand's primary web presence — designed to convert visitors into customers through sharp visual identity, intentional copy, and a disciplined design system.

The build prioritises performance and craft over complexity. Every design decision is deliberate. Nothing is decorative.

---

## Built With

| Layer      | Choice                                                               |
| ---------- | -------------------------------------------------------------------- |
| Markup     | HTML5 (semantic)                                                     |
| Styling    | CSS3 — Flexbox, CSS Grid, custom properties                          |
| Responsive | Hand-written media queries (`queries.css`)                           |
| Fonts      | Barlow Condensed (700, 800) + Inter (400, 500, 600) via Google Fonts |
| Hosting    | Netlify                                                              |
| JavaScript | None                                                                 |

---

## Project Structure

```
tatakae/
├── index.html                  # Single-page markup
├── style.css                   # All base styles (no media queries)
├── queries.css                 # All responsive breakpoints
├── manifest.webmanifest        # PWA / home screen manifest
├── favicon.ico                 # Legacy browser favicon
└── img/
    ├── favicon-16.png          # Browser tab icon
    ├── favicon-32.png          # Browser tab icon (retina)
    ├── apple-touch-icon.png    # iOS home screen (180×180)
    ├── icon-192.png            # Android home screen (192×192)
    ├── icon-512.png            # Android splash / manifest (512×512)
    ├── og-preview.jpg          # Social share preview (1200×630)
    ├── product-01-Tights.jpg
    ├── product-02-Hoodie.jpg
    ├── product-03-Shorts.jpg
    └── product-04-Tank.jpg
```

---

## Page Sections

| Section  | ID       | Purpose                             |
| -------- | -------- | ----------------------------------- |
| Header   | —        | Sticky nav with logo and Shop CTA   |
| Hero     | `#home`  | Full-viewport brand statement       |
| Features | `#about` | Four brand principles               |
| Products | `#gear`  | Four product cards with real images |
| CTA      | `#shop`  | Conversion section                  |
| Footer   | —        | Brand, nav, socials, legal          |

---

## Design System

### Colours

| Token          | Value     | Usage                             |
| -------------- | --------- | --------------------------------- |
| `--black`      | `#0d0d0d` | Primary background                |
| `--black-soft` | `#1a1a1a` | Features section background       |
| `--red`        | `#e50914` | Primary accent — CTAs, highlights |
| `--red-hover`  | `#ff2e2e` | Button hover state                |
| `--light`      | `#f5f5f5` | Primary text                      |
| `--mid`        | `#cccccc` | Secondary text                    |
| `--muted`      | `#888888` | Tertiary text                     |
| `--gold`       | `#c9a227` | Elite product badge               |

### Typography

| Role                | Font             | Weight        |
| ------------------- | ---------------- | ------------- |
| Headlines, wordmark | Barlow Condensed | 700, 800      |
| Body, UI            | Inter            | 400, 500, 600 |

### Responsive Breakpoints

| Breakpoint         | Targets                                      |
| ------------------ | -------------------------------------------- |
| `max-width: 900px` | Features grid → 2 col, Products grid → 2 col |
| `max-width: 768px` | Nav hides text links, Footer → 2 col         |
| `max-width: 600px` | Hero CTAs stack, CTA section condenses       |
| `max-width: 560px` | Features → 1 col, Products maintain 2 col    |
| `max-width: 480px` | Footer → 1 col, footer-bottom stacks         |

---

## Head & SEO

The `<head>` is fully production-optimised:

- ✅ Meta description for search engines
- ✅ Open Graph tags (Facebook, WhatsApp, LinkedIn)
- ✅ Twitter / X card tags
- ✅ Favicon set — `.ico`, 16px, 32px, 180px, 192px, 512px
- ✅ Web app manifest for Android home screen
- ✅ `theme-color` for mobile browser chrome
- ✅ `canonical` URL
- ✅ Google Fonts preconnect hints for faster load

---

## Favicon

The favicon is the kanji character **戦** (read: _tatakae_ / meaning: _fight_) — rendered in `#e50914` red on a `#0d0d0d` near-black square canvas. Bold geometric strokes, flat design, no gradients. Created to remain legible at 16×16px.

---

## Browser Support

Tested across:

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- iOS Safari
- Android Chrome

---

## Licence

All rights reserved. © 2026 TATAKAE.
