# MyState Bank (mystate-bank)

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
