# Trading Monitor (Dashboard UI)

Wireframe-ready README + structure for a trading monitor / trading dashboard UI.

## Why this layout
* Keep critical market context visible at all times (price, positions, risk)
* Minimize mode switching while placing orders
* Make the data hierarchy predictable: **watchlist → instrument → orders/positions → chart**

## Wireframe layout

```
[Top bar: brand | env/time | search/ticker picker | notifications | user]

┌──────────────────────────────────────────────────────────────┐
│ NAV (watchlists/accounts) │ Main workspace (tabs)             │
│ - Watchlist A             │ - Summary cards (P&L/exposure)    │
│ - Watchlist B             │ - Trade blotter (open orders)     │
│ - Account selector        │ - Positions / risk table          │
│                           │ - Chart + depth view placeholder  │
└──────────────────────────────────────────────────────────────┘

[Bottom status/log: connection state, last update, system messages]
```

## Regions

1) **Top navigation (global)**
- brand/project name
- instrument search / quick ticker picker
- time zone display + clock
- connectivity indicator
- notifications / user menu

2) **Left navigation panel**
- watchlists (multi list)
- account selector (accounts/portfolios)
- filter buttons (e.g., Asset class, active orders, favorites)

3) **Main workspace (tabbed)**
- Tab: `Trading`
  - summary cards (equity, P&L, margin)
  - blotter table (orders)
  - positions table + risk metrics
  - chart panel with depth view placeholder
  - order ticket drawer (inline panel)
- Tab: `Risk`
  - exposure breakdown
  - risk limits
  - concentration map
- Tab: `Settings`
  - UI prefs
  - data source config

4) **Bottom status/log**
- event log (fills, cancel, rejects)
- system messages (latency, feed status)

## This repo (wireframe-ready)
- `README.md` (this file)
- `index.html` (Cigma-like skeleton markup)
- `styles/` + `scripts/` directories reserved for next iteration

## Next iteration ideas
- add Tailwind or CSS utility layer
- data table component for blotter/positions
- charting (lightweight placeholder first)
- connect to mocked data feed
