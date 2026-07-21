# ThetaData (thetadata)

ThetaData is a developer-first US market data vendor founded in 2022 by Bailey Danseglio, selling real-time and historical options, stocks, indices, and interest-rates data with unfiltered tick-level trades, quotes, and Greeks. Delivery is self-serve via the Theta Terminal, a local Java application that authenticates with an API key or account credentials and exposes a local REST API (127.0.0.1:25503/v3), a WebSocket streaming API (127.0.0.1:25520), and an MCP server, backed by a published OpenAPI 3.1 spec, Python library, flat files, and tiered monthly subscriptions.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/thetadata/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/thetadata/refs/heads/main/apis.yml)

## Tags

- Financial
- Market Data
- Options
- Stocks
- Indices
- Real-Time
- Historical Data
- Trading

## Timestamps

- **Created:** 2026-07-21
- **Modified:** 2026-07-21

## APIs

### ThetaData v3 REST API

Real-time and historical US options, stocks, and indices data - tick-level trades and quotes, OHLC aggregates, end-of-day summaries, option chain snapshots, and 1st/2nd/3rd order Greeks - served as a local REST API by the Theta Terminal, a Java 21 application that authenticates to ThetaData with an API key or account credentials and proxies data over a proprietary compressed protocol. Responses in CSV, JSON, NDJSON, or HTML; 66 documented endpoints in a published OpenAPI 3.1 spec.

- **Human URL:** [https://docs.thetadata.us/](https://docs.thetadata.us/)
- **Base URL:** `http://127.0.0.1:25503/v3` (local Theta Terminal)

#### Tags

- Options
- Stocks
- Indices
- Historical Data
- Snapshots

#### Properties

- [Documentation](https://docs.thetadata.us/Articles/Getting-Started/Getting-Started.html)
- [API Reference](https://docs.thetadata.us/operations/stock_list_symbols.html)
- [OpenAPI](openapi/thetadata-v3-openapi.yml) — harvested verbatim from [https://docs.thetadata.us/openapiv3.yaml](https://docs.thetadata.us/openapiv3.yaml)

### ThetaData Streaming WebSocket API

JSON WebSocket streaming of US stock trade/quote, options trade/quote, and index price streams, served locally by the Theta Terminal at `ws://127.0.0.1:25520/v1/events`. Requires a paid subscription with streaming permissions; a single connection per user is permitted, with CONNECTED/DISCONNECTED status headers and QUOTE/TRADE/STATUS message types.

- **Human URL:** [https://docs.thetadata.us/Streaming/Getting-Started.html](https://docs.thetadata.us/Streaming/Getting-Started.html)
- **Base URL:** `ws://127.0.0.1:25520/v1/events` (local Theta Terminal)

#### Tags

- Streaming
- WebSocket
- Trades
- Quotes
- Real-Time

#### Properties

- [Documentation](https://docs.thetadata.us/Streaming/Getting-Started.html)

### ThetaData MCP Server

Model Context Protocol server built into Theta Terminal v3, exposing the full v3 API to LLM CLIs (documented for Claude CLI and Gemini CLI) over SSE at `http://127.0.0.1:25503/mcp/sse`. Requires the terminal running locally and a valid ThetaData subscription.

- **Human URL:** [https://docs.thetadata.us/Mcp/Getting-Started.html](https://docs.thetadata.us/Mcp/Getting-Started.html)
- **Base URL:** `http://127.0.0.1:25503/mcp/sse` (local Theta Terminal)

#### Tags

- MCP
- Agents
- SSE

#### Properties

- [Documentation](https://docs.thetadata.us/Mcp/Getting-Started.html)

## Common Properties

- [Website](https://thetadata.net/)
- [Portal](https://thetadata.net/portal)
- [Documentation](https://docs.thetadata.us/)
- [Blog](https://thetadata.net/blog)
- [Pricing](https://thetadata.net/pricing)
- [Sign Up](https://thetadata.net/signup)
- [Terms of Service](https://thetadata.net/terms-and-conditions)
- [Privacy Policy](https://thetadata.net/privacy-policy)
- [Support (Discord)](https://discord.thetadata.us/)
- [Status Page](https://thetadata.statuspage.io/)
- [LinkedIn](https://www.linkedin.com/company/axiomx-theta-data)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
