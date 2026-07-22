# kw-data-proj-hub

> Kay Wiegand — Case-Hub für Bewerbungen. Ein Link, der auf die fertig
> aufbereiteten Data-Cases zeigt.

---

## Überblick

Schlanke, statische Hub-Seite die alle portfolio-reifen Data-Cases von Kay
Wiegand auflistet und verlinkt — Data Engineering, Data Science, Data
Analysis, plus ein Meta-Case zum AI-Dev-Workflow selbst.

Gedacht als der eine Link für Bewerbungen und Gespräche, solange die grosse
Portfolio-Website (`kw-data-portfolio`, data.kaywiegand.de) noch nicht fertig
ist. Wird später durch diese abgelöst.

## Stack

Plain HTML/CSS, keine Build-Tools, keine Dependencies. Visuelle Identität
übernommen aus den Bewerbungsunterlagen (Cover-Letter): Font Lato, Akzentfarbe
`#594B3B`, Logo-Mark (`public/img/logo-k.png`).

## Setup

```bash
cd public && python3 -m http.server 8000
# → http://localhost:8000
```

Deploy: Push auf `main` triggert `.github/workflows/pages.yml` →
GitHub Pages aus `public/`.

## Live

→ https://kaywiegand.github.io/kw-data-proj-hub/
