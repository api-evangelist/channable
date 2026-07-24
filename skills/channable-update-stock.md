---
name: Update Channable stock and offers
description: Push stock, price, and offer updates to all connected marketplaces at once through Channable, and read current offers.
api: openapi/channable-order-connection-openapi.json
operations:
- get_stock_updates_companies__company_id__projects__project_id__offers_get
- stock_updates_update_companies__company_id__projects__project_id__stock_updates_post
---

# Update Channable stock and offers

Keep marketplace listings in sync by pushing stock/price updates through Channable.

## Auth & setup
- Base URL `https://api.channable.com/v1`; `Authorization: Bearer <token>`.
- Paths scoped `/companies/{company_id}/projects/{project_id}/...`.
- Rate limit 2 req/s, burst 100 per company; batch updates rather than sending one call per SKU.

## Steps
1. **Read current offers** — `GET /.../offers` (operationId `get_stock_updates...`) to see current stock/price per offer. Page with `offset`/`limit`.
2. **Push stock updates** — `POST /.../stock_updates` (`stock_updates_update...`) with the batch of offer updates (stock, price, title). This is the current endpoint; the legacy `POST /.../offers` (`Stock_Updates_Update__deprecated...`) is deprecated — do not use it.
3. Handle responses: 202 accepted for async processing, 413 if the payload is too large (split the batch), 400/422 for invalid items, 401 for a bad token.

## Rules
- One `stock_updates` call fans out to every connected marketplace for the project.
- No idempotency key — a repeated update overwrites; ensure your payload reflects the desired end state.
- See conventions/channable-conventions.yml and errors/channable-problem-types.yml.
