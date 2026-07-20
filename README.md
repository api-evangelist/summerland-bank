# Summerland Bank (summerland-bank)

Summerland Bank is a customer-owned (mutual) bank based in Lismore in the Northern Rivers region of New South Wales, Australia, tracing its origins to the former Summerland Credit Union (Summerland Financial Services Limited, ABN 21 087 650 360, AFSL and Australian Credit Licence 241167) and rebranded as Summerland Bank in 2023. As an APRA-regulated authorised deposit-taking institution (ADI) and certified B Corporation, it is owned by its customers rather than shareholders and has announced plans to merge with fellow customer-owned Regional Australia Bank. Under Australia's Consumer Data Right (CDR / Open Banking), Summerland Bank operates as a data holder and exposes a live, public, unauthenticated Product Reference Data (PRD) API conforming to the Data Standards Body (DSB) Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/summerland-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/summerland-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Data Right
- Consumer Banking
- Australia
- Mutual Bank

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Summerland Bank CDR Product Reference Data API

Public, unauthenticated Product Reference Data (PRD) endpoints under the Consumer Data Right. Serves `GET /banking/products` and `GET /banking/products/{productId}` at the CDS public base, returning machine-readable product, fee, rate, and eligibility data. Confirmed live on 2026-07-20: a `GET` with the mandatory CDS `x-v: 5` header returned HTTP 200 with 25 products across seven categories. The contract is the shared DSB Consumer Data Standards Banking OpenAPI (OpenAPI 3.0.3, "CDR Banking API"), not a bank-proprietary specification.

- **Human URL:** [https://www.summerland.com.au/services/digital-and-payments/open-banking/](https://www.summerland.com.au/services/digital-and-payments/open-banking/)
- **Base URL:** `https://public.cdr-api.summerland.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Public

#### Properties

- [Documentation](https://www.summerland.com.au/services/digital-and-payments/open-banking/)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#cdr-banking-api_get-products)
- [OpenAPI](openapi/summerland-bank-cds-banking-products-openapi.yml) — harvested verbatim from the shared DSB Consumer Data Standards Banking OpenAPI 3.0.3 (not bank-proprietary)

## Common Properties

- [Website](https://www.summerland.com.au/)
- [Developer Portal](https://www.summerland.com.au/services/digital-and-payments/open-banking/)
- [Documentation](https://www.summerland.com.au/services/digital-and-payments/open-banking/)
- [LinkedIn](https://www.linkedin.com/company/summerlandbank)
- [Blog](https://www.summerland.com.au/about-us/news-insights/)
- [Privacy Policy](https://www.summerland.com.au/privacy-policy/)
- [Terms of Service](https://www.summerland.com.au/legal-and-disclosure-documents/)
- [Domain Security](https://www.summerland.com.au/security-hub/)
- [Support](https://www.summerland.com.au/contact-us/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
