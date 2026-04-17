## Context Engineering: nicht mehr hinein, sondern besser herein

- Jedes Element im Kontext kostet Platz — und verdrängt dabei anderes.
- Die relevante Frage ist nicht „Wie bekomme ich mehr in den Kontext?", sondern: „Was verdient einen Platz im nächsten Turn?"
- Signale sind präzise Dateiinhalte, klare Ziele und relevante Tool-Ergebnisse. Rauschen sind veraltete Reads, lange Tracebacks und abgeschlossene Turns, die weiter mitgetragen werden.

## Was der Operator tatsächlich steuern kann

- Direktes Herausfiltern einzelner Items ist in den meisten AI Coding Agents nicht möglich — der Kontext ist kein manuell bearbeitbares Array.
- Was zur Verfügung steht: `/compact` komprimiert den Verlauf, `/reset` leert ihn vollständig.
- Der eigentliche Hebel liegt deshalb davor: Was kommt gar nicht erst hinein?

## Einfluss auf den Eingang, nicht auf den Ausgang

- Präzise, enge Aufgaben statt breiter Aufträge — weniger Rauschen durch den Auftrag selbst.
- Gezielte Dateireferenzen statt „schau mal alles an" — der Agent liest genau das, was für den nächsten Schritt relevant ist.
- Stabile Fakten (Entscheidungen, TODOs, Pläne) gehören in externe Dateien, nicht in den Transcript — so bleiben sie verfügbar, ohne das Context Window aufzublasen.

