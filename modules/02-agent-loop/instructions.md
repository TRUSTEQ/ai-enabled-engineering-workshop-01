# Modul 2 — Instructions für den Arbeitsblock

## Haltungswechsel

Ihr seid jetzt nicht mehr "der, der den Prompt schreibt", sondern *Operator des Loops*. Das heißt: vorher überlegen, welchen Kontext der Agent braucht — und diesen Kontext bewusst klein und scharf halten.

## Arbeitsauftrag

1. **Macht mit der Task weiter**, an der ihr in Modul 1 gearbeitet habt — oder startet eine neue RPI-Runde, wenn die erste durch ist.
2. **Vor jeder Stufe (Research, Plan, Implement) Kontext aktiv setzen.** Bevor ihr den Agent loslaufen lasst:
  - Welche Dateien sind für diesen Schritt wirklich relevant?
  - Welche davon referenziert ihr selbst explizit (statt zu hoffen, der Agent findet sie)?
  - Was kann weggelassen werden, weil es für diesen Schritt nicht gebraucht wird?
3. **Condense statt Akkumulation.** Nach jedem Schritt nur die wirklich wichtigen Punkte in `research.md` oder `plan.md` festhalten:
  - Ergebnisse, Entscheidungen, offene Fragen — ja
  - Zwischenstände, ausprobierte Sackgassen, Tool-Output-Dumps — nein
  - Diese verdichteten Artefakte sind euer Kontext für die nächste Stufe, nicht der gesamte Transcript
4. **Transcript lesen als Diagnose.** Während der Agent läuft, mitlesen:
  - Wiederholt er sich, halluziniert er Pfade, überspringt er Reads?
  - Wird er bei jedem Turn sicherer, obwohl er weniger verifiziert? (Spiral of Confidence)
  - Macht er Edits, bevor er genug gelesen hat?
  - Das sind Signale, dass Kontext fehlt oder kippt — nicht, dass ihr härter prompten müsst.
5. **Context Window beobachten.** Sobald der Indikator über ~50% geht:
  - ist der Rest klein genug, um ihn in einem Turn zu beenden?
  - wenn nein: `reset` mit den verdichteten `research.md` / `plan.md` als Einstieg
  - Entscheidung bewusst treffen, nicht durchlaufen lassen
6. **Interrupt nur, wenn nötig.** Nicht als Übung. Eingreifen, wenn der Agent lange läuft, ohne einem Ergebnis näherzukommen — dann stoppen, Kontext gerade ziehen, neu ansetzen.
7. **Pre-built Skill nutzen.** Probiert einen der bereitgestellten Skills oder Slash Commands (z.B. `/review`, `/simplify`) an eurem aktuellen Stand aus. Beobachtet, was sich im nächsten Turn am Verhalten ändert.

## Failure Modes, auf die ihr aktiv achtet

- **Spiral of Confidence** — der Agent wird sicherer, obwohl er weniger verifiziert
- **Premature Edits** — Code-Änderungen, bevor genug gelesen wurde
- **Blind Edits** — Code Änderungen, die nicht Teil des Plans waren 
- **Silent Skip** — eine Datei, die hätte gelesen werden müssen, wurde übersprungen
- **Context Rot** — Transcript wird zu voll, Halluzinationen nehmen zu

Antwort darauf ist fast immer: Kontext verdichten und neu ansetzen, nicht härter prompten.

## Was ihr im Recap teilen werdet

- Welche Dateien habt ihr selbst referenziert, die der Agent allein nicht gefunden hätte?
- Was habt ihr bewusst *nicht* in `research.md` / `plan.md` übernommen?
- Wann war reset der richtige Zug?

