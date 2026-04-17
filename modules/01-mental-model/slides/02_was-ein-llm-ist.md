

## Was ein LLM eigentlich ist

- Ein **statistisches Sprachmodell**: es wählt wahrscheinliche nächste Tokens — kein garantiertes „Verstehen“ wie bei spezifiziertem Programmverhalten.
- Nützlich als **Werkzeug im Fließtext**, riskant, wenn man implizit Annahmen über Wahrheit oder Vollständigkeit macht.

## Unstrukturierter Input → unstrukturierter Output

- **Text rein, Text raus** — ohne von selbst euer Projektschema, eure API-Verträge oder eure Tabellenstruktur zu erzwingen.
- Wenn ihr **JSON, Schritte oder Schnittstellen** braucht, müsst ihr das **explizit verlangen** und das Ergebnis **gegen Erwartung prüfen**.



## Kein implizites Weltmodell

- Klassische Software: Zustände, Invarianten (Regeln, die immer gelten müssen, z. B. `balance >= 0`), Tests — Verhalten ist (idealerweise) **nachweisbar** aus Code und Specs.
- LLM: **kein fester innerer Zustand** eures Systems; Kontext kommt aus dem, was ihr **mitgebt** — und aus dem, was im Training/Fenster steckt, nicht aus „dem Repo an sich“.

## Plausibel ≠ richtig

- Antworten können **überzeugend klingen** und trotzdem **halluzinieren**, Kontext verfehlen oder Risiken ausblenden.
- **Verify** heißt: gegen Fakten, Specs, Tests und eure eigenen Acceptance Conditions — nicht gegen „es klang schlüssig“.

## Konsequenz fürs Engineering

- **Explizit machen:** Ziele, Constraints, Definition of Done, relevante Dateien und Team-Konventionen.
- **Artefakte und Schleifen** (Research, Plan, Implement, Verify) statt der Annahme: „Der Agent weiß schon, was ich meine.“

