## Workflows sind wiederverwendbare Rezepte

- Wenn ihr denselben Ablauf in jedem zweiten Task erklärt (Review-Schritte, Release-Checkliste, „so testen wir X“), ist das ein **Workflow** — nicht mehr Prompt-Fließtext.
- Einmal sauber festhalten, dann **konsistent auslösen** statt jedes Mal neu zu improvisieren.
- Auch bei der Verwendung von Skills gilt, konsistente Patterns und hohe Code-Standards sind besser als Skills 

## Skills kapseln längere, wiederkehrende Abläufe

- **Skills** bündeln Kontext, Schritte und Guardrails für Aufgaben, die mehr brauchen als einen Einzeiler — z. B. „Folien nach Workshop-Skill“, „Migrationsmuster in diesem Repo“.
- Gut, wenn der Skill sagt: **was** zu tun ist, **in welcher Reihenfolge**, und **wo aufhören** (Human-in-the-loop, keine riesigen Edits ohne OK).
- Der Agent holt sich die Skills nach Bedarf in den Kontext.
- Sie helfen dort, wo der Code nichts zeigt: bei Prozessschritten, Tool-Fallen, Sicherheitsvorgaben oder stillen Teamkonventionen.

## Slash Commands sind der kurze Einstieg

- **Slash Commands** starten ein bekanntes Muster mit wenig Tippaufwand — ideal für Standardstarts („Plane“, „Refactor nur diese Datei“, feste Vorlagen).
- Unterschied zur bloßen Erinnerung: Der Befehl **triggert** denselben Ablauf; der Agent muss nicht raten, was ihr meint.

## Der richtige Ablauf ist: Skill lesen, dann Zustand und Quelle prüfen

- Erst Skill als Startpunkt, dann Repo-Zustand, Tool-Schema, offizielle Doku, vorhandene Patterns und Auswirkungen validieren, bevor etwas installiert oder ausgeführt wird.
- Skills sind ein beliebtes Ziel für Prompt Injections, daher genau überprüfen, was der Inhalt ist.

