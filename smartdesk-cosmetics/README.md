# SmartDesk Cosmetics
> **Interaktive Projektdemo: KI-gestützte Studioorganisation & Kundenkommunikation für moderne Kosmetikstudios & Medical Beauty**

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38bdf8?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![ElevenLabs](https://img.shields.io/badge/ElevenLabs-Turbo_v2.5-orange?style=flat-square)](https://elevenlabs.io/)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-2.5_Flash-4285F4?style=flat-square&logo=google)](https://ai.google.dev/)
[![Privacy by Design](https://img.shields.io/badge/DSGVO_%26_EU_AI_Act-Konzipiert-emerald?style=flat-square)]()

---

## Executive Summary

**SmartDesk Cosmetics** ist ein prototypisches KI-Betriebssystem für Kosmetik- und Medical-Beauty-Institute. Das Projekt demonstriert, wie moderne multimodale Sprachassistenz, eine 5-stufige evidenzbasierte Wissensdatenbank und automatisierte Terminabläufe in einer einheitlichen Luxus-Benutzeroberfläche zusammengeführt werden können.

Das System adressiert ein zentrales Problem im Studioalltag: **Wiederkehrende Terminanfragen und Beratungsgespräche während laufender Behandlungen**, ohne den persönlichen, empathischen Kundenservice zu verlieren.

---

## Funktions- & Entwicklungsstatus

Um den genauen Umsetzungsstand transparent darzustellen, ist jedes Modul nach seinem Status gekennzeichnet:

| Modul | Status | Beschreibung |
| :--- | :---: | :--- |
| **Glow Voice-Call (Browser)** | **Live integriert** | Multimodaler Echtzeit-Sprachdialog via *Google Gemini 2.5 Flash* & *ElevenLabs Turbo v2.5* (Streaming mit Latenzen unter 1 Sekunde), dynamisches Datums-Grounding & Tap-to-Talk/Barge-In. |
| **Glassmorphism HUD & Rollen-Dock** | **Live integriert** | Responsives Design-System mit 5 interaktiven Perspektiven (Startseite, SuperAdmin, Studio, Kundenportal, QA-Testing). |
| **Phonetische Sprachnormalisierung** | **Live integriert** | Automatische Aufbereitung deutscher Fachbegriffe, Währungen, Uhrzeiten und LSF-Angaben für natürliche Aussprache. |
| **QA- & Testsuite (Testing Hub)** | **Live integriert** | 100 kategorisierte Testfälle zur Verifikation von Wirkstoff-Abfragen, Kontraindikationen und Latenzen mit interaktivem Runner. |
| **Studio-Cockpit (Inhaberin)** | **Mit Beispieldaten simuliert** | Tageskalender, Belegungs-Heatmap, Umsatz-Projektionen und Mitarbeiter-Schulungsmatrix. |
| **WhatsApp No-Show Gap-Filler** | **Mit Beispieldaten simuliert** | Automatisierter Benachrichtigungsflow für Wartelisten-Kundinnen bei spontanen Slot-Absagen. |
| **3D Studio-Raumplaner** | **Mit Beispieldaten simuliert** | Visualisierung der Kabinenbelegung und Geräte-Rüstzeiten. |
| **Kundenportal (Concierge)** | **Mit Beispieldaten simuliert** | Personalisierter Skin-Concierge, Pflegeplan und Behandlungshistorie. |
| **Festnetz-Telefonanbindung (SIP/VoIP)** | **Geplant (Roadmap)** | Direkte VoIP-Anbindung via Twilio/Vapi zur Entgegennahme klassischer Telefonanrufe über die Studiorufnummer. |
| **Praxissoftware-Synchronisation** | **Geplant (Roadmap)** | 2-Wege-Schnittstellen zu Branchen-Software (z. B. Treatwell, Phorest, Shore). |
| **Multimodale Kamera-Hautanalyse** | **Geplant (Roadmap)** | Vision-basierter Hautbarriere-Check über Smartphone-Kamera. |

---

## Kernmodule im Detail

### 1. Autonomer Voice-Avatar „Glow“
* **Echtzeit-Sprachdialog**: Sub-Sekunden-Streaming über serverseitig angebundenes *Google Gemini 2.5 Flash* und *ElevenLabs Turbo v2.5* (inklusive Graceful Browser-TTS-Fallback).
* **Kontext-Intelligenz**: Dynamisches Termin- und Datums-Grounding, Memory-Historie und saubere Unterbrechungsmöglichkeit (Barge-In).
* **Phonetische Engine**: Spezialisierte Regex-Normalisierung deutscher Kosmetik-Fachwörter und Zahlen.

### 2. 5-Stufen Evidenz-Wissensdatenbank (Konzept & QA)
* **Wirkstoff- & INCI-Prüfung**: Vorab-Filter für Retinoide, Fruchtsäuren (AHA/BHA), Peptide und Antioxidantien.
* **Kosmetische Leitplanken**: Standardisierte Sicherheitsabfragen bei Schwangerschaft, Stillzeit oder Vorbehandlungen. *(Hinweis: Dient als kosmetische Vorab-Hilfe, ersetzt keine dermatologische oder medizinische Diagnose).*

### 3. WhatsApp Gap-Filler & No-Show-Prävention (Simulation)
* **Ziel-KPI (Modellrechnung)**: Bis zu 84 % Besetzung stornierter Termine durch automatisiertes Nachrücken von Wartelisten-Kundinnen.
* **Smart Reminders**: Vorab-Check-in via Messenger mit 1-Click-Bestätigung.

---

## Technologie-Stack

| Schicht | Technologie |
| :--- | :--- |
| **Frontend Framework** | [Next.js 15 (App Router)](https://nextjs.org/) |
| **Sprache** | [TypeScript](https://www.typescriptlang.org/) |
| **Styling & HUD Design** | [Tailwind CSS](https://tailwindcss.com/) + Custom Glassmorphism HUD |
| **Voice & Speech Synthesis** | [ElevenLabs Turbo v2.5](https://elevenlabs.io/) (Streaming Audio API) |
| **Spracherkennung (STT)** | Native Web Speech Recognition API mit Interim-Tracking |
| **Sprachmodell (LLM)** | [Google Gemini 2.5 Flash](https://ai.google.dev/) via Next.js API Routes |
| **Icons & UI Assets** | [Lucide Icons](https://lucide.dev/) |
| **Hosting & Deployment** | [Vercel](https://vercel.com/) |

---

## Governance & Datenschutz (Privacy by Design)

* **Sichere API-Architektur**: Sämtliche API-Schlüssel (Gemini, ElevenLabs) verbleiben serverseitig in geschützten Next.js Edge-/API-Routen.
* **Keine permanente Audiospeicherung**: Audiodaten werden flüchtig im Arbeitsspeicher gestreamt und nach der Wiedergabe verworfen.
* **Transparenzgebot**: Eindeutige Kennzeichnung des KI-Assistenten bei jedem Sprach- und Textkontakt.
* **Abgrenzung**: Klare Beschränkung auf kosmetische Beratung und Terminfindung – keine medizinischen Heilaussagen oder Diagnosen.

---

## Lokale Entwicklung & Setup

```bash
# 1. Repository klonen
git clone https://github.com/Roxylein/SmartDesk-Cosmetics.git

# 2. Abhängigkeiten installieren
npm install

# 3. Umgebungsvariablen anlegen (.env.local)
GEMINI_API_KEY=dein_gemini_api_key
ELEVENLABS_API_KEY=dein_elevenlabs_api_key

# 4. Entwicklungsserver starten
npm run dev
```

---

## Projekt-Urheberschaft

*Konzipiert, designt und entwickelt von **Timo Seng, Olaf Marohn, Sören Klose und Gerd Zschäbitz, Stefanie Wolf*** als B2B Beauty-Tech Showcase für moderne KI-gestützte Studioorganisation.
