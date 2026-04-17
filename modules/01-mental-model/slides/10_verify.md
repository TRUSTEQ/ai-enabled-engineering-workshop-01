## Verify ist kein Nachtrag, sondern Teil jedes Loop-Durchlaufs

- Verify passiert nicht erst am Ende, sondern nach jedem sinnvollen Zwischenschritt.
- So werden Fehler, Missverständnisse und Scope-Drift sichtbar, bevor sie sich im nächsten Durchlauf verfestigen.

## Geprüft wird gegen Acceptance Conditions, nicht gegen Bauchgefühl

- Gute Verify-Arbeit vergleicht Ergebnis und Erwartungen explizit, statt nur auf Plausibilität zu schauen.
- Was als fertig gilt, sollte an klaren Bedingungen erkennbar sein und nicht an einem vagen „sieht gut aus“.

## Ohne klare Zielbedingungen wird Verify weich und beliebig

- Wenn vorher nicht feststeht, woran Erfolg erkennbar ist, wird Prüfen zur nachträglichen Interpretation.
- Dann bestätigt man leicht Output, der überzeugend wirkt, aber das eigentliche Ziel verfehlt.

## Verify prüft Verhalten, Artefakte und Nebenwirkungen

- Nicht nur „funktioniert“, sondern auch Scope, Konsistenz, Tests, Doku und unbeabsichtigte Änderungen zählen zur Prüfung.
- Gute Verify-Arbeit schaut deshalb auch auf das, was versehentlich mit verändert oder verschlechtert wurde.

## Jeder Loop sollte mit einem überprüften Zwischenstand enden

- Kleine, verifizierte Schritte sind stabiler als große Sprünge mit später Sammelprüfung.
- So bleibt der nächste Loop auf belastbarem Boden statt auf ungeprüfter Plausibilität.

<!-- DIAGRAM: RPIV-Schleife mit kleinem Verify-Check nach jedem Durchlauf statt einer einzigen Endkontrolle -->
