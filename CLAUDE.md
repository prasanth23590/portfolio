# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

# Portfolio — Prasanth Padmanabhan Menon

Single-file static portfolio site deployed to GitHub Pages at `https://prasanth23590.github.io/portfolio/`.

## Commands

```bash
# Local preview
python3 -m http.server 8765   # serves from this directory → http://localhost:8765

# Deploy
git add -A && git commit -m "..." && git push origin main
# GitHub Pages auto-deploys from main branch root /
```

## Architecture

Single `index.html` — no build step, no framework, no dependencies except Google Fonts CDN.

- **Design tokens**: CSS custom properties in `:root` (colors, fonts, radii)
- **Fonts**: Bricolage Grotesque (display) + Public Sans (body) via Google Fonts
- **Palette**: `--paper: #ECEFF3` (cool grey), `--ink: #0E1B2C` (navy), `--cobalt: #2348D6` (accent), `--shipped: #177245` (used only for "Now" / shipped markers). Avoid cream + terracotta + serif: it reads as AI-generated.
- **Sections** (in order): nav → hero (name, portrait, now/studying strip) → #agents (AI coding and PM work) → #education (full cobalt block) → #releases (career as versioned release notes) → #writing (posts with view bars) → #skills → #contact → footer
- **Motion**: one CSS load animation on the hero only, disabled under `prefers-reduced-motion`. No scroll-triggered fades, no JS.
- **Photo**: `photo.jpeg` in `.portrait`
- **Writing bars**: `.bar span` widths are each post's views as a % of the top post (16,984)

## Rules

- [`.claude/rules/content.md`](.claude/rules/content.md) — data sources, blog URLs, stats
