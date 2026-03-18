# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static HTML/CSS CV website hosted on GitHub Pages at `https://vickot.github.io/resume/`. No build system — files are served directly from the `master` branch root.

## Deployment

Push to `master` to deploy:
```
git push origin master
```

GitHub Pages is configured to serve from the root of `master`. Changes are live within ~1 minute.

## Architecture

Two files + one asset:
- `index.html` — all markup; one-page CV with sidebar + main content layout
- `styles.css` — all styles; uses CSS custom properties defined in `:root`
- `assets/profile.jpeg` — profile photo

Font Awesome 6.5.0 is loaded via CDN (`cdnjs.cloudflare.com`) for contact icons.

## Layout

The page uses a two-column flexbox layout:
- Left: `<aside class="sidebar">` — fixed-width dark green panel with photo, name, contact, skills, languages
- Right: `<main class="main">` — flex-grows to fill remaining space; profile, work experience, education

The outer wrapper is `.page-wrapper > .page` (flex row). A `<footer>` sits below `.page` inside `.page-wrapper`.

## Key CSS variables (`:root`)

| Variable | Purpose |
|---|---|
| `--sidebar-bg` | Dark green sidebar background |
| `--accent` | Green accent color (section headers, bullets, icons) |
| `--sidebar-width` | Fixed sidebar width (240px) |
| `--bg` / `--surface` | Page background vs card background |

## Collapsible entries

Earlier work roles use `<details class="entry entry-collapsible">` / `<summary>`. The CSS rotates a `›` arrow in `h3::after` when `[open]`. The inner roles sit in `.earlier-roles` with a left border.

## Profile photo

`assets/profile.jpeg` was extracted from the DOCX file (DOCX is a ZIP; image was at `word/media/image1.jpeg`).
