# Hume Bank (hume-bank)

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

Hume Bank is a customer-owned (mutual) Australian bank headquartered in Albury, New South Wales. Founded in 1955 as the Hume Co-operative Building & Investment Society, it became Hume Building Society and then Hume Bank on 1 July 2014, serving roughly 65,000 customers with around A$1.70 billion in assets. As an authorised deposit-taking institution (ADI) it participates in Australia's Consumer Data Right (CDR / Open Banking) regime, exposing a public, unauthenticated Product Reference Data (PRD) API built to the Consumer Data Standards for its retail and business deposit and credit card products.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hume-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hume-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Mutual
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Hume Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data API conforming to the Australian Consumer Data Standards (CDS). Confirmed live returning HTTP 200 with 25 products (x-v 4) at the CDR-registered base `https://ibankob.humebank.com.au/OpenBanking`, covering Hume Bank's retail and business term deposits, savings/transaction accounts, home loans, personal loans, and credit card products with rates, fees, and eligibility.

- **Human URL:** [https://www.humebank.com.au/tools-help/open-banking/](https://www.humebank.com.au/tools-help/open-banking/)
- **Base URL:** `https://ibankob.humebank.com.au/OpenBanking/cds-au/v1/banking/products`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://www.humebank.com.au/tools-help/open-banking/)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#cdr-banking-api_get-products)
- [OpenAPI](openapi/hume-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.humebank.com.au/)
- [Developer Portal](https://www.humebank.com.au/tools-help/open-banking/)
- [Documentation](https://www.humebank.com.au/tools-help/open-banking/)
- [Privacy Policy](https://www.humebank.com.au/privacy-policy/)
- [Support](https://www.humebank.com.au/contact-us/)
- [LinkedIn](https://www.linkedin.com/company/humebank)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
