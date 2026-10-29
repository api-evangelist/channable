# Channable

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

Channable is a feed management and marketplace integration platform that helps online retailers, brands, and agencies optimize, distribute, and advertise their product data across more than 2,500 marketing channels, price comparison sites, affiliate networks, and online marketplaces. Beyond feed optimization and PPC ad automation, Channable operates an order-connection layer that synchronizes orders, shipments, stock, and returns between marketplaces and a seller's ERP, WMS, or e-commerce platform. The Channable order connection API (v1) exposes this layer programmatically: retailers and platform integrators can retrieve orders and returns, post shipment and cancellation updates, push stock/offer updates to every connected marketplace at once, upload order attachments, resolve standardized transporter codes, and pull order statistics. Authentication is a company-level bearer token, requests are rate limited per company with a leaky-bucket policy, and a Channable Sandbox connection lets integrators test order flows without touching live marketplaces.

**Areas:** Company · Applicative Saas · Feed Management · Marketplace · E-Commerce · Product Data · Order Management · Advertising · PPC · Retail

## Channable on APIs.io

Everything profiled for Channable is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/channable/](https://apis.io/providers/channable/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Channable Order Attachments API](https://apis.io/apis/channable/channable-order-attachments-api/) — The order_attachments API from Channable — 2 operation(s) for order_attachments.
- [Channable Orders API](https://apis.io/apis/channable/channable-orders-api/) — The orders API from Channable — 10 operation(s) for orders.
- [Channable Returns API](https://apis.io/apis/channable/channable-returns-api/) — The returns API from Channable — 5 operation(s) for returns.
- [Channable Statistics API](https://apis.io/apis/channable/channable-statistics-api/) — The statistics API from Channable — 2 operation(s) for statistics.
- [Channable Stock Updates API](https://apis.io/apis/channable/channable-stock-updates-api/) — The stock_updates API from Channable — 2 operation(s) for stock_updates.
- [Channable Transporters API](https://apis.io/apis/channable/channable-transporters-api/) — The transporters API from Channable — 3 operation(s) for transporters.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [channable](https://apis.io/servers/channable/channable/)

#### Collections (6)

Postman and Open Collection request collections.

- [Channable order connection order_attachments API](https://apis.io/collections/channable/open-channable-order-attachments-api/)
- [Channable order connection order_attachments orders API](https://apis.io/collections/channable/open-channable-orders-api/)
- [Channable order connection order_attachments returns API](https://apis.io/collections/channable/open-channable-returns-api/)
- [Channable order connection order_attachments statistics API](https://apis.io/collections/channable/open-channable-statistics-api/)
- [Channable order connection order_attachments stock_updates API](https://apis.io/collections/channable/open-channable-stock-updates-api/)
- [Channable order connection order_attachments transporters API](https://apis.io/collections/channable/open-channable-transporters-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Channable Order Connection Overlay](https://apis.io/overlays/channable/channable-order-connection-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Channable Authentication](https://apis.io/security/channable/channable-authentication/)
- [Channable Domain Security](https://apis.io/security/channable/channable-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Channable Plans Pricing](https://apis.io/plans/channable/channable-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Channable Rate Limits](https://apis.io/rate-limits/channable/channable-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.channable.com/)
- [Documentation](https://docs.channable.com/api/v1/)
- [Getting started](https://helpcenter.channable.com/hc/en-us/articles/360011209639-Using-the-Channable-API-for-an-order-connection)
- [API reference](https://api.channable.com/v1/docs)
- [Pricing](https://www.channable.com/pricing)
- [Sign up](https://app.channable.com/)
- [Support](https://support.channable.com/)
- [Changelog](https://helpcenter.channable.com/changelog/)
- [Blog](https://www.channable.com/blog)
- [Terms of service](https://www.channable.com/terms-and-conditions)
- [Privacy policy](https://www.channable.com/privacy-policy)
- [GitHub](https://github.com/channable)
- [Status](https://www.channablestatus.com/)

## API Evangelist rating

**Kin Score 49.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 41.6 |
| Contract governance | 4.5 |
| Operational transparency | 63.2 |
| Developer ergonomics | 67.3 |
| Access clarity | 47.4 |

**Agent readiness 27.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 20.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/channable/](https://apis.io/providers/channable/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Channable: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/channable/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
