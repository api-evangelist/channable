---
name: Fulfill Channable marketplace orders
description: Retrieve new marketplace orders from Channable and report shipment (or cancellation) back so the marketplace and buyer are updated.
api: openapi/channable-order-connection-openapi.json
operations:
- all_orders_v2_v2_companies__company_id__projects__project_id__orders_get
- single_order_v2_v2_companies__company_id__projects__project_id__orders__order_id__get
- shipment_companies__company_id__projects__project_id__orders__order_id__shipment_post
- cancellation_companies__company_id__projects__project_id__orders__order_id__cancel_post
---

# Fulfill Channable marketplace orders

Use the Channable order connection API to pull orders and push fulfillment updates.

## Auth & setup
- Base URL: `https://api.channable.com/v1`.
- Send the company API token: `Authorization: Bearer <token>` (or `?access_token=<token>`).
- All order paths are scoped `/companies/{company_id}/projects/{project_id}/...`; get `company_id` and `project_id` from app.channable.com.
- Respect the rate limit: 2 req/s, burst 100, per company (leaky bucket).

## Steps
1. **List new orders** — `GET /v2/companies/{company_id}/projects/{project_id}/orders` (operationId `all_orders_v2...`). Page with `offset`/`limit` (default 15, max 100). Prefer the v2 endpoints; the v1 order reads are deprecated.
2. **Read one order** — `GET /v2/.../orders/{order_id}` (`single_order_v2...`) to get items, addresses, and current status/events.
3. **Report shipment** — `POST /.../orders/{order_id}/shipment` (`shipment...`) with the tracking info and a standardized transporter code (resolve via the transporters endpoints). A 409 means the order is not in a shippable state; a 404 means the order id is unknown.
4. **Cancel when needed** — `POST /.../orders/{order_id}/cancel` (`cancellation...`) to mark an order cancelled. 409 signals an incompatible state.

## Rules
- Errors are `{ "status": "error", "message": ... }`; 401 uses `error` instead of `message`; 422 returns `HTTPValidationError` with `detail[]`. See errors/channable-problem-types.yml.
- No idempotency key exists — before retrying a shipment/cancel, re-read the order and check its status to avoid duplicate transitions (409).
