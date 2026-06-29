# P099 — A320 Fuselage Visualizer & Fusion 360 Generator

## Project Goal
Interactive web tool for visualizing Airbus A320 fuselage geometry and generating
Fusion 360 Python scripts based on real aircraft dimensions.

## Key Facts
- Aircraft: Airbus A320 (NOT Boeing — common mix-up)
- Fuselage OD: 3.95 m | Internal cabin width: 3.7 m
- Overall length: 37.57 m | Wingspan: 35.8 m | Height: 11.76 m
- Frame stations: reference origin 2540 mm forward of nose, in millimeters

## Stack
- Pure HTML/CSS/JS (no build step) — single file or small set of files in src/
- Fusion 360 API: Python scripts (adsk.fusion, adsk.core)

## Workflow
1. User sets scale (1%–100%)
2. Side profile + cross-section SVG renders update live
3. Station table shows 10 key fuselage zones
4. Copy-paste Fusion 360 Python script into Tools → Scripts → Run
5. AI Workflow tab: OpenVSP → Fusion → Claude prompts → Simulation → Export

## Files
- src/index.html — main React/vanilla app
- src/fusion360_generator.py — standalone Fusion 360 script
- tasks/todo.md — task tracker
