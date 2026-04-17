## Always-on: nur für wirklich allgemeine Leitplanken

- Always-on nur für Dinge, die wirklich bei jeder Task gelten müssen — kurz, konkret, stabil.
- Was nur in bestimmten Situationen relevant ist, sollte eher gezielt aktiviert werden als immer mitzuwandern.
- Zu viel always-on Text **kostet Kontext** und verwässert das Wichtige; lieber schärfen als ansammeln, im Zweifelsfall leer lassen. Auch ohne Guidelines, AGENTS.md, CLAUDE.md kann ein Agent arbeiten.

## On-demand: situatives Wissen bei Bedarf

- Skills und Slash Commands holen situatives Wissen nur dann in den Kontext, wenn es tatsächlich gebraucht wird.
- Ideal für Workflows, Spezialwissen und seltene Entscheidungen — kein dauerhafter Kontextverbrauch.

## Off-context: maschinell prüfbar und außerhalb des Prompts

- Hooks, Lint, Tests und CI-Checks prüfen vieles besser ganz ohne zusätzlichen Prompt-Kontext.
- Was zuverlässig automatisch verifiziert werden kann, gehört ins System, nicht in eine Dauerinstruktion.

## Faustregel

- Je konkreter und mechanischer, desto weiter nach unten: always-on → on-demand → off-context.
- Ziel ist nicht maximale Dokumentation, sondern minimale Reibung bei maximaler Verlässlichkeit.

