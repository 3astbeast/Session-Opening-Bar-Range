<p align="center">
  <img src="https://avatars.githubusercontent.com/u/209633456?v=4" width="160" alt="RedTail Indicators Logo"/>
</p>

<h1 align="center">Session Opening Bar Range</h1>

<p align="center">
  <b>A session opening bar range indicator for NinjaTrader 8.</b><br>
  Captures the first bar's high/low/mid of a configurable session, then projects those levels forward with statistical extensions, range extensions, and OR rotation levels.
</p>

---

## Credit

Original TradingView Pine Script by **[@notprofessorgreen](https://twitter.com/notprofgreen)**. 

---

## Overview

Session Opening Bar Range captures the high, low, and midpoint of the first bar of a trading session at a configurable timeframe (e.g., the 5-minute opening bar), then draws those levels across the rest of the session. On top of the core OR zone, it can project statistical levels derived from historical OR ranges, range-multiplied extension levels, and fixed-increment rotation levels — giving you a complete opening range framework from a single indicator.

---

## Session Presets

The indicator ships with 7 preset sessions plus a fully custom option:

- **New York RTH** — 9:30 AM – 4:00 PM
- **New York Futures** — 8:00 AM – 5:00 PM
- **London** — 2:00 AM – 8:00 AM
- **Asia** — 7:00 PM – 2:00 AM (crosses midnight)
- **Midnight to 5 PM**
- **ZB/Gold/Silver OR** — 8:20 AM – 4:00 PM
- **CL OR** — 9:00 AM – 4:00 PM
- **Custom** — Enter any HHMM start and end times

Timezone is configurable with common presets: America/New_York, America/Chicago, Europe/London, Asia/Tokyo, or any Windows timezone ID.

---

## Opening Bar Range

The core of the indicator — captures the first bar of the session at a configurable minute resolution, then draws the high, low, and optional midline forward.

- **OBR Timeframe** — The minute-based bar size used to define the opening bar (e.g., 5 = the 5-minute opening bar). Adds a secondary data series at this resolution.
- **Bullish/Bearish Color Coding** — The OR zone color reflects whether the opening bar closed above (bullish) or below (bearish) its open.
- **Fill** — The area between OR high and OR low is filled with a semi-transparent shading. Independent bullish and bearish fill opacity.
- **Midline** — Optional dashed midline at (High + Low) / 2.
- **Projection Offset** — Extends levels forward by a configurable number of bars beyond the current bar (default: 50).
- **Historical Display** — Show previous sessions' OR zones on the chart with configurable max history count (default: 20).
- **Labels** — Optional High/Low/Mid labels with optional price display, positionable on the left or right side.

---

## Statistical Levels

Derived from a rolling lookback of historical OR ranges (default: 60 periods). These levels answer: "Based on past opening ranges, how far might price extend today?"

- **Two standard deviation bands** projected above the OR high and below the OR low
- Configurable multipliers (default: 1.0σ and 2.0σ)
- Only displayed when at least 2 historical ranges are available
- Independent line color, line width, label color, and label size (Tiny/Small/Normal/Large)

---

## Range Extensions

Projects the OR range size as equidistant levels above and below the OR boundaries.

- **Range Multiplier** — Scales the extension increment (default: 1.0 = full OR range per level)
- **Number of Extension Levels** — Up to 20 levels above and below (default: 5)
- Labels show "R+1", "R+2", etc. with the extension distance in parentheses
- Independent line color, line width, label color, and label size

---

## OR Rotations

Fixed-increment rotation levels above the OR high and below the OR low — 5 levels in each direction.

- **Rotation Increment** — The fixed point value per level (e.g., 65 for NQ, 15 for ES)
- Labels show "R+1 (65)", "R-2 (130)", etc.
- Independent line color, line style (Solid/Dash/Dot), line width, label color, and label size

---

## Visual Settings

- **Range Line Style** — Solid, Dash, or Dot for the OR high/low lines
- **Range Line Width** — 1 to 10
- **Midline Style** — Independent dash style
- **Midline Width** — Independent width
- **Bullish Color / Bearish Color** — Full color customization
- **Fill Opacity** — Independent bullish and bearish fill transparency (0–100%)
- **Label Position** — Left or Right

---

## Installation

1. Download the `.cs` file from this repository
2. Open NinjaTrader 8
3. Go to **Tools → Import → NinjaScript Add-On**
4. Select the downloaded file and click **OK**
5. The indicator will appear in your **Indicators** list — add it to any chart

---

## Part of the RedTail Indicators Suite

This indicator is part of the [RedTail Indicators](https://github.com/3astbeast/RedTailIndicators) collection — free NinjaTrader 8 tools built for futures traders who demand precision.

---

<p align="center">
  <a href="https://buymeacoffee.com/dmwyzlxstj">
    <img src="https://img.shields.io/badge/☕_Buy_Me_a_Coffee-Support_My_Work-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" alt="Buy Me a Coffee"/>
  </a>
</p>
