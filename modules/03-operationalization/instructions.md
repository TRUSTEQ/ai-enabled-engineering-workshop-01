# Modul 3 — Instructions für den Arbeitsblock

## Ausgangspunkt

Ihr habt in Modul 1 und 2 Kontext *ad hoc* gesetzt — für diese eine Task. Jetzt geht es darum, das, was sich wiederholt hat oder sich wiederholen wird, so festzuschreiben, dass der Agent es beim nächsten Mal von selbst weiß.

## Context-Engineering gilt weiter (Lektion aus M2)

Alles, was in `CLAUDE.md` / `AGENTS.md` / Rules / Guidelines landet, wird bei **jedem** Request mitgeschickt. Das ist Kontextbudget, das ihr dauerhaft ausgebt. Je voller dieser Dauer-Kontext, desto schneller landet ihr in der Dumb Zone, egal wie gut die Task vorbereitet ist.

Deshalb vor jedem Artefakt die Ladezeit-Frage stellen:

- **Always-on** (`CLAUDE.md` / `AGENTS.md`, Rules, Guidelines) — wird jeden Turn geladen. Nur für Dinge, die wirklich *immer* gelten müssen.
- **On-demand** (Skills, Slash Commands) — wird nur geladen, wenn gebraucht. Für Workflows und Spezialwissen.
- **Off-context** (Hooks, Lint, Formatter, CI-Checks) — läuft außerhalb des Context Windows. Ideal für alles mechanisch Prüfbare und für Verify ohne zusätzliche Context-Kosten.

Faustregel: **je konkreter und mechanischer, desto weiter nach unten in dieser Liste.**

Modellwahl gehört dazu: starkes Modell für Denken, Research und Plan; günstigeres Modell für Ausführung, wenn der Pfad schon klar ist.

## Arbeitsauftrag

Wählt aus jeder der drei Gruppen **mindestens ein Artefakt**, das ihr heute gegen eure aktuelle Task erstellt oder ergänzt. Klein und konkret schlägt groß und allgemein.

### (a) Wissen, das der Agent braucht — `CLAUDE.md` / `AGENTS.md`

Was hätte der Agent heute von Anfang an wissen müssen, das ihm niemand gesagt hat *und* was wirklich für (fast) jede Task gilt?

Rein gehört nur, was im Code nicht sichtbar ist und trotzdem jede Task betrifft:

- Abwesenheiten: "wir machen X nicht mehr, weil …" — Patterns, die der Agent gerade *nicht* im Code findet
- nicht-offensichtliche Konventionen, die im Code *nicht durchgehend* sichtbar sind (z. B. "Timestamps immer UTC", wenn grep das Gegenteil zeigen würde)
- Pointer statt Inhalt: wo liegen Build/Test-Details, welche Skills gibt es — nicht die Details selbst

Explizit **nicht** rein:

- Build-/Test-/Deploy-Kommandos — stehen in `package.json`, `Makefile`, CI-Config, und der Agent findet sie per grep
- allgemeiner Architektur-Überblick — das meiste ist im Code sichtbar; nur bewusste Nicht-Entscheidungen gehören in die Abwesenheiten-Liste
- externe Systeme, Dashboards, Ticket-Projekte, auf die der Agent keinen Zugriff hat — das ist Deko, die jeden Turn Kontext kostet; wenn der Agent sie nutzen soll, ist es ein MCP oder Tool-Call

Diese Datei sollte sehr kurz gehalten werden, sofern sie überhaupt notwendig ist.

Ergänzt `CLAUDE.md / AGENTS.md` (oder legt sie an) mit **einem** konkreten Punkt aus eurem heutigen Tag.

### (b) Wiederverwendbare Workflows — Skills / Slash Commands

Welche Sequenz an Schritten habt ihr heute mehr als einmal gebraucht?

- ein Review-Schritt, der immer gleich abläuft
- ein Standard-Research-Vorgehen für Bug-Tickets
- ein Test-Setup-Skript, das ihr erklärt habt

Schreibt daraus einen Skill oder Slash Command — so klein wie möglich, nur die Schritte, die wirklich gleich sind.

Wichtig: Ein Skill ersetzt kein Prüfen. Wenn ein Skill Downloads, externe Tools oder neue Dependencies vorschlägt, wird das nicht blind übernommen, sondern explizit geprüft.

### (c) Always-on Constraints — Rules / Guidelines / Hooks

Was soll der Agent *nie wieder* vergessen, egal welche Task?

- konkret und checkbar: Naming, Lint-Regel, Pflicht-Test, verbotene Library
- **kein** "sei hochqualitativ" — das ist äquivalent zu "mach keine Fehler" und damit wertlos
- wenn es automatisch prüfbar ist, hook es (z.B. lint, format, typecheck, Tests) — das ist Verify ohne Context-Kosten

Ergänzt eine Rule oder einen Hook für genau eine konkrete Constraint.

## Bevor ihr ein Artefakt schreibt — fragt euch

1. Steht das schon irgendwo im Code und der Agent würde es per grep finden? → kein Artefakt nötig
2. Ist das "vage gut sein"? → kein Artefakt, sondern aktiveres Review im Alltag
3. Ist es automatisch prüfbar? → Hook / Lint / CI, nicht Guideline
4. Braucht es das wirklich *jeden* Turn? → wenn nein: Skill oder Slash Command, nicht `CLAUDE.md`
5. Ist es konkret, wiederkehrend, nicht aus dem Code ablesbar, und überall relevant? → dann und nur dann always-on

## Was ihr im Recap teilen werdet

- Welches Artefakt habt ihr geschrieben — und welches habt ihr *bewusst nicht* geschrieben, weil der Codebase es schon lehrt?
- Was habt ihr bewusst *nicht* in `CLAUDE.md` gepackt, weil es den Dauer-Kontext nur aufgebläht hätte?
- Wo habt ihr gemerkt, dass eine Guideline zu vage war, um wirklich zu greifen?

