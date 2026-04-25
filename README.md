# Roulette Pressure Engine — Real-Time Oppositional State & Streak Analyzer

A real-time roulette analysis tool that transforms raw spin outcomes into structured statistical "pressure states" and oppositional tracking systems.

It is designed to visualize how roulette sequences evolve over time using derived metrics such as streak pressure, delay accumulation, and opposite-state imbalance.

---

## Live Demo

> `https://wesharethisplace.github.io/roulette-pressure-engine/`

---

## ⚙ Core Concept

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

### 1. Live Pressure & Occurrence (v2)
The live stats panel now renders as a structured **table** with two metrics per combo:

**Occurrence (last 20 spins)** — how many times each combo appeared in the most recent 20 spins, computed by `calcLast20Counts()`.

**Pressure** — how many spins have occurred since the last occurrence of the opposite state:
- RO ↔ BE  
- BO ↔ RE  

Both metrics are displayed as **badge + progress bar** pairs:

| Threshold | Occurrence badge | Pressure badge |
|---|---|---|
| ≥ 8 occ / ≥ 7 pres | 🔥 Hot (orange glow) | 🧊 Ice (cyan glow) |
| ≥ 6 pres | — | 🔥 Fire |
| ≥ 5 pres | — | 🔥 Warm |
| ≤ 2 occ | 🧊 Cold (blue glow) | — |

Progress bars are color-tinted to match badge state (hot/fire/ice/cold).

---

### 2. Historic Pressure Distribution (≤ 500 spins)
Each system is analyzed across past spins and bucketed into:

- **Normal** (0–1)
- **Mild** (2–3)
- **Elevated** (4–5)
- **High** (6–7)
- **Extreme** (8+)

Also includes a **Max** column showing the highest observed pressure per system, rendered as a color-coded badge:

| Max value | Badge style |
|---|---|
| ≥ 7 | 🧊 Ice (cyan pulse) |
| ≥ 5 | 🔥 Fire (orange pulse) |
| ≥ 3 | Warm (amber glow) |
| < 3 | Default (grey) |

---

### 3. Zero Impact Model
Unlike standard roulette trackers, this system treats `0` as:

> a universal delay event that increases pressure across all systems

This ensures time continuity in statistical modeling.

---

### 4. Oppositional Pair Structure
The system is built around two competing pressure pairs:

- RO ↔ BE  
- BO ↔ RE  

This allows comparison of directional imbalance over time.

---

### 5. Visual Stream (last 50)
A horizontally scrollable row shows the most recent 50 spins as color-coded combo badges (RO / BE / BO / RE / 0). Below it, all raw numbers are displayed in a wrapped grid colored red, black, or green.

---

## Input Format

You can paste or stream numbers like:

```
25 19 13 17 1 28 33 28 31 4 ...
```

Press **ENTER** to update the analysis. Multiple numbers can be pasted at once; they are prepended to the history in order.

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
- how "pressure" accumulates in sequence-based betting logic
- how Martingale-style exposure behaves under real randomness
- how zero outcomes distort perceived continuity

---

## Tech Stack

- HTML
- CSS (with CSS animations for badge pulse effects)
- Vanilla JavaScript (no dependencies)

Fully client-side, no backend required.

---

## Changelog

### v2
- Replaced plain-text stat output with structured `<table>` layout for both Live and Historic panels
- Added **Occurrence (last 20)** metric via `calcLast20Counts()` — new column alongside Pressure in the live table
- Introduced **badge system** with six tiers: default, warm, hot, fire, ice, cold — each with distinct border color and CSS glow animation
- Added **progress bar** visualizations for both Occurrence and Pressure, color-tinted to match badge state
- Added **Max pressure badge** column to the Historic table with warm / fire / ice color tiers
- Introduced `@keyframes pulse-hot` and `pulse-cold` animations for high-intensity badge states
- `box-sizing: border-box` added to input for consistent layout
- `section-divider` HR between live and historic panels
- Centered `<h2>` heading

### v1
- Initial release: plain-text live pressure and historic distribution output

---

## Disclaimer

This tool is for statistical exploration and visualization only.  
It does not provide predictive advantage over fair roulette.

---

## License

MIT (or your preferred license)