# PROCESS_LOG.md — kw-data-proj-hub

Verlauf + Entscheidungen. Pointer auf Files — kein Inhalt kopieren.
Metriken, Findings, Outputs gehören in Notebooks/Code — nicht hier.

---

## 2026-07-22 — Projekt-Setup

- Projekt initialisiert via `/project-init kw-data-proj-hub web`
- MD-Files angelegt: CLAUDE.md · README.md · ROADMAP.md · BACKLOG.md · PROCESS_LOG.md
- Entscheidung: schlanker Case-Hub statt Erweiterung der "Data Cases"-Sektion
  in `kw-data-portfolio` — wird jetzt für Bewerbungen gebraucht, `kw-data-portfolio`
  ist noch nicht fertig. Löst `kw-data-portfolio` später ab (Kay-Entscheidung).
- Stil-Referenz: `wgnd-skills/project-case/templates/index-template.html` +
  `zh-tram-data/public/css/slides.css` — gleiche Tokens wie alle Case-Hubs.
- Gelistet: zh-tram-flow (DS), zh-tram-data (DE), us-used-vehicle-resales (DS),
  wgnd-ai-dev-toolchain (Meta-Case, verlinkt auf GitHub-README statt Hub).
- Nächster Schritt: `public/index.html` schreiben, GitHub-Repo anlegen, Pages deployen.
