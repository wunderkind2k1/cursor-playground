# Notion Setup — Ideen auf Probe

Anleitung zum Anlegen der **öffentlichen Leseschicht** und des **privaten Cycle-Workspaces**.

**Source of Truth:** [GitHub](https://github.com/wunderkind2k1/cursor-playground) · Tag `v1.0.0`  
**Sync:** Manuell bei Version-Bumps (~30 Min.) — siehe [SYNC.md](./SYNC.md)

---

## Zwei Workspaces

| Workspace | Sichtbarkeit | Zweck |
|-----------|--------------|-------|
| **Öffentlich** | „Share to web" | Hübsche Lesefassung für LinkedIn Featured |
| **Privat** | Nur du | Volle Daten: Ideen, Interviews, Scores |

---

## Öffentlicher Workspace — Seitenbaum

```
📘 Ideen auf Probe                          ← Startseite (notion/public-startseite.md)
├── 📅 Das Curriculum                       ← Visuelles Overview (notion/public-curriculum.md)
├── 📖 Playbook
│   ├── Start hier                          ← playbook/00-start-hier.md
│   ├── Monat 1 — 5PM                       ← playbook/01-monat-1-5pm.md
│   ├── Monat 2 — ICP                       ← playbook/02-monat-2-icp.md
│   ├── Monat 3 — Discovery                 ← playbook/03-monat-3-discovery.md
│   ├── Monat 4 — Positionierung            ← playbook/04-monat-4-positionierung.md
│   ├── Monat 5 — Pricing                   ← playbook/05-monat-5-pricing.md
│   ├── Monat 6 — Stop oder Weitermachen            ← playbook/06-monat-6-stop-weitermachen.md
│   └── Phase 2 — Weitermachen                    ← playbook/07-phase-2-weitermachen.md
├── 📋 Templates                            ← Link zu GitHub / eingebettete Kopien
├── 🔄 Cycles                               ← Öffentliche Codename-Logs
│   └── (leer bis erster Lauf)
├── 🔗 Links
│   ├── GitHub (Source of Truth)
│   └── LinkedIn Newsletter (wenn live)
└── 📝 Changelog                            ← Aus CHANGELOG.md, gekürzt
```

---

## Schritt-für-Schritt (öffentlich)

### 1. Neue Top-Level-Seite

1. Notion → Neue Seite → **„Ideen auf Probe"**
2. Icon: 💡 oder 🧪
3. Cover: neutral, professionell (optional)
4. Inhalt aus [public-startseite.md](./public-startseite.md) kopieren

### 2. Unterseiten anlegen

Für jede Seite im Baum oben:

1. `/page` → Unterseite erstellen
2. Markdown aus dem entsprechenden `playbook/*.md` kopieren
3. Code-Blöcke in Notion-Callouts umwandeln (Gates = gelb, Stop = rot, Weitermachen = grün)
4. Footer auf jeder Seite:

> Version 1.1 · [GitHub](https://github.com/wunderkind2k1/cursor-playground) · [Changelog](https://github.com/wunderkind2k1/cursor-playground/blob/main/CHANGELOG.md)

### 3. Curriculum-Seite

Inhalt aus [public-curriculum.md](./public-curriculum.md) — enthält Mermaid-Diagramm und Gate-Tabelle.

### 4. Templates-Seite

Nicht alles duplizieren. Stattdessen:

| Template | Notion | GitHub-Link |
|----------|--------|-------------|
| 5PM Scorecard | Kurzbeschreibung + Link | `templates/5pm-scorecard.md` |
| ICP-Brief | Kurzbeschreibung + Link | `templates/icp-brief.md` |
| … | … | … |

Privat: Volle Templates als Notion-Duplikate zum Ausfüllen (s. unten).

### 5. Öffentlich schalten

1. Share → **Publish to web**
2. URL kopieren → LinkedIn Featured Slot 1
3. Suchmaschinen-Indexierung: optional an

---

## Privater Workspace — Seitenbaum

```
🔒 Ideen auf Probe — Intern
├── 🗂️ Cycles
│   └── [Template] Neuer Cycle              ← notion/private-cycle-template.md
│       ├── Idee (intern, voll)
│       ├── 5PM Scorecard
│       ├── ICP-Liste (Sales Nav Export)
│       ├── Interview-Log (Database)
│       ├── Muster & Synthese
│       ├── Pricing-Hypothese
│       └── Stop-Weitermachen-Memo
├── 📤 Export-Queue                         ← Was geht öffentlich (L1–L4)
└── 🔄 Sync-Log                             ← Datum, Version, was kopiert wurde
```

Details: [private-workspace.md](./private-workspace.md)

---

## Interview-Log (Notion Database)

| Property | Typ | Beispiel |
|----------|-----|----------|
| Name | Text | (intern) |
| Firma | Text | (intern) |
| Rolle | Select | IT-Leiter, Head of Ops, … |
| Datum | Date | 2026-08-15 |
| Schmerz | Text | In eigenen Worten |
| Workaround | Text | Excel, Agentur, … |
| Budget-Signal | Select | Stark / Mittel / Schwach |
| Economic Buyer | Checkbox | ✓ |
| Öffentlich zitierbar | Checkbox | Nur wenn anonym OK |
| Zitat (anonym) | Text | Für L2-Posts |

**View:** „Muster-Tracker" — Group by Schmerz

---

## Checkliste — Notion live

- [ ] Öffentliche Startseite publiziert
- [ ] Alle 8 Playbook-Monatsseiten angelegt
- [ ] Curriculum-Visual-Seite mit Diagramm
- [ ] Templates-Seite mit GitHub-Links
- [ ] Privater Cycle-Template-Duplikat bereit
- [ ] Interview-Database angelegt
- [ ] URL in LinkedIn Featured eingetragen
- [ ] Sync-Log-Eintrag: „v1.1 initial mirror"

---

## Nächster Schritt

→ Inhalte kopieren: [public-startseite.md](./public-startseite.md)  
→ Sync-Prozess: [SYNC.md](./SYNC.md)
