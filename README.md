# ThetaData

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ThetaData is a developer-first US market data vendor founded in 2022 by Bailey Danseglio, selling real-time and historical options, stocks, indices, and interest-rates data with unfiltered tick-level trades, quotes, and Greeks. Delivery is self-serve via the Theta Terminal, a local Java application that authenticates with an API key or account credentials and exposes a local REST API (127.0.0.1:25503/v3), a WebSocket streaming API (127.0.0.1:25520), and an MCP server, backed by a published OpenAPI 3.1 spec, Python library, flat files, and tiered monthly subscriptions.

**Areas:** Finance · Market Data · Options · Stocks · Indices · Real-Time · Historical Data · Trading

## ThetaData on APIs.io

Everything profiled for ThetaData is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/thetadata/](https://apis.io/providers/thetadata/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [ThetaData Streaming WebSocket API](https://apis.io/apis/thetadata/thetadata-streaming-websocket-api/) — JSON WebSocket streaming of US stock trade/quote, options trade/quote, and index price streams, served locally by the Theta Terminal at…
- [ThetaData MCP Server](https://apis.io/apis/thetadata/thetadata-mcp-server/) — Model Context Protocol server built into Theta Terminal v3, exposing the full v3 API to LLM CLIs (documented for Claude CLI and Gemini CLI) over SSE at…
- [ThetaData Calendar API](https://apis.io/apis/thetadata/thetadata-calendar-api/) — The Calendar API from ThetaData — 3 operation(s) for calendar.
- [ThetaData Index API](https://apis.io/apis/thetadata/thetadata-index-api/) — The Index API from ThetaData — 10 operation(s) for index.
- [ThetaData Interest Rate API](https://apis.io/apis/thetadata/thetadata-interest-rate-api/) — The Interest Rate API from ThetaData — 1 operation(s) for interest rate.
- [ThetaData Option API](https://apis.io/apis/thetadata/thetadata-option-api/) — The Option API from ThetaData — 37 operation(s) for option.
- [ThetaData Stock API](https://apis.io/apis/thetadata/thetadata-stock-api/) — The Stock API from ThetaData — 15 operation(s) for stock.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [ThetaData Streaming WebSocket API (derived)](https://apis.io/asyncapis/thetadata/thetadata-streaming-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/v1/events](https://apis.io/channels/thetadata/v1-events/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [thetadata](https://apis.io/servers/thetadata/thetadata/)

#### Collections (24)

Postman and Open Collection request collections.

- [Theta Data v3 At-Time API](https://apis.io/collections/thetadata/open-thetadata-at-time-api/)
- [Theta Data v3 At-Time Calendar API](https://apis.io/collections/thetadata/open-thetadata-calendar-api/)
- [Theta Data v3 At-Time FlatFile API](https://apis.io/collections/thetadata/open-thetadata-flatfile-api/)
- [Theta Data v3 At-Time History API](https://apis.io/collections/thetadata/open-thetadata-history-api/)
- [Theta Data v3 At-Time Index API](https://apis.io/collections/thetadata/open-thetadata-index-api/)
- [Theta Data v3 At-Time Interest Rate API](https://apis.io/collections/thetadata/open-thetadata-interest-rate-api/)
- [Theta Data v3 At-Time List API](https://apis.io/collections/thetadata/open-thetadata-list-api/)
- [Theta Data v3 At-Time Option API](https://apis.io/collections/thetadata/open-thetadata-option-api/)
- [Theta Data v3 At-Time Single Day API](https://apis.io/collections/thetadata/open-thetadata-single-day-api/)
- [Theta Data v3 At-Time Snapshot API](https://apis.io/collections/thetadata/open-thetadata-snapshot-api/)
- [Theta Data v3 At-Time Stock API](https://apis.io/collections/thetadata/open-thetadata-stock-api/)
- [Theta Data v3 At-Time Year API](https://apis.io/collections/thetadata/open-thetadata-year-api/)
- [Theta Data v3 At-Time API](https://apis.io/collections/thetadata/postman-thetadata-at-time-api/)
- [Theta Data v3 At-Time Calendar API](https://apis.io/collections/thetadata/postman-thetadata-calendar-api/)
- [Theta Data v3 At-Time FlatFile API](https://apis.io/collections/thetadata/postman-thetadata-flatfile-api/)
- [Theta Data v3 At-Time History API](https://apis.io/collections/thetadata/postman-thetadata-history-api/)
- [Theta Data v3 At-Time Index API](https://apis.io/collections/thetadata/postman-thetadata-index-api/)
- [Theta Data v3 At-Time Interest Rate API](https://apis.io/collections/thetadata/postman-thetadata-interest-rate-api/)
- [Theta Data v3 At-Time List API](https://apis.io/collections/thetadata/postman-thetadata-list-api/)
- [Theta Data v3 At-Time Option API](https://apis.io/collections/thetadata/postman-thetadata-option-api/)
- [Theta Data v3 At-Time Single Day API](https://apis.io/collections/thetadata/postman-thetadata-single-day-api/)
- [Theta Data v3 At-Time Snapshot API](https://apis.io/collections/thetadata/postman-thetadata-snapshot-api/)
- [Theta Data v3 At-Time Stock API](https://apis.io/collections/thetadata/postman-thetadata-stock-api/)
- [Theta Data v3 At-Time Year API](https://apis.io/collections/thetadata/postman-thetadata-year-api/)

#### Overlays (12)

OpenAPI overlays, including conversational phrasing for each operation.

- [Thetadata At Time Api Overlay](https://apis.io/overlays/thetadata/thetadata-at-time-api-overlay/)
- [Thetadata Calendar Api Overlay](https://apis.io/overlays/thetadata/thetadata-calendar-api-overlay/)
- [Thetadata Flatfile Api Overlay](https://apis.io/overlays/thetadata/thetadata-flatfile-api-overlay/)
- [Thetadata History Api Overlay](https://apis.io/overlays/thetadata/thetadata-history-api-overlay/)
- [Thetadata Index Api Overlay](https://apis.io/overlays/thetadata/thetadata-index-api-overlay/)
- [Thetadata Interest Rate Api Overlay](https://apis.io/overlays/thetadata/thetadata-interest-rate-api-overlay/)
- [Thetadata List Api Overlay](https://apis.io/overlays/thetadata/thetadata-list-api-overlay/)
- [Thetadata Option Api Overlay](https://apis.io/overlays/thetadata/thetadata-option-api-overlay/)
- [Thetadata Single Day Api Overlay](https://apis.io/overlays/thetadata/thetadata-single-day-api-overlay/)
- [Thetadata Snapshot Api Overlay](https://apis.io/overlays/thetadata/thetadata-snapshot-api-overlay/)
- [Thetadata Stock Api Overlay](https://apis.io/overlays/thetadata/thetadata-stock-api-overlay/)
- [Thetadata Year Api Overlay](https://apis.io/overlays/thetadata/thetadata-year-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Thetadata Authentication](https://apis.io/security/thetadata/thetadata-authentication/)
- [Thetadata Domain Security](https://apis.io/security/thetadata/thetadata-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Thetadata Plans](https://apis.io/plans/thetadata/thetadata-plans/)

#### Rate limits (1)

Published request limits.

- [Thetadata Rate Limits](https://apis.io/rate-limits/thetadata/thetadata-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://thetadata.net/)
- [Documentation](https://docs.thetadata.us/)
- [Getting started](https://docs.thetadata.us/Articles/Getting-Started/Getting-Started.html)
- [API reference](https://docs.thetadata.us/)
- [Pricing](https://thetadata.net/pricing)
- [Sign up](https://thetadata.net/signup)
- [Support](https://discord.thetadata.us/)
- [Blog](https://thetadata.net/blog)
- [Terms of service](https://thetadata.net/terms-and-conditions)
- [Privacy policy](https://thetadata.net/privacy-policy)
- [GitHub](https://github.com/AXIOMXLLC)
- [Status](https://thetadata.statuspage.io/)

## API Evangelist rating

**Kin Score 59.9** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 48.2 |
| Contract governance | 4.5 |
| Operational transparency | 78.9 |
| Developer ergonomics | 69.6 |
| Access clarity | 76.3 |

**Agent readiness 30.3** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 28.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/thetadata/](https://apis.io/providers/thetadata/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ThetaData: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/thetadata/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
