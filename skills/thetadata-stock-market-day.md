---
name: Read a stock's market day (calendar, history, live snapshot)
description: >-
  Check the trading calendar, pull a stock's recent history, and take a live
  quote snapshot from the ThetaData v3 local API.
api: openapi/thetadata-stock-api-openapi.yml
operations: [stock_list_symbols, stock_history_eod, stock_snapshot_quote]
additional_apis:
  - api: openapi/thetadata-calendar-api-openapi.yml
    operations: [calendar_open_today]
generated: '2026-07-22'
method: generated
---

# Read a stock's market day

Prereqs: Theta Terminal v3 running and authenticated (free tier works for EOD
history). Base URL: `http://127.0.0.1:25503/v3`.

## Steps

1. **Is the market open today?** — `calendar_open_today` (from `openapi/thetadata-calendar-api-openapi.yml`)
   `GET /calendar/today`
2. **Verify the symbol exists** — `stock_list_symbols`
   `GET /stock/list/symbols` (updated overnight; free tier accessible)
3. **Recent end-of-day history** — `stock_history_eod`
   `GET /stock/history/eod?symbol=AAPL&start_date=2026-06-22&end_date=2026-07-22`
   Free tier covers 1 year of EOD with a 20 req/min limit; note UTP-tape
   coverage starts 2012-06-01 but CTA-only symbols (e.g. SPY, GE) start
   2020-01-01.
4. **Live NBBO quote** — `stock_snapshot_quote`
   `GET /stock/snapshot/quote?symbol=AAPL&format=json`
   Requires VALUE+ (15-min delayed) or STANDARD+ (real-time); expect 471
   PERMISSION on free accounts.

## Rules

- GET-only, idempotent, retry-safe (`conventions/thetadata-conventions.yml`).
- Handle 472 NO_DATA and 474 DISCONNECTED; check
  `GET /v3/terminal/mdds/status` when disconnected.
- Use one consistent host form (127.0.0.1 OR localhost) for every request.
