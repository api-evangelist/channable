---
name: Process Channable returns
description: Retrieve marketplace returns from Channable and update their status as they are received, accepted, or rejected.
api: openapi/channable-order-connection-openapi.json
operations:
- all_returns_companies__company_id__projects__project_id__returns_get
- single_return_companies__company_id__projects__project_id__returns__return_id__get
- update_return_status_companies__company_id__projects__project_id__returns__return_id__status_post
---

# Process Channable returns

Handle marketplace returns end to end through the Channable order connection API.

## Auth & setup
- Base URL `https://api.channable.com/v1`; `Authorization: Bearer <token>`.
- Paths scoped `/companies/{company_id}/projects/{project_id}/...`.

## Steps
1. **List returns** — `GET /.../returns` (operationId `all_returns...`). Page with `offset`/`limit`.
2. **Read one return** — `GET /.../returns/{return_id}` (`single_return...`) for items, addresses, and current status.
3. **Update return status** — `POST /.../returns/{return_id}/status` (`update_return_status...`) to move the return forward (e.g. received/accepted/rejected). A 409 means the requested status transition conflicts with the current state.

## Test first
- Use the sandbox: `POST /.../returns/test` (`create_test_return...`) creates a test return you can then read and transition. See sandbox/channable-sandbox.yml.

## Rules
- Errors follow the standard `{status,message}` envelope; 422 is `HTTPValidationError` with `detail[]`. See errors/channable-problem-types.yml.
- No idempotency key — re-read the return before retrying a status update to avoid a 409.
