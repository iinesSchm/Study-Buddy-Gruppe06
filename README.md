# Study Buddy – Gruppe 06

Repository der Gruppe 06 für die Gruppenarbeit in der Lehrveranstaltung **SED605 – Requirements Engineering** (ITMA, WS 2026/27) an der Ferdinand Porsche FernFH.

## Inhalt

1. [Projektkontext](#projektkontext)
2. [Teammitglieder](#teammitglieder)
3. [Struktur des Repositorys](#struktur-des-repositorys)
4. [Umstrukturierung des Repositorys](#umstrukturierung-des-repositorys)
5. [Artefakte der Aufgabe 3](#artefakte-der-aufgabe-3)
6. [Arbeitsstand](#arbeitsstand)
7. [Hinweis zur Nutzung von KI](#hinweis-zur-nutzung-von-ki)

## Projektkontext

Die Ferdinand Porsche FernFH (Projektauftraggeber) plant unter dem Arbeitstitel **„Study Buddy“** eine Studienbegleitung, die in den bestehenden Online Campus integriert wird. Der Study Buddy soll Studierende dabei unterstützen, Lernfortschritt, Aufgaben und Fristen im Blick zu behalten, und möglichst früh erkennen, wann Unterstützung hilfreich sein könnte. Dafür sollen unter anderem die im Online Campus vorhandenen Learning-Analytics-Daten genutzt werden.

Laut Auftrag ist ausdrücklich **keine fertige technische Lösung** zu entwickeln. Aufgabe des Projektteams ist es, Bedürfnisse zu verstehen, Anforderungen abzuleiten, Zielkonflikte aufzuzeigen und die für eine spätere Entwicklung relevanten Anforderungen herauszuarbeiten. Die Ergebnisse sollen eine Grundlage für die Entscheidung bilden, ob und wie ein Study Buddy umgesetzt werden kann.

Quellen: Auftrag des „Kunden“ und Project Brief „Study Buddy“.

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
| [`elicitation`](elicitation/) | Stakeholderanalysen und Interviewleitfäden für Studierende und Lehrende, Register der offenen Annahmen (A-001 bis A-009) und der offenen Fragen (F-001 bis F-015) sowie die „AI Challenge Analyse“ |
| [`stakeholders`](stakeholders/) | Übergreifende Stakeholder Map mit Bewertung und Portfolio |
| [`requirements`](requirements/) | Qualitätsanalyse der 15 KI-generierten Anforderungen und die Abgabeartefakte der Aufgabe 3, siehe [Artefakte der Aufgabe 3](#artefakte-der-aufgabe-3) |
| [`97 - Templates`](<97 - Templates/>) | Vorlagen für die Projektarbeit, derzeit eine Checkliste zur Qualitätsprüfung von Anforderungen |
| `98 - Literatur` | Nur lokal: Ablage für Fachliteratur; per `.gitignore` von der Versionierung ausgeschlossen |
| [`99 - icebox`](<99 - icebox/>) | Ablage für zurückgestellte Inhalte (derzeit nur eine leere Platzhalterdatei) |

### Dateien im Detail

**elicitation**

- `Stakeholder - Studierende.docx` und `Stakeholder - Lehrende.docx` – Beschreibung, Persona-Schema (angelehnt an Rupp & SOPHIST, 2021), benötigte Informationen, Erkenntnisziele und Begründung der gewählten Elicitation-Technik (Workshop).
- `Stakeholder - Studierende - Interviewleitfaden.docx` – Interviewleitfaden mit 12 Fragen (STF-01 bis STF-12).
- `Stakeholder - Lehrende - Interviewleitfaden.docx` – Interviewleitfaden mit 14 Fragen (LPF-01 bis LPF-14).
- `Register - offene Annahmen.xlsx` – Annahmen A-001 bis A-009, z. B. Aktivitätsmessung, Invasivität von Erinnerungen, Messung des Lernfortschritts und Integration des Authentifizierungssystems der FernFH. Alle Annahmen haben den Status „nicht validiert“.
- `Register - offene Fragen.xlsx` – Fragen F-001 bis F-015, z. B. Budget, Zeitrahmen, MVP, Datenminimierung und Rolle der Studiengangsleitung, außerdem Schnittstellen und Benutzerverwaltung (F-011 bis F-013), Gastzugang (F-014) und Reporting für Datenschutzbeauftragte (F-015). Alle Fragen haben den Status „offen“.
- `AI Challenge Analyse.docx` – Analyse der KI-generierten Anforderungen REQ-001 (Erinnerung nach sieben Tagen Inaktivität) und REQ-003 (automatische Information der Studiengangsleitung bei kritischem Lernrückstand). Je Anforderung: getroffene Annahmen, fehlende Informationen, zu befragende Stakeholder, Prüffragen und Einordnung nach Rupp et al. Die Nummerierung ist nicht identisch mit der Qualitätsanalyse in `requirements`.

**stakeholders**

- `D2 - Stakeholder Map.xlsx` – Übersicht über acht Stakeholder: Studierende, Studierendenvertretung, Lehrende, Lehrendenvertretung, Studiengangsleitung, Studienadministration, IT & Online-Campus-Team sowie Datenschutz & Informationssicherheit. Je Stakeholder sind Interessen und Begründung beschrieben und Auswirkung, Einfluss und Risiko bei fehlender Einbindung auf einer Skala von 0 bis 10 bewertet. Der Handlungsbedarf wird als Einfluss minus Auswirkung berechnet. Ein Streudiagramm stellt Auswirkung und Einfluss als Portfolio dar (Mittelachsen bei 5).

**97 – Templates**

- `Requirements Quality Checklist.md` – Checkliste mit neun Prüffragen zur Qualität einer Anforderung, gegliedert nach Inhalt, Dokumentation und Abgestimmtheit.

## Umstrukturierung des Repositorys

Mit der Abgabe der Aufgabe 3 wurde das Repository umstrukturiert, um die Analyse und Bewertung der Bearbeitung zu erleichtern. Die bestehenden Artefakte wurden sinngemäß in die im Online Campus vorgegebene Ordnerstruktur verschoben und teilweise umbenannt. Inhaltlich wurden die Dateien dabei nicht verändert.

| Neuer Ort | Aufgabe | Bisheriger Ort |
|---|---|---|
| `elicitation/Stakeholder - Studierende.docx` | Aufgabe 1 | `02 - Stakeholderanalyse/021 - Studierende/Stakeholder - Studierende.docx` |
| `elicitation/Stakeholder - Studierende - Interviewleitfaden.docx` | Aufgabe 1 | `02 - Stakeholderanalyse/021 - Studierende/Stakeholder - Studierende - Interviewleitfaden.docx` |
| `elicitation/Stakeholder - Lehrende.docx` | Aufgabe 1 | `02 - Stakeholderanalyse/022 - Lehrende/Stakeholder - Lehrende.docx` |
| `elicitation/Stakeholder - Lehrende - Interviewleitfaden.docx` | Aufgabe 1 | `02 - Stakeholderanalyse/022 - Lehrende/Stakeholder - Lehrende - Interviewleitfaden.docx` |
| `elicitation/Register - offene Annahmen.xlsx` | Aufgabe 1 und 2 | `01 - Projektmanagement und Tracking/Register - offene Annahmen.xlsx` |
| `elicitation/Register - offene Fragen.xlsx` | Aufgabe 1 und 2 | `01 - Projektmanagement und Tracking/Register - offene Fragen.xlsx` |
| `elicitation/AI Challenge Analyse.docx` | Aufgabe 1 | `03 - Requirements/AI Challenge Analyse.docx` |
| `stakeholders/D2 - Stakeholder Map.xlsx` | Aufgabe 2 | `02 - Stakeholderanalyse/StakeholderAnalyse.xlsx` |
| `requirements/quality-review.md` | Aufgabe 3 | `03 - Requirements/quality-review.md` |

## Artefakte der Aufgabe 3

Alle Artefakte der Aufgabe 3 liegen im Ordner [`requirements`](requirements/). Grundlage ist die Qualitätsanalyse; daraus wurden fünf Anforderungen ausgewählt und in vier Runden bearbeitet.

| Datei | Runde | Inhalt |
|---|---|---|
| [`quality-review.md`](requirements/quality-review.md) | Grundlage | Qualitätsanalyse von 15 KI-generierten Anforderungen (REQ-001 bis REQ-015). Je Anforderung: betroffene Qualitätsaspekte (Inhalt, Dokumentation, Abgestimmtheit) und Qualitätskriterien, Empfehlung, Fehlerbeschreibung, mögliche Konsequenz und fehlende Informationen, mit Verweisen auf die Register (A-xxx, F-xxx). Empfehlungen: 4 × rewrite, 6 × investigate, 5 × reconsider. |
| [`repaired-requirements.md`](requirements/repaired-requirements.md) | Runde 1 | Fünf menschlich erarbeitete Überarbeitungen bzw. begründete Klärungsentscheidungen zu REQ-001, REQ-005, REQ-006, REQ-014 und REQ-015. Je Anforderung: Original, Qualitätsmangel, Strategie, offene Fragen, Stakeholder und Ergebnis. |
| [`human-vs-ai.md`](requirements/human-vs-ai.md) | Runde 2 und 3 | Fünf Vergleiche zwischen Human- und KI-Version. Dokumentiert sind der verwendete Prompt, das Modell (Claude Opus 5.5, für REQ-005 ChatGPT GPT 6), die unveränderte KI-Version und die Bewertung nach einem Raster mit fünf Kriterien (max. 25 Punkte). Abschließend eine Reflexion „Wer hat gewonnen?“. |
| [`final-requirements.md`](requirements/final-requirements.md) | Runde 4 | Fünf abschließende Anforderungsfassungen bzw. begründete offene Entscheidungen (4 × `INVESTIGATE`, 1 × `RECONSIDER`) mit Begründung, nicht validierten Annahmen, offenen Fragen samt Stakeholdern, Abstimmung und Konflikten, Akzeptanzkriterien und Ergebnis. |

Ergänzend dient die [`Requirements Quality Checklist`](<97 - Templates/Requirements Quality Checklist.md>) als Vorlage für die Qualitätsprüfung.

## Arbeitsstand

Stand: 08.11.2026

- **Aufgabe 1:** Detaillierte Stakeholderanalysen für Studierende und Lehrende mit Erkenntniszielen, Interviewleitfäden und Workshop als Elicitation-Technik; Analyse von zwei KI-generierten Anforderungen (REQ-001, REQ-003).
- **Aufgabe 2b:** Register überarbeitet und in zwei getrennte Dateien für Annahmen und Fragen aufgeteilt. Neue Einträge betreffen vor allem Authentifizierung, Schnittstellen, Benutzerverwaltung und Datenschutz.
- **Aufgabe 2:** Übergreifende Stakeholderanalyse mit acht Stakeholdern, Bewertung und Portfolio-Darstellung. Neu gegenüber Aufgabe 1 sind unter anderem Studiengangsleitung, Studienadministration, IT & Online-Campus-Team sowie Datenschutz & Informationssicherheit.
- **Aufgabe 3:** Qualitätsanalyse von 15 KI-generierten Anforderungen mit Empfehlung je Anforderung (rewrite, investigate, reconsider), abgeglichen mit den Registern und der Stakeholderanalyse, dazu eine Checkliste zur Qualitätsprüfung als Vorlage. Anschließend Bearbeitung von fünf Anforderungen in vier Runden: Human-Version, KI-Version, Bewertung im Vergleich und finale Fassung (siehe [Artefakte der Aufgabe 3](#artefakte-der-aufgabe-3)). Zur Abgabe wurde das Repository umstrukturiert (siehe [Umstrukturierung des Repositorys](#umstrukturierung-des-repositorys)).

## Hinweis zur Nutzung von KI

Gemäß der Dokumentationspflicht im LV-Konzept SED605 (Abschnitt „KI in der Lehre“):

- **Tool:** Claude Code (Anthropic)
- **Modell:** Claude Opus 5.5 (`claude-opus-5-5`), Überarbeitungen am 10.10.2026, 23.10.2026, 30.10.2026 und 08.11.2026
- **Art der Nutzung:**
  - Überarbeitung und Strukturierung dieser README-Datei. Grundlage waren die im Repository vorhandenen Dateien sowie das LV-Konzept.
  - `requirements/quality-review.md`: Überführung der Excel-basierten Analyse in .md
  - `97 - Templates/Requirements Quality Checklist.md`: Checkliste lt. Online Kurs in .md file für weitere Verwendung überführt
  - `requirements/repaired-requirements.md`, `requirements/human-vs-ai.md`, `requirements/final-requirements.md`: Formatierung der Einzelanalysen in Markdown und Zusammenführung
