# Roulette Pressure Engine — Real-Time Oppositional State & Streak Analyzer

A real-time roulette analysis tool that transforms raw spin outcomes into structured statistical "pressure states" and oppositional tracking systems.

It is designed to visualize how roulette sequences evolve over time using derived metrics such as streak pressure, delay accumulation, and opposite-state imbalance.

---

## Live Demo

> `https://wesharethisplace.github.io/roulette-pressure-engine/`

---

## ⚙Core Concept

Instead of treating roulette outcomes as isolated events, this tool models them as a **state pressure system**:

### Outcome Mapping
Each number is categorized into one of four structural states:

- 🔴 RO = Red + Odd  
- ⚫ BE = Black + Even  
- 🔵 BO = Black + Odd  
- 🟡 RE = Red + Even  

Additionally:
- `0` is treated as a **global delay event**, affecting all systems equally.

---

## What the Tool Tracks

### 1. Live Pressure
Shows how many spins have occurred since the last occurrence of the opposite state:

- RO ↔ BE
- BO ↔ RE

This creates a real-time “stress level” per system.

---

### 2. Historic Pressure Distribution (≤500 spins)
Each system is analyzed across past spins and bucketed into:

- normal (0–1)
- mild (2–3)
- elevated (4–5)
- high (6–7)
- extreme (8+)

Also includes:
- Maximum observed pressure per system

---

### 3. Zero Impact Model
Unlike standard roulette trackers, this system treats `0` as:

> a universal delay event that increases pressure across all systems

This ensures time continuity in statistical modeling.

---

### 4. Oppositional Pair Structure
The system is built around two competing pressure pairs:

- RO ↔ BE (blue/grey system)
- BO ↔ RE (black/burgundy system)

This allows comparison of directional imbalance over time.

---

## Input Format

You can paste or stream numbers like:

25 19 13 17 1 28 33 28 31 4 1 14 35 0 19 15 11 18 4 8 19 10 21 33 24 22 13 35 12 1 24 1 10 29 13 32 13 6 30 34 5 18 18 31 4 35 33 17 24 28 36 3 9 32 14 12 11 25 34 19 13 14 14 21 6 13 8 28 15 9 32 30 8 29 24 11 30 9 24 7 23 36 20 30 4 10 5 15 12 31 10 2 5 28 29 5 28 35 2 24 3 5 14 0 6 8 31 24 14 20 12 0 21 30 23 3 25 22 30 21 35 35 29 14 3 15 35 6 24 14 28 36 35 23 24 0 15 12 26 6 19 27 20 9 0 26 17 7 33 1 21 0 30 25 30 0 26 27 13 35 11 14 22 34 30 26 31 2 31 33 2 13 19 1 21 33 18 6 5 36 25 9 13 17 19 36 4 20 36 0 6 19 32 27 35 4 34 10 4 12 34 8 14 28 8 24 24 35 8 3 35 17 19 7 17 27 32 19 9 21 19 8 16 3 10 19 1 24 34 27 23 15 31 12 18 33 14 7 2 10 27 11 5 7 4 36 5 24 15 15 17 3 4 24 24 10 14 23 34 31 35 23 17 6 26 27 32 8 20 28 5 20 6 8 22 12 13 5 30 19 5 9 0 17 3 21 29 15 31 18 6 30 8 25 5 32 18 7 12 25 3 24 22 21 7 0 18 1 23 27 36 18 2 28 27 8 15 1 34 26 23 32 20 23 14 7 15 1 36 17 16 29 5 34 0 35 23 0 8 31 23 11 14 23 36 30 17 19 10 9 6 1 29 27 2 27 30 29 4 11 8 31 5 9 26 27 32 15 21 31 16 28 12 1 15 23 23 24 2 6 27 7 20 33 8 36 6 21 22 8 13 27 17 32 12 19 14 24 34 7 18 19 7 18 0 23 33 11 10 22 11 22 4 17 1 15 27 17 1 1 0 13 36 28 24 32 1 19 29 0 22 35 23 6 10 7 22 7 11 14 19 0 31 27 14 18 34 16 17 19 14 29 27 29 17 12 30 2 23 11 23 6 2 26 10 28 17 4 10 36 20 35 21 25 8 31 30 36 10 8 5 19 14 33 2 9 7 7 3 5 9 6 20 17 14 34 26 31 21 30

Press ENTER to update the analysis.

---

## What This Project Is (and is NOT)

### It IS:
- A sequence analysis tool
- A state pressure simulator
- A visual volatility tracker
- A study of run-length behavior

### It is NOT:
- A prediction tool
- A guaranteed profit system
- A bias detector for roulette wheels

Roulette remains statistically random.

---

## Why This Exists

This project was built to explore:

- how streaks emerge in random systems
- how “pressure” accumulates in sequence-based betting logic
- how Martingale-style exposure behaves under real randomness
- how zero outcomes distort perceived continuity

---

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript (no dependencies)

Fully client-side, no backend required.

---

## Disclaimer

This tool is for statistical exploration and visualization only.  
It does not provide predictive advantage over fair roulette.

---

## License

MIT (or your preferred license)