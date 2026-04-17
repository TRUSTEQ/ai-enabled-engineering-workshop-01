## Constraints sind keine Wünsche, sondern Grenzen

- Gute Constraints sagen **konkret**, was erlaubt, erwartet oder verboten ist — nicht „hohe Qualität" oder „keine Fehler" (das ist nicht steuerbar).
- Je **prüfbarer** die Grenze (Lint, Naming, Pflicht-Tests), desto weniger hängt sie von Stimmung und Modell ab.

## Rules und Guidelines steuern Verhalten im Alltag

- **Rules** und **Guidelines** sind **always-on** Steuerung: Standards, Sicherheitsgeländer, Projektjargon — solange sie kurz und wirklich relevant bleiben.
- Zu viel always-on Text **kostet Kontext** und verwässert das Wichtige; lieber schärfen als ansammeln.

## Hooks verschieben Kontrolle aus dem Prompt ins System

- **Hooks** binden Regeln an Ereignisse (vor/nach Tool, Commit, …): ein Teil der Kontrolle wird **automatisch** angestoßen statt jedes Mal mitgeschickt.
- Sinnvoll, wenn ihr **verifizieren** oder **blockieren** wollt, ohne den Prompt aufzublähen.

## Tests sind Verify ohne Kontextkosten

- **Tests** prüfen Verhalten maschinell und außerhalb des Context Windows — sie sagen dem Agenten nicht ständig, wie er denken soll, sondern zeigen nachgelagert, ob die Änderung funktioniert.
- Was zuverlässig automatisch prüfbar ist, sollte als Test, Hook oder Lint abgesichert werden statt als vager Dauerinstruktion im Prompt.

<!-- DIAGRAM: Drei Ebenen der Steuerung: Prompt-Kontext (Rules/Guidelines), wiederverwendeter Workflow (Skills), automatischer Check (Hooks/Tests/Lint) -->
