# Crew Health Companion

**One line:** A companion app that helps astronauts check their own health on long missions, and sends a flight surgeon alert when a value needs human attention.

**Challenge:** NASA Space Apps Challenge, "Create Health Monitoring Software for Astronauts on Space Missions."

## The problem

Long missions expose crews to space radiation, isolation and confinement, altered gravity, and a hostile closed environment. These can cause immune changes, bone loss, cardiovascular events, and behavioral health problems. On long missions, astronauts carry much of the responsibility for spotting these changes in themselves. NASA's Human Research Program (HRP) groups these threats into five hazards: space radiation, isolation and confinement, distance from Earth, gravity fields, and hostile closed environments.

## What the app does

- **Body map.** Each body region is clickable. It shows the function of that system, the linked spaceflight hazard, and the indicators to check.
- **Guided measurements.** Step-by-step instructions for heart rate and sleep, with a 60-second timer and a context tag (rest, exercise, after a meal, after poor sleep).
- **Color-coded status.** Green, amber, red, and grey, each with a text label and a shape, so the status reads without color.
- **Triage and escalation.** Emergency signs stop the normal flow and show the crew procedure screen. Red values create an escalation message for the flight surgeon. Three amber days in a row create a routine escalation.
- **Trends.** A chart shows each indicator over time, with the normal range shaded.
- **Weekly handoff.** A one-page summary of recent readings and unresolved items for the flight surgeon.

## How it uses NASA resources

Each status card shows the rule that produced it and the source for that rule. Each body region links to the NASA HRP page for its hazard. The indicator list is based on the HRP risk index, which names 17 risks.

## What is simulated

All readings are simulated. The app does not connect to any sensor, camera, or real person's data. The escalation messages are displayed only and are not sent to anyone.

## What is not yet validated

- The thresholds are provisional. They come from general clinical reference values and have not been validated for spaceflight.
- The mood screen, vision check, and blood pressure indicator are planned, not built.
- The app has not been tested with astronauts, flight surgeons, or space medicine staff.


## Demo

The demo is a seven-slide deck, linked under Links above. It covers the problem, the app, a red-reading screenshot, the NASA data used, next steps, and the team.

## Team

Team KGians: JANANI S, DHAMAYANTHI P, JANANI R, NITHIKA MURUGAN

## How AI was used

This project was built with AI assistance (Claude, by Anthropic). AI drafted the knowledge document, the prototype code, the README, the slide text. A team member then made changes to the code. The team chose the challenge and the approach, tested the prototype, took the screenshots, and reviewed the content. The team is responsible for the final submission. All readings in the app are simulated, and the thresholds are provisional.

## Links

- Prototype source: https://github.com/janani-kumaresan-1992/crew_health_companion
- - Demo slides (PDF): https://drive.google.com/file/d/1vD2xBSZcS0X4ObkkrlHhW6_n-iEbhmHy/view?usp=sharing
- Data sources: see `SOURCES.md`

## Next steps

1. Confirm each provisional threshold against a clinical guideline.
2. Open and confirm each NASA HRP page listed in `SOURCES.md`.
3. Add blood pressure and the vision check.
4. Test the triage logic with a space medicine clinician.
5. Test usability with people who have not measured their own health before.
