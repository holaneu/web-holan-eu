# CLAUDE.md

## Project overview

Company website for holan.eu — offering Automation & AI as a main service, plus delivering Website and Web Analytics services. All targeting small Czech businesses.

## Related
This repo belongs to the project located at `$PROJECTS/holan.eu`, if user asks for creation or edits of project related files (e.g. TODO.md, README.md, ref materials, JOURNAL.md etc.), go there.

## Tech stack

- Pure HTML/CSS/JS, no framework, no build step
- `index.html` — HTML structure and content
- `style.css` — all styles
- `script.js` — hamburger menu + navbar scroll transition
- No package manager needed for the site itself (only dev tooling like Playwright)

## Design and UI

- Theme: light (white `#ffffff` default, `#f4f6f8` for alternate sections)
- Primary color: `#cdf5ec` (mint) — used for navbar and hero background
- Gradient: top area (nav + hero) wrapped in `.top-bg` with `linear-gradient(to bottom, #e8fdf8, #cdf5ec)`
- Accent color: `#0a7c68` (dark teal) — CTAs, buttons, highlights
- CSS variables: always use `:root` variables, never hardcode colors
- Layout container: `max-width: 1200px` centered via `.container`
- Navbar: sticky, transparent over gradient, transitions to white + shadow on scroll (JS `scrolled` class)
- Hero: transparent background over `.top-bg` gradient; two-line super-large headline (`clamp(2.8rem, 6vw, 5rem)`, weight 900) with dark and accent colored lines
- Services grid: 3 columns on desktop (≥901px), 2 columns on tablet (≤900px), 1 column on mobile (≤768px)
- Hamburger menu: visible on ≤768px; clicking opens a right-side drawer (300px wide, full viewport height, mint background); icon animates to ×
- Files: HTML in `index.html`, CSS in `style.css`, JS in `script.js`

## Deployment

- **Production**: push to `main` → GitHub Pages auto-deploys (via GitHub Actions)
- **Staging**: Netlify/Cloudflare Pages from `dev` branch (not yet configured)

## Content

- The canonical content source is `content_2026-02-26_v2.md` — use it as reference when editing copy in `index.html`
- Language: Czech (cs), targeting non-technical small business owners — avoid jargon, write in plain language

## Design conventions

CSS variables defined in `:root` — always use them, never hardcode colors:
- `--bg` / `--bg2` — page backgrounds
- `--border` — borders
- `--text` / `--muted` — text colors
- `--accent` / `--accent2` — purple accent colors

Dark theme only. Layout max-width: 760px centered via `.container`.
