## Drei Gruppen von Artefakten: Wissen, Workflows, Constraints

Die Steuerfrage „Wie bringe ich den Agent dazu …?" führt immer zu einer dieser drei Gruppen:

- **Wissen:** Fakten, Konventionen und Pointer, die der Agent bei jeder relevanten Task abrufen können soll — persistent und auffindbar, nicht nur im Prompt.
- **Workflows:** Wiederkehrende Abläufe als wiederverwendbare Rezepte — einmal sauber festgehalten, dann konsistent auslösen statt jedes Mal neu improvisieren.
- **Constraints:** Harte, prüfbare Grenzen und Standards — nicht als Wunsch formuliert, sondern so, dass man sie einhalten und maschinell oder manuell prüfen kann.

## Warum diese Trennung trägt

- Jede Gruppe hat einen anderen Zweck und einen anderen Ort: Wissen gehört dorthin, wo der Agent es beim nächsten Run findet; Workflows gehören in auslösbare Skripte oder Skills; Constraints gehören in Linter, Tests, Rules oder Hooks.
- Wer alle drei vermischt und in einen einzigen Prompt-Block kippt, zahlt immer die Kontextkosten — auch wenn nur ein Drittel davon gerade relevant ist.
- Gute Operationalisierung trennt: **immer nötig**, **nur manchmal nötig**, **maschinell prüfbar**.

## Die drei Gruppen im Überblick


| Gruppe      | Zweck                            | Typische Form                   |
| ----------- | -------------------------------- | ------------------------------- |
| Wissen      | Kontext, der immer gilt          | `CLAUDE.md`, `AGENTS.md`        |
| Workflows   | Ablauf, der sich wiederholt      | Skills, Slash Commands          |
| Constraints | Grenzen, die prüfbar sein müssen | Rules, Guidelines, Hooks, Tests |


## Gute Operationalisierung fragt zuerst: Welche Gruppe?

- Erst die Gruppe bestimmen, dann das kleinstmögliche Artefakt wählen.
- Ein Artefakt, das in die falsche Gruppe wandert, kostet entweder Kontext bei jedem Turn oder bleibt unwirksam, weil niemand es auslöst.

