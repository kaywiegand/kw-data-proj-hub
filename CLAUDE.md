# CLAUDE.md — kw-data-proj-hub

> Projektspezifische Anweisungen für Claude Code.
> Ergänzt die globale CLAUDE.md aus dem Workspace-Root.

---

## Projekt

| Feld | Inhalt |
| :--- | :--- |
| Slug | `kw-data-proj-hub` |
| Typ | web |
| Stack | Plain HTML/CSS, keine Build-Tools |
| Status | 🟢 aktiv |

---

## Zweck

Schlanker Case-Hub — ein Link für Bewerbungen, der auf die fertig aufbereiteten
Data-Cases zeigt. Kein Build-Tool, kein JS-Framework, bewusst im gleichen
visuellen Vokabular wie die einzelnen Case-Hubs (zh-tram-data, us-used-vehicle-resales:
`index-template.html` + `slides.css` aus `wgnd-skills/project-case/`).

Wird später durch `kw-data-portfolio` (data.kaywiegand.de) abgelöst, sobald die
fertig ist — dieser Hub ist bewusst der Zwischenstand, jetzt nutzbar.

---

## Struktur

```
public/
├── index.html      ← die Hub-Seite selbst (GitHub-Pages-Quelle)
└── css/slides.css  ← unverändert kopiert aus zh-tram-data — identische Tokens
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
