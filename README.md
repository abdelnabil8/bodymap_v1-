# BodyMap

## Projekt klonen und lokal starten

1. Repo klonen:
git clone https://github.com/abdelnabil8/bodymap_v1-.git
cd bodymap_v1-

2. Dependencies installieren:
npm install

3. .env Datei erstellen im Root-Ordner (neben package.json):
VITE_GROQ_KEY=dein_groq_key_hier
VITE_RAPIDAPI_KEY=dein_rapidapi_key_hier

Die Keys bekommst du von Abdellah per WhatsApp.

4. App starten:
npm run dev

Dann im Browser öffnen: http://localhost:5173

---

## Was wir verwendet haben

- React + Vite als Frontend Framework
- Groq API (kostenlos) für die KI-Planerstellung mit dem Modell llama-3.3-70b-versatile
- ExerciseDB API über RapidAPI für Übungsdaten und Ausführungsanleitungen
- localStorage für persistente Datenspeicherung ohne Backend

---

## Struktur der App

src/
├── components/
│   ├── onboarding/        8 Schritte des Onboarding Flows
│   └── workout/           Workout Übersicht, aktive Übung, Abschluss
├── screens/               Alle Hauptseiten (Home, Plan, Dashboard, Workout, Loading)
├── utils/
│   └── api.js             Groq und ExerciseDB API Calls
├── tokens.js              Design System (Farben, Abstände, Button-Styles)
├── App.jsx                Haupt-App mit State Management
└── index.css              Globale Styles

---

## Funktionen

- 8-schrittiger Onboarding Flow
- KI generiert personalisierten Trainingsplan basierend auf Nutzerprofil
- Workout Modus mit Timer, Satz-Tracking und Schritt-für-Schritt Anleitungen
- Wochenkalender mit abgeschlossenen Trainingstagen
- Dashboard mit BMI, Muskelgruppen und wöchentlichem Volumen
- Daten bleiben beim Reload gespeichert
