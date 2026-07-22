---
name: Snapshot a live option chain with Greeks
description: >-
  Discover an underlying's option chain (expirations and strikes) and pull
  real-time quote and Greeks snapshots for it from the ThetaData v3 local API.
api: openapi/thetadata-option-api-openapi.yml
operations: [option_list_expirations, option_list_strikes, option_snapshot_quote, option_snapshot_greeks_all]
generated: '2026-07-22'
method: generated
---

# Snapshot a live option chain with Greeks

Prereqs: Theta Terminal v3 running and authenticated (API key or creds — see
`authentication/thetadata-authentication.yml`); an options subscription tier
that includes snapshots (VALUE+ for quotes, see `plans/thetadata-plans.yml`).
Base URL: `http://127.0.0.1:25503/v3`.

## Steps

1. **List expirations** — `option_list_expirations`
   `GET /option/list/expirations?symbol=AAPL`
2. **List strikes for one expiration** — `option_list_strikes`
   `GET /option/list/strikes?symbol=AAPL&expiration=2026-08-21`
3. **Snapshot quotes for the chain** — `option_snapshot_quote`
   `GET /option/snapshot/quote?symbol=AAPL&expiration=2026-08-21&strike=*&right=call&format=json`
   Use `*` wildcards for `expiration`/`strike` to pull the whole chain in one
   request; there is no pagination.
4. **Snapshot all Greeks** — `option_snapshot_greeks_all`
   `GET /option/snapshot/greeks/all?symbol=AAPL&expiration=2026-08-21&strike=*&right=call&format=json`

## Rules

- All operations are GET and idempotent — retry freely on 429 OS_LIMIT and
  571 SERVER_STARTING (`conventions/thetadata-conventions.yml`).
- Handle 471 PERMISSION (tier too low), 472 NO_DATA, and 474 DISCONNECTED
  explicitly (`errors/thetadata-problem-types.yml`).
- `right` is `call`/`put`; `strike` is a float in dollars; dates accept
  `YYYY-MM-DD`, `YYYYMMDD`, or `*`.
- Stay within the account-wide concurrency limit (1/2/4/8 by tier); use one
  consistent host form — never mix `127.0.0.1` and `localhost` (476 WRONG_IP).
