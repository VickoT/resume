# Viktor Törnblom — CV

Personal CV website hosted on GitHub Pages.

**Live:** https://vickot.github.io/resume/

## Features

- Two-column layout: dark green sidebar + main content
- Trilingual toggle (🇬🇧 🇸🇪 🇩🇰) — language preference saved in localStorage
- Collapsible sections for earlier work experience and exchange semester
- Publications with DOI links

## Stack

Plain HTML + CSS, no build step. Deployed directly from the `master` branch root.

## Local development

```bash
python3 -m http.server 8080
# → http://localhost:8080
```

## Deploy

```bash
git push origin master
```

Changes are live on GitHub Pages within ~1 minute.
