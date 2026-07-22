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
- GitHub-Repo `kaywiegand/kw-data-proj-hub` angelegt (Kay manuell, `gh` CLI lokal
  nicht installiert), erster Push erfolgreich. Pages-Source auf "GitHub Actions"
  umgestellt.

## 2026-07-22 — Redesign: Bewerbungsunterlagen-Look statt project-case-Stil

- Entscheidung: visuelle Identität jetzt aus `Cover-Letter.docx`
  (`~/Notes/projects/2605_job-search/ssot/05_application-profile/`) übernommen,
  nicht mehr aus `slides.css`/`index-template.html` — der Hub soll zu
  Anschreiben/CV passen, da er genau dafür verschickt wird. `public/css/slides.css`
  entfernt, alle Styles jetzt inline in `public/index.html`.
- Extrahiert (XML-Analyse des docx, kein soffice/pandoc lokal verfügbar):
  Font Lato, Akzentfarbe `#594B3B`, Logo-Mark (`public/img/logo-k.png`, 1:1
  aus `word/media/image1.png` übernommen), exakter Kontakt-Wortlaut aus dem
  Anschreiben-Header.
- Positionierung/Wortwahl auf `profile-master.md`-Kernsatz umgestellt
  ("Applied Data Analyst / Data Scientist mit 15+ Jahren Erfahrung...") statt
  der ursprünglichen freien Formulierung ("Senior Tech Consultant mit 20+
  Jahren") — deckt sich jetzt mit der aktuellen Bewerbungspositionierung.
- Seite um vier Sektionen erweitert: Data-Approach (H-Timeline, Element E9),
  Analytics-Workflow (Timeline+Copy, Element E8), Tooling-Box-Grid (Element E6,
  Tech-Stack-Scan über alle CLAUDE.md/pyproject.toml im Workspace), 5er-Ressourcen-
  Grid (GitHub, LinkedIn, Xing, Mail, Telefon). Layout-Bausteine E6/E8/E9 stammen
  strukturell aus `css-style-guides/b/STYLEGUIDE.html`, umgefärbt auf die neue Palette.
- Kein Profilfoto im Header (Kay-Entscheidung) — kommt später, wenn auch die
  Anschreiben ein Foto bekommen.
- Verifiziert per Preview-Tool (Desktop 1400px + Mobile 375px, alle Sektionen
  inkl. Timeline-/Box-Grid-Umbruch geprüft).
- Nächster Schritt: committen, pushen, Kay-Review abwarten (offene Punkte:
  KPI-Zählweise DA-Projekte, Textlänge Approach/Workflow-Sektionen).
- **Custom Domain `data.kaywiegand.de` bewusst hierher umgezogen** (Kay-Entscheidung,
  nicht versehentlich): für die Bewerbungsphase soll der Hub unter der Haupt-Domain
  laufen, da er sofort nutzbar ist. `kw-data-portfolio` bleibt als Repo/Code bestehen,
  hat aber bis auf Weiteres keine aktive Custom Domain mehr. Wird zurückgetauscht,
  sobald `kw-data-portfolio` fertig ist. Footer-Link "Volle Portfolio-Site" zeigt
  deshalb auf den GitHub-Repo statt auf `data.kaywiegand.de` (sonst zirkulär).
