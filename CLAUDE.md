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

- **Design direction**: monochrome, inspired by the Dribbble "Alexfolio" template. No accent colour. Avoid cream + terracotta + serif, which reads as AI-generated.
- **Design tokens**: CSS custom properties in `:root`: `--light: #E3E3E1`, `--dark: #1A1A1A`, `--card: #222222`, `--grey: #8C8C8C`
- **Fonts**: Inter Tight (everything) + JetBrains Mono (bracketed year labels like `(2026)`) via Google Fonts
- **Sections** (in order): hero (light; full-width name over greyscale photo with `mix-blend-mode: difference`) → statement (dark, ghost name behind) → #work (AI coding and PM work: 3 card pairs + list) → #education (light) → #career (light) → #writing (dark) → skills + patent (dark) → #contact (light, giant name sign-off) → footer
- **Photo**: `photo.jpeg`, shown greyscale with a radial CSS mask in `.photo`. A background-removed PNG would look better.
- **Motion**: one CSS load animation on the hero only, disabled under `prefers-reduced-motion`. No JS.

## Rules

- [`.claude/rules/content.md`](.claude/rules/content.md) — data sources, blog URLs, stats
