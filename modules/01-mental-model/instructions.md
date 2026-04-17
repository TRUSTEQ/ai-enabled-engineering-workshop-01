# Modul 1 — Instructions für den Arbeitsblock

## Vorbereitung (vor dem ersten Prompt)

1. **Wählt eure erste Task bewusst aus.** Kriterien:
  - well-scoped (ihr wisst was "fertig" heißt)
  - nicht blockiert durch externe Inputs
  - realistisch — keine Toy-Task, aber auch kein Epic
2. **Startet den Loop auf der R-Stufe.** Nicht mit "implementiere X", sondern mit Research.
3. Nutzt für Research und Plan "schlauere" und für Implementierung die simpleren Modelle

## Arbeitsauftrag

1. **Research** — der Agent macht nicht alles allein. Ihr recherchiert mit:
  - **Agent-seitig**, in einem `research.md`:
    - was ist die aktuelle Situation im Code?
    - welche Dateien, Module, Abhängigkeiten sind betroffen?
    - welche Team-Conventions gelten hier (SOLID, REST, Naming, Tests)?
    - welche offenen Fragen bleiben?
  - **Euer Beitrag:** Alles, was ihr zusätzlich recherchiert, ergänzt den Kontext des Agents:
    - Release Notes / Changelogs der betroffenen Libraries
    - GitHub Issues und PRs (offen wie geschlossen) zum Thema
    - Architektur- oder Design-Vorschläge aus eurem Team, ADRs, Tickets
    - alles, was der Agent aus dem Repo allein nicht sehen kann
  - Gute Research heißt: Der Agent bringt Code-Kontext und bereits einiges aus der Welt, aber ihr ergänzt gezielt die Aspekte, die ihm noch fehlen oder im Projekt besonders wichtig sind. Ihr macht den Agent so erst komplett für eure konkrete Aufgabe.
2. **Plan** — lasst den Agent einen `plan.md` schreiben, der explizit enthält:
  - Schritt-für-Schritt-Vorgehen
  - **Quality Criteria**: welche Standards gelten (Konsistenz zum bestehenden Code, SOLID, REST, Test-Coverage-Erwartung)
  - **Acceptance Conditions**: woran erkennt ihr nach dem Implement, dass es wirklich fertig ist
3. **Review** beide Artefakte als Mensch. Lest sie Zeile für Zeile. Wenn ihr sie nicht unterschreiben würdet, geht der Implement nicht los.
4. **Implement** erst wenn `plan.md` steht. Währenddessen nur auf den Plan referenzieren. Nutzt, wenn sinnvoll, ein stärkeres Modell für Research/Plan und ein günstigeres für Implement.
5. **Verify** gegen die Acceptance Conditions aus `plan.md` — nicht gegen "läuft halt".
6. **Sauber abschließen.** Wenn der Loop an einem sinnvollen Zwischenstand ist: Verify fertig machen, committen, nächster Durchlauf startet von festem Boden. Haltet die Historie klein und lesbar; wenn ihr Commit-Messages strukturiert, dann mit einer einfachen Konvention wie Conventional Commits.

## Woran ihr merkt, dass es funktioniert

- Ihr merkt Fehler in Research, bevor sie in den Plan wandern
- Ihr merkt Fehler im Plan, bevor sie in den Code wandern
- Der Verify-Schritt fühlt sich wie Abhaken an, nicht wie Debugging

## Was ihr im Recap teilen werdet

- Hat der Agent im Research etwas übersehen, das ihr erst beim Review gemerkt habt?
- Konntet ihr beobachten, wie sich die Code Qualität im Repo auf die Ergebnisse des Agents ausgewirkt hat?
- Stand das, was ihr unter "Qualität" versteht, wirklich explizit im `plan.md`?
- Wo hat die Error-Cascade zugeschlagen?

