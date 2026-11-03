# 2026 Senate Control Tracker

A single-file, interactive election-night tracker for control of the U.S. Senate in 2026.

- Check off Democratic pickups (7 Republican-held seats) and Democratic defenses (3 seats) as races are called, or play out scenarios.
- The seat count, net pickups, and majority status update live. Starting balance is 47 D (incl. 2 independents) – 53 R; 51 seats are needed for a Democratic majority (the VP breaks 50–50 ties).
- Selections are saved in your browser (`localStorage`) and can be shared via **Copy scenario link** (`?f=NC,OH&h=MI,GA,NH`).
- Each race shows a Kalshi prediction-market snapshot. **Refresh Live Odds** fetches current prices through a public CORS proxy, falling back to Adjacent's ~15-minute-delayed public API.

## Usage

Open `index.html` in a browser — no build step or dependencies. It can also be hosted as-is on GitHub Pages.

## Editing races

Each race is one `<label class="race">` row in `index.html`. The state lists, counters, and refresh logic are all derived from those rows, so adding or removing a race only requires editing the markup (state key, Kalshi ticker, candidates, snapshot odds).

Probabilities are market prices, not vote counts.
