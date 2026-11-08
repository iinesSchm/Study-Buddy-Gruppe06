# Final Requirements

**RE – Mission 3 · Runde 4**

Abschließende Anforderungsfassungen beziehungsweise begründete offene Entscheidungen mit dokumentierten Annahmen. Sie bauen auf der Human-Version in [repaired-requirements.md](repaired-requirements.md) und dem Vergleich in [human-vs-ai.md](human-vs-ai.md) auf.

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

**Strategie:** `INVESTIGATE`

**Status:** Entwurf, offen bis zur Klärung der Fragen 1–6.

### Begründung der Entscheidung

Die Anforderung ist präzise, beruht aber auf einer unbelegten Annahme und legt mit der automatischen Benachrichtigung bereits eine Lösung fest, bevor das Problem geklärt ist. Eine Neuformulierung würde Definition von „Aktivität“, Zeitraum und Kanal erfinden.

### Vorläufige Formulierung

Lösungsneutrale Klärungsfrage (statt der Anforderung):

> *„Wie können Studierende, die Unterstützung benötigen, rechtzeitig erkannt oder erreicht werden, und wer entscheidet darüber?“*

### Nicht validierte Annahmen

* Inaktivität im Online Campus bedeutet Unterstützungsbedarf.
* Sieben Tage sind ein geeigneter Schwellenwert.
* Eine automatische Benachrichtigung ist die passende Reaktion.
* Der Online Campus liefert die nötigen Aktivitätsdaten.

### Offene Fragen

1. Welches Problem soll gelöst werden, und gibt es einen belegten Zusammenhang zwischen Inaktivität und Unterstützungsbedarf?
2. Was zählt als „Aktivität“ (Login, Seitenaufruf, Download, Abgabe), und welche Daten stellt der Online Campus bereit?
3. Worauf beruht der Zeitraum von sieben Tagen?
4. Über welchen Kanal, mit welchem Inhalt und wie oft würde benachrichtigt?
5. Wollen Studierende solche Benachrichtigungen, und sollen sie sie aktivieren bzw. deaktivieren können?
6. Ist die Auswertung der Aktivitätsdaten für diesen Zweck datenschutzrechtlich zulässig?

### Abstimmung und Konflikte

* **Stakeholder:** Zu klären mit Studierenden, Studiengangsleitung, Lehrenden, IT-Verantwortlichen (Online Campus) und Datenschutzverantwortlichen.
* **Möglicher Konflikt:** Die Studiengangsleitung möchte früh reagieren, Studierende möchten selbst über ihre Daten entscheiden. Dieser Konflikt muss sichtbar gemacht und geklärt werden, bevor eine Lösung festgelegt wird.

### Akzeptanzkriterien

* **Keine**, solange der Bedarf nicht geklärt ist.

### Ergebnis

REQ-001 wird in der vorliegenden Form vorerst nicht übernommen. Es bleibt als Entwurf mit Status `INVESTIGATE`, bis der dahinterliegende Bedarf geklärt ist.

---

## REQ-005 – Monday Morning

**Original:**

> „Alle Studierenden müssen jeden Montag um 08:00 Uhr eine personalisierte Fortschrittsübersicht per E-Mail erhalten.“

**Strategie:** `INVESTIGATE`. Die Anforderung wird vorerst nicht als verbindliche Anforderung übernommen.

### Begründung der Entscheidung

* **Warum nicht REWRITE?** Die Mängel betreffen nicht nur die Formulierung. Fachliche Entscheidungen sind ungeklärt, und der Widerspruch zu REQ-007 ist nicht aufgelöst.
* **Warum nicht RECONSIDER?** Der Zweck, Studierenden einen Überblick über ihren Studienfortschritt zu geben, ist plausibel und passt zum Projektauftrag.

### Qualitätsmängel

* **Inkonsistenz:** „Alle Studierenden müssen … erhalten“ widerspricht REQ-007, nach dem sämtliche Benachrichtigungen jederzeit abschaltbar sind.
* **Vorzeitige Entwurfsentscheidungen:** Kanal (E-Mail), Rhythmus (wöchentlich) und Zeitpunkt (Montag, 08:00 Uhr) sind festgelegt, ohne dass ein Bedarf belegt ist.
* **Pauschaler Empfängerkreis:** „Alle Studierenden“ berücksichtigt weder unterschiedliche Studienstatus noch individuelle Präferenzen.
* **Unklare Begriffe:** „Personalisiert“ und „Fortschrittsübersicht“ sind nicht definiert. Laut IT & Online-Campus-Team lässt sich Lernfortschritt bei unterschiedlich gestalteten Lehrveranstaltungen nur schwer deuten.
* **Unvollständige Zeitangabe:** Eine Zeitzone fehlt, und es ist unklar, ob 08:00 Uhr der Versand- oder der Empfangszeitpunkt ist. *(Erkenntnis aus dem KI-Vergleich)*
* **Nicht überprüfbar:** Ohne definierten Inhalt lässt sich die Umsetzung nicht objektiv testen.
* **Nicht abgestimmt:** Es ist keine Abstimmung mit den Stakeholder\*innen dokumentiert, weder zu Bedarf und Kanal noch zum Datenschutz.

### Vorläufige Formulierung

Vorläufiger, lösungsneutraler Kern (nicht validiert):

> „Der Study Buddy soll Studierenden eine individuelle Übersicht über ihren Studienfortschritt bereitstellen.“

### Nicht validierte Annahmen

* Ein Bedarf an einer Fortschrittsübersicht ist plausibel, aber nicht bestätigt.
* Die Zuordnung der Stakeholder\*innen zu den Fragen ist ein Vorschlag und keine bestätigte Zuständigkeit.

### Offene Fragen

| Nr. | Offene Frage | Stakeholder\*innen |
| :---: | :--- | :--- |
| 1 | Wünschen sich Studierende eine regelmäßige Übersicht? Welcher Rhythmus, Kanal und Zeitpunkt passen? | Studierende bzw. Studierendenvertretung |
| 2 | Wie wird der Konflikt mit REQ-007 aufgelöst: Ist die Übersicht abbestellbar, und ist sie zu Beginn aktiviert (Opt-in oder Opt-out)? | Studierende, Datenschutzbeauftragte, Projektauftraggeber |
| 3 | Was bedeutet „personalisiert“, und welche Daten dürfen genutzt werden? | Datenschutzbeauftragte, IT & Online-Campus-Team |
| 4 | Welche Inhalte gehören in die Übersicht, und was lässt sich aus den vorhandenen Daten verlässlich ableiten? | Lehrende, Studiengangsleitung, IT & Online-Campus-Team |
| 5 | Wer erhält die Übersicht, z. B. auch Studierende, die die Plattform nicht aktiv nutzen oder pausieren? | Studierende, Studienadministration |

### Abstimmung und Konflikte

Siehe Qualitätsmängel (Inkonsistenz mit REQ-007, nicht abgestimmt) und Offene Fragen (Frage 2).

### Akzeptanzkriterien

* **AK-01** *(nicht validiert)*: Für Studierende kann der Study Buddy eine ihnen zugeordnete Übersicht über ihren Studienfortschritt bereitstellen.

Konkrete Kriterien zu Kanal, Uhrzeit und Rhythmus sind derzeit nicht begründbar.

### Ergebnis

Eine endgültige Neuformulierung ist noch nicht möglich. Kanal, Zeitpunkt, Rhythmus, Inhalt, Empfängerkreis und Verbindlichkeit lassen sich nicht festlegen, ohne Annahmen zu erfinden. Erst müssen der Konflikt mit REQ-007 aufgelöst und die offenen Fragen geklärt sein.

---

## REQ-006 – The Missing Definition

**Original:**

> „Wenn ein kritischer Lernrückstand vorliegt, muss das System geeignete Maßnahmen einleiten.“

**Strategie:** `INVESTIGATE` – das Requirement wird vorerst nicht übernommen.

### Begründung der Entscheidung

Die Worte „kritisch“ und „geeignete Maßnahmen“ sind nicht ausformuliert, daher kann das Requirement weder umgesetzt noch auf seine Erfüllung überprüft werden. Eine Neuformulierung ist ohne erfundene Annahmen nicht möglich. Aus dem KI-Vergleich übernehme ich, dass das Requirement eigentlich zwei Teile hat: das Erkennen eines kritischen Lernrückstands und die Reaktion darauf. Diese sollten nach der Klärung getrennt beschrieben werden.

### Vorläufige Formulierung

Struktur für die spätere Formulierung (nur Platzhalter, keine gültige Anforderung):

* **REQ-006a – Erkennung:** Ein kritischer Lernrückstand liegt vor, wenn `<Definition gemäß Frage 1>` erfüllt ist. Festgestellt wird dieser durch `<System oder Person gemäß Frage 2>`.
* **REQ-006b – Reaktion:** Wenn ein kritischer Lernrückstand gemäß REQ-006a festgestellt wurde, muss das System `<Maßnahme gemäß Frage 4>` für `<Empfänger gemäß Frage 4>` `<auslösen oder vorschlagen gemäß Frage 6>`.

### Nicht validierte Annahmen

* Es ist nicht gesichert, dass diese Funktion tatsächlich benötigt wird (laut Angabe sind alle Requirements ungeprüfte Entwürfe).
* Es ist nicht bekannt, ob dem System die nötigen Lerndaten zur Verfügung stehen.
* Ob Studierende eine solche Funktion als Unterstützung oder als Überwachung empfinden, ist nicht erhoben.

### Offene Fragen

| Nr. | Offene Frage | Stakeholder |
| :---: | :--- | :--- |
| 1 | Woran wird ein Lernrückstand gemessen, und ab wann gilt er als kritisch? | Lehrende, Studiengangsleitung |
| 2 | Wer stellt fest, dass ein kritischer Lernrückstand vorliegt – das System oder eine Person? | Lehrende, Studiengangsleitung |
| 3 | Welche Daten stehen dafür zur Verfügung, und aus welchen Systemen? | IT-Verantwortliche |
| 4 | Welche Maßnahmen sind gewünscht, und wer soll sie erhalten? | Studierende, Lehrende, Studiengangsleitung |
| 5 | Wer legt fest, welche Maßnahmen geeignet sind? | Lehrende, Studiengangsleitung |
| 6 | Soll das System Maßnahmen selbst auslösen oder nur vorschlagen? | Studierende, Lehrende, Studiengangsleitung |
| 7 | Ist die Auswertung der Lerndaten datenschutzrechtlich zulässig? | Datenschutzverantwortliche |

### Abstimmung und Konflikte

*TODO*

### Akzeptanzkriterien

*TODO*

### Ergebnis

Das Requirement bleibt offen, bis die Fragen 1–7 geklärt sind.

---

## REQ-014 – The Accessibility Shortcut

**Original:**

> „Der Study Buddy muss auf allen Geräten vollständig barrierefrei funktionieren.“

**Strategie:** `INVESTIGATE`

**Status:** Entwurf, offen bis zur Klärung der Fragen 1–5.

### Begründung der Entscheidung

Barrierefreiheit ist ein wichtiges Anliegen, das die Anforderungssammlung erst vollständig macht. Ohne Barrierefreiheit wäre die Anforderungssammlung nicht vollständig.

Die Formulierungen „alle Geräte“ und „vollständig“ lassen sich jedoch nicht prüfen. Der Standard, der Geräteumfang und das Prüfverfahren dürfen nicht festgelegt werden, bevor man das geklärt hat. Die Barrierefreiheit muss also erst geklärt werden, bevor man den Standard, den Geräteumfang und das Prüfverfahren festlegt.

### Vorläufige Formulierung

Vorläufige Zielformulierung (nicht abgestimmt):

> *„Der Study Buddy soll für Studierende mit Beeinträchtigungen barrierefrei nutzbar sein. Standard, Geräteumfang und Prüfkriterien werden nach Klärung der offenen Fragen festgelegt.“*

Geplante Aufteilung nach der Klärung (Inhalte noch offen):

* **Teilanforderung 1:** Geltender Standard bzw. rechtliche Vorgaben
* **Teilanforderung 2:** Unterstützter Geräte-, Betriebssystem- und Browserumfang
* **Teilanforderung 3:** Zu unterstützende Hilfstechnologien
* **Teilanforderung 4:** Prüfverfahren

### Nicht validierte Annahmen

* „Vollständige“ Barrierefreiheit auf „allen“ Geräten ist realistisch und klar definierbar.
* Ob Barrierefreiheit für die Hochschule rechtlich verbindlich ist, ist nicht belegt (die Einschätzung der KI „vermutlich verbindlich“ wurde bewusst nicht übernommen).

### Offene Fragen

1. Welche rechtlichen Vorgaben oder Standards gelten für die Hochschule (z. B. WCAG), und auf welcher Stufe?
2. Welche Geräte, Betriebssysteme und Browser sollen unterstützt werden?
3. Welche Nutzergruppen mit welchen Einschränkungen müssen berücksichtigt werden?
4. Welche Hilfstechnologien müssen unterstützt werden?
5. Wie wird Barrierefreiheit überprüft (z. B. Tests mit Betroffenen, Reviews, Messungen)?

### Abstimmung und Konflikte

* **Stakeholder:** Zu klären mit Studierenden (insbesondere mit Beeinträchtigungen), IT-Verantwortlichen, Studiengangsleitung und den für Barrierefreiheit bzw. Recht zuständigen Stellen der Hochschule.
* **Möglicher Konflikt:** Ein breiter Geräteumfang erhöht den Aufwand für IT und Entwicklung. Der Umfang muss daher begründet und abgestimmt werden.

### Akzeptanzkriterien

* **Keine**, solange Standard und Geräteumfang nicht festgelegt sind.

### Ergebnis

REQ-014 wird als Ziel übernommen, aber noch nicht als prüfbare Anforderung. Nach der Klärung wird es in mehrere konkrete Teilanforderungen aufgeteilt.

---

## REQ-015 – The AI Knows Best

**Original:**

> „Ein KI-Modell muss anhand der Nutzungsdaten automatisch entscheiden, welche Studierenden zusätzliche Betreuung benötigen.“

**Strategie:** `RECONSIDER` – Anforderung vorerst nicht übernehmen.



### Qualitätsmängel

**Inhalt**

* **Lösung statt Bedarf:** „Ein KI-Modell“ legt die technische Lösung fest, bevor das fachliche Problem beschrieben ist. Ob KI überhaupt das geeignete Mittel ist, bleibt offen.
* **Unklare Begriffe:** „Nutzungsdaten“, „zusätzliche Betreuung“ und „benötigen“ sind nicht definiert. Ohne ein fachliches Kriterium für Betreuungsbedarf kann weder ein Mensch noch ein Modell entscheiden.
* **„Automatisch entscheiden“ ist unklar und kritisch:** Es ist offen, was aus der Entscheidung folgt (Hinweis, Kontaktaufnahme, Pflichtmaßnahme) und ob ein Mensch beteiligt ist. Davon hängen die rechtliche Zulässigkeit und das Risiko von Fehlentscheidungen ab, etwa Stigmatisierung oder übersehener Bedarf.
* **Zweck und Nutzen fehlen.**

**Dokumentation**

* Es fehlen Quelle (Stakeholder, Dokumente …), Begründung und Priorität.
* Die Anforderung vermischt mehrere Aspekte: Datenerhebung, Auswertung, Entscheidung und Maßnahme.

**Abgestimmtheit**

* Es ist nicht erkennbar, dass die Anforderung mit betroffenen Stakeholder\*innen abgestimmt wurde.
* Es gibt mögliche Überschneidungen mit **REQ-004** und **REQ-006**.

### Vorläufige Formulierung

Bewusst keine, siehe Ergebnis.

### Nicht validierte Annahmen

* dass sich Betreuungsbedarf aus Nutzungsdaten ableiten lässt,
* dass eine automatisierte Entscheidung gewünscht und zulässig ist,
* dass die benötigten Daten verfügbar und nutzbar sind,
* dass die Funktion nicht bereits durch REQ-004 und REQ-006 abgedeckt ist.

### Offene Fragen

| Nr. | Offene Frage | Stakeholder |
| :---: | :--- | :--- |
| 1 | Welchen Zweck und Nutzen verfolgt die Anforderung? Wer hat sie eingebracht? | Auftraggeber\*in / Studiengangsleitung |
| 2 | Ist die Anforderung notwendig, oder decken REQ-004 und REQ-006 die gewünschte Funktion bereits ab? | Auftraggeber\*in, Requirements Engineer |
| 3 | Was wird unter „zusätzlichem Betreuungsbedarf“ verstanden, und woran wird er heute erkannt? | Lehrendenvertretung, Studierendenvertretung |
| 4 | Welche Betreuungsangebote gibt es, und wer leistet sie? | Studienadministration, Studierendenvertretung |
| 5 | Welche Nutzungsdaten sollen verwendet werden, und sind sie technisch verfügbar? | IT & Online-Campus-Team |
| 6 | Gibt es für die Verarbeitung dieser Daten eine Rechtsgrundlage? | Datenschutz & Informationssicherheit |
| 7 | Ist eine automatisierte Entscheidung ohne menschliche Prüfung zulässig, oder muss eine Person entscheiden? | Datenschutz & Informationssicherheit |
| 8 | Wie stehen die Studierenden zur Auswertung ihrer Daten (Transparenz, Freiwilligkeit)? | Studierende / Studierendenvertretung |

### Abstimmung und Konflikte

Siehe Qualitätsmängel (Abgestimmtheit: Überschneidungen mit REQ-004 und REQ-006) und Offene Fragen (Fragen 2, 7, 8).

### 
### Ergebnis

Die Anforderung wird vorerst **nicht übernommen**. Es wird bewusst kein Rewrite-Entwurf formuliert, weil dieser bereits voraussetzen würde, dass die Anforderung in irgendeiner Form bestehen bleibt. Eine Neuformulierung ist erst sinnvoll, wenn diese Punkte geklärt sind:

1. Zweck und Notwendigkeit sind bestätigt, auch in Abgrenzung zu REQ-004 und REQ-006.
2. Betreuungsbedarf ist fachlich definiert.
3. Datenschutz und Rechtsabteilung haben die Datenverarbeitung und die Art der Entscheidung freigegeben.
