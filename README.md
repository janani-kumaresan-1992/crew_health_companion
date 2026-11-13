# Crew Health Companion (prototype)

A prototype health monitoring app for astronauts on long-duration missions. It helps a crew member take a few measurements, see a color-coded status, read a plain-language explanation, and send a flight surgeon escalation when a value needs human attention.

**This is a prototype. It uses simulated data. It is not a medical device and has not been validated for spaceflight.**

## What is in this repository

- `index.html`: the whole app in one file, with inline CSS and JavaScript. No server, no build step, no internet connection needed to run.
- `SOURCES.md`: the sources behind the hazards, risks, and thresholds, with the status of each one.
- `PROJECT_PAGE.md`: the project summary and demo script.

## How to run it

1. Download `index.html`.
2. Open it in any modern desktop or phone browser.
3. Start on the Home tab. Use the Body map, Measure, Trends, Escalation, and Handoff tabs from the top bar.

## What to try (about 3 minutes)

1. Home: the overall status and the two indicators.
2. Body map: tap the chest to see heart rate and the linked hazard. Tap the head to see sleep.
3. Measure, heart rate: complete the four steps. Use the quick-fill buttons to test green (72), amber (110), and red (128) readings. A red result opens the Immediate action screen and an escalation message.
4. Measure, sleep: enter three nights. The default values form an amber pattern.
5. Trends: the shaded band is the normal range. Use "Undo my last entry" to remove a reading you entered. Simulated history is never removed.
6. Escalation: the log of messages. Nothing is sent to a real person.
7. Handoff: the weekly summary for the flight surgeon.

## How the status logic works

Each reading is scored against provisional ranges. The rule number on each card points to the matching row in the knowledge document. The main rules are:

- Emergency signs stop the normal flow and show the crew procedure screen. The app never offers self-treatment.
- Heart rate: green 60 to 100 bpm; amber 101 to 120 or 40 to 59; red above 120, or below 40 with symptoms.
- Sleep: green 7 to 9 hours; amber below 7 hours; red below 5 hours on two nights in a row.
- Three amber days in a row create a routine escalation.
- Missing or out-of-range data is shown in grey and is not scored.

All thresholds are **provisional**. They come from general clinical reference values and must be confirmed against a clinical guideline and validated for spaceflight before any real use.

## Limits of this version

- Only heart rate and sleep are scored. The body map shows the other regions as planned features.
- Readings are simulated. No sensor, camera, or device input is connected.
- Escalation messages are displayed only. No message is sent.
- The HTML page does not save data between sessions.
- The app has not been tested with astronauts, flight surgeons, or a space medicine team.

## Safety statement

This app supports the crew and the flight surgeon. It does not diagnose, prescribe, or replace medical care.

## License

Choose a license before publishing (for example MIT or Apache-2.0). Keep it consistent with the Space Apps rules.
