# MyState Bank (mystate-bank)

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

MyState Bank is an Australian retail bank headquartered in Hobart, Tasmania, and the principal banking brand of ASX-listed MyState Limited (ASX:MYS). It grew from a Tasmanian credit union, took its current group shape in the 2009 merger of Tasmanian Perpetual Trustees and MyState Financial, was authorised to use the MyState Bank name in 2014, and completed a merger with Queensland regional lender Auswide Bank in February 2025. As an authorised deposit-taking institution (ADI) it is a regulated data holder under the Australian Consumer Data Right (CDR / Open Banking) and exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Consumer Data Standards (CDS).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mystate-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mystate-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Data Right
- Consumer Banking
- Australia
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### MyState Bank CDR Product Reference Data API

Public, unauthenticated Product Reference Data (PRD) API mandated by the Australian Consumer Data Right. Conforms to the Consumer Data Standards (CDS) with Get Products (`GET /banking/products`) and Get Product Detail (`GET /banking/products/{productId}`) endpoints, versioned via the `x-v` header. Confirmed live returning HTTP 200 with a `data.products` array and `x-v: 3` on 2026-07-20.

- **Human URL:** [https://consumerdatastandardsaustralia.github.io/standards/#banking-products](https://consumerdatastandardsaustralia.github.io/standards/#banking-products)
- **Base URL:** `https://public.cdr.mystate.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://consumerdatastandardsaustralia.github.io/standards/#banking-products)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/mystate-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.mystate.com.au/)
- [LinkedIn](https://www.linkedin.com/company/mystate-limited)
- [Investor Relations](https://mystatelimited.com.au/)
- [Product Reference Data](https://public.cdr.mystate.com.au/cds-au/v1/banking/products)
- [Standards](https://consumerdatastandardsaustralia.github.io/standards/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
