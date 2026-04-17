## Wissen gehört dorthin, wo der Agent es wiederfindet

- `CLAUDE.md` und `AGENTS.md` sind typische Orte für **persistentes Wissen**: nicht für lange Essays, sondern für das, was im Code oder in der Toolchain nicht klar genug steht.
- Die Leitfrage ist: **Was müsste ein kompetenter Entwickler über dieses Repo einmal gesagt bekommen, damit er hier nicht an stillen Konventionen vorbeiarbeitet?**

## Gute Inhalte: Abwesenheiten, Konventionen, Pointer

- **Abwesenheiten:** Was fehlt im Repo oder ist leicht falsch zu lesen? Zum Beispiel versteckte Annahmen, Umgebungen oder Namenskonventionen.
- **Konventionen:** Was gilt hier immer, obwohl es nicht zuverlässig aus dem Code hervorgeht?
- **Pointer:** Verweise auf die eine README, das eine Modul oder die Stelle im Code, wo die Wahrheit steht, statt die Wahrheit doppelt zu pflegen.
- **Konkretes Repo-Beispiel:** `Umlaute benutzen, nicht ae, oe, ue.` Das ist klein, gilt aber überall und ist ohne Hinweis leicht falsch.

## Was hier nicht hingehört

- **Kein aufgeblähter Build- oder Architektur-Überblick**, wenn das schon aus dem Code oder der Doku folgt. Sonst veraltet es doppelt und frisst Kontext.
- **Keine Workflows**, die erst ausgelöst werden müssen. Dafür sind Skills, Commands oder andere wiederverwendbare Abläufe da.
- **Keine vagen Qualitätswünsche oder harten Constraints.** Was prüfbar oder erzwingbar sein soll, gehört in Rules, Hooks, Lint oder Tests.
- **Kein externes Wissen ohne Anbindung**. APIs oder Doku-Fakten ohne feste Quelle werden schnell falsch oder unprüfbar, also lieber verlinken oder in einen kontrollierten Workflow packen.

<!-- DIAGRAM: CLAUDE.md / AGENTS.md als Filter: links „ein guter Entwickler müsste es einmal gesagt bekommen“, rechts „soll persistent auffindbar sein“ -->
