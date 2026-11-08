# Repaired Requirements – Human-Version

**RE – Mission 3 · Runde 1**

Menschlich erarbeitete Überarbeitungen beziehungsweise begründete Klärungsentscheidungen, ohne KI-Unterstützung. Die Grundlage bildet die Qualitätsanalyse in [quality-review.md](quality-review.md).

## Übersicht

| Requirement-ID | Titel | Strategie |
| :--- | :--- | :---: |
| [REQ-001](#req-001--the-seven-day-rule) | The Seven-Day Rule | `INVESTIGATE` |
| [REQ-005](#req-005--monday-morning) | Monday Morning | `INVESTIGATE` |
| [REQ-006](#req-006--the-missing-definition) | The Missing Definition | `INVESTIGATE` |
| [REQ-014](#req-014--the-accessibility-shortcut) | The Accessibility Shortcut | `INVESTIGATE` |
| [REQ-015](#req-015--the-ai-knows-best) | The AI Knows Best | `RECONSIDER` |

---

## REQ-001 – The Seven-Day Rule

**Original:**

> „Das System muss Studierende automatisch benachrichtigen, wenn sie sieben Tage lang nicht im Online Campus aktiv waren.“

### Qualitätsmangel

Die Anforderung ist klar formuliert – sie nennt den Auslöser, den Zeitraum und die Systemreaktion – aber sie beruht auf einer nicht geprüften Annahme. Die Annahme ist, dass Inaktivität im Online Campus automatisch bedeutet, dass ein Studierender Unterstützung braucht. Die Studierenden können aber am Wochenende, offline oder nur kurz vor den Abgabeterminen lernen. Der Zeitraum von sieben Tagen ist nicht erklärt, eine Quelle fehlt. Außerdem ist nicht definiert, was „aktiv“ genau bedeutet, und es ist offen, über welchen Kanal die Benachrichtigung kommt und ob man sie ausschalten kann.

**Strategie:** `INVESTIGATE`

### Offene Fragen

1. Welches Problem soll die Benachrichtigung lösen, und gibt es Belege dafür, dass Inaktivität wirklich mit Unterstützungsbedarf zusammenhängt?
2. Was versteht man unter „Aktivität“, und welche Daten stellt der Online Campus dafür bereit?
3. Warum wurde der Zeitraum von sieben Tagen gewählt?
4. Wollen die Studierenden solche Benachrichtigungen erhalten, und sollen sie die Möglichkeit haben, sie abzuschalten?
5. Darf man die Aktivitätsdaten für diesen Zweck datenschutzrechtlich auswerten?

### Stakeholder

* Studierende
* Studiengangsleitung
* Lehrende
* IT-Verantwortliche vom Online Campus
* Datenschutzverantwortliche

### Ergebnis

Eine endgültige Neuformulierung ist noch nicht möglich, weil wir neue Annahmen erfinden müssten – zum Beispiel eine genaue Definition von „Aktivität“, einen festen Zeitraum oder einen konkreten Kanal. Die Anforderung bleibt deshalb im Status *Entwurf*, bis wir die offenen Fragen mit den Stakeholdern geklärt haben.

---

## REQ-005 – Monday Morning

**Original:**

> „Alle Studierenden müssen jeden Montag um 08:00 Uhr eine personalisierte Fortschrittsübersicht per E-Mail erhalten.“

### Qualitätsmangel

* **Inkonsistenz:** Anforderung 5 – Die Studierenden **müssen** erhalten – widerspricht Anforderung 7 – Alles **abschaltbar sein** – in der Logik.
* **Unklare Entwurfsentscheidung:** Weder Kanal noch Rhythmus oder Zeitpunkt wurde mit Studierenden abgestimmt und könnte für die Zielgruppe unpassend sein.
* **Fehlende Abstimmung:** Keine Abstimmung mit den Stakeholdern bekannt.
* **Unklare Begriffe:** Der Begriff „Personalisiert“ ist nicht definiert, was eine Fortschrittsübersicht enthält ist unklar.

**Strategie:** `INVESTIGATE`

### Offene Fragen

1. Ist die Anforderung von Studierenden gewünscht, welcher Rhythmus, Kanal und Zeitpunkt sind praktisch?
2. Soll die Übersicht abbestellbar sein (REQ-005 zu REQ-007?) und soll die Option am Anfang angewählt sein?
3. Was bedeutet „personalisiert“ und was ist beinhaltet?
4. Welche Inhalte soll die Fortschrittsübersicht beinhalten?

### Stakeholder

* **Studierende inklusive deren Vertretung** → Fragen 1, 2
* **IT & OC-Team:** Daten, Schnittstellen und Umsetzbarkeit der Personalisierung → Frage 4
* **Lehrende:** Lernfortschritt je nach Kurs → Frage 4
* **Datenschutzbeauftragte:** Datennutzung, Option default an → Fragen 2, 3

### Ergebnis

Eine endgültige Neuformulierung ist noch nicht möglich. Kanal, Zeitpunkt, Rhythmus, Inhalt und Verbindlichkeit der Übersicht lassen sich nicht festlegen, ohne Annahmen zu erfinden. Erst müssen der Konflikt mit REQ-007 aufgelöst und die Fragen oben mit den Stakeholdern geklärt sein. Fest steht nur der Kern des Bedarfs, den Studierenden einen Überblick über ihren Studienfortschritt zu geben. Wie das umgesetzt wird, bleibt offen.

---

## REQ-006 – The Missing Definition

**Original:**

> „Wenn ein kritischer Lernrückstand vorliegt, muss das System geeignete Maßnahmen einleiten.“

### Qualitätsmangel

Das Requirement kann weder bearbeitet noch zur Fertigstellung überprüft werden. Der Begriff kritisch ist in dieser Formulierung nicht messbar, die Frage die sich stellt ist was kritisch konkret bedeutet. Ein weiterer Punkt ist der Teil um die „geeigneten Maßnahmen“ die ebenfalls nur reine Mutmaßungen sein können, da sie nicht näher spezifiziert wurden.

**Strategie:** `INVESTIGATE`

### Offene Fragen

1. Woran wird ein Lernrückstand gemessen, und ab wann gilt er als kritisch?
2. Welche Maßnahmen sind gewünscht, wer soll sie erhalten, und soll das System sie selbst auslösen oder nur vorschlagen?
3. Wer legt fest, welche Maßnahmen geeignet sind?

### Stakeholder

* Studierende
* Lehrende
* Studiengangsleitung
* IT-Verantwortliche

### Ergebnis

Noch keine endgültige Neuformulierung möglich, da die Anforderung nicht verbessert werden kann, ohne neue Annahmen zu erfinden. Der Anforderungsentwurf bleibt offen, bis die notwendigen Informationen vorliegen.

---

## REQ-014 – The Accessibility Shortcut

**Original:**

> „Der Study Buddy muss auf allen Geräten vollständig barrierefrei funktionieren.“

### Qualitätsmangel

Barrierefreiheit ist ein wichtiges Thema, aber die Formulierungen „alle Geräte“ und „vollständig“ wirken zu allgemein. Es ist nicht klar, welche Geräte genau gemeint sind, welcher Standard gelten soll und wie man die Anforderung prüfen kann. In einem Satz werden viele einzelne Anforderungen zusammengefasst.

**Strategie:** `INVESTIGATE`

### Offene Fragen

1. Welche rechtlichen Vorgaben oder Standards gelten für die Hochschule?
2. Welche Geräte, Betriebssysteme und Browser sollen unterstützt werden?
3. Welche Nutzergruppen und Hilfstechnologien müssen berücksichtigt werden?
4. Wie wird Barrierefreiheit überprüft?

### Stakeholder

* Studierende (insbesondere mit Beeinträchtigungen)
* IT-Verantwortliche
* Studiengangsleitung
* Für Barrierefreiheit bzw. Recht zuständige Stellen der Hochschule

### Ergebnis

Noch keine endgültige Neuformulierung möglich. Nach der Klärung sollte die Anforderung in mehrere konkrete, überprüfbare Anforderungen aufgeteilt werden.

---

## REQ-015 – The AI Knows Best

**Original:**

> „Ein KI-Modell muss anhand der Nutzungsdaten automatisch entscheiden, welche Studierenden zusätzliche Betreuung benötigen.“

### Qualitätsmangel

* „Nutzungsdaten“ und „zusätzliche Betreuung“ müssten genauer beschrieben werden.
* Das KI-Modell soll auf personenbezogene Nutzungsdaten zugreifen und daraus Entscheidungen über Studierende ableiten. Das könnte datenschutzrechtlich problematisch sein (DSGVO).
* Der konkrete Zweck bzw. Nutzen dieser Anforderung wird nicht ausreichend beschrieben.

**Strategie:** `RECONSIDER`

### Offene Fragen

1. Welchen Zweck bzw. Nutzen verfolgt diese Anforderung?
2. Ist diese Anforderung notwendig, obwohl es Überschneidungen mit REQ-004 und REQ-006 gibt?
3. Welche Nutzungsdaten sollen für die Entscheidung herangezogen werden? Ist deren Verarbeitung datenschutzrechtlich zulässig?
4. Anhand welcher Kriterien soll das KI-Modell entscheiden, ob bei Studierenden zusätzlicher Betreuungsbedarf besteht? Ist dieses Vorgehen datenschutzrechtlich zulässig?
5. Was genau wird unter „zusätzlichem Betreuungsbedarf“ verstanden?

### Stakeholder

* Studierende
* Datenschutz und Informationssicherheit
* Lehrende

### Ergebnis

Der Anforderungsentwurf bleibt vorerst offen, bis entschieden wurde, ob diese Anforderung überhaupt notwendig und sinnvoll ist oder ob sich die gewünschten Funktionen bereits mit REQ-004 und REQ-006 abdecken lassen. Außerdem muss geprüft werden, ob die Verarbeitung der dafür benötigten Nutzungsdaten datenschutzrechtlich zulässig ist und ob eine automatische Entscheidung durch ein KI-Modell geeignet ist.
