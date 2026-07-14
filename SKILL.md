---
name: portfolio-website
description: Portfolio website project guide — dev workflow, deploy, conventions.
---

# Portfolio Website — SKILL.md

## What Is This

Henry Lee's personal portfolio site. Static HTML/CSS/JS, dark theme, no build tools.

## Quick Start

```bash
python3 -m http.server 8080
# Open http://localhost:8080
```

## Architecture

- `index.html` — Single page, all sections inline
- `css/styles.css` — Custom properties, dark/light theme
- `js/main.js` — Core logic
- `js/animations.js` — Scroll-triggered animations
- `js/i18n.js` — Language switching

## Conventions

- **No frameworks** — vanilla JS only, keep it fast
- **CSS variables** for theming — never hardcode colors
- **Mobile-first** — test on phone before desktop
- **Performance** — no external JS dependencies, minimal HTTP requests

## Content Updates

Edit `index.html` directly. Sections follow this order:
1. Hero (name + tagline)
2. How I Think (5 principles)
3. Signature Work (case studies)
4. Demos
5. Experience
6. Skills
7. Contact

## Deploy

Push to `main` → GitHub Pages or any static host.

## Do NOT

- Add npm/node_modules
- Add build tools (webpack, vite, etc.)
- Add external JS libraries
- Commit large images (optimize first)
