## BIBO — bullshit in, bullshit out

- Die **Qualität des Outputs** hängt an Kontext, Fakten und Klarheit der Aufgabe — nicht daran, welches Modell ihr wählt, wenn der Input schwach ist.
- Ein starkes Modell macht aus **unklarem Input** eher **überzeugenden Unsinn** als eine sichere Lösung.

## Wo „Bullshit“ herkommt

- **Vage Prompts** („mach mal besser“), **fehlende Fakten**, **widersprüchliche Vorgaben**, **veralteter oder falscher Kontext** — das Modell füllt Lücken plausibel.
- **Plausibel klingend** heißt nicht **richtig** oder **passend zu eurem System**; ohne Referenz merkt ihr das oft erst spät.

## Konsequenz für eure Arbeit

- **Research und explizite Artefakte** sind Input-Qualität: was ihr nicht festhaltet, kann der Agent nicht zuverlässig berücksichtigen.
- Ohne sauberen Input kein verlässlicher Output — das ist die Brücke zum **RPI-Loop** und zu `research.md` / `plan.md`.

## Codebase-Qualität ist Input-Qualität

- Der Agent liest **euren Ist-Stand im Repo** mit: unklare Grenzen, uneinheitliche Patterns, technische Schulden — das landet **als Kontext** in Analyse und Vorschlägen; das Modell **ersetzt** keine saubere Architektur durch reines Nachfragen.
- **Hohe Qualität im Code** hält deshalb den Kontext stabil und **reduziert BIBO**, bevor ihr den Loop startet — nicht erst als „Aufräum-Projekt“ nach dem fünften Halluzinations-Patch.
- **Clean Code, SOLID und Team-Standards** vertiefen wir im Modul noch einmal gezielt — hier der gemeinsame Nenner: **Schlechter Code ist schlechter Input; guter Code ist besserer Kontext.**

<!-- DIAGRAM: Pfeil Input-Qualität → Output-Qualität, Warnsymbol bei schwachem Input (BIBO) -->
