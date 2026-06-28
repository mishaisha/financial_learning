# Financial Literacy Study Plan

Self-contained, multi-phase financial literacy curriculum with interactive tools. Built as static HTML — no server, no build step, no dependencies.

**Live:** https://mishaisha.github.io/financial_learning/

## Phases

| Phase | File | Duration | Focus |
|-------|------|----------|-------|
| 1: Basics | `basics.html` | 4 weeks (28 days) | Stocks, bonds, ETFs, FA/TA, risk, DCA, behavioral, portfolio construction |
| 2: Portfolio & Trading | `portfolio-trading.html` | 2 weeks (14 days) | MPT, asset allocation, options, hedging, execution |
| 3: Stock Research & Trading | `stock-trading.html` | 2 weeks (14 days) | Screening, deep-dive, moat, entry/exit, journal, psychology |

Each phase has an accordion-based day-by-day lesson plan with localStorage progress tracking and per-week interactive quizzes (8 weeks × 6 questions = 48 total).

## Tools

### Paper Trading Simulator (`trading-simulator.html`)
Practice trading with $100K virtual money. Simulated market of 20 stocks with daily price moves via lognormal random walk.

- **Trade** — buy/sell at current simulated prices, market table with filter + quick-trade buttons
- **Portfolio** — holdings with avg cost, market value, P&L
- **Dashboard** — account stats, equity curve chart (Chart.js), recent trades
- **History** — full trade log with timestamps
- **Next Day** — advances the simulation
- **localStorage** — persist portfolio across sessions

### Invest Agent (`invest-agent.html`)
Portfolio co-pilot for planning and analysis.

- **Risk assessment quiz** — 5 questions → risk profile (Conservative to Aggressive)
- **Target allocation** — suggested asset mix per risk profile
- **Holdings CRUD** — track tickers, quantity, cost basis, current price
- **Portfolio dashboard** — total value, gain/loss, allocation bar chart
- **Rebalance view** — current vs target allocation with buy/sell actions
- **Stock research copilot** — 5-step wizard (screening → financials → moat → management → thesis)
- **Pre-trade decision checker** — position size, stop-loss, bias check → GO/CAUTION/NO verdict
- **Trade journal** — log trades with notes

## Features

- **Self-contained** — all HTML, CSS, JS inline; no server required
- **Progress tracking** — click day cards to mark complete; stored in localStorage
- **Completion banners** — phase 1 unlocks phase 2 at 28/28; phase 2 unlocks phase 3 at 14/14
- **Sticky sidebar** — collapsible week navigation on all phases
- **Dark theme** — simulator uses a dark theme; phases use light theme
- **Dynamic timestamps** — last-updated fetched from GitHub API

## Usage

Open `index.html` in any browser, or deploy to any static host (GitHub Pages, Netlify, etc.).

No build step, no npm install, no API keys required.

## Tech Stack

- Vanilla HTML / CSS / JS
- Chart.js (CDN) for charts
- localStorage for persistence
- GitHub API for dynamic timestamps
