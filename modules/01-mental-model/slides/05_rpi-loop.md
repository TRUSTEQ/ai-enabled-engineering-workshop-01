## Der RPI-Loop

- Mit LLMs arbeiten wir nicht in einem Sprung, sondern in einer kontrollierten Schleife: `Research → Plan → Implement → Verify`.
- Jeder Schritt macht Annahmen expliziter und senkt das Risiko, dass plausible Fehler unbemerkt in den nächsten Schritt wandern.

## Research macht den Kontext explizit

- Bevor etwas gebaut wird, klären wir Ist-Stand, betroffene Dateien, relevante Fakten, Abhängigkeiten und offene Fragen.
- Was hier unscharf bleibt, taucht später als Fehler im Plan oder im Code wieder auf.

## Plan macht aus Erkenntnissen ein konkretes Vorgehen

- Der Plan übersetzt Research in Reihenfolge, Qualitätskriterien und Acceptance Conditions.
- Erst wenn klar ist, was getan werden soll und woran "fertig" erkennbar ist, lohnt sich Implementierung.

## Implement ist nur ein Schritt im Loop

- Implementierung ist die Ausführung auf Basis des Plans, nicht der Moment, in dem Ziel und Qualität erst noch erraten werden.
- So bleibt der Agent an explizite Artefakte gebunden statt an implizite Absicht.

## Verify schließt den Loop

- Geprüft wird gegen Fakten, Tests und Acceptance Conditions, nicht gegen "klingt plausibel" oder "läuft irgendwie".
- Verify ist kein Bonus-Schritt am Ende, sondern der Abschluss jedes sauberen Durchlaufs.

<!-- DIAGRAM: Kreis oder Flow Research -> Plan -> Implement -> Verify -> zurück zu Research; jeder Schritt reduziert Fehlannahmen -->
