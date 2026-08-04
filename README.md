# Summerland Bank (summerland-bank)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
