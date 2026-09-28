# SmartDesk Cosmetics

> **Interaktive Projektdemo für KI-gestützte Studioorganisation und Kundenkommunikation**

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38bdf8?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![ElevenLabs](https://img.shields.io/badge/ElevenLabs-Turbo_v2.5-orange?style=flat-square)](https://elevenlabs.io/)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-2.5_Flash-4285F4?style=flat-square&logo=google)](https://ai.google.dev/)

**[Live-Demo öffnen](https://smartdesk-cosmetics.vercel.app)** · Die Video-Präsentation ist über die Startseite erreichbar.

Diese README gibt einen Einblick in Idee, Aufbau und Umsetzung des Projekts. Für Fragen zur Technik erreichst du mich gern direkt.

## Projektidee

Während einer Behandlung klingelt das Telefon, eine Kundin fragt nach einem Termin, und gleichzeitig wird kurzfristig ein Platz im Kalender frei. SmartDesk Cosmetics untersucht, wie KI solche wiederkehrenden Abläufe in Kosmetikstudios unterstützen kann, ohne den persönlichen Kundenservice zu verlieren.

Die Projektdemo verbindet einen multimodalen KI-Sprachassistenten mit Oberflächen für Studioorganisation, Kundenkommunikation und Qualitätssicherung. Grundlage ist eine 5-stufige, evidenzbasierte Wissensdatenbank, dazu kommen automatisierte Terminabläufe. Das Projekt richtet sich an Kosmetikstudios und zeigt auch Anwendungsszenarien im Umfeld von Medical Beauty.

Im Mittelpunkt steht die Verbindung von Geschäftsprozessen, Nutzerführung und technischer Umsetzung: Welche Aufgaben lassen sich unterstützen, welche Informationen braucht die KI und wo liegen die Grenzen der Automatisierung?

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

Glow verbindet browserbasierte Spracherkennung, KI-generierte Antworten und synthetische Sprachausgabe. Gesprächsverlauf und aktuelles Datum dienen als Kontext, eine Unterbrechungsfunktion stoppt laufende Antworten. Fällt die Sprachausgabe des Dienstes aus, springt die Browser-Stimme ein. Deutsche Fachbegriffe, Währungen und Uhrzeiten werden vor der Ausgabe für eine natürlichere Aussprache aufbereitet.

Zur Antwortzeit macht die Demo bewusst keine Angabe, da sie unter anderem von Verbindung, Modell und Sprachausgabe abhängt.


### Wissenskonzept und Qualitätssicherung

Glow soll Fachfragen aus geprüften Wissenskarten beantworten statt frei aus dem Sprachmodell. Wie diese fünfstufige Prüfung aufgebaut ist, steht im Abschnitt [Wissenskonzept](#wissenskonzept-fünfstufige-prüfpipeline). Die Testfälle im Testing-Hub enthalten auch sensible Situationen wie Schwangerschaft oder Vorbehandlungen und machen Antworten und Fehlerbilder nachvollziehbar.

Die Testfälle belegen weder bestandene Prüfungen noch eine medizinische Validierung. Das Konzept ersetzt keine Diagnose und keine individuelle fachliche Freigabe.

### Terminorganisation und Gap-Filler

Die Simulation zeigt, wie nach einer Absage passende Kundinnen von der Warteliste benachrichtigt und freie Termine erneut angeboten werden könnten. Dazu kommen Erinnerungs- und Bestätigungsabläufe. Belegung und Umsätze beruhen auf Beispieldaten, eine Wirkung auf Terminausfälle oder eine Wiederbesetzungsquote wurde nicht untersucht.


## Wissenskonzept: fünfstufige Prüfpipeline

Damit Glow Fachfragen nicht frei aus einem Sprachmodell beantwortet, ist ein Wissenskonzept mit mehrstufiger Prüfung vorgesehen. Offene Datenquellen wie das EU-Kosmetikregister liefern Stoffdaten, aber keine Behandlungsregeln, etwa zu Karenzzeiten vor einem Peeling. Diese Lücke soll die Pipeline schließen:

1. **Erfassung:** Eine zeitlich getaktete Datenerfassung legt eine unfertige Wissenskarte an.
2. **Recherche:** Drei unabhängige Recherche-Agenten suchen parallel nach allen Feldern.
3. **Abgleich:** Die Agenten gleichen ihre Ergebnisse ab und erstellen einen gemeinsamen Entwurf.
4. **Kritik:** Ein Kritiker-Agent greift den Entwurf gezielt an, etwa bei Kontraindikationen und Gegenstudien.
5. **Freigabe:** Ein Schiedsrichter-Agent bewertet den Konsens. Unterhalb eines Schwellenwerts entscheidet ein Mensch.

Das Konzept soll zeigen, wie Wissen für einen Sprachassistenten prüfbar aufbereitet werden kann.


## Technologie-Stack

| Bereich | Eingesetzte Technologie |
| :--- | :--- |
| Frontend | [Next.js 15](https://nextjs.org/) mit App Router, [TypeScript](https://www.typescriptlang.org/) |
| Gestaltung | [Tailwind CSS](https://tailwindcss.com/), individuelles Glassmorphism-Design |
| Sprachmodell | [Google Gemini 2.5 Flash](https://ai.google.dev/) über Next.js API-Routen |
| Spracherkennung | Web Speech API des Browsers |
| Sprachausgabe | [ElevenLabs](https://elevenlabs.io/) Turbo v2.5, Browser-TTS als Rückfalloption |
| Icons | [Lucide Icons](https://lucide.dev/) |
| Hosting | [Vercel](https://vercel.com/) |


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

## Datenschutz und verantwortungsvoller KI-Einsatz

- **Serverseitige API-Schlüssel:** Gemini und ElevenLabs werden über serverseitige API-Routen angebunden. Die Schlüssel liegen nicht im Browser und sind nicht Teil des Portfolios.
- **KI-Kennzeichnung:** Glow wird als KI-Assistent kenntlich gemacht.
- **Datenverarbeitung:** Die Sprachfunktionen nutzen externe Dienste, die Spracherkennung zudem browserabhängig. Aussagen zur Speicherung müssen die gesamte Verarbeitungskette berücksichtigen, eine pauschale Zusicherung gibt es deshalb nicht.
- **Fachliche Grenzen:** Die Demo ist auf organisatorische Unterstützung und kosmetische Informationsszenarien ausgerichtet. Medizinische Entscheidungen bleiben qualifizierten Fachpersonen vorbehalten.
- **Entwicklungsstand:** Datenschutz und KI-Transparenz sind Gestaltungsthemen des Projekts. Eine abgeschlossene Prüfung der DSGVO- oder EU-AI-Act-Konformität wird nicht behauptet.

> **Hinweis zur Demo:** Bitte nur mit fiktiven Angaben testen und keine personenbezogenen Kunden- oder Gesundheitsdaten eingeben. Die Spracheingabe funktioniert am zuverlässigsten in Chrome oder Edge.

## Projektteam

Konzipiert, gestaltet und entwickelt von Timo Seng, Olaf Marohn, Sören Klose, Gerd Zschäbitz und Stefanie Wolf. Die Dokumentation wird im Portfolio von Stefanie Wolf präsentiert.
