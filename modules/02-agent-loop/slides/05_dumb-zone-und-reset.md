## Die Dumb Zone beginnt nicht bei 100%

- Praktisch problematisch wird Kontext oft schon deutlich vor Vollauslastung — Relevanz, Präzision und Steuerbarkeit lassen vorher spürbar nach.
- Entscheidend ist nicht, ob formal noch Tokens frei sind, sondern ob der nächste Turn die richtigen Signale klar gewichtet sieht.

## Unter ~50% ist eine nützliche Operator-Heuristik

- Die Faustregel schafft Reserve für neue Reads, Tool-Outputs, Korrekturen und unerwartete Abzweigungen im laufenden Loop.
- Oberhalb davon steigt das Risiko stiller Qualitätsverluste: der Agent wirkt flüssig, übersieht aber Randbedingungen oder reagiert träger auf neue Informationen.

## Wenn es kippt: verdichten, resetten oder neu starten

- Dann hilft nicht noch mehr Prompting, sondern Kontext aktiv verkleinern, per `/reset` aufräumen oder direkt einen neuen Chat öffnen.
- Gute Operatoren behandeln einen frischen Arbeitsraum nicht als Rückschritt, sondern als Werkzeug für klarere nächste Turns.

## Was außerhalb des Chats stabil existieren muss

- Pläne, Entscheidungen, TODOs und Zwischenstände gehören in konkrete Dateien — nicht nur in den laufenden Transcript.
- Ein Reset wird dann stark, wenn das Wesentliche vorher dokumentiert und damit wieder anschlussfähig gemacht wurde.

## Faustregel: stabilisieren, dann resetten

- Erst das Wichtige in `research.md` oder `plan.md` festhalten, dann den Kontext leeren und mit klaren Referenzen neu starten.
- Ein Reset ist kein Rückschritt, sondern ein Werkzeug für einen kleineren, klareren und belastbareren nächsten Turn.

<!-- DIAGRAM: Kontextbalken mit Zonen komfortabel/kritisch/riskant; daneben Operator-Aktionen verdichten, /reset, neuer Chat; rechts Reset mit externen Artefakten als Einstieg -->
