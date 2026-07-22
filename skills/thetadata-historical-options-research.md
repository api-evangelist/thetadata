---
name: Pull historical option data for research or backtesting
description: >-
  Retrieve historical EOD, tick, and Greeks series for an option contract from
  the ThetaData v3 local API, sized to avoid LARGE_REQUEST errors.
api: openapi/thetadata-option-api-openapi.yml
operations: [option_list_expirations, option_history_eod, option_history_trade, option_history_greeks_eod]
generated: '2026-07-22'
method: generated
---

# Pull historical option data for research or backtesting

Prereqs: Theta Terminal v3 running and authenticated, or the Python library
(`pip install thetadata`, `client = ThetaClient()` — no terminal needed).
Base URL: `http://127.0.0.1:25503/v3`.

## Steps

1. **Find contract expirations** — `option_list_expirations`
   `GET /option/list/expirations?symbol=SPXW`
2. **Daily series first** — `option_history_eod`
   `GET /option/history/eod?symbol=SPXW&expiration=2026-06-19&strike=6000&right=call&start_date=2026-05-01&end_date=2026-05-31`
   EOD/1-month ranges are safe; EOD data goes back to 2012-06-01.
3. **Tick-level trades where needed** — `option_history_trade`
   `GET /option/history/trade?symbol=SPXW&expiration=2026-06-19&strike=6000&right=call&start_date=2026-05-28&end_date=2026-05-28`
   Keep tick requests to ~1 week (1 day for liquid tickers like AAPL/SPX/SPY);
   responses should stay under ~1M ticks or you get 570 LARGE_REQUEST.
4. **Greeks over time** — `option_history_greeks_eod`
   `GET /option/history/greeks/eod?symbol=SPXW&expiration=2026-06-19&strike=6000&right=call&start_date=2026-05-01&end_date=2026-05-31`
   For symbols without stored underlying history (e.g. NDX before
   2026-05-11), pass `stock_price` to supply the underlying price.

## Rules

- GET-only, idempotent, retry-safe; no pagination — control size with date
  ranges (`conventions/thetadata-conventions.yml`).
- 472 NO_DATA is a normal outcome for illiquid contracts/dates, not a failure.
- `format=csv|json|ndjson`; `json_new` groups rows by contract.
- Tier gates history depth (VALUE 4y / STANDARD 8y / PRO 12y for options);
  471 PERMISSION means the tier does not cover the request.
