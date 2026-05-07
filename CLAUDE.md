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

- **Design tokens**: CSS custom properties in `:root` (colors, fonts, spacing)
- **Fonts**: DM Serif Display (headings) + DM Sans (body) via Google Fonts
- **Palette**: `--bg: #f8f6f2`, `--ink: #0f0f0f`, `--accent: #c8622a` (terracotta)
- **Sections** (in order): nav → hero → #impact → #career → #skills → #agentic → #blogs → #certs → #contact → footer
- **Animations**: IntersectionObserver drives `.fade-in` → `.visible` and `.timeline-item` → `.visible` on scroll
- **Photo**: placeholder `<div class="photo-placeholder">` inside `.hero-photo-wrap` — replace with `<img>` pointing to photo file

## Rules

- [`.claude/rules/content.md`](.claude/rules/content.md) — data sources, blog URLs, stats
