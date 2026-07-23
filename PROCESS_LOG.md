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

## 2026-07-22 — Header-Iteration + vollständige Content-Überarbeitung nach Kay-Briefing

- Header über mehrere Iterationen korrigiert: enthält jetzt nur Logo (weiße
  Variante, `public/img/logo-k-white.png`) + Kontaktblock (Name, Position,
  Ausbildung, Ort, Telefon, E-Mail — ein zusammenhängender Text mit `<br>`,
  Wortlaut 1:1 von Kay vorgegeben). Hintergrund `#3E4A5C` (Blaugrau aus dem
  ursprünglichen `index-template.html`-Header), Höhe/Padding von dort übernommen.
  Titel ("Data & AI Projects", Uppercase, 4rem) + Subline + KPI-Row bleiben
  bewusst außerhalb des Headers, eigener Block mit großem Abstand darunter.
- Lektion aus dieser Iteration: mehrfach zu viel eigenständig entschieden
  (Copy, Farben, wann gepusht wird) — siehe Memory `feedback_autonomy_boundaries_live_deploys`.
  Ab jetzt: Änderungen vor Commit/Push im Preview zeigen, Copy/Zahlen/Design
  nicht selbst erfinden.
- Komplette Content-Überarbeitung nach Kays Abschnitt-für-Abschnitt-Briefing:
  KPI-Row jetzt 5 Werte (DE/DS/DA-Projektzahl + max. Datensätze + max. ML-Runs,
  DA aktuell ehrlich bei 0). Projektkarten-Struktur getauscht (view-label =
  Projektname, h3 = Projektziel, Badge = volle Disziplin statt Abkürzung),
  5. Karte (AI Dev Toolchain, Badge "Business Intelligence") als Platzhalter
  für ein noch kommendes Projekt ergänzt — Text wird aktualisiert sobald das
  Projekt da ist. "Mein Data-Approach" (E9) ersetzt durch 3-spaltige
  "Data-to-Value Approach"-Struktur (Business Understanding / Data & Technology
  / Business Impact). "Mein Analytics-Workflow" (E8) ersetzt durch 7-stufige
  CRISP-DM-Timeline, letzter Schritt farblich hervorgehoben. Tooling-Grid um
  DuckDB und Folium bereinigt (kein aktives Projekt nutzt sie). Ressourcen-Grid
  auf 5 Spalten (GitHub/LinkedIn/Xing/Mail/Telefon), Footer auf reine
  Kurzzeile reduziert.
- Nächster Schritt: 5. Projektkarte mit echtem Case aktualisieren sobald verfügbar.

## 2026-07-23 — Approach-Layout, Fixed-Nav, Hero-Feinschliff, Design-System

- **Data-to-Value Approach**: 3 Layout-Alternativen (Card-Stil, Verbundene
  Linie, Zentriert) gebaut und alle drei zusätzlich in
  `css-style-guides/b/STYLEGUIDE.html` als Beispiel 31/32/33 unter Element E9
  dokumentiert (bleibt lokal, Ordner ist bewusst nicht in git). Kay wählt
  "Verbundene Linie" — Timeline-Punkte mit Verbindungsstrich zur Headline,
  Bulletpoints in Akzentfarbe, dritte Spalte auf drei parallele Zeilen
  (Insight & Discovery / Decision & Action / Value & Growth).
- **Spacing-System**: auf Kays Prinzip "Abstände als Bruchteil eines
  Basiswerts berechnen, nicht nach Auge" umgestellt (Memory
  `feedback_design_spacing_system`) — 8rem-Grundrhythmus zwischen
  Header/Hero/Sections/Footer, Header-Padding testweise 4rem → 6rem,
  `.section-label`/`.section-intro`-Abstände ebenfalls auf feste
  em-Werte (1em / 3em) gebracht statt Einzelwerte.
- **Navigation mehrfach iteriert**: von Klartext-Liste → Tab-Bar mit
  Unterstrich-Hover → schließlich fixed Sidebar rechts, Links untereinander
  rechtsbündig, Unterstrich zieht sich rechts→links auf, aktive Section wird
  beim Scrollen hervorgehoben. Technische Notiz: Scroll-Highlight läuft über
  einen `scroll`-Event + `getBoundingClientRect`-Check, nicht über
  `IntersectionObserver` — Observer feuerte im Preview-Tool (headless)
  nicht zuverlässig, der Scroll-Event-Ansatz ist robuster und in jedem
  Browser gleich verlässlich. Nav-Top-Anker sitzt auf der Position der
  Hero-Subline (per JS gemessen, nicht hart codiert).
- **Hero verschlankt**: KPI-Row + Nav aus eigener "Schnelleinstieg"-Section
  wieder aufgelöst und direkt in den Hero integriert, zweite Klartext-Subline
  (Sektionsliste) entfernt, da die echte Nav diese Funktion übernimmt.
  "Weitere Ressourcen" durchgängig zu "Kontakt" umbenannt (Section-Label, ID,
  Nav-Label).
- Alles committed + gepusht, live auf `data.kaywiegand.de` verifiziert.
- **Session-Ende (Kay, 2026-07-23):** Hub ist in aktuellem Zustand
  einsatzbereit für Bewerbungen. Weiterarbeit erst wieder, wenn neue
  Projekte/Cases anstehen (siehe BACKLOG #2 — weitere Cases ergänzen sobald
  Portfolio-Status wechselt; BACKLOG #3 — KPI-Vertiefung).
