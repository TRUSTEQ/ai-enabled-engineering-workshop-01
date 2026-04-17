## So arbeitet ein Coding Agent in einem Turn

- Ein Turn beginnt nicht erst bei der Antwort, sondern bei Auftrag, Kontext und den ersten Entscheidungen im Loop.
- Wer den Turn verstehen will, schaut auf den ganzen Ablauf statt nur auf den finalen Output.

## Schritt 1: Ziel und Auftrag präzisieren

- Am Anfang steht die Klärung, was genau erledigt werden soll und woran ein gutes Ergebnis erkennbar ist.
- Ohne klares Ziel produziert der Turn leicht Aktivität, aber nicht unbedingt Fortschritt.

## Schritt 2: Kontext einsammeln, bevor editiert wird

- Gute Turns lesen erst relevante Dateien, suchen Signale und prüfen Randbedingungen, bevor sie etwas verändern.
- Frühe Edits ohne genug Kontext sind ein häufiger Startpunkt für Folgefehler im Loop.

## Schritt 3: Plan für diesen Turn bilden

- Auf Basis des Kontexts zerlegt der Agent die Aufgabe in kleine nächste Schritte für genau diesen Durchlauf.
- Der Plan muss nicht groß sein, aber klar genug, um Tool-Nutzung und die anschließende Prüfung gegen das Ziel zu steuern.

## Schritt 4: Tools gezielt ausführen

- Reads, Suchen, Shell-Kommandos und Edits erzeugen beobachtbare Zwischenergebnisse, auf denen der Turn weiterarbeitet.
- Gute Tool-Nutzung ist nicht hektisch, sondern passend zum aktuellen Erkenntnisstand.

## Schritt 5: Ergebnisse prüfen und Kurs halten

- Nach jedem sinnvollen Eingriff wird geprüft, ob das Ergebnis zum Auftrag passt oder ob nachgesteuert werden muss.
- So endet der Turn nicht auf Plausibilität, sondern auf überprüfter Zwischenstabilität.

## Schritt 6: Den Turn sauber abschließen

- Ein guter Abschluss fasst Ergebnis, Grenzen und offene Punkte knapp zusammen, statt den letzten Schritt nur zu wiederholen.
- Dadurch startet der nächste Turn auf einem klareren und belastbareren Zustand.

## Was im Turn technisch passiert

- Auftrag, Regeln und aktueller Kontext kommen als Token-Sequenz ins Modell — das Modell sieht nur, was jetzt im Context Window steht.
- Das Modell erzeugt als nächsten Schritt Antworttext oder einen Tool-Call; das Modell selbst führt aber kein Tool aus.
- Ein Tool-Call wird lokal durch die Agent-Umgebung ausgeführt, zum Beispiel als Datei-Read, Suche, Shell-Kommando oder Edit.
- Das Ergebnis dieser lokalen Ausführung, etwa Dateiinhalte, Suchtreffer, Terminal-Output oder Fehlermeldungen, wird als neuer Kontext an das Modell zurückgespielt.
- Erst auf Basis dieses zurückgespielten Ergebnisses entscheidet das Modell über den nächsten Schritt.
- Dieser Zyklus wiederholt sich innerhalb des Turns, bis der Agent eine abschließende Antwort produziert.
- Jeder Zwischenschritt landet im Transcript — als Spur aus Modell-Ausgaben, lokalen Tool-Ausführungen und zurückgespielten Ergebnissen.

<!-- DIAGRAM: Agent-Turn als Loop: Auftrag -> Kontext -> Plan -> Tools -> Verify -> Antwort -->