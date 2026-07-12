# Agent Braindump — Ideen auf Probe

> **Zweck:** Vollständiger Wissensstand für einen künftigen Agenten, der dieses Projekt nahtlos fortsetzt.  
> **Stand:** 2026-07-12 · main @ PR #3 merged · Git-Tag `v1.0.0` (v1.2.0-Inhalt auf main, Tag noch setzen)  
> **Repo:** https://github.com/wunderkind2k1/cursor-playground  
> **Branch-Konvention (Cloud Agent):** `cursor/<beschreibung>-349b`

---

## 1. Was ist dieses Projekt?

**Ideen auf Probe** ist ein **persönliches, öffentliches 6-Monats-Protokoll** zur Validierung von **B2B-SaaS-Ideen in DACH** — im Geist von Bootstrapping (*Startup for the Rest of Us*, MicroConf, Rob Walling), **nicht** VC/Y Combinator.

Der Nutzer (Gründer) testet **eine Idee gleichzeitig** über ~6 Monate bei **~5 Stunden/Woche** (Spikes möglich). Jeder Lauf hat einen **Codename** (z. B. *Projekt Linde*). Am Ende: **Stop oder Weitermachen** — nicht zwingend MVP oder Launch.

| Phase | Ziel |
|-------|------|
| **Phase 1 (Monat 1–6)** | Evidenz sammeln → Entscheidung Stop/Weitermachen |
| **Phase 2 (Weitermachen)** | POC/Prototyp/MVP → erste zahlende Kunden, flexibel |

**Wichtig:** Das Playbook startet **mit einer gegebenen Idee** (Day 0). Kein Idea Sourcing im Curriculum. Der Nutzer hat **keine konkrete Idee** mit dem Agenten geteilt — das Playbook bleibt **abstrakt/idea-agnostisch**.

---

## 2. Nutzer-Profil & feste Entscheidungen

Diese Antworten kamen iterativ (Runden 1–5) und sind **verbindlich**:

| Thema | Entscheidung |
|-------|--------------|
| Parallelität | **Eine Idee zur Zeit**, kein Parallelbetrieb |
| Erfolg Monat 6 | **Stop oder Weitermachen** (nicht MVP als Pflicht) |
| Markt | **B2B only**, nicht Prosumer, nicht B2C |
| Geo / Sprache | **DACH**, **Deutsch only** (Englisch später möglich, aber Aufwand) |
| Zeitbudget | **~5 h/Woche**, spontane Spikes erlaubt |
| Transparenz | Alles *darf* öffentlich sein; **Tiefe variiert case-by-case** |
| Öffentlich oberflächlicher | **Produktidee, Pricing, Interview-Metriken** |
| Playbook-Name | **Ideen auf Probe** (Nr. 2 aus Namensliste; persönlich, warm) |
| Repo-Name | Bleibt **`cursor-playground`** (nicht umbenennen, unless asked) |
| Cycle-Logs öffentlich | **Codenames** (z. B. Projekt Linde), nicht Produktnamen |
| GitHub | **Öffentlich ab Tag 1**, Source of Truth |
| Notion | **Reading Layer** — manuell bei Releases syncen |
| Newsletter | **Ja**, 14-tägig, Start **Woche 6–8**, Deutsch |
| Compleadly | **Lead Gen + Erstkontakt only**; danach **manuell** |
| Sales Navigator | Nutzer hat **Jahresabo** |
| Notion | Nutzer nutzt es bereits |
| LinkedIn | **1000+ Connections**, etabliert, Creator Mode relevant |
| Terminologie | **Stop / Weitermachen** (nicht Kill/Hustle — zu hart/englisch für DE-Publikum) |

### Abgelehnte Richtungen

- VC / YC / Demo-Day-Narrativ
- Company Page als Hauptkanal (Personal Profile first)
- Parallele Ideen-Tracks
- Englische Inhalte parallel (früh)
- Compleadly für Follow-ups automatisieren
- Idea Sourcing als Monat 1

---

## 3. Architektur (drei Schichten)

```
┌─────────────────────────────────────────────────────────────┐
│  PRIVAT (Notion intern)                                     │
│  Volle Idee, 5PM, ICP-Listen, Interviews, Rohdaten         │
└──────────────────────────┬──────────────────────────────────┘
                           │ kuratiert (L1–L4)
┌──────────────────────────▼──────────────────────────────────┐
│  ÖFFENTLICH                                                 │
│  GitHub (SoT) ←→ Notion (hübsch) ←→ LinkedIn (Distribution) │
│  cycles/[codename]/README.md = öffentliches Cycle-Log       │
└─────────────────────────────────────────────────────────────┘
```

| Schicht | Rolle |
|---------|-------|
| **GitHub** | Source of Truth, Versionierung (Tags, CHANGELOG), Markdown-Playbook |
| **Notion öffentlich** | Lesefreundliche Spiegelung für Featured + Newsletter |
| **Notion privat** | Volle Cycle-Daten, Interview-DB, Export-Queue |
| **LinkedIn Personal** | Distribution, Discovery, Glaubwürdigkeit, Gespräche |
| **LinkedIn Company** | Optional, sekundär — nicht für Reach |

**Sync-Regel:** Nur bei Version-Bumps (~30 Min.), nicht täglich. Siehe `notion/SYNC.md`.

---

## 4. Offenlegungsrichtlinien (L1–L4)

| Stufe | Was | Öffentlich typischerweise |
|-------|-----|---------------------------|
| **L1** | Methodik, Gates, Playbook-Schritte | Voll |
| **L2** | Interview-Anzahl, Muster, Trends | Aggregiert, gerundet |
| **L3** | Produktidee, Pricing | Kategorie, Range — oberflächlich |
| **L4** | Stop/Weitermachen-Entscheidung | Entscheidung + 3–5 Bullets |

**Faustregel:** Erkenntnis öffentlich, Rohdaten in Notion privat.  
**Export-Queue** in privatem Notion vor jedem Post prüfen (`notion/private-workspace.md`).

---

## 5. Terminologie (aktuell — nicht zurückdrehen)

| Alt (verworfen) | Neu (aktiv) |
|-----------------|-------------|
| Kill or Hustle | **Stop oder Weitermachen** |
| Kill | **Stop** |
| Hustle | **Weitermachen** |
| Early Kill | **Früher Stop** |
| Kill-Signal | **Stop-Signal** |

**Hinweis:** In frühen Agent-Turns und PR-Beschreibungen kann noch „Kill/Hustle" vorkommen — im Repo-Inhalt ist alles umgestellt.

---

## 6. Playbook-Struktur (Phase 1)

| Monat | Datei | Fokus | ~h | Gate |
|-------|-------|-------|-----|------|
| 0 | `playbook/00-start-hier.md` | Cycle-Start, Codename | 2 | — |
| 1 | `01-monat-1-5pm.md` | 5PM Stress-Test | 4–6 | G1: ≥4/5 |
| 2 | `02-monat-2-icp.md` | Landschaft + ICP | 8–10 | G2: 75+ ICP |
| 3 | `03-monat-3-discovery.md` | LinkedIn Discovery | 18–22 | G3: Muster ≥5 Gespräche |
| 4 | `04-monat-4-positionierung.md` | Positionierung + Rauchtest | 8–12 | G4: ≥3 Signale |
| 5 | `05-monat-5-pricing.md` | Zahlungsbereitschaft | 8–12 | G5: ≥2 Budget-Signale |
| 6 | `06-monat-6-stop-weitermachen.md` | Entscheidung | 6–8 | Stop/Weitermachen |
| 2* | `07-phase-2-weitermachen.md` | Nach Weitermachen | flexibel | erste zahlende Kunden |

**Prior Art im Playbook:** Rob Walling 2/20/200, 5PM Framework, Mom Test, MicroConf-Phasen — adaptiert für LinkedIn-first DACH.

### Phase 2 (Weitermachen)

- Kein fixes 6-Monats-Raster
- Meilensteine: H1 Scope → H2 Build → H3 Beta → H4 Pay → H5 Evolve
- Inhalt **bewusst dünn** — soll nach erstem echten Weitermachen aus Praxis gefüllt werden

---

## 7. Compleadly-Workflow (Monat 3)

```
Sales Navigator → ICP-Liste → Compleadly (Erstkontakt) → Annahme → MANUELL → Gespräch → Notion
```

- **Automatisierung nur bis Erstkontakt**
- 2–3 Textvarianten rotieren
- Tageslimits einhalten (Account-Safety)
- **Keine** Follow-up-Automation
- Templates: `templates/outreach-erstkontakt.md`, `templates/outreach-manuell.md`

---

## 8. LinkedIn GTM

### Profil

- **Headline:** `Ideen auf Probe — 6 Monate B2B-Validierung in DACH, öffentlich dokumentiert`
- **Info:** Copy in `linkedin/profil-info.md`
- **Featured:** 1) Notion 2) GitHub 3) Newsletter (wenn live)
- **Creator Mode:** an

### Content-Kadenz (~5 h/Woche)

| Aktivität | Zeit | Rhythmus |
|-----------|------|----------|
| Feed-Posts | ~1,5 h | 2×/Woche |
| Kommentare | ~30 Min | 3×/Woche |
| Newsletter | ~2 h | 14-tägig ab Woche 6–8 |

### Content-Säulen

- 40% Playbook-Log (wenn Cycle läuft)
- 30% Methodik
- 20% Problem-first (L3)
- 10% Version / Entscheidung

### Editorialer Ton (Posts 1–5 überarbeitet)

- Persönlicher oder meinungsstarker Einstieg
- Fließtext vor Bullet-Walls
- Prior Art benennen wo passend
- Gedankenstriche, **keine Emoji-Struktur**
- Schluss mit **echter Frage** (Diskussion, nicht CTA)
- Pro Post: Hook A/B/C + Redaktionsnotizen in der Datei
- Wort „Protokoll" im Fließtext für Seriosität

**Fertige Posts:** `linkedin/posts/01` … `05` + `README.md` mit Launch-Reihenfolge

### Newsletter

- Name: **Ideen auf Probe**
- Ausgabe #0-Outline in `linkedin/posts/04-newsletter-teaser.md`
- **Ausgabe #0 noch nicht geschrieben** — nur Outline

---

## 9. Notion-Setup

| Datei | Inhalt |
|-------|--------|
| `notion/SETUP.md` | Seitenbaum öffentlich + privat |
| `notion/public-startseite.md` | Copy-paste Startseite |
| `notion/public-curriculum.md` | Curriculum + Gates |
| `notion/private-workspace.md` | Interner Workspace, Export-Queue |
| `notion/private-cycle-template.md` | Template pro Codename |
| `notion/SYNC.md` | GitHub ↔ Notion Workflow |

**Status:** Dokumentation fertig, **Nutzer hat Notion-Seite vermutlich noch nicht live** (nicht bestätigt).

---

## 10. Templates (`templates/`)

| Datei | Zweck |
|-------|-------|
| `5pm-scorecard.md` | Monat 1 |
| `icp-brief.md` | Monat 2 |
| `outreach-erstkontakt.md` | Compleadly |
| `outreach-manuell.md` | Nach Annahme |
| `interview-leitfaden.md` | Mom Test |
| `stop-weitermachen-memo.md` | Monat 6 |
| `cycle-log-vorlage.md` | Öffentliches Log |
| `codename-cycle-start.md` | Day 0 |

---

## 11. Assets

| Datei | Status |
|-------|--------|
| `assets/curriculum-visual.txt` | ✅ ASCII-Timeline (Screenshot für Notion/LinkedIn) |
| `assets/curriculum-visual.png` | ❌ Noch nicht erstellt |
| `assets/stop-weitermachen-visual.png` | ❌ Geplant (hieß früher kill-or-hustle-visual) |

---

## 12. Git / Release-Stand

| Item | Stand |
|------|-------|
| **main** | PR #1, #2, #3 merged |
| **Tag v1.0.0** | Gesetzt auf initialem Release |
| **Tag v1.2.0** | **Noch nicht gesetzt** — Inhalt ist auf main |
| **CHANGELOG** | v1.2 unter `[Unreleased]` — beim nächsten Release formalisieren |
| **README** | Verweist auf v1.2.0 |

### PR-Historie

1. **PR #1** — v0.5/v1.0 Playbook-Grundgerüst
2. **PR #2** — v1.1 Notion-Setup + LinkedIn-Posts (Rohfassung)
3. **PR #3** — Editorial Posts 1–5 + Stop/Weitermachen-Terminologie

---

## 13. Was ist FERTIG vs. OFFEN

### ✅ Fertig (im Repo)

- Vollständiges Playbook Monat 0–6 + Phase-2-Rahmen
- Alle Templates
- Codename-System + `cycles/README.md`
- LinkedIn GTM + 5 editorial Posts + Profiltext
- Notion-Dokumentation + Copy-paste-Inhalte
- Launch-Checklist
- Offenlegungsrichtlinien
- ASCII Curriculum-Visual

### ❌ Noch nicht erledigt (vom Nutzer / nächster Agent)

1. **Notion öffentlich live** (nach `notion/SETUP.md`)
2. **Notion privat** (Cycle-Template, Interview-DB)
3. **LinkedIn Profil** aktualisieren (Headline, Info, Featured)
4. **LinkedIn Post 1** posten (`[Notion-URL]` ersetzen)
5. **Newsletter** anlegen + Ausgabe #0 schreiben (nur Outline existiert)
6. **PNG Curriculum-Visual** erstellen
7. **Git-Tag v1.2.0** setzen + CHANGELOG `[Unreleased]` → Release
8. **Erster echter Cycle** — Idee + Codename vom Nutzer (noch unbekannt)
9. **Phase-2-Playbook** aus Praxis füllen (nach erstem Weitermachen)
10. Optional: **Newsletter Ausgabe #0** als vollständiger Markdown-Text
11. Optional: Terminologie **„Stop"** weiter abschwächen (Nutzer erwähnte „Pausieren" als Alternative — nicht entschieden)

---

## 14. Iterationsgeschichte (für Kontext)

1. **Initial:** Nutzer wollte privaten Startup-Idea-Evaluator auf LinkedIn, 6-Monats-Curriculum, versioniertes Playbook, Kill-or-Hustle-Rhyme
2. **Scope geschärft:** B2B DACH only, eine Idee, ~5h/Woche, bootstrapped not VC
3. **Architektur:** GitHub SoT + Notion Leseschicht + LinkedIn Labor/Bühne
4. **Name:** „Ideen auf Probe" (persönlich, deutsch)
5. **v1.1:** Notion-Struktur + LinkedIn-Posts
6. **Editorial Pass:** Posts zu kurz → editorialer Ton, persönlicher Anker, Seriosität
7. **Terminologie:** Kill/Hustle → Stop/Weitermachen (deutsches Publikum)
8. **Braindump:** Dieses Dokument

---

## 15. Regeln für künftige Agenten

### Immer

- Auf **Deutsch** schreiben (LinkedIn, Playbook, Posts)
- **Minimale Diffs** — nicht unnötig refactoren
- **GitHub = SoT** — Notion ist Spiegel
- **Eine Idee zur Zeit** im Playbook-Design respektieren
- **Stop/Weitermachen** Terminologie verwenden
- **Codenames** in öffentlichen Logs
- Cloud-Agent-Branches: `cursor/<name>-349b`
- Nach Änderungen: commit, push, PR erstellen/updaten

### Nie (ohne explizite Anweisung)

- Kill/Hustle wieder einführen
- Repo in `ideen-auf-probe` umbenennen
- Englische Parallel-Inhalte
- Company Page als Hauptkanal
- Compleadly-Follow-ups automatisieren
- Nutzers konkrete Idee erfinden oder eintragen
- VC/YC-Framing
- Markdown-Dateien erstellen, die der Nutzer nicht braucht (kein Over-documentation)

### Editorial-Stil (LinkedIn)

Siehe `linkedin/posts/README.md` — bei neuen Posts gleichen Ton verwenden.

---

## 16. Datei-Map (Quick Reference)

```
/
├── AGENT-BRAINDUMP.md          ← DIESE DATEI
├── README.md                   ← Projekt-Einstieg
├── CHANGELOG.md
├── LAUNCH-CHECKLIST.md         ← Woche 1 für Nutzer
├── playbook/                   ← Curriculum 00–07
├── templates/                  ← Kopierbare Vorlagen
├── cycles/                     ← Öffentliche Codename-Logs
├── linkedin/
│   ├── gtm-strategie.md
│   ├── profil-info.md
│   └── posts/                  ← 01–05 fertig
├── notion/                     ← Setup + Copy-paste
└── assets/                     ← curriculum-visual.txt
```

---

## 17. Nächste sinnvolle Tasks (priorisiert)

1. **CHANGELOG v1.2.0** formalisieren + Git-Tag `v1.2.0`
2. **Newsletter Ausgabe #0** als vollständigen Text in `linkedin/newsletter/00-manifest.md`
3. Nutzer beim **Notion-Setup** begleiten (Schritt-für-Schritt, falls gewünscht)
4. **PNG** aus `curriculum-visual.txt` generieren
5. Wenn Nutzer Idee nennt: **Cycle anlegen** unter `cycles/projekt-xxx/`
6. Nach erstem Cycle: **Phase 2** Playbook aus Erfahrung schreiben

---

## 18. Prompt-Snippet für neue Agent-Session

```
Projekt: Ideen auf Probe — öffentliches 6-Monats-B2B-Validierungsprotokoll für DACH.
Repo: github.com/wunderkind2k1/cursor-playground (Name bleibt).
SoT: GitHub. Notion = Leseschicht. LinkedIn = Distribution + Discovery.
Eine Idee/Codename zur Zeit. ~5h/Woche. Ende Monat 6: Stop oder Weitermachen.
Terminologie: Stop/Weitermachen (nicht Kill/Hustle). Deutsch only. B2B only.
Braindump: AGENT-BRAINDUMP.md lesen.
```

---

*Letzte Aktualisierung durch Agent-Session Juli 2026. Bei widersprüchlichen Angaben: GitHub `main` + dieses Dokument + CHANGELOG sind maßgeblich.*
