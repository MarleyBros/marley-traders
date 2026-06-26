# Marley Traders

**Institutional-grade market intelligence platform for professional day traders.**

🌐 **Live:** [marleytraders.com](https://marleytraders.com)

---

## Overview

Marley Traders is a real-time market intelligence workstation built for the independent professional trader. The platform continuously analyses 16 instruments across FX, US indices, gold, and DXY — delivering confluence-based signals, session context, and voice alerts without requiring manual chart reading.

The core design principle: within 30 seconds of opening the platform, the trader knows what is happening, what to focus on, and why it matters.

---

## Platform Capabilities

- **Multi-instrument intelligence** — continuous analysis across EURUSD, GBPUSD, USDJPY, USDCHF, EURCAD, GBPCAD, EURJPY, GBPJPY, CADJPY, USDCAD, SPX500, NDQ100, US30, US2000, XAUUSD, DXY
- **Session-based context** — London Kill Zone, New York Reversal, Asia Reversal, and all major ICT session windows
- **T-Rex oscillator cascade** — proprietary multi-timeframe momentum engine across 1m, 5m, 15m, 1h, 4h, 1D
- **Level monitoring** — real-time price approach and tap detection for trader-defined key levels
- **Correlation & divergence engine** — group divergence, SMT divergence, and inter-market analysis
- **Voice intelligence layer** — institutional-quality voice alerts (Lisa) triggered only on high-conviction setups
- **Agent-based architecture** — 10 independent agents running concurrently via async event bus

---

## Stack

| Layer | Technology |
|---|---|
| Intelligence Engine | Python 3.10, asyncio |
| API Bridge | FastAPI, uvicorn |
| Frontend | React, Next.js, TypeScript |
| Database | Supabase (PostgreSQL) |
| Live Data | MetaAPI (Eightcap MT5 broker connection) |
| Voice | ElevenLabs TTS |
| Event Bus | Redis (production), FastAPI (local) |
| Deployment | Docker, Vultr VPS (Frankfurt) |

---

## Architecture

The platform runs as a multi-agent system. Each agent operates independently and communicates via a central event bus:

- **Session Agent** — trading session clock and window detection
- **T-Rex Agent** — oscillator engine and state cascade across all instruments and timeframes
- **Correlation Agent** — group divergence and SMT detection
- **Market Watcher** — level monitoring and price approach detection
- **Level Context Agent** — confluence scoring and grade assignment (B+ / A / A+ / A++)
- **Lisa** — voice synthesis layer, speaks only on A-grade setups and above
- **TS3 Agent** — market structure analysis
- **Supabase Loader** — real-time level synchronisation
- **Reminder Engine** — session pre-alerts
- **API Bridge** — FastAPI server bridging engine events to the web terminal

---

## Status

Platform in active private development. Running 24/7 in production on Vultr VPS (Frankfurt).

Public access opening soon — join the waitlist at [marleytraders.com](https://marleytraders.com)

---

## Company

Marley Consulting & Mentorship Ltd — registered company.  
© 2026 Marley Consulting & Mentorship Ltd. All rights reserved. Proprietary software.
