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
| [`01 - Projektmanagement und Tracking`](<01 - Projektmanagement und Tracking/>) | Register der offenen Annahmen (A-001 bis A-009) und der offenen Fragen (F-001 bis F-015), jeweils mit Kategorie, betroffenen Stakeholdern, Priorität, Komplexität und Status |
| [`02 - Stakeholderanalyse`](<02 - Stakeholderanalyse/>) | Übergreifende Stakeholderanalyse (Bewertung und Portfolio) sowie detaillierte Analysen je Stakeholder-Gruppe |
| ↳ `021 - Studierende` | Stakeholderanalyse und Interviewleitfaden für Studierende |
| ↳ `022 - Lehrende` | Stakeholderanalyse und Interviewleitfaden für Lehrende |
| [`03 - Requirements`](<03 - Requirements/>) | „AI Challenge Analyse“: Validierung KI-generierter Anforderungen (REQ-001, REQ-003) |
| [`99 - icebox`](<99 - icebox/>) | Ablage für zurückgestellte Inhalte (derzeit nur eine leere Platzhalterdatei) |

### Dateien im Detail

**01 – Projektmanagement und Tracking**

- `Register - offene Annahmen.xlsx` – Annahmen A-001 bis A-009, z. B. Aktivitätsmessung, Invasivität von Erinnerungen, Messung des Lernfortschritts und (neu) Integration des Authentifizierungssystems der FernFH. Alle Annahmen haben den Status „nicht validiert“.
- `Register - offene Fragen.xlsx` – Fragen F-001 bis F-015, z. B. Budget, Zeitrahmen, MVP, Datenminimierung und Rolle der Studiengangsleitung. Neu hinzugekommen sind Fragen zu Schnittstellen und Benutzerverwaltung (F-011 bis F-013), zu einem Gastzugang (F-014) und zum Reporting für Datenschutzbeauftragte (F-015). Alle Fragen haben den Status „offen“.

**02 – Stakeholderanalyse**

- `StakeholderAnalyse.xlsx` – Übersicht über acht Stakeholder: Studierende, Studierendenvertretung, Lehrende, Lehrendenvertretung, Studiengangsleitung, Studienadministration, IT & Online-Campus-Team sowie Datenschutz & Informationssicherheit. Je Stakeholder sind Interessen und Begründung beschrieben und Auswirkung, Einfluss und Risiko bei fehlender Einbindung auf einer Skala von 0 bis 10 bewertet. Der Handlungsbedarf wird als Einfluss minus Auswirkung berechnet. Ein Streudiagramm stellt Auswirkung und Einfluss als Portfolio dar (Mittelachsen bei 5).
- `021 - Studierende/Stakeholder - Studierende.docx` und `022 - Lehrende/Stakeholder - Lehrende.docx` – Beschreibung, Persona-Schema (angelehnt an Rupp & SOPHIST, 2021), benötigte Informationen, Erkenntnisziele und Begründung der gewählten Elicitation-Technik (Workshop).
- `021 - Studierende/Stakeholder - Studierende - Interviewleitfaden.docx` – Interviewleitfaden mit 12 Fragen (STF-01 bis STF-12).
- `022 - Lehrende/Stakeholder - Lehrende - Interviewleitfaden.docx` – Interviewleitfaden mit 14 Fragen (LPF-01 bis LPF-14).

**03 – Requirements**

- `AI Challenge Analyse.docx` – Analyse der KI-generierten Anforderungen REQ-001 (Erinnerung nach sieben Tagen Inaktivität) und REQ-003 (automatische Information der Studiengangsleitung bei kritischem Lernrückstand). Je Anforderung: getroffene Annahmen, fehlende Informationen, zu befragende Stakeholder, Prüffragen und Einordnung nach Rupp et al.

## Arbeitsstand

Stand: 23.10.2026

- **Aufgabe 1:** Detaillierte Stakeholderanalysen für Studierende und Lehrende mit Erkenntniszielen, Interviewleitfäden und Workshop als Elicitation-Technik; Analyse von zwei KI-generierten Anforderungen (REQ-001, REQ-003).
- **Mission 2b:** Register überarbeitet und in zwei getrennte Dateien für Annahmen und Fragen aufgeteilt. Neue Einträge betreffen vor allem Authentifizierung, Schnittstellen, Benutzerverwaltung und Datenschutz.
- **Aufgabe 2:** Übergreifende Stakeholderanalyse mit acht Stakeholdern, Bewertung und Portfolio-Darstellung. Neu gegenüber Aufgabe 1 sind unter anderem Studiengangsleitung, Studienadministration, IT & Online-Campus-Team sowie Datenschutz & Informationssicherheit.

## Hinweis zur Nutzung von KI

Gemäß der Dokumentationspflicht im LV-Konzept SED605 (Abschnitt „KI in der Lehre“):

- **Tool:** Claude Code (Anthropic)
- **Modell:** Claude Opus 5.5 (`claude-opus-5-5`), Überarbeitungen am 10.10.2026 und 23.10.2026
- **Art der Nutzung:** Überarbeitung und Strukturierung dieser README-Datei. Grundlage waren die im Repository vorhandenen Dateien sowie das LV-Konzept. Die inhaltlichen Arbeitsergebnisse in den Ordnern `00` bis `99` wurden durch diese Überarbeitung nicht verändert.
- **Übernommene Inhalte:** Der Text dieser README-Datei wurde von der KI formuliert und vom Team geprüft. Die Verantwortung für Richtigkeit und Vollständigkeit liegt beim Team.
