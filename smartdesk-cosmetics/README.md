# SmartDesk Cosmetics

> **Interaktive Projektdemo für KI-gestützte Studioorganisation und Kundenkommunikation**

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38bdf8?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![ElevenLabs](https://img.shields.io/badge/ElevenLabs-Turbo_v2.5-orange?style=flat-square)](https://elevenlabs.io/)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-2.5_Flash-4285F4?style=flat-square&logo=google)](https://ai.google.dev/)

**[Live-Demo öffnen](https://smartdesk-cosmetics.vercel.app)** · Die Video-Präsentation ist über die Startseite erreichbar.

Dieses Verzeichnis dokumentiert das Projekt als Teil eines öffentlichen Portfolios. Der Quellcode wird nicht veröffentlicht.

## Projektidee

Während einer Behandlung klingelt das Telefon, eine Kundin fragt nach einem Termin und kurzfristig wird ein Platz im Kalender frei. SmartDesk Cosmetics untersucht, wie KI solche wiederkehrenden Abläufe in Kosmetikstudios unterstützen kann.

Die Projektdemo verbindet einen KI-Sprachassistenten mit Oberflächen für Studioorganisation, Kundenkommunikation und Qualitätssicherung. Sie richtet sich an Kosmetikstudios und zeigt auch Anwendungsszenarien im Umfeld von Medical Beauty.

Im Mittelpunkt steht die Verbindung von **Geschäftsprozessen, Nutzerführung und technischer Umsetzung**: Welche Aufgaben lassen sich unterstützen, welche Informationen braucht die KI und wo liegen die Grenzen der Automatisierung?

## Funktions- und Entwicklungsstatus

**Integriert** bezeichnet Funktionen innerhalb der Projektdemo. **Simuliert** kennzeichnet Abläufe mit Beispieldaten. **Konzept / geplant** bezeichnet noch nicht vollständig umgesetzte Erweiterungen. Diese Angaben beschreiben den Entwicklungsstand, keine Freigabe für den produktiven Studiobetrieb.

| Modul | Status | Umfang |
| :--- | :--- | :--- |
| **Sprachassistent „Glow“ im Browser** | Integriert | Sprachdialog mit Gemini und ElevenLabs, Streaming-Sprachausgabe, Einbeziehung des aktuellen Datums sowie Tap-to-Talk und Unterbrechungsfunktion. |
| **Benutzeroberfläche und Navigation** | Integriert | Fünf interaktive Ansichten: Startseite, SuperAdmin, Studio, Kundenportal und QA-Testing. |
| **Sprachnormalisierung** | Integriert | Aufbereitung deutscher Fachbegriffe, Währungen, Uhrzeiten und Lichtschutzfaktor-Angaben für die Sprachausgabe. |
| **QA-Testing-Hub** | Integriert | Interaktiver Testbereich mit 100 kategorisierten Testfällen zu Wirkstofffragen, sensiblen Beratungssituationen und Antwortzeiten. |
| **Studio-Cockpit** | Simuliert | Tageskalender, Belegungsübersicht, Umsatz-Projektionen und Schulungsmatrix mit Beispieldaten. |
| **WhatsApp Gap-Filler und Erinnerungen** | Simuliert | Ablauf zur Benachrichtigung von Wartelisten-Kundinnen und zur Terminbestätigung; keine produktive WhatsApp-Anbindung. |
| **3D Studio-Raumplaner** | Simuliert | Darstellung von Kabinenbelegung und Geräte-Rüstzeiten. |
| **Kundenportal** | Simuliert | Beispielansichten für Pflegeplan, Behandlungshistorie und personalisierte Kundenkommunikation. |
| **Fünfstufiges Wissenskonzept** | Konzept / QA | Strukturierte Aufbereitung und Prüfung von Antworten zu kosmetischen Wirkstoffen und Beratungssituationen. |
| **Telefonanbindung über SIP/VoIP** | Geplant | Entgegennahme klassischer Anrufe über die Studiorufnummer. |
| **Anbindung an Studio- und Buchungssoftware** | Geplant | Synchronisation von Terminen und Verfügbarkeiten mit externen Systemen. |
| **Kameragestützte Hautanalyse** | Geplant | Untersuchung eines möglichen visuellen Assistenzmoduls; Aussagekraft und fachliche Grenzen sind noch zu evaluieren. |

## Ausgewählte Funktionen

### Sprachassistenz mit „Glow“

Glow verbindet browserbasierte Spracherkennung, KI-generierte Antworten und synthetische Sprachausgabe. Gesprächsverlauf und aktuelles Datum dienen als Kontext. Eine Unterbrechungsfunktion ermöglicht es, laufende Antworten zu stoppen; Browser-Sprachausgabe dient als Rückfalloption.

Die Demo enthält keine garantierte Latenzangabe. Die Antwortzeit hängt unter anderem von Verbindung, Modellverarbeitung und Sprachausgabe ab.

### Wissenskonzept und Qualitätssicherung

Das fünfstufige Wissenskonzept adressiert Fragen zu Inhaltsstoffen und kosmetischen Anwendungen, beispielsweise zu Retinoiden, Fruchtsäuren, Peptiden und Antioxidantien. Testfälle berücksichtigen auch sensible Situationen wie Schwangerschaft, Stillzeit und Vorbehandlungen.

Der Testing-Hub dient dazu, Antworten und Fehlerbilder nachvollziehbar zu untersuchen. Die Anzahl der Testfälle ist keine Aussage über bestandene Tests oder medizinische Validierung. Das Konzept bietet keine Diagnose oder individuelle medizinische Freigabe für Produkte und Behandlungen.

### Terminorganisation und Gap-Filler

Die Simulation zeigt, wie nach einer Absage passende Wartelisten-Kundinnen benachrichtigt und freie Termine erneut angeboten werden könnten. Ergänzend werden Erinnerungs- und Bestätigungsabläufe dargestellt.

Belegung und Umsatzdarstellungen beruhen auf Beispieldaten. Eine tatsächliche Verringerung von Terminausfällen oder eine bestimmte Wiederbesetzungsquote wurde damit nicht nachgewiesen.

## Technologie-Stack

| Bereich | Eingesetzte Technologie |
| :--- | :--- |
| Frontend | Next.js 15 mit App Router, TypeScript |
| Gestaltung | Tailwind CSS, individuelles Glassmorphism-Design |
| Sprachmodell | Google Gemini 2.5 Flash über Next.js API-Routen |
| Spracherkennung | Web Speech Recognition API |
| Sprachausgabe | ElevenLabs Turbo v2.5, Browser-TTS als Rückfalloption |
| Icons | Lucide Icons |
| Hosting | Vercel |

## Datenschutz und verantwortungsvoller KI-Einsatz

- **Serverseitige API-Schlüssel:** Die Anbindung von Gemini und ElevenLabs erfolgt über serverseitige API-Routen; die zugehörigen Schlüssel werden nicht im öffentlichen Portfolio bereitgestellt.
- **KI-Kennzeichnung:** Glow wird als KI-Assistent kenntlich gemacht.
- **Datenverarbeitung:** Die Sprachfunktionen beziehen externe Dienste und browserabhängige Spracherkennung ein. Aussagen zur Speicherung und Verarbeitung müssen deshalb die gesamte Verarbeitungskette berücksichtigen; eine pauschale Zusicherung, dass keinerlei Audiodaten gespeichert werden, wird hier nicht gegeben.
- **Fachliche Grenzen:** Die Demo ist auf organisatorische Unterstützung und kosmetische Informationsszenarien ausgerichtet. Medizinische Entscheidungen bleiben qualifizierten Fachpersonen vorbehalten.
- **Entwicklungsstand:** Datenschutz und KI-Transparenz sind Gestaltungsthemen des Projekts. Eine abgeschlossene Prüfung der DSGVO- oder EU-AI-Act-Konformität wird nicht behauptet.

**Bitte die öffentliche Demo ausschließlich mit fiktiven Angaben testen und keine personenbezogenen Kunden- oder Gesundheitsdaten eingeben.**

## Projektteam

Konzipiert, gestaltet und entwickelt von **Timo Seng, Olaf Marohn, Sören Klose, Gerd Zschäbitz und Stefanie Wolf**.

Die Dokumentation wird im Portfolio von Stefanie Wolf präsentiert.
