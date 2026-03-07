# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Personal website for Vladimír Holan (holan.eu) — a freelancer offering Web Analytics, Automation & AI, and Web Development services targeting small Czech businesses.

## Tech stack

- Pure HTML/CSS, no framework, no build step
- Single-file: all HTML, CSS, and any JS live in `index.html`
- No package manager, no node_modules, no build commands

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
