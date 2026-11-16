# Structured Requirements Catalogue (D4)

**RE – Mission 4 · Aufgabe 04 „Ordnung im Chaos“, Teil D**

Alle Aussagen aus den Missionen 01 bis 03, eingeordnet nach Art (Funktional, Qualität, Randbedingung), Ebene (Business, User, System) und Quelle. Systemanforderungen verweisen in der Spalte „Bezug“ auf eine User- oder Business-Anforderung. Die Priorität bleibt bis Mission 06 leer. Alle Einträge haben den Status „Entwurf“.

Zielwerte mit dem Vermerk „Zielwert Vorschlag Team“ sind Vorschläge der Gruppe und noch mit den Stakeholdern abzustimmen (F-003).

## Übersicht

| Ebene | Anzahl |
| :--- | ---: |
| Business | 5 |
| User | 10 |
| System | 19 |
| **Gesamt** | **34** |

## Business-Anforderungen

| ID | Titel | Text | Art | Quelle | Bezug | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| BUS-01 | Studierende früh unterstützen | Die FernFH will Studierende, die Unterstützung brauchen, früher erreichen, damit weniger Studierende ihr Studium abbrechen. | Funktional | Project Brief; Studiengangsleitung (Stakeholder Map) | – | Entwurf |
| BUS-02 | Integration in den Online Campus | Der Study Buddy wird in den bestehenden Online Campus integriert. Eine eigene, parallele Plattform wird nicht aufgebaut. | Randbedingung | Auftrag / Project Brief; IT & Online-Campus-Team (Stakeholder Map) | – | Entwurf |
| BUS-03 | Weniger organisatorische Anfragen | Die Studienadministration will weniger organisatorische Anfragen bearbeiten, weil Informationen übersichtlich bereitstehen und Anfragen bei der zuständigen Person landen. | Funktional | Studienadministration (Stakeholder Map) | – | Entwurf |
| BUS-04 | DSGVO-konforme Verarbeitung | Die Verarbeitung personenbezogener Daten im Study Buddy muss der DSGVO entsprechen (Rechtsgrundlage, Zweckbindung, Datenminimierung). | Randbedingung | DSGVO; Datenschutz & Informationssicherheit (Stakeholder Map); F-008 | – | Entwurf |
| BUS-05 | Unterstützung statt Kontrolle | Studierende sollen den Study Buddy als freiwillige Unterstützung erleben und nicht als Überwachung. Messgröße und Zielwert werden mit der Studierendenvertretung festgelegt. | Qualität | Studierendenvertretung (Stakeholder Map) | – | Entwurf |

## User-Anforderungen

| ID | Titel | Text | Art | Quelle | Bezug | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| USR-01 | Fristen an einem Ort | Als Studierende:r will ich alle anstehenden Abgaben und Fristen meiner Lehrveranstaltungen an einem Ort sehen. | Funktional | Persona Studierende (Mission 01); REQ-003 (Mission 03) | BUS-03 | Entwurf |
| USR-02 | An Termine erinnert werden | Als Studierende:r will ich rechtzeitig vor Abgabeterminen erinnert werden. | Funktional | Persona Studierende (Mission 01); A-002 nicht validiert | BUS-01 | Entwurf |
| USR-03 | Benachrichtigungen selbst steuern | Als Studierende:r will ich selbst festlegen, welche Benachrichtigungen ich erhalte. | Funktional | Studierendenvertretung (Stakeholder Map); REQ-007 (Mission 03); STF-11 | BUS-05 | Entwurf |
| USR-04 | Eigenen Fortschritt sehen | Als Studierende:r will ich sehen, wie weit ich in meinen Lehrveranstaltungen bin. | Funktional | REQ-005, vorläufiger Kern (Mission 03, final-requirements) | BUS-01 | Entwurf |
| USR-05 | Unterwegs nutzen | Als Studierende:r will ich den Study Buddy auf Smartphone und Notebook nutzen, auch unterwegs. | Funktional | Persona Studierende, Nutzungskonzept (Mission 01); STF-08 | BUS-01 | Entwurf |
| USR-06 | Zuständige Person finden | Als Studierende:r will ich zu einer Frage schnell die zuständige Ansprechperson finden. | Funktional | Studienadministration (Stakeholder Map) | BUS-03 | Entwurf |
| USR-07 | Datennutzung nachvollziehen | Als Studierende:r will ich nachvollziehen, welche meiner Daten der Study Buddy auswertet und wer sie sehen kann. | Funktional | Studierendenvertretung (Stakeholder Map); STF-03, STF-04 | BUS-04 | Entwurf |
| USR-08 | Probleme früh erkennen (Lehrende) | Als Lehrende:r will ich früh erfahren, wenn es in meiner Lehrveranstaltung inhaltliche oder organisatorische Probleme gibt, ohne zusätzliche Daten pflegen zu müssen. | Funktional | Persona Lehrende (Mission 01); Lehrendenvertretung (Stakeholder Map) | BUS-01 | Entwurf |
| USR-09 | Barrierefrei nutzen | Als Studierende:r mit Beeinträchtigung will ich den Study Buddy mit meinen Hilfstechnologien nutzen können. | Funktional | REQ-014 als Ziel (Mission 03); Persona Studierende, besondere Bedürfnisse | BUS-01 | Entwurf |
| USR-10 | Datenverarbeitung prüfen | Als Datenschutzbeauftragte:r will ich die Verarbeitung personenbezogener Daten im Study Buddy prüfen können. | Funktional | Datenschutz & Informationssicherheit (Stakeholder Map); F-015 | BUS-04 | Entwurf |

## System-Anforderungen

| ID | Titel | Text | Art | Quelle | Bezug | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| SYS-01 | Fristenübersicht | Das System muss Studierenden nach der Anmeldung alle Abgabe- und Prüfungstermine der Lehrveranstaltungen, in denen sie angemeldet sind, nach Datum sortiert anzeigen. | Funktional | Persona Studierende; Aufgabe 04 Teil C | USR-01 | Entwurf |
| SYS-02 | Ladezeit Fristenübersicht | Das System zeigt die Fristenübersicht in 95 % der Aufrufe innerhalb von 2 s vollständig an, gemessen am Endgerät bei mobiler Verbindung ab 10 Mbit/s und bis zu 500 gleichzeitig angemeldeten Nutzenden. | Qualität | Aufgabe 04 Teil C; Zielwert Vorschlag Team, abzustimmen (F-003) | USR-05 | Entwurf |
| SYS-03 | Termine übernehmen | Das System muss Abgabe- und Prüfungstermine aus dem Online Campus übernehmen, ohne dass Lehrende sie ein zweites Mal erfassen. | Funktional | REQ-010 (Mission 03); Lehrendenvertretung (Stakeholder Map) | USR-01 | Entwurf |
| SYS-04 | Aktualität der Termine | Änderungen an Abgabeterminen im Online Campus werden in 99 % der Fälle innerhalb von 15 Minuten im Study Buddy angezeigt. | Qualität | REQ-013 (Mission 03); Aufgabe 04 Teil C; Zielwert Vorschlag Team, abzustimmen (F-003) | USR-01 | Entwurf |
| SYS-05 | Terminänderung anzeigen | Wenn sich ein Abgabetermin ändert, muss das System den betroffenen Studierenden die Änderung mit altem und neuem Termin anzeigen. | Funktional | REQ-013 (Mission 03) | USR-01 | Entwurf |
| SYS-06 | Erinnerung vor Frist | Das System muss Studierenden, die Erinnerungen aktiviert haben, vor einem Abgabetermin eine Erinnerung anzeigen. Die Vorlaufzeit legen die Studierenden selbst fest. | Funktional | Persona Studierende; A-002 nicht validiert | USR-02 | Entwurf |
| SYS-07 | Pünktliche Erinnerung | Erinnerungen werden in 99 % der Fälle spätestens 5 Minuten nach dem eingestellten Zeitpunkt zugestellt. | Qualität | Zielwert Vorschlag Team, abzustimmen (F-003) | USR-02 | Entwurf |
| SYS-08 | Benachrichtigungen einzeln abschalten | Das System muss Studierenden ermöglichen, jede Benachrichtigungsart einzeln zu aktivieren und zu deaktivieren. | Funktional | REQ-007 (Mission 03); STF-11 | USR-03 | Entwurf |
| SYS-09 | Abgabestand je Lehrveranstaltung | Das System muss Studierenden je Lehrveranstaltung anzeigen, wie viele der vorgesehenen Abgaben sie bereits eingereicht haben. | Funktional | REQ-005, vorläufiger Kern (Mission 03) | USR-04 | Entwurf |
| SYS-10 | Web-App | Der Study Buddy muss als Web-App im Browser nutzbar sein. | Randbedingung | IT der FernFH (Plot Twist, Aufgabe 04) | USR-05 | Entwurf |
| SYS-11 | Verfügbarkeit | Das System ist je Kalendermonat in mindestens 99,5 % der Zeit erreichbar, angekündigte Wartungsfenster ausgenommen. | Qualität | Zielwert Vorschlag Team, abzustimmen (F-003); IT & Online-Campus-Team | USR-05 | Entwurf |
| SYS-12 | Mobile Darstellung | Alle Funktionen sind ab einer Bildschirmbreite von 360 px ohne horizontales Scrollen bedienbar. | Qualität | Persona Studierende, Nutzungskonzept; Zielwert Vorschlag Team, abzustimmen (F-003) | USR-05 | Entwurf |
| SYS-13 | Ansprechperson anzeigen | Das System muss zu jeder Lehrveranstaltung die zuständige Ansprechperson für organisatorische und für fachliche Fragen anzeigen. | Funktional | Studienadministration (Stakeholder Map); Aufgabe 04 Teil C | USR-06 | Entwurf |
| SYS-14 | Anmeldung über FH-Konto | Die Anmeldung erfolgt über das bestehende Authentifizierungssystem der FernFH. Ein separates Benutzerkonto wird nicht angelegt. | Randbedingung | IT & Online-Campus-Team; REQ-011 verworfen (Mission 03); A-009, F-011 | USR-05 | Entwurf |
| SYS-15 | Datennutzung anzeigen | Das System muss Studierenden anzeigen, welche ihrer Daten es zu welchem Zweck verarbeitet und welche Rollen darauf zugreifen. | Funktional | Studierendenvertretung; STF-03, STF-04 | USR-07 | Entwurf |
| SYS-16 | Datenminimierung | Das System darf nur die personenbezogenen Daten verarbeiten, die für die freigegebenen Funktionen erforderlich sind. | Randbedingung | Art. 5 Abs. 1 lit. c DSGVO; Datenschutz & Informationssicherheit; F-008 | USR-07 | Entwurf |
| SYS-17 | Auskunft nach DSGVO | Auskunftsersuchen von Studierenden zu ihren im Study Buddy verarbeiteten Daten müssen innerhalb eines Monats beantwortet werden können. | Randbedingung | Art. 12 Abs. 3 und Art. 15 DSGVO; Datenschutz & Informationssicherheit | USR-07 | Entwurf |
| SYS-18 | Zugriffsprotokoll | Das System muss jeden Zugriff auf personenbezogene Daten mit Zeitpunkt, Rolle und Art des Zugriffs protokollieren und für Datenschutzprüfungen auswertbar machen. | Funktional | Datenschutz & Informationssicherheit (Stakeholder Map); F-015 | USR-10 | Entwurf |
| SYS-19 | Problem melden | Das System muss Studierenden ermöglichen, zu einer Lehrveranstaltung ein inhaltliches oder organisatorisches Problem zu melden, das der zuständigen lehrenden Person angezeigt wird. | Funktional | Persona Lehrende (Mission 01) | USR-08 | Entwurf |

## Nicht in den Katalog aufgenommen

Unklare Aussagen stehen nicht im Katalog, sondern bleiben als offene Fragen bestehen (siehe [`final-requirements.md`](final-requirements.md), [`quality-review.md`](quality-review.md) und das Register der offenen Fragen in [`00_Projekt`](../00_Projekt/)).

| Aussage (Mission 03) | Grund | Offene Punkte |
| :--- | :--- | :--- |
| REQ-001 Benachrichtigung nach sieben Tagen Inaktivität | `INVESTIGATE`: Bedarf und Aussagekraft von Inaktivität ungeklärt (A-001) | Ziel in BUS-01 erfasst, Systemlösung offen |
| REQ-004 Vorhersage des Studienabbruchs | `RECONSIDER`: nicht überprüfbar, Profiling rechtlich bedenklich | Rechtliche und ethische Einschätzung |
| REQ-006 Maßnahmen bei kritischem Lernrückstand | `INVESTIGATE`: „kritisch“ und „geeignete Maßnahmen“ nicht definiert | Fragen 1–7 in final-requirements |
| REQ-008 Benachrichtigung unabhängig von Einstellungen | Widerspruch zu REQ-007 (SYS-08), „kritische Studienereignisse“ nicht definiert | Liste kritischer Ereignisse, Rechtsgrundlage |
| REQ-009 Vollzugriff der Studiengangsleitung | `RECONSIDER`: Zweck fehlt, möglicher DSGVO-Verstoß | Zweck und Umfang des Zugriffs, F-010 |
| REQ-012 Optimale Lernstrategie | `RECONSIDER`: „optimal“ hat keinen Maßstab | Lernstrategie der FH |
| REQ-014 Standard für Barrierefreiheit | `INVESTIGATE`: Verbindlichkeit und Standard nicht belegt | Ziel in USR-09 erfasst, Standard offen (F-006) |
| REQ-015 KI entscheidet über Betreuungsbedarf | `RECONSIDER`: automatisierte Entscheidung über Personen, Zweck fehlt | Siehe final-requirements |
