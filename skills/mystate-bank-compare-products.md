---
name: Compare MyState Bank banking products
description: >-
  Fetch MyState Bank's publicly offered banking products and drill into a single
  product's fees, rates, features and eligibility using the unauthenticated CDR
  Product Reference Data API. Read-only, no credentials required.
api: openapi/mystate-bank-cds-banking-products-openapi.yml
operations:
- listProducts
- getProductDetail
---

# Compare MyState Bank banking products

Use the MyState Bank CDR Product Reference Data (PRD) API to list and compare the
products the bank openly offers. The API is **public and unauthenticated** — no
API key or OAuth token. Base URL: `https://public.cdr.mystate.com.au/cds-au/v1`.

## Conventions you must follow

- **Version header (required):** send `x-v: 3` on every request. The response
  echoes the served version in the `x-v` header.
- **No auth:** do not send any Authorization header.
- **Pagination:** `list` responses page via `page` / `page-size` (default 25),
  with `links` (self/first/prev/next/last) and `meta.totalRecords` /
  `meta.totalPages`.

## Steps

1. **List products** — call `listProducts` (`GET /banking/products`) with header
   `x-v: 3`. Optionally filter with `product-category` (e.g. `TRANS_AND_SAVINGS_ACCOUNTS`,
   `RESIDENTIAL_MORTGAGES`, `TERM_DEPOSITS`), `effective` (`CURRENT` | `FUTURE` | `ALL`),
   `brand`, or `updated-since`. Read `data.products[]`; each item has `productId`,
   `name`, `productCategory`, `brand` and `description`.
2. **Page through** if `meta.totalPages > 1`, incrementing `page` until you have
   the full set (or the categories you care about).
3. **Get product detail** — for a chosen `productId`, call `getProductDetail`
   (`GET /banking/products/{productId}`) with header `x-v: 3`. The `data` object
   adds `fees[]`, `depositRates[]`, `lendingRates[]`, `features[]`,
   `eligibility[]`, `constraints[]` and `bundles[]`.
4. **Compare** — line up `depositRates[].rate` / `lendingRates[].rate` (and
   `comparisonRate`), `fees[].amount`, and `eligibility[]` across the products
   you retrieved. Rate tiers live under `depositRates[].tiers[]` /
   `lendingRates[].tiers[]`.

## Notes

- This is a read-only surface; there are no mutating operations and no idempotency
  contract. Re-run freely.
- Errors follow the CDS `ResponseErrorListV2` envelope (`errors[]` of
  `{code, title, detail}`). A missing/invalid `x-v` header is the most common cause
  of a non-200 response.
