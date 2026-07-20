---
name: Query Summerland Bank product reference data
description: >-
  Retrieve Summerland Bank's publicly published banking products and their fees,
  rates and eligibility via the Consumer Data Right (CDR) Product Reference Data
  API — a public, unauthenticated surface. Use to compare accounts, term
  deposits, mortgages, personal/business loans, overdrafts and cards.
api: openapi/summerland-bank-cds-banking-products-openapi.yml
base_url: https://public.cdr-api.summerland.com.au/cds-au/v1
auth: none (public PRD — no key or token required)
operations:
  - listBankingProducts
  - getBankingProductDetail
---

# Query Summerland Bank product reference data

Summerland Bank exposes its product catalogue through the shared CDR Banking API.
These two operations are **public and unauthenticated** — no API key, OAuth token,
or CDR accreditation is required. Every request MUST carry the CDS version header.

## Prerequisites

- Base URL: `https://public.cdr-api.summerland.com.au/cds-au/v1`
- Required header on every call: `x-v: 5` (omitting it returns HTTP 406).
- No credentials.

## Step 1 — List products (`listBankingProducts`)

`GET /banking/products` with header `x-v: 5`.

Optional query parameters:
- `product-category` — filter to one category (e.g. `TRANS_AND_SAVINGS_ACCOUNTS`,
  `TERM_DEPOSITS`, `RESIDENTIAL_MORTGAGES`, `PERS_LOANS`, `BUSINESS_LOANS`,
  `OVERDRAFTS`, `CRED_AND_CHRG_CARDS`).
- `effective` — `CURRENT` (default), `FUTURE`, or `ALL`.
- `updated-since` — ISO 8601 datetime to fetch only recently changed products.
- `page`, `page-size` — 1-based pagination (`page-size` max 1000).

Read `data.products[]` for each product's `productId`, `name`, `productCategory`
and `brand`. Read `meta.totalRecords` / `meta.totalPages` and `links.next` to
page through results.

## Step 2 — Get product detail (`getBankingProductDetail`)

For any `productId` from Step 1, call
`GET /banking/products/{productId}` with header `x-v: 5`.

The `data` object returns full detail: `features`, `constraints`, `eligibility`,
`fees` (with nested `discounts`), and `depositRates` / `lendingRates` (with
`rateTiers`). A missing/invalid `productId` returns HTTP 404.

## Conventions and errors

- Versioning: send `x-v: 5`; the response echoes the served version in its `x-v`
  header. Unsupported/missing version → HTTP 406.
- Pagination: `page` / `page-size`; an out-of-range page → HTTP 422.
- Errors use the CDS `ResponseErrorListV2` envelope
  (`{ errors: [ { code, title, detail, meta } ] }`), URN-coded — not RFC 9457.
  See `errors/summerland-bank-problem-types.yml`.
- This surface is read-only; there is no idempotency or write contract.

## Out of scope

Account, balance, transaction, direct-debit, scheduled-payment and payee data are
**not** available here — they require ACCC-accredited data-recipient status and a
consumer's CDR consent (OAuth2/OIDC/MTLS), and are accessed through the Summerland
Bank app / internet banking, not this public API.
