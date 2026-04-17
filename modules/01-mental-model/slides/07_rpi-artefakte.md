## Explizite Artefakte schlagen implizite Absicht

- Gute Zusammenarbeit mit einem LLM basiert nicht auf "es müsste doch klar sein", sondern auf sichtbaren, überprüfbaren Arbeitsgrundlagen.
- Was nicht explizit gemacht wird, ergänzt das Modell oft plausibel, aber nicht zwingend richtig.

## Artefakte entlasten Gedächtnis und Interpretation

- Wenn Kontext nur im Kopf bleibt, muss das Modell Lücken aus unscharfen Hinweisen rekonstruieren.
- Explizite Artefakte stabilisieren Annahmen, Fakten und Ziele über mehrere Loop-Durchläufe hinweg.

## `research.md` hält fest, was wir wissen

- `research.md` sammelt Ist-Stand, relevante Fakten, betroffene Stellen und offene Fragen, bevor daraus Maßnahmen werden.
- So startet der nächste Schritt nicht mit Vermutungen, sondern mit nachvollziehbarem Kontext.

## `plan.md` macht aus Wissen ein Vorgehen

- `plan.md` übersetzt Erkenntnisse in Reihenfolge, Quality Criteria und Acceptance Conditions.
- Dadurch muss Implementierung nicht raten, was wichtig ist und woran "fertig" erkennbar wird.

## Ohne Artefakte wird der Loop fragil

- Fehlt diese explizite Basis, springt der Agent direkt von vager Absicht zu plausibler Ausführung.
- Das erhöht das Risiko, dass Missverständnisse unbemerkt in Plan, Code und Verify weitergetragen werden.

<!-- DIAGRAM: Gegenüberstellung implizite Absicht im Kopf vs explizite Artefakte im Repo; research.md und plan.md stabilisieren den RPI-Loop -->
