# CLAUDE.md — kw-data-proj-hub

> Projektspezifische Anweisungen für Claude Code.
> Ergänzt die globale CLAUDE.md aus dem Workspace-Root.

---

## Projekt

| Feld | Inhalt |
| :--- | :--- |
| Slug | `kw-data-proj-hub` |
| Typ | web |
| Stack | Plain HTML/CSS, keine Build-Tools, Font Lato via Google Fonts |
| Status | 🟢 aktiv |

---

## Zweck

Schlanker Case-Hub — ein Link für Bewerbungen, der auf die fertig aufbereiteten
Data-Cases zeigt. Kein Build-Tool, kein JS-Framework.

**Visuelle Identität (seit Redesign):** übernommen aus den Bewerbungsunterlagen
(`Cover-Letter.docx`, siehe `~/Notes/projects/2605_job-search/ssot/05_application-profile/`)
statt aus dem internen project-case-Stil — Font Lato, Akzentfarbe `#594B3B`
(warmes Braun), Logo-Mark (`public/img/logo-k.png`, 1:1 aus dem Cover-Letter
extrahiert). Layout-Bausteine (H-Timeline, Timeline+Copy, Box-Grid) stammen
strukturell aus `css-style-guides/b/STYLEGUIDE.html` (E9/E8/E6), aber umgefärbt
auf diese Palette. Grund: der Hub soll zu Anschreiben/CV passen, nicht zu den
internen Case-Hub-Slides.

Wird später durch `kw-data-portfolio` (data.kaywiegand.de) abgelöst, sobald die
fertig ist — dieser Hub ist bewusst der Zwischenstand, jetzt nutzbar.

---

## Struktur

```
public/
├── index.html      ← die Hub-Seite selbst (GitHub-Pages-Quelle), Styles inline
└── img/logo-k.png  ← Logo-Mark aus dem Cover-Letter
.github/workflows/pages.yml   ← Deploy public/ → GitHub Pages
```

Kein `notebooks/`, `data/`, `src/` — reine Content-Seite.

---

## Session-Einstieg

1. PROCESS_LOG.md lesen — aktueller Stand und letzte Session
2. ROADMAP.md lesen — offene Phasen
3. Globale CLAUDE.md aus dem Workspace-Root gilt weiterhin

---

## Pflege

Neuer portfolio-ready Case in `docs/PROJECTS.md` → Karte in `public/index.html`
ergänzen. Case verliert Portfolio-Status → Karte entfernen. Rein manuell
kuratiert, keine `portfolio.md`-Automatisierung wie bei Einzelprojekten.
