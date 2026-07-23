# BACKLOG.md — kw-data-proj-hub

Projektspezifische offene Tasks und Todos.
Nie mitten in einer Session den Kontext wechseln — hier notieren, gesammelt abarbeiten.

Prio: `1` = hoch · `2` = mittel · `3` = niedrig

---

| # | Beschreibung | Prio | Entdeckt in |
| :--- | :--- | :--- | :--- |
| 1 | Sobald `kw-data-portfolio` fertig ist: Hub archivieren oder auf sie umleiten | 3 | Setup |
| 2 | Neue portfolio-ready Cases (research-engine, telefonica-churn, nyc-taxi-routes) ergänzen sobald Status wechselt | 2 | Setup |
| 3 | KPI-Leiste erweitern sobald mehr Cases da sind — Komplexitäts-/Tiefe-Metriken statt reiner Volumen-Zahlen (voller Vorschlag siehe Notiz unten) | 2 | Kay-Feedback 2026-07-23 |
| ~~4~~ | ~~5. Projektkarte mit echtem Case befüllen~~ — erledigt: fl-airport-company (fLAirport, Business Intelligence) ersetzt die Dopplung | ~~1~~ | Redesign 2026-07-23, erledigt 2026-07-23 |

---

## Notiz — KPI-Erweiterung, Kay-Feedback (2026-07-23)

Ziel: Recruiter/Data Leads/Fachverantwortliche neugieriger machen und echte
technische Tiefe belegen. Statt reiner Volumen-Zahlen (Datensatz-Größen,
wirken oft wie "Big Data um des Big Datas willen") eignen sich Metriken zu
Komplexität, Iterationsgeschwindigkeit, Modellgüte, Engineering-Disziplin.

**1. Modellierungs- & Experimentier-Tiefe (Data Science)**
- Hyperparameter-Kombinationen — z. B. „450+ getestete Kombinationen (Grid/Random Search)" (methodische Sorgfalt)
- Feature-Dimensionalität — z. B. „Reduktion von 120+ rohen Features auf 35 prägnante Predictors" (Feature Engineering & Selektion)
- Cross-Validation-Stabilität — z. B. „5-Fold CV mit konsistentem ROC-AUC von 0.89 ± 0.02" (robust, kein Overfitting)
- Inferenz-Latenz/Skalierung — z. B. „Model-Scoring von 10.000 Records in < 450 ms" (Production-Readiness)

**2. Engineering- & Pipeline-Performance (Data Engineering)**
- Speicher-/Komprimierungs-Effizienz — z. B. „38 GB Rohdaten komprimiert & optimiert auf X GB Parquet/Polars LazyFrames"
- Pipeline-Laufzeit (Performance-Gain) — z. B. „ETL-Laufzeitoptimierung von 45 Min. auf 3 Min. (Vectorization/Polars)" — starker Eyecatcher für Engineers, falls Benchmark vorhanden
- Datenqualitäts-/Bereinigungs-Quote — z. B. „Automated Cleansing: 99.4% Validierungserfolgsrate bei Millionen Zeilen"
- Reproduzierbarkeit/Automatisierung — z. B. „100% Code-Coverage durch automated linting & testing" oder „End-to-End Pipeline in X Sekunden lauffähig"

**3. Workflow- & AI-Tooling (Process & Efficiency)**
- Time-to-MVP — z. B. „Strukturierter Projekt-Bootstrap von der Idee zum produktionsbereiten Repo in < X Stunden"
- Automatisierte Code-Reviews/Iterationen — z. B. „Dutzende automatisierte Agenten-Loops für Refactoring und Dokumentation pro Projekt"

**Einbindungs-Idee:** bestehende 5er-KPI-Row um 1–2 knackige Metriken ergänzen,
oder eine zweite, kleine "Performance- & Code-Metriken"-Leiste direkt bei den
Projekten oder im Tech-Stack-Bereich. Beispiel erweiterte Leiste:
„94 M+ Halt-Ereignisse verarbeitet" · „448 ML-Model-Runs im Experiment" ·
„35 optimierte Features im Final Model" · „< 0,5s Inferenz-Latenz im Benchmark".

Voraussetzung: diese Zahlen müssen aus den tatsächlichen Projekten stammen
(nicht erfunden) — erst umsetzen, wenn die Cases entsprechend dokumentiert sind.
