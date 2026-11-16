# Human vs. AI – Vergleich

**RE – Mission 3 · Runde 2 und 3**

Vergleich der menschlich erarbeiteten Versionen aus [repaired-requirements.md](repaired-requirements.md) mit KI-generierten Versionen derselben Anforderungen. Je Anforderung sind Modell, Prompt, KI-Ergebnis und Bewertung dokumentiert. Die Reflexion am Ende fasst die Erkenntnisse über alle Vergleiche zusammen.

## Übersicht

| Requirement-ID | Titel | Modell | Strategie Human | Strategie KI | Human | KI |
| :--- | :--- | :--- | :---: | :---: | :---: | :---: |
| [REQ-001](#req-001--the-seven-day-rule) | The Seven-Day Rule | Claude Opus 5.5 | `INVESTIGATE` | `INVESTIGATE` | 20/25 | 22/25 |
| [REQ-005](#req-005--monday-morning) | Monday Morning | ChatGPT (GPT 6) | `INVESTIGATE` | `INVESTIGATE` | 23/25 | 21/25 |
| [REQ-006](#req-006--the-missing-definition) | The Missing Definition | Claude Opus 5.5 | `INVESTIGATE` | `INVESTIGATE` | 18/25 | 22/25 |
| [REQ-014](#req-014--the-accessibility-shortcut) | The Accessibility Shortcut | Claude Opus 5.5 | `INVESTIGATE` | `INVESTIGATE` | 22/25 | 21/25 |
| [REQ-015](#req-015--the-ai-knows-best) | The AI Knows Best | Claude Opus 5.5 | `RECONSIDER` | `RECONSIDER` | 17/25 | 22/25 |

## Prompt

Basis-Prompt für die KI-Versionen. Abweichungen sind bei der jeweiligen Anforderung vermerkt.

> Du bist Requirements Engineer und überprüfst Anforderungsentwürfe für den Digital Study Buddy, ein digitales Unterstützungssystem für Studierende einer Fernhochschule. Analysiere die Anforderung anhand der Qualitätsaspekte Inhalt, Dokumentation und Abgestimmtheit.
>
> 1. Identifiziere konkrete Qualitätsmängel und begründe sie.
> 2. Formuliere eine verbesserte Anforderung, soweit die vorliegenden Informationen dies erlauben.
> 3. Erfinde keine Stakeholderbedürfnisse, Interviewergebnisse, rechtlichen Freigaben oder technischen Rahmenbedingungen.
> 4. Kennzeichne fehlende Informationen, unbegründete Annahmen und notwendige Abstimmungen ausdrücklich.
> 5. Schlage geeignete Akzeptanzkriterien nur vor, wenn diese fachlich begründbar sind.
> 6. Gib für die Anforderung den Status REWRITE, INVESTIGATE oder RECONSIDER an.
>    * **REWRITE – Anforderung überarbeiten:** Die notwendigen Informationen liegen vor. Sie können die Formulierung präzisieren, strukturieren oder in mehrere Anforderungen aufteilen.
>    * **INVESTIGATE – Weitere Informationen beschaffen:** Wesentliche Informationen fehlen. Formulieren Sie konkrete Fragen und benennen Sie die Stakeholder\*innen, mit denen diese geklärt werden müssen.
>    * **RECONSIDER – Anforderung hinterfragen:** Die Notwendigkeit, Angemessenheit oder Zulässigkeit ist unklar. Begründen Sie, warum die Anforderung nicht ohne weitere Klärung übernommen werden sollte.
>
> Hier ist die Anforderung: [Anforderungstext]

## Bewertungsraster

Jede Version wird je Kriterium mit Punkten bewertet, maximal 25 Punkte.

1. Fachliche Angemessenheit
2. Eindeutigkeit und Verständlichkeit
3. Vollständigkeit und Überprüfbarkeit
4. Umgang mit Annahmen
5. Abstimmung und Konflikte

---

## REQ-001 – The Seven-Day Rule

> „Das System muss Studierende automatisch benachrichtigen, wenn sie sieben Tage lang nicht im Online Campus aktiv waren.“

**Human-Version:** siehe [repaired-requirements.md](repaired-requirements.md#req-001--the-seven-day-rule) · Strategie `INVESTIGATE`

### KI-Version

**Modell:** Claude Opus 5.5

**Prompt:** Variante des Basis-Prompts für zwei Anforderungen gemeinsam, ohne Definition der Strategien:

> Du bist Requirements Engineer und überprüfst Anforderungsentwürfe für den Digital Study Buddy, ein digitales Unterstützungssystem für Studierende einer Fernhochschule. Analysiere jede Anforderung anhand der Qualitätsaspekte Inhalt, Dokumentation und Abgestimmtheit.
> 1. Identifiziere konkrete Qualitätsmängel und begründe sie.
> 2. Formuliere eine verbesserte Anforderung, soweit die vorliegenden Informationen dies erlauben.
> 3. Erfinde keine Stakeholderbedürfnisse, Interviewergebnisse, rechtlichen Freigaben oder technischen Rahmenbedingungen.
> 4. Kennzeichne fehlende Informationen, unbegründete Annahmen und notwendige Abstimmungen ausdrücklich.
> 5. Schlage geeignete Akzeptanzkriterien nur vor, wenn diese fachlich begründbar sind.
> 6. Gib für jede Anforderung den Status REWRITE, INVESTIGATE oder RECONSIDER an.
>
> Hier sind die Anforderungen: [REQ-001, REQ-014]

Die KI vergibt für REQ-001 ebenfalls `INVESTIGATE` und schlägt keine Neuformulierung sowie keine Akzeptanzkriterien vor.

#### Qualitätsmängel

* **Inhalt – Korrektheit/Adäquatheit:** Die Annahme, dass Inaktivität auf Unterstützungsbedarf hinweist, ist nicht belegt. Studierende einer Fernhochschule lernen häufig unregelmäßig, offline oder abgabeorientiert.
* **Inhalt – Notwendigkeit:** Kein Bezug zu Projektziel, Stakeholder-Bedarf oder Rahmenbedingung erkennbar.
* **Inhalt – Vorzeitige Entwurfsentscheidung:** „Automatisch benachrichtigen“ legt eine Lösung fest, bevor das Problem geklärt ist.
* **Inhalt – Vollständigkeit:** Kanal, Inhalt, Wiederholung und Deaktivierbarkeit fehlen.
* **Dokumentation – Eindeutigkeit:** „Aktiv“ ist nicht definiert (Login, Seitenaufruf, Download, Abgabe?).
* **Dokumentation – Verfolgbarkeit:** Keine Quelle oder Begründung für die sieben Tage.
* **Abgestimmtheit:** Die Auswertung von Aktivitätsdaten betrifft Datenschutz und Akzeptanz; eine Abstimmung ist nicht dokumentiert.

#### Ergebnis

* **Verbesserte Anforderung:** Nicht seriös möglich. Jede Neuformulierung würde Aktivitätsdefinition, Zeitraum und Kanal erfinden.
* **Fehlende Informationen:** Definition von Aktivität; verfügbare Daten des Online Campus; Kanal; Opt-in oder Opt-out.
* **Unbegründete Annahmen:** Inaktivität bedeutet Unterstützungsbedarf; sieben Tage sind ein geeigneter Schwellenwert.
* **Abstimmung nötig mit:** Studierenden, Studiengangsleitung, Lehrenden, IT-Verantwortlichen (Online Campus), Datenschutzverantwortlichen.
* **Akzeptanzkriterien:** Keine, da ohne geklärten Bedarf nicht fachlich begründbar.
* **Status:** `INVESTIGATE`

### Bewertung

| Bewertungskriterium | Human | KI |
| :--- | :---: | :---: |
| **Fachliche Angemessenheit** | 4 | 5 |
| **Eindeutigkeit und Verständlichkeit** | 5 | 4 |
| **Vollständigkeit und Überprüfbarkeit** | 3 | 4 |
| **Umgang mit Annahmen** | 4 | 5 |
| **Abstimmung und Konflikte** | 4 | 4 |
| **Gesamt** | **20/25** | **22/25** |

Die KI-Version liegt knapp vorne, vor allem weil sie Annahmen und fehlende Informationen ausdrücklicher kennzeichnet. Beide Versionen erfinden keine Zahlen, Kanäle oder Entscheidungen.

* **Fachliche Angemessenheit:** Beide erkennen den Kernmangel, die unbelegte Annahme „Inaktivität = Unterstützungsbedarf“. Die KI benennt zusätzlich die vorzeitige Entwurfsentscheidung („automatisch benachrichtigen legt eine Lösung fest“) und die fehlende Notwendigkeit.
* **Eindeutigkeit und Verständlichkeit:** Die Human-Version ist knapp und in einem Absatz verständlich. Die KI-Version ist gut gegliedert, aber länger und wiederholt Punkte (z. B. Kanal unter Vollständigkeit und unter fehlende Informationen).
* **Vollständigkeit und Überprüfbarkeit:** Die Human-Version erwähnt Kanal und Deaktivierbarkeit nicht. Die KI nennt beides und begründet, warum keine Akzeptanzkriterien möglich sind („ohne geklärten Bedarf nicht fachlich begründbar“).
* **Umgang mit Annahmen:** Die KI trennt fehlende Informationen und unbegründete Annahmen in eigenen Absätzen und lehnt eine Neuformulierung ausdrücklich ab, weil sie „Aktivitätsdefinition, Zeitraum und Kanal erfinden“ würde. Sie ergänzt keinen neuen Zeitraum und keine Technik.

---

## REQ-005 – Monday Morning

> „Alle Studierenden müssen jeden Montag um 08:00 Uhr eine personalisierte Fortschrittsübersicht per E-Mail erhalten.“

**Human-Version:** siehe [repaired-requirements.md](repaired-requirements.md#req-005--monday-morning) · Strategie `INVESTIGATE`

### KI-Version

**Modell:** ChatGPT (GPT 6)

**Prompt:** Suggested Prompt aus dem Online Campus (Basis-Prompt), unverändert.

#### 1. Ursprüngliche Anforderung

> Alle Studierenden müssen jeden Montag um 08:00 Uhr eine personalisierte Fortschrittsübersicht per E-Mail erhalten.

**Status:** `INVESTIGATE`

**Begründung:** Die Anforderung beschreibt eine nachvollziehbare Funktion, enthält jedoch mehrere fachlich unbegründete Festlegungen. Insbesondere Empfängerkreis, Versandzeitpunkt, Kommunikationskanal und Personalisierung müssen mit den Stakeholdern geklärt werden, bevor die Anforderung verbindlich formuliert werden kann.

#### 2. Qualitätsanalyse

| Qualitätsaspekt | Konkreter Mangel | Begründung |
| :--- | :--- | :--- |
| Inhalt | Nutzen und Bedarf nicht belegt | Es ist nicht nachgewiesen, dass alle Studierenden eine wöchentliche Fortschrittsübersicht benötigen oder wünschen. |
| Inhalt | „Personalisiert“ nicht definiert | Unklar ist, welche individuellen Daten berücksichtigt werden und wie der Studienfortschritt berechnet wird. |
| Inhalt | Empfängerkreis pauschal festgelegt | „Alle Studierenden“ berücksichtigt weder unterschiedliche Studienstatus noch individuelle Präferenzen. |
| Inhalt | Kommunikationskanal vorgegeben | Die E-Mail ist als Lösungsentscheidung festgelegt, ohne dass ihre Eignung nachgewiesen ist. |
| Dokumentation | Zeitangabe unvollständig | Es fehlen Zeitzone und Festlegung, ob 08:00 Uhr der Versand- oder Empfangszeitpunkt ist. |
| Dokumentation | Nicht vollständig verifizierbar | Ohne Definition von Inhalt und Personalisierung lässt sich die korrekte Umsetzung nicht objektiv testen. |
| Abgestimmtheit | Keine dokumentierte Stakeholder-Abstimmung | Es ist nicht belegt, dass Studierende und zuständige Hochschulvertreter Empfängerkreis, Häufigkeit und Kanal bestätigt haben. |
| Abgestimmtheit | Umgang mit personenbezogenen Daten ungeklärt | Datenquellen, Zugriffsberechtigungen und datenschutzrechtliche Voraussetzungen müssen geprüft werden. Eine rechtliche Freigabe ist nicht dokumentiert. |

#### 3. Verbesserte Anforderung

Da wesentliche fachliche Informationen fehlen, ist zunächst nur eine vorläufige, lösungsneutrale Formulierung möglich:

> „Der Digital Study Buddy soll Studierenden eine individuelle Übersicht über ihren Studienfortschritt bereitstellen.“

Diese Formulierung bewahrt die erkennbare Kernfunktion. Die Festlegungen zu Häufigkeit, Uhrzeit, Empfängerkreis und Kommunikationskanal bleiben ausdrücklich offen. Auch der konkrete Inhalt der Übersicht ist noch zu definieren.

Die Umformulierung ist keine bereits abgestimmte oder vollständig spezifizierte Anforderung.

#### 4. Offene Informationen und notwendige Abstimmungen

| Klärungsbedarf | Zuständige Stakeholder (Vorschlag) |
| :--- | :--- |
| Welche Informationen gehören zum Studienfortschritt? | Studierende, Studiengangsverantwortliche |
| Wer soll die Übersicht erhalten und wer gegebenenfalls nicht? | Studierende, Hochschulverwaltung |
| Ist eine wöchentliche Bereitstellung erforderlich? Warum montags um 08:00 Uhr? | Studierende, Produktverantwortliche |
| Ist E-Mail der geeignete Kommunikationskanal oder sind Alternativen gewünscht? | Studierende, Produktverantwortliche |
| Welche Datenquellen dürfen für die Personalisierung verwendet werden? | IT, Datenschutzverantwortliche, Fachbereich |
| Welche Voraussetzungen gelten für die Verarbeitung und Übermittlung individueller Fortschrittsdaten? | Datenschutzverantwortliche, IT |

Die vorgeschlagenen Ansprechpartner sind keine bestätigten Zuständigkeiten.

#### 5. Akzeptanzkriterien

Auf Grundlage der vorliegenden Informationen lässt sich nur ein allgemeines, vorläufiges Akzeptanzkriterium begründen:

* **AK-01:** Für einen Studierenden kann der Digital Study Buddy eine diesem Studierenden zugeordnete Studienfortschrittsübersicht bereitstellen.

Für eine objektive Prüfung müssen zuvor die Bedeutung von „Studienfortschritt“, die darzustellenden Informationen und die zulässigen Datenquellen definiert werden.

Konkrete Akzeptanzkriterien zum E-Mail-Versand, zur Uhrzeit oder zur wöchentlichen Wiederholung wären derzeit fachlich nicht ausreichend begründet.

#### 6. Gesamtbewertung

**Entscheidung:** `INVESTIGATE` – Klärungsbedarf

Die Anforderung ist nicht allein durch sprachliche Überarbeitung qualitätsgesichert. Zunächst muss überprüft werden, ob die konkreten Vorgaben tatsächlich den Stakeholderbedürfnissen entsprechen.

* **Warum nicht REWRITE?** Die Defizite betreffen nicht nur Formulierungen, sondern auch ungeklärte fachliche Entscheidungen.
* **Warum nicht RECONSIDER?** Der grundsätzliche Zweck einer individuellen Studienfortschrittsübersicht ist plausibel. Es liegen keine Informationen vor, die eine Verwerfung oder grundlegende Neuausrichtung der Funktion rechtfertigen.

### Bewertung

| Bewertungskriterium | Human | KI |
| :--- | :---: | :---: |
| **Fachliche Angemessenheit** | 5 | 4 |
| **Eindeutigkeit und Verständlichkeit** | 4 | 5 |
| **Vollständigkeit und Überprüfbarkeit** | 4 | 5 |
| **Umgang mit Annahmen** | 5 | 4 |
| **Abstimmung und Konflikte** | 5 | 3 |
| **Gesamt** | **23/25** | **21/25** |

* **Fachliche Angemessenheit:** Human – Mängel und Strategie erkannt. KI – Konflikt zu REQ-007 fehlt, da nicht bekannt.
* **Eindeutigkeit und Verständlichkeit:** Human – knappe Stichpunkte und vage Erläuterung „in der Logik“. KI – klare Gliederung, Begründungen, präzise Wortwahl.
* **Vollständigkeit und Überprüfbarkeit:** Human – Konflikt erörtert, knapp. KI – vorläufige Lösung inkl. Akzeptanzkriterium etc.
* **Umgang mit Annahmen:** Human – nichts erfunden, nur Fragen. KI – Annahmen gekennzeichnet.
* **Abstimmung und Konflikte:** Human – Konflikt mit REQ-007 erkannt und Fragen zugeordnet. KI – Konflikt aufgrund fehlenden Kontexts nicht erkannt.

---

## REQ-006 – The Missing Definition

> „Wenn ein kritischer Lernrückstand vorliegt, muss das System geeignete Maßnahmen einleiten.“

**Human-Version:** siehe [repaired-requirements.md](repaired-requirements.md#req-006--the-missing-definition) · Strategie `INVESTIGATE`

### KI-Version

**Modell:** Claude Opus 5.5

**Prompt:** Basis-Prompt, unverändert.

**Status:** `INVESTIGATE`

**Begründung:** Die Anforderung beschreibt ein nachvollziehbares Anliegen: Studierende mit Lernrückstand sollen Unterstützung erhalten. Sowohl der Auslöser („kritischer Lernrückstand“) als auch die Reaktion („geeignete Maßnahmen“) sind jedoch unbestimmt. Ohne diese Festlegungen lässt sich die Anforderung weder umsetzen noch prüfen. Die fehlenden Informationen sind fachlicher Natur und lassen sich nicht durch eine bessere Formulierung ersetzen. REWRITE ist deshalb nicht möglich. Für RECONSIDER gibt es keinen ausreichenden Anlass, weil der Zweck plausibel ist. Die Zulässigkeit der dafür nötigen Datenauswertung muss allerdings geprüft werden.

#### 1. Qualitätsmängel

**Inhalt**

| Mangel | Begründung |
| :--- | :--- |
| „Kritischer Lernrückstand“ nicht definiert | Es fehlen Bezugsgröße (Studienplan, individueller Lernplan oder Kohorte), Messgröße, Schwellenwert und Betrachtungszeitraum. Die Anforderung ist damit mehrdeutig. |
| Feststellung offen | „Wenn … vorliegt“ sagt nicht, wer den Rückstand feststellt (das System oder eine Person) und wann bzw. wie oft geprüft wird. |
| „Geeignete Maßnahmen“ unbestimmt | Es ist offen, welche Maßnahmen gemeint sind, wen sie betreffen und wer über ihre Eignung entscheidet. „Geeignet“ ist nicht prüfbar. |
| „Einleiten“ mehrdeutig | Unklar ist, ob das System eine Maßnahme selbst durchführt, auslöst oder nur vorschlägt. |
| Nicht atomar | Die Anforderung enthält zwei Anforderungen: das Erkennen eines Lernrückstands und die Reaktion darauf. Beide sollten getrennt beschrieben und geprüft werden. |
| Zweck nicht dokumentiert | Welches Ziel oder Stakeholderbedürfnis die Anforderung erfüllen soll, ist nicht angegeben. |

**Dokumentation**

* Die zentralen Begriffe sind weder definiert noch auf eine Definition (z. B. ein Glossar) verwiesen.
* Aus der Formulierung lässt sich kein Abnahmekriterium ableiten. Die Anforderung ist nicht überprüfbar.
* Quelle, Begründung und Priorität fehlen.

**Abgestimmtheit**

* Eine Abstimmung mit Stakeholdern ist nicht dokumentiert. Offen ist auch, wer festlegen darf, was als „kritisch“ gilt.
* Die Anforderung setzt eine personenbezogene Auswertung von Lerndaten voraus. Ob und unter welchen Bedingungen das zulässig ist, ist nicht geklärt.
* Ob Studierende eine solche Funktion als Unterstützung oder als Überwachung wahrnehmen, ist nicht bekannt. Das ist eine zu prüfende Frage, kein festgestelltes Bedürfnis.

#### 2. Verbesserte Anforderung

Eine inhaltliche Neuformulierung ist ohne erfundene Werte nicht möglich. Möglich ist nur eine Aufteilung mit Platzhaltern. Die Platzhalter sind mit `[…]` gekennzeichnet und müssen erhoben werden.

* **REQ-006a – Erkennung:** Das System muss erkennen, ob bei Studierenden ein kritischer Lernrückstand gemäß `[Definition: Messgröße, Bezugsgröße, Schwellenwert, Zeitraum]` vorliegt.
* **REQ-006b – Reaktion:** Wenn ein kritischer Lernrückstand gemäß REQ-006a erkannt wurde, muss das System `[Maßnahme]` für `[Empfänger]` `[auslösen | vorschlagen]`.

Diese Struktur ist kein abgestimmter Inhalt, sondern eine Vorlage für die Klärung.

#### 3. Fehlende Informationen, Annahmen und notwendige Abstimmungen

**Unbegründete Annahmen in der Anforderung:**

* dass sich ein Lernrückstand aus verfügbaren Daten verlässlich messen lässt,
* dass eine systemseitige Reaktion gewünscht und zulässig ist,
* dass Studierende die Auswertung ihrer Lerndaten akzeptieren.

| Offene Frage | Stakeholder (Vorschlag) |
| :--- | :--- |
| Welches Ziel verfolgt die Anforderung, und wer hat sie eingebracht? | Auftraggeber\*in |
| Woran wird ein Lernrückstand gemessen, und ab wann ist er kritisch? | Lehrende, Studiengangsleitung |
| Wer stellt den Rückstand fest, und wie oft wird geprüft? | Lehrende, Studiengangsleitung |
| Welche Maßnahmen sind gewünscht, wer erhält sie, und soll das System sie auslösen oder nur vorschlagen? | Studierende, Lehrende, Studiengangsleitung |
| Welche Daten stehen dafür zur Verfügung, und in welcher Qualität? | IT bzw. Betrieb der Lernplattform |
| Ist die Auswertung der Lerndaten zulässig, und ist eine Einwilligung nötig? | Datenschutzbeauftragte\*r |
| Wie stehen Studierende zu einer solchen Auswertung? | Studierende bzw. Studierendenvertretung |

Die Zuordnung der Stakeholder ist ein Vorschlag und keine bestätigte Zuständigkeit.

#### 4. Akzeptanzkriterien

Fachlich begründete Akzeptanzkriterien lassen sich derzeit nicht formulieren. Sie hängen von Messgröße, Schwellenwert, Maßnahme und Empfänger ab, und diese sind nicht festgelegt. Sobald sie vorliegen, sollten die Kriterien mindestens einen Fall genau am Schwellenwert sowie knapp darüber und darunter abdecken und die erwartete Reaktion des Systems beschreiben.

### Bewertung

| Bewertungskriterium | Human | KI |
| :--- | :---: | :---: |
| **Fachliche Angemessenheit** | 4 | 5 |
| **Eindeutigkeit und Verständlichkeit** | 4 | 4 |
| **Vollständigkeit und Überprüfbarkeit** | 3 | 5 |
| **Umgang mit Annahmen** | 4 | 4 |
| **Abstimmung und Konflikte** | 3 | 4 |
| **Gesamt** | **18/25** | **22/25** |

Die KI-Version liegt vorne, vor allem weil sie alle drei Qualitätsaspekte abdeckt und die Anforderung in Erkennung und Reaktion aufteilt. Beide Versionen wählen `INVESTIGATE` und erfinden keine Schwellenwerte oder Maßnahmen.

* **Fachliche Angemessenheit:** Beide erkennen die Kernmängel, die unbestimmten Begriffe „kritisch“ und „geeignete Maßnahmen“. Die KI benennt zusätzlich, dass die Anforderung nicht atomar ist und dass „einleiten“ mehrdeutig ist. Die Human-Version spricht das zweite nur indirekt in Frage 2 an („selbst auslösen oder nur vorschlagen“).
* **Eindeutigkeit und Verständlichkeit:** Die Human-Version ist knapp, einzelne Formulierungen sind aber unscharf („weder bearbeitet noch zur Fertigstellung überprüft“, „reine Mutmaßungen“). Die KI-Version ist klar gegliedert, aber deutlich länger und wiederholt Punkte zwischen Mängeln und offenen Fragen.
* **Vollständigkeit und Überprüfbarkeit:** Die Human-Version bezieht sich nur auf den Inhalt. Die KI geht auch auf Dokumentation und Abgestimmtheit ein, schlägt eine Struktur mit Platzhaltern vor und begründet, warum keine Akzeptanzkriterien möglich sind.
* **Umgang mit Annahmen:** Beide erfinden nichts. Die KI nennt die unbegründeten Annahmen ausdrücklich und kennzeichnet Platzhalter und Stakeholder-Zuordnung als Vorschlag. Die Human-Version formuliert alles als offene Frage, benennt Annahmen aber nicht ausdrücklich.
* **Abstimmung und Konflikte:** Die Human-Version nennt Stakeholder, ordnet sie aber keiner Frage zu, und Datenschutz fehlt. Die KI ordnet jeder Frage Stakeholder zu und spricht Datenschutz und den möglichen Zielkonflikt zwischen Unterstützung und Überwachung an. Keine Version erkennt die Überschneidungen mit anderen Anforderungen, etwa REQ-003 und REQ-015. Die KI kannte diese nicht.


---

## REQ-014 – The Accessibility Shortcut

> „Der Study Buddy muss auf allen Geräten vollständig barrierefrei funktionieren.“

**Human-Version:** siehe [repaired-requirements.md](repaired-requirements.md#req-014--the-accessibility-shortcut) · Strategie `INVESTIGATE`

### KI-Version

**Modell:** Claude Opus 5.5

**Prompt:** Gemeinsamer Prompt für REQ-001 und REQ-014, siehe [REQ-001](#req-001--the-seven-day-rule).

#### Qualitätsmängel

* **Inhalt – Notwendigkeit:** Barrierefreiheit ist berechtigt und vermutlich verbindlich, die rechtliche Grundlage ist aber nicht benannt.
* **Inhalt – Vollständigkeit:** Nutzergruppen, Einschränkungen, Funktionen und Hilfstechnologien fehlen.
* **Inhalt – Überprüfbarkeit:** Ohne Standard oder Kriterien ist nicht feststellbar, wann die Anforderung erfüllt ist.
* **Dokumentation – Eindeutigkeit:** „Alle Geräte“ und „vollständig“ sind Requirements Smells; Geräte, Betriebssysteme und Browser sind nicht abgegrenzt.
* **Dokumentation – Struktur:** Viele Einzelanforderungen in einem Satz; später aufteilen.
* **Abgestimmtheit:** Nicht erkennbar, ob Betroffene und zuständige Stellen einbezogen wurden.

#### Analyseergebnisse

* **Verbesserte Anforderung:** Nicht seriös möglich. Ein Referenzstandard (z. B. WCAG) und eine Konformitätsstufe dürfen nicht ohne Klärung festgelegt werden.
* **Fehlende Informationen:** Geltende rechtliche Vorgaben bzw. Standard; Geräte-, Betriebssystem- und Browserumfang; Nutzergruppen; Prüfverfahren.
* **Unbegründete Annahmen:** Dass „vollständige“ Barrierefreiheit auf „allen“ Geräten realistisch und klar definiert ist.
* **Abstimmung nötig mit:** Studierenden (insbesondere mit Beeinträchtigungen), IT-Verantwortlichen, Studiengangsleitung, für Barrierefreiheit bzw. Recht zuständigen Stellen.
* **Akzeptanzkriterien:** Keine, da sie vom noch nicht festgelegten Standard abhängen.
* **Status:** `INVESTIGATE`

### Bewertung

| Bewertungskriterium | Human | KI |
| :--- | :---: | :---: |
| **Fachliche Angemessenheit** | 4 | 4 |
| **Eindeutigkeit und Verständlichkeit** | 5 | 4 |
| **Vollständigkeit und Überprüfbarkeit** | 4 | 5 |
| **Umgang mit Annahmen** | 5 | 4 |
| **Abstimmung und Konflikte** | 4 | 4 |
| **Gesamt** | **22/25** | **21/25** |

Die Human-Version liegt knapp vorne: Die KI ist gründlicher bei der Überprüfbarkeit, führt aber eine kleine unbelegte Annahme ein.

* **Fachliche Angemessenheit:** Beide halten Barrierefreiheit für ein berechtigtes Anliegen und sehen das Problem in der Konkretisierung, nicht in der Notwendigkeit.
* **Eindeutigkeit und Verständlichkeit:** Die Human-Version fasst die Mängel in drei Sätzen zusammen. Die KI verteilt dieselben Punkte auf sechs Bullets und mehrere Absätze, was die Lesbarkeit leicht senkt.
* **Vollständigkeit und Überprüfbarkeit:** Die KI führt Überprüfbarkeit als eigenen Mangel („ohne Standard oder Kriterien nicht feststellbar“) und begründet, warum keine Akzeptanzkriterien möglich sind. Die Human-Version fragt nur, wie Barrierefreiheit überprüft wird.
* **Umgang mit Annahmen:** Die KI schreibt, Barrierefreiheit sei „vermutlich verbindlich“. Dafür gibt es im Material keine Grundlage. Positiv: Sie nennt WCAG nur als Beispiel und lehnt ausdrücklich ab, Standard oder Konformitätsstufe festzulegen. Die Human-Version formuliert die rechtliche Lage nur als offene Frage.
* **Abstimmung und Konflikte:** Beide nennen dieselben Stakeholder. Keine Version spricht mögliche Konflikte an, etwa zwischen dem Anspruch „alle Geräte“ und dem Aufwand für IT und Entwicklung.

---

## REQ-015 – The AI Knows Best

> „Ein KI-Modell muss anhand der Nutzungsdaten automatisch entscheiden, welche Studierenden zusätzliche Betreuung benötigen.“

**Human-Version:** siehe [repaired-requirements.md](repaired-requirements.md#req-015--the-ai-knows-best) · Strategie `RECONSIDER`

### KI-Version

**Modell:** Claude Opus 5.5

**Prompt:** Basis-Prompt, unverändert.

**Status:** `RECONSIDER`

Die Anforderung beschreibt eine automatisierte Entscheidung über einzelne Studierende auf Basis ihrer Daten. Ob das notwendig, angemessen und zulässig ist, ist offen. Deshalb sollte sie nicht übernommen werden, solange das nicht geklärt ist. Erst danach lohnt sich eine Überarbeitung (REWRITE). Mehrere Teilfragen sind außerdem INVESTIGATE-Punkte, siehe unten.

#### 1. Qualitätsmängel

**Inhalt**

| Mangel | Begründung |
| :--- | :--- |
| Lösung statt Bedarf | „Ein KI-Modell“ legt die Technik fest, bevor das fachliche Problem beschrieben ist. Unklar bleibt, welches Ziel verfolgt wird, etwa Studienabbrüche verringern oder Beratung früher anbieten. Ebenso unklar ist, ob KI dafür überhaupt nötig ist. |
| „Nutzungsdaten“ nicht definiert | Offen ist, welche Daten gemeint sind (Logins, Lernzeiten, Abgaben, Noten, Forenaktivität?), aus welchen Systemen sie kommen und über welchen Zeitraum sie erfasst werden. Ohne diese Angaben lässt sich die Anforderung weder umsetzen noch prüfen. |
| „Zusätzliche Betreuung“ nicht definiert | Unklar ist, welche Art von Betreuung gemeint ist (fachlich, organisatorisch, psychosozial), wer sie leistet und welches Angebot es heute schon gibt. |
| „Benötigen“ ohne Kriterium | Es fehlt eine fachliche Definition, wann jemand Betreuungsbedarf hat. Ein Modell kann nur etwas vorhersagen, das vorher definiert wurde. |
| „Automatisch entscheiden“ unklar und kritisch | Offen ist, was aus der Entscheidung folgt: ein Hinweis an Betreuende, eine Nachricht an die Studierenden, eine Pflichtmaßnahme? Und ob ein Mensch beteiligt ist. Davon hängen Zulässigkeit und Risiko stark ab. |
| Keine Qualitätsanforderungen | Es fehlen Angaben zu Genauigkeit, zum Umgang mit Fehlklassifikationen (falsch positiv: Stigmatisierung; falsch negativ: Bedarf wird übersehen), zu Nachvollziehbarkeit, Fairness und zur Häufigkeit der Auswertung. |
| Nicht prüfbar | Ohne Kriterien, Daten und Folgen lässt sich kein Abnahmetest formulieren. |

**Dokumentation**

* Es fehlen ID, Quelle bzw. Stakeholder, Begründung, Priorität und Version.
* Die Anforderung folgt keiner Satzschablone. Das System als Akteur fehlt, stattdessen ist „ein KI-Modell“ Subjekt.
* Mehrere Aspekte sind vermischt: Datenerhebung, Auswertung, Entscheidung und (implizit) Maßnahme. Sie sind nicht atomar.
* Es gibt keinen Bezug zu einem Ziel, einem Use Case oder Datenschutz- und Ethikanforderungen.

**Abgestimmtheit**

* Nichts deutet darauf hin, dass die Anforderung mit den Betroffenen oder den Verantwortlichen abgestimmt ist.
* Der Datenschutz ist offenbar nicht eingebunden. Ob es eine Rechtsgrundlage, eine Zweckbindung oder eine Datenschutz-Folgenabschätzung gibt, ist unbekannt.
* Es ist unklar, ob es den Bedarf überhaupt gibt und ob die Studienberatung bzw. das Betreuungspersonal die Ergebnisse verarbeiten kann.

#### 2. Warum RECONSIDER?

1. **Rechtliche Zulässigkeit ist offen.** Eine automatisierte Entscheidung, die Personen auf Basis ihrer Daten einstuft, kann unter Art. 22 DSGVO fallen, wenn sie die Betroffenen erheblich beeinträchtigt. Möglicherweise ist sie auch ein Hochrisiko-System im Bildungsbereich nach dem EU AI Act (Anhang III). Ob das hier zutrifft, kann ich nicht beurteilen. Das hängt von den Folgen der Entscheidung ab und muss rechtlich geprüft werden.
2. **Die Angemessenheit ist offen.** Profiling auf Basis von Verhaltensdaten greift in die Privatsphäre ein. Ob dieser Eingriff im Verhältnis zum Nutzen steht und ob es mildere Mittel gibt, ist nicht begründet. Ein milderes Mittel wäre etwa ein freiwilliges Self-Assessment oder ein Opt-in.
3. **Die Notwendigkeit ist offen.** Das zugrunde liegende Problem und Ziel sind nicht beschrieben. Deshalb lässt sich nicht beurteilen, ob KI das richtige Mittel ist.
4. **Ethische Risiken** wie Bias, Stigmatisierung und fehlende Transparenz für die Studierenden sind nicht berücksichtigt.

#### 3. Fehlende Informationen und notwendige Abstimmungen

| Offene Frage | Mit wem klären |
| :--- | :--- |
| Welches Problem soll gelöst werden, und welches Ziel wird verfolgt? Wer hat die Anforderung eingebracht? | Auftraggeber\*in / Hochschulleitung, Anforderungsquelle |
| Wie ist „Betreuungsbedarf“ fachlich definiert? Woran erkennt man ihn heute? | Studienberatung, Tutor\*innen, Lehrende |
| Welche Betreuungsangebote gibt es, und welche Kapazitäten haben sie? | Studienberatung / Studierendenservice |
| Welche Daten dürfen für welchen Zweck verwendet werden? Gibt es eine Rechtsgrundlage, und ist eine Datenschutz-Folgenabschätzung nötig? | Datenschutzbeauftragte\*r, Rechtsabteilung |
| Fällt das Vorhaben unter Art. 22 DSGVO bzw. den EU AI Act? | Rechtsabteilung / Compliance |
| Was folgt aus einer Einstufung, und wer entscheidet am Ende? | Studienberatung, Hochschulleitung |
| Wie sehen die Studierenden das: Akzeptanz, Opt-in oder Opt-out, Transparenz? | Studierendenvertretung, Studierende als Nutzer\*innen |
| Welche Daten sind technisch verfügbar und in welcher Qualität? | IT / Betreiber der Lernplattform |
| Welche Fehlerraten sind vertretbar? | Studienberatung, Datenschutz, Ethik-Gremium (falls vorhanden) |

**Unbegründete Annahmen in der Anforderung:**

* dass sich Betreuungsbedarf aus Nutzungsdaten ableiten lässt,
* dass eine automatisierte Entscheidung erwünscht und zulässig ist,
* dass die nötigen Daten verfügbar und nutzbar sind.

#### 4. Möglicher überarbeiteter Entwurf (nur als Diskussionsgrundlage)

Für einen endgültigen REWRITE reichen die vorliegenden Informationen nicht. Der folgende Entwurf ist deshalb ausdrücklich ein Vorschlag zur Abstimmung und kein festgestellter Stakeholderbedarf. Er zeigt eine weniger eingriffsintensive Variante, die auf eine automatisierte Entscheidung verzichtet. Platzhalter stehen in eckigen Klammern.

> **REQ-[ID] **
> Das System soll [Rolle, z. B. Studienberater\*innen] die Möglichkeit bieten, Hinweise auf möglichen Unterstützungsbedarf von Studierenden einzusehen. Die Hinweise beruhen auf [abgestimmten Datenkategorien] und [fachlich definierten Kriterien].
> **Begründung:** [Ziel, noch zu klären]
> **Quelle:** [Stakeholder, noch zu klären]
> **Voraussetzungen:** Rechtsgrundlage und Datenschutzprüfung liegen vor [offen].

Mögliche Folgeanforderungen, die nach der Klärung einzeln zu formulieren wären:

* Die Entscheidung über eine Kontaktaufnahme trifft ein Mensch (falls rechtlich oder fachlich gefordert).
* Für jeden Hinweis wird nachvollziehbar angezeigt, welche Kriterien ihn ausgelöst haben.
* Studierende werden über die Datenverarbeitung informiert [Opt-in oder Opt-out ist zu klären].
* Es werden ausschließlich die freigegebenen Datenkategorien verarbeitet.

#### 5. Akzeptanzkriterien

Fachlich begründete Akzeptanzkriterien lassen sich derzeit nicht formulieren. Dafür fehlen Definitionen, Daten, Folgen und Qualitätsziele. Konkrete Werte wie Genauigkeit oder Reaktionszeiten wären erfunden.

Sobald die oben genannten Punkte geklärt sind, sollten die Kriterien mindestens Folgendes abdecken:

* die vereinbarte Definition von „Unterstützungsbedarf“,
* die zulässigen Datenquellen,
* die menschliche Kontrolle über die Entscheidung,
* die Nachvollziehbarkeit jedes Hinweises,
* vereinbarte Grenzen für Fehlklassifikationen,
* eine Fairnessprüfung über Studierendengruppen hinweg.

### Bewertung

| Bewertungskriterium | Human | KI |
| :--- | :---: | :---: |
| **Fachliche Angemessenheit** | 3 | 5 |
| **Eindeutigkeit und Verständlichkeit** | 4 | 4 |
| **Vollständigkeit und Überprüfbarkeit** | 3 | 5 |
| **Umgang mit Annahmen** | 3 | 4 |
| **Abstimmung und Konflikte** | 4 | 4 |
| **Gesamt** | **17/25** | **22/25** |

* **Fachliche Angemessenheit:** Der KI-Text ist um einiges detaillierter und berücksichtigt Aspekte, an die bei der Human-Version nicht gedacht wurde. Ein Beispiel dafür ist der von der KI genannte Punkt „Lösung statt Bedarf“. Auch die Feststellung der KI, dass „automatisch entscheiden“ unklar und kritisch ist, kommt in meiner Variante nicht deutlich hervor.
* **Eindeutigkeit und Verständlichkeit:** Der KI-Text ist dank des Prompts zwar gut strukturiert, aber trotzdem sehr ausführlich. Für ein Prüfergebnis wäre er vermutlich zu lang, wodurch die Kernaussage untergehen kann. Was die KI-Version an Text zu viel hat, fehlt in meinem Text: Er ist zwar knapp und gut verständlich, könnte aber etwas ausführlicher sein.
* **Vollständigkeit und Überprüfbarkeit:** Meine Version bezieht sich hauptsächlich auf den Inhalt. Die KI geht dagegen in zwei kurzen Abschnitten auch auf „Dokumentation“ und „Abgestimmtheit“ ein und berücksichtigt somit alle Punkte der Aufgabenstellung.
* **Umgang mit Annahmen:** Mit meiner Frage „Anhand welcher Kriterien soll das KI-Modell entscheiden, ob bei Studierenden zusätzlicher Betreuungsbedarf besteht? Ist dieses Vorgehen datenschutzrechtlich zulässig?“ setze ich bereits voraus, dass ein KI-Modell diese Entscheidung treffen wird. Durch die vorherigen Fragen wird das zwar etwas abgeschwächt, es könnte aber trotzdem zu Missverständnissen führen. Allerdings macht auch die KI denselben Fehler, indem sie einen Rewrite-Entwurf ausgibt. Auch wenn dieser klar als „Vorschlag zur Abstimmung und kein festgestellter Stakeholderbedarf“ gekennzeichnet ist, geht sie damit davon aus, dass es die Anforderung geben wird.
* **Abstimmung und Konflikte:** Der KI-Text ordnet die offenen Fragen direkt einer Stakeholdergruppe zu, was in meiner Version fehlt. Dafür weist meine Version auf mögliche Überschneidungen mit REQ-004 und REQ-006 hin. Da im Prompt die anderen Anforderungen nicht aufgeführt waren, berücksichtigt die KI keine Überschneidungen mit anderen Anforderungen.

---

## Reflexion

### 1. Bei welchen Qualitätskriterien war die KI besonders hilfreich, wo weniger zuverlässig?

Besonders hilfreich war die KI bei *Eindeutigkeit und Verständlichkeit* und bei *Vollständigkeit und Überprüfbarkeit*. Ihre Analysen waren klar gegliedert, die Mängel jeweils begründet. Sie hat außerdem formale Lücken aufgedeckt, die wir übersehen hatten, bei REQ-005 zum Beispiel die fehlende Zeitzone. Häufig hat sie lösungsneutrale Kernformulierungen und vorläufige Akzeptanzkriterien ergänzt und ihre Strategiewahl begründet.

Weniger zuverlässig war sie bei *Abstimmung und Konflikte*. Die KI hat jede Anforderung für sich betrachtet und kannte weder das Gesamtdokument noch den Projektkontext. Widersprüche zwischen Anforderungen, wie der zwischen REQ-005 und REQ-007, konnte sie deshalb nicht erkennen.

### 2. Hat die KI Informationen ergänzt, die nicht aus der Aufgabenstellung hervorgingen?

Ja. Sie hat zum Beispiel Rollen eingeführt, die es in unserem Projekt nicht gibt, etwa „Produktverantwortliche“ oder „Hochschulverwaltung“. Solche Ergänzungen wirken auf den ersten Blick plausibel und fallen deshalb leicht durch. Positiv ist, dass die KI ihre Annahmen oft selbst als Vorschlag gekennzeichnet hat. Trotzdem mussten wir jede Ergänzung gegen die Aufgabenstellung und die Stakeholder-Mails prüfen, bevor wir sie in die finale Version übernommen haben.

### 3. Hat die KI nur sprachlich verbessert oder auch die fachliche Notwendigkeit hinterfragt?

Sie ging über rein sprachliche Verbesserungen hinaus. Sie hat fehlenden Bedarf, vorzeitige Lösungsentscheidungen und ungeklärten Datenschutz benannt. Die grundsätzliche Notwendigkeit einer Funktion hat sie aber eher bestätigt als kritisch geprüft. Ob eine Anforderung zu den Werten und Interessen der Stakeholder\*innen passt oder mit anderen Anforderungen kollidiert, hat sie nur so weit hinterfragt, wie der Prompt ihr Informationen gegeben hat.

### 4. Gab es Fälle, in denen die Human Version überzeugender war?

Ja, immer dann, wenn der Projektkontext entscheidend war. Unser Team kannte das Gesamtdokument, die Stakeholder-Mails und die vorangegangenen Analysen. Dadurch konnten wir Konflikte zwischen Anforderungen erkennen, zum Beispiel zwischen REQ-005 und REQ-007. Offene Fragen haben wir gezielt den tatsächlichen Stakeholder\*innen zugeordnet und Hinweise wie die des IT & Online-Campus-Teams zur Datenqualität einbezogen. Außerdem haben wir keine Annahmen erfunden. Bei Struktur und Vollständigkeit war dagegen meist die KI stärker.

### 5. Welche Rolle sollte generative KI künftig bei der Qualitätssicherung von Requirements spielen?

KI eignet sich als unterstützender zweiter Prüfer. Sie bringt schnell Struktur in eine Analyse, deckt formale Lücken auf und liefert Formulierungsvorschläge. Den Requirements Engineer ersetzt sie nicht. Konflikte, Projektkontext und Stakeholder-Interessen erkennt sie nur, wenn sie diesen Kontext auch bekommt. Ihre Ergänzungen muss ein Mensch auf nicht belegte Annahmen prüfen. Am besten funktioniert eine Kombination: Die KI liefert Struktur und Vollständigkeit, der Mensch prüft den Kontext, stimmt mit den Stakeholdern ab und trifft die Entscheidungen.
