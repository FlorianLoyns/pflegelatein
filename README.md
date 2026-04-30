# Pflegelatein

**Vokabeltrainer für die Pflegeausbildung — Latein, Griechisch und klinische Begriffe als Karteibox**

[![Lizenz: CC BY-NC-SA 4.0](https://img.shields.io/badge/Lizenz-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.de)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue)](https://florianloyns.github.io/pflegelatein/)
![Keine Abhängigkeiten](https://img.shields.io/badge/Abh%C3%A4ngigkeiten-keine-brightgreen)
![PWA](https://img.shields.io/badge/PWA-offline--f%C3%A4hig-teal)

Eine browser-basierte Karteibox für Pflege-Azubis: Lateinische und griechische Fachbegriffe aus der Anatomie, Pathologie und dem Klinikalltag — gepaart mit deutschen Übersetzungen, organisiert nach dem Leitner-System. Wer ehrlich bewertet, kommt schneller voran.

**[Jetzt lernen](https://florianloyns.github.io/pflegelatein/)**

## Lernprinzip

Du bekommst eine Karte gezeigt — vorne der lateinische Begriff (z. B. *cor*), hinten die deutsche Übersetzung (Herz). Tippen flippt die Karte um. Danach bewertest du dich selbst über drei Knöpfe: **Wusste nicht** (rot, Karte wandert zurück in Fach 1), **Unsicher** (gelb, Karte bleibt im aktuellen Fach), **Wusste ich** (grün, Karte rutscht ein Fach weiter).

Karten in Fach 1 wiederholst du am nächsten Tag, in Fach 2 nach 2 Tagen, dann 4, 8 und 16 Tagen. Wer eine Karte fünfmal hintereinander wusste, sieht sie nur noch alle 16 Tage — gerade oft genug, um sie nicht zu verlieren, selten genug, um Zeit für neue zu haben.

Die Lernrichtung kannst du in den Einstellungen wählen: **Latein → Deutsch** (Erkennen üben — gut für Arztbriefe und OP-Berichte), **Deutsch → Latein** (aktiv produzieren — gut für eigene Dokumentation), oder **gemischt** — bei jeder Karte zufällig die eine oder die andere Richtung. Lernpsychologisch ist Mischen das Stärkste.

## Was die App trainiert

- **Anatomische Fachsprache**: Knochen, Muskeln, Organe, Lagebezeichnungen (proximal, distal, dorsal, ventral, sagittal …)
- **Pathologie und Krankheitsbilder**: Apoplex, Sepsis, Pneumonie, Hypertonie, Anämie, Embolie, Phlebitis …
- **Pflegepraxis und Diagnostik**: Dekubitus, Punktion, Reanimation, Katheter, Asepsis, Anamnese …
- **Wortbausteine zum Selbst-Entschlüsseln**: *-itis* = Entzündung, *-ektomie* = operative Entfernung, *hyper-* = über, *brady-* = langsam — mit diesen Bausteinen kannst du unbekannte Begriffe wie *Cholezystektomie* oder *Bradykardie* selbst zerlegen
- **Symptome und Befunde**: Cyanose, Dyspnoe, Pruritus, Exanthem, Tachykardie …
- **Verben aus dem Alltag**: palpieren, auskultieren, perkutieren, mobilisieren, intubieren …

## Kern-Mechanik

| Element | Effekt |
| ------- | ------ |
| 5 Lernfächer | Wiederholungsintervall: 1 / 2 / 4 / 8 / 16 Tage |
| Wusste nicht | Karte zurück in Fach 1 |
| Unsicher | Karte bleibt im aktuellen Fach |
| Wusste ich | +1 XP, Karte rutscht ein Fach weiter |
| Tägliches Pensum | 10, 20, 30 oder 50 Karten pro Session, frei wählbar |
| Reihenfolge | Alphabetisch oder zufällig |
| Streak-Anzeige | Heatmap der letzten 30 Tage als 15×2-Streifen |
| Persistenz | Lernstand, XP, Tageshistorie in `localStorage` (kein Server) |

## XP & Stations-Karriere

Jede „Wusste ich"-Antwort zählt dauerhaft 1 XP, gespeichert lokal im Browser:

| Stufe | XP |
| ----- | --- |
| Pflegeazubi 1. Jahr | 0 |
| Pflegeazubi 2. Jahr | 50 |
| Pflegeazubi 3. Jahr | 150 |
| Pflegefachkraft | 350 |
| Praxisanleitung | 700 |
| Stationsleitung | 1500 |
| Pflegedirektion | 3000 |

Der Start-Screen zeigt aktuelle Stufe + Fortschrittsbalken. Bei Aufstieg nach einer Session gibt's eine Konfetti-Fanfare auf dem End-Screen.

## Bonus-Mechaniken

**Streak-Heatmap** — die letzten 30 Tage als kleine Kacheln, gefärbt nach Anzahl gelernter Karten. Heutiger Tag mit Outline markiert. Lücken werden sichtbar, das aktiviert das „Don't break the chain"-Gefühl.

**Wackelkandidaten kommen automatisch zurück** — falsch beantwortete Karten landen sofort wieder in Fach 1 und sind morgen wieder dran. Schwächen werden gezielt geübt, ohne dass du dir merken musst, was schiefgelaufen ist.

**Adaptive Sessions** — der Session-Bauer befüllt zuerst alle fälligen Karten, dann erst neue. Du läufst nie ins Leere, solange noch Stoff offen ist.

**Keyboard-Shortcuts** für den Schreibtisch: Leertaste flippt, 1/2/3 (oder J/K/L) bewerten.

## Didaktischer Hintergrund

Pflege-Azubis stehen am ersten Tag im Praxiseinsatz vor Begriffen wie *Cholezystektomie*, *Trochanter*, *Iso-Tonus*, ohne dass sie diese je gehört haben. Anatomie und medizinische Fachsprache werden im Unterricht meist beiläufig vermittelt — nicht systematisch trainiert. Genau diese Lücke schließt eine **Karteibox mit Spaced Repetition**: kein Frontalunterricht, sondern verteiltes Üben in kleinen Häppchen über Wochen, mit dem Effekt, dass das Vokabular ins Langzeitgedächtnis rutscht.

Das Leitner-System ist seit den 1970ern erforscht und in Apps wie Anki bewährt. Die Selbstbewertung („wusste ich" vs. „unsicher") kalibriert das System auf das individuelle Tempo — Schüler:innen lernen schnell, sich ehrlich einzuschätzen. Die Heatmap und die XP-Stufen lehnen sich bewusst an Suchtmechaniken erfolgreicher Lern-Apps an, gezielt eingesetzt für Konstanz statt Inhaltsbreite.

Der Wortschatz wurde ausgehend vom anatomischen Mini-Wörterbuch von Dr. Hamid Emminger (Thieme) kuratiert und um klinische Pflege-Begriffe ergänzt, die im ursprünglichen Wörterbuch fehlten. Ergebnis: rund 600 Begriffe, die im Pflegealltag tatsächlich vorkommen.

## Technik

- Einzelne HTML-Datei, Vanilla JavaScript, keine Frameworks, kein Build-Tool
- Kein externes CDN, keine Abhängigkeiten zur Laufzeit
- **PWA**: installierbar auf Desktop und Smartphone, offline-fähig via Service Worker
- **Mobile-First-Layout**: `viewport-fit=cover` für iPhone-Notch, `safe-area-inset` für Home-Indicator, Touch-Targets über 44px
- Lernstand, Streak und XP persistent in `localStorage`
- Web Audio API für Sound-Feedback (kein Audio-File)
- Inline-SVG für Icons (kein Bild-Asset nötig)
- Tageshistorie und Aktivitäts-Heatmap als JSON im Browser-Speicher
- DSGVO-konform: keine Tracker, keine externen Ressourcen, keine Datenübertragung

## Impressum

Verantwortlich: Florian Loyns. Pflichtangaben nach § 5 DDG und Kontakt: [Impressum](https://florianloyns.github.io/Impressum/)

## Lizenz

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.de) · Nutzen, anpassen und teilen — unter Namensnennung, nicht-kommerziell und unter gleichen Bedingungen.
