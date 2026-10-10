# Study Buddy – Gruppe 06

Repository der Gruppe 06 für die Gruppenarbeit in der Lehrveranstaltung **SED605 – Requirements Engineering** (ITMA, WS 2026/27) an der Ferdinand Porsche FernFH.

## Inhalt

1. [Projektkontext](#projektkontext)
2. [Teammitglieder](#teammitglieder)
3. [Struktur des Repositorys](#struktur-des-repositorys)
4. [Arbeitsstand](#arbeitsstand)
5. [Hinweis zur Nutzung von KI](#hinweis-zur-nutzung-von-ki)

## Projektkontext

Die Ferdinand Porsche FernFH (Projektauftraggeber) plant unter dem Arbeitstitel **„Study Buddy“** eine Studienbegleitung, die in den bestehenden Online Campus integriert wird. Der Study Buddy soll Studierende dabei unterstützen, Lernfortschritt, Aufgaben und Fristen im Blick zu behalten, und möglichst früh erkennen, wann Unterstützung hilfreich sein könnte. Dafür sollen unter anderem die im Online Campus vorhandenen Learning-Analytics-Daten genutzt werden.

Laut Auftrag ist ausdrücklich **keine fertige technische Lösung** zu entwickeln. Aufgabe des Projektteams ist es, Bedürfnisse zu verstehen, Anforderungen abzuleiten, Zielkonflikte aufzuzeigen und die für eine spätere Entwicklung relevanten Anforderungen herauszuarbeiten. Die Ergebnisse sollen eine Grundlage für die Entscheidung bilden, ob und wie ein Study Buddy umgesetzt werden kann.

Quellen: Auftrag des „Kunden“ und Project Brief, siehe Ordner [`00 - Projektinformationen`](<00 - Projektinformationen/>).

## Teammitglieder

| Name |
|---|
| Stefan Brezina |
| Franziska Leonie Schmuck-Längle |
| Nicholas David Müller |
| Patrick Töpfl |
| Ines Schmid |

## Struktur des Repositorys

| Ordner | Inhalt |
|---|---|
| [`00 - Projektinformationen`](<00 - Projektinformationen/>) | Auftrag des „Kunden“ (E-Mail) und Project Brief „Study Buddy“ (HTML) |
| [`01 - Projektmanagement und Tracking`](<01 - Projektmanagement und Tracking/>) | Register der offenen Annahmen (A-001 bis A-008) und der offenen Fragen (F-001 bis F-010), jeweils mit Kategorie, betroffenen Stakeholdern, Priorität, Komplexität und Status |
| [`02 - Stakeholderanalyse`](<02 - Stakeholderanalyse/>) | Stakeholderanalyse je Stakeholder-Gruppe mit Beschreibung, Persona-Schema (angelehnt an Rupp & SOPHIST, 2021), benötigten Informationen, Erkenntniszielen und Interviewleitfaden |
| ↳ `021 - Studierende` | Stakeholderanalyse und Interviewleitfaden für Studierende |
| ↳ `022 - Lehrende` | Stakeholderanalyse und Interviewleitfaden für Lehrende |
| [`03 - Requirements`](<03 - Requirements/>) | „AI Challenge Analyse“: Validierung KI-generierter Anforderungen (REQ-001, REQ-003) mit getroffenen Annahmen, fehlenden Informationen, zu befragenden Stakeholdern, Prüffragen und Einordnung nach Rupp et al. |
| [`99 - icebox`](<99 - icebox/>) | Ablage für zurückgestellte Inhalte (derzeit nur eine leere Platzhalterdatei) |

### Dateien im Detail

- `01 - Projektmanagement und Tracking/Register - offene Annahmen.xlsx` – Annahmen A-001 bis A-008 (z. B. Aktivitätsmessung, Invasivität von Erinnerungen, Messung des Lernfortschritts), alle mit Status „nicht validiert“
- `01 - Projektmanagement und Tracking/Register - offene Fragen und Annahmen.xlsx` – Fragen F-001 bis F-010 (z. B. Budget, Zeitrahmen, MVP, Datenminimierung, Rolle der Studiengangsleitung), alle mit Status „offen“
- `02 - Stakeholderanalyse/021 - Studierende/Stakeholder - Studierende.docx`
- `02 - Stakeholderanalyse/021 - Studierende/Stakeholder - Studierende - Interviewleitfaden.docx`
- `02 - Stakeholderanalyse/022 - Lehrende/Stakeholder - Lehrende.docx`
- `02 - Stakeholderanalyse/022 - Lehrende/Stakeholder - Lehrende - Interviewleitfaden.docx`
- `03 - Requirements/AI Challenge Analyse.docx`

## Arbeitsstand

Stand: 10.10.2026 (Version 0.1 der Register)

- Stakeholderanalysen für **Studierende** und **Lehrende** liegen vor, inklusive Erkenntniszielen und Interviewleitfäden.
- Offene Annahmen und offene Fragen werden in zwei Registern geführt; Priorität und Komplexität sind bei den Annahmen noch nicht bewertet.
- Zwei KI-generierte Anforderungen (REQ-001, REQ-003) wurden kritisch analysiert. Dabei wurde unter anderem festgestellt, dass die Studiengangsleitung als weiterer Stakeholder zu berücksichtigen ist.
- Die Interviewleitfäden enthalten Felder für Durchführung und Antworten; durchgeführte Interviews sind im Repository noch nicht dokumentiert.

## Hinweis zur Nutzung von KI

Gemäß der Dokumentationspflicht im LV-Konzept SED605 (Abschnitt „KI in der Lehre“):

- **Tool:** Claude Code (Anthropic)
- **Modell:** Claude Opus 5.5 (`claude-opus-5-5`), Stand 10.10.2026
- **Art der Nutzung:** Überarbeitung und Strukturierung dieser README-Datei. Grundlage waren die im Repository vorhandenen Dateien sowie das LV-Konzept. Die inhaltlichen Arbeitsergebnisse in den Ordnern `00` bis `99` wurden durch diese Überarbeitung nicht verändert.
- **Übernommene Inhalte:** Der Text dieser README-Datei wurde von der KI formuliert und vom Team geprüft. Die Verantwortung für Richtigkeit und Vollständigkeit liegt beim Team.
