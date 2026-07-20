---
name: Hume Bank product lookup
description: Discover and inspect Hume Bank's openly-offered banking products (deposit, lending, and card products) via the public Consumer Data Right Product Reference Data API — no authentication required.
api: openapi/hume-bank-cds-banking-products-openapi.yml
operations: [listProducts, getProductDetail]
---

# Hume Bank product lookup

Use the public Australian CDR Product Reference Data API to browse Hume Bank's
current products and pull full detail (fees, rates, eligibility) for any one.

## Auth

None. These are public, unauthenticated PRD endpoints. You MUST send the
mandatory `x-v` request header declaring the endpoint version (Hume Bank serves
`x-v: 4`); optionally send `x-min-v`. See `conventions/hume-bank-conventions.yml`.

Base URL: `https://ibankob.humebank.com.au/OpenBanking/cds-au/v1`

## Steps

1. **List products** — call `listProducts` (`GET /banking/products`).
   - Optional filters: `product-category` (e.g. `RESIDENTIAL_MORTGAGES`,
     `TERM_DEPOSITS`, `PERS_LOANS`, `CRED_AND_CHRG_CARDS`,
     `TRANS_AND_SAVINGS_ACCOUNTS`), `effective` (`CURRENT`/`FUTURE`/`ALL`),
     `brand`, `updated-since`.
   - Paginate with `page` / `page-size` (default page-size 25); read
     `meta.totalRecords` / `meta.totalPages` and follow `links.next`.
   - Each item is a `BankingProductV3`; capture its `productId`.

2. **Get product detail** — call `getProductDetail`
   (`GET /banking/products/{productId}`) with a `productId` from step 1.
   - Returns a `BankingProductDetailV3` with `fees[]`, `depositRates[]`,
     `lendingRates[]`, `features[]`, `constraints[]`, `eligibility[]`, and
     `bundles[]`. See `data-model/hume-bank-data-model.yml` for the entity graph.

## Rules

- Both operations are safe, read-only GETs — no idempotency key, no writes.
- `productId` values are data-holder-specific and NOT guaranteed permanent;
  always resolve them fresh from `listProducts` rather than caching long-term.
- Monetary fields use CDS string types (`AmountString`, `RateString`); parse
  accordingly. Amounts assume AUD unless a `currency` is given.
- The spec documents only 200 responses; on error, expect a CDS `ErrorList`
  envelope (`{ errors: [ { code, title, detail } ] }`).
