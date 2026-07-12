# GitHub ↔ Notion Sync

**Regel:** GitHub ist Source of Truth. Notion wird nur bei Releases aktualisiert — nicht täglich.

---

## Wann syncen?

| Event | Aktion |
|-------|--------|
| Neuer Git-Tag (`v1.x.0`) | Öffentliche Notion-Seiten aktualisieren |
| Cycle Monats-Log | `cycles/[codename]/` auf GitHub + kurze Notion-Cycles-Seite |
| LinkedIn-Post | Kein Sync nötig (außer neuer Cycle-Eintrag) |
| Interview-Daten | **Nie** nach Notion öffentlich |

---

## Release-Sync (~30 Min.)

### 1. GitHub prüfen

```bash
git fetch origin main
git log --oneline -5
git tag -l
```

### 2. CHANGELOG lesen

Was hat sich geändert? Nur **geänderte** Playbook-Abschnitte kopieren.

### 3. Notion öffentlich aktualisieren

| Seite | Quelle |
|-------|--------|
| Startseite | `notion/public-startseite.md` + README |
| Curriculum | `notion/public-curriculum.md` |
| Monat 1–6 | `playbook/01-*.md` … `06-*.md` |
| Changelog | `CHANGELOG.md` (gekürzt) |
| Footer überall | Version + GitHub-Link |

### 4. Privates Sync-Log

Eintrag in Notion privat: Datum, Version, was kopiert wurde.

### 5. LinkedIn

Post-Vorlage: [linkedin/posts/05-version-bump.md](../linkedin/posts/05-version-bump.md)

---

## Cycle-Log Sync

Wenn ein Monat abgeschlossen ist:

1. `cycles/[codename]/README.md` auf GitHub aktualisieren (kuratiert, L2)
2. Notion öffentlich → Cycles → Unterseite `[Codename]` mit gleichem Inhalt
3. **Nicht** kopieren: Interview-Notizen, ICP-Namen, Preise

---

## Diff-Checkliste

Vor dem Sync:

- [ ] Git-Tag gesetzt?
- [ ] CHANGELOG aktuell?
- [ ] Nur geänderte Seiten kopiert (nicht alles)?
- [ ] Footer-Version überall gleich?
- [ ] Keine privaten Daten in öffentlicher Notion?
- [ ] LinkedIn-Post geplant?

---

## Version-Mapping

| Git-Tag | Notion Footer | GitHub Release |
|---------|---------------|----------------|
| v1.0.0 | Version 1.0 | Initial |
| v1.1.0 | Version 1.1 | Notion + LinkedIn Launch |
| v1.x.0 | Version 1.x | Cycle-Learnings |
