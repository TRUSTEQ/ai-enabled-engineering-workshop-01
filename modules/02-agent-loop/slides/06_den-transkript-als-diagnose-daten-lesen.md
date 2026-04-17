## Was das Transkript für Operateure ist

- Chronologischer Rohlog: Nachrichten, Modellantworten, Tool-Aufrufe und Tool-Ausgaben in der Reihenfolge, in der sie wirklich passiert sind.
- Nicht primär „Chat zum Mitlesen“, sondern die sichtbare Spur des Loops — vergleichbar mit Logzeilen, nur in natürlicher Sprache und Struktur.

## Warum es Diagnose-Daten sind

- Es ist die objektive Quelle dafür, was gelaufen ist — unabhängig davon, was man sich erinnert oder was die letzte Antwort plausibel klingen ließ.
- Wer das Transkript liest, kann Lücken zwischen Erwartung und Lauf schließen, bevor sie sich in falschen Commits oder kaputten Annahmen materialisieren.

## Was du gezielt scanst

- Reihenfolge der Schritte: kam ein Read vor einem Edit, oder wurde „geraten“, obwohl noch keine Fakten im Kontext waren?
- Wiederholte oder fehlgeschlagene Tool-Aufrufe, sehr große Eingaben oder plötzliche Themenwechsel ohne neuen Read.
- Stellen, an denen der Agent eine Zwischenbehauptung trifft, bevor relevante Tool-Ausgaben eingetroffen sind.

## Typische Lesefalle

- Nur die letzte Modellantwort zu lesen und die Tool-Kette davor zu ignorieren — dort steht oft, woher Zahlen, Pfade oder „Fakten“ eigentlich kamen.
- Lange Tool-Outputs überfliegen, obwohl sie die nächste Entscheidung tragen; kurz: nicht narrativ lesen, sondern die technische Spur mitdenken.

## Brücke zu Kontext und Steuerung

- Das Transkript zeigt, was das Kontextfenster gefüllt hat und wo es unnötig dicht oder redundant wurde — Anhaltspunkte für Verdichten, Entfernen oder Reset.
- Zusammen mit den Heuristiken aus den Folien zu Kontextbudget und externen Artefakten wird Lesen zum Steuerinstrument, nicht zur Nachbereitung.

<!-- DIAGRAM: Horizontales Band mit Blöcken User, Modell, Tool-Call, Tool-Resultat; Markierung „hier lesen“ über der Kette statt nur unter dem letzten Modellblock -->
