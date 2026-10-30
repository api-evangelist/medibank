# Medibank

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Medibank Private Limited (ASX: MPL) is Australia's largest private health insurer, headquartered in Melbourne and operating two retail brands, Medibank and ahm, alongside the Amplar Health services arm. Founded in 1976 as a government-owned fund and privatised through an ASX listing in 2014, it underwrites hospital, extras and ambulance cover for Australian residents, Overseas Student Health Cover and Overseas Visitors Health Cover, and distributes travel, pet, life, income protection and accident cover (Recover Boost) alongside its core private health insurance book. Its home market is Australia, where private health insurance is a separately regulated market supervised by APRA and the Private Health Insurance Ombudsman, and where the Consumer Data Right that opened banking and energy was designated for general insurance and then deferred — so there is no open insurance obligation and no CDR seam reaching a health fund like Medibank. Medibank's API posture is fully partner-gated and there is no public API. No developer portal exists on any conventional host: developer, developers, docs and apis subdomains of medibank.com.au do not resolve in DNS, api.medibank.com.au resolves but does not accept public TCP connections on port 443, and /developers, /api, /developer, /partners and /integrations all return HTTP 404 on www.medibank.com.au, whose 1,364-URL sitemap contains no developer or API page at all. The only first-party integration surfaces are login walls and email-gated onboarding: providers.medibank.com.au is a React single-page "Medibank - Provider Self Service" application (Provider Central, ESP) that returns its shell for every path, portal.medibank.com.au is a Palo Alto GlobalProtect corporate VPN, and the HCP Portal for Hospital Casemix Protocol submissions is granted only by emailing Medibank's HCP team. The real machine-to-machine claiming rails are third-party and government-operated rather than Medibank-published: ECLIPSE, the Services Australia in-patient online claiming system, carries hospital claims and 25 percent Fund Gap medical claims under claim type "MB" and serves Online Eligibility Check with Presenting Illness codes, with ECFWeb and THELMA as alternative eligibility channels and HICAPS and iSOFT terminals handling ancillary claiming. No ACORD reference of any kind appears on Medibank's public estate, which is the expected result — Australian private health insurance runs on ECLIPSE, HCP and the MBS rather than on ACORD AL3 or ACORD XML. No OpenAPI or Swagger definition, no Postman collection, no GraphQL or gRPC surface, no webhook or event catalog, and no documented authentication scheme could be confirmed anywhere on Medibank's public web estate as of 2026-07-25, and none of the four insurance API verbs — quote, bind, issue or FNOL — is exposed to unauthenticated developers.

**Areas:** Insurance · Australia · Health Insurance · Private Health Insurance · Life and Health · Carrier · Claims · Policy Administration · Travel Insurance · Pet Insurance

## Medibank on APIs.io

Everything profiled for Medibank is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/medibank/](https://apis.io/providers/medibank/)** — or go straight to one of the APIs or properties below.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Medibank Domain Security](https://apis.io/security/medibank/medibank-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Medibank Plans Pricing](https://apis.io/plans/medibank/medibank-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Medibank Rate Limits](https://apis.io/rate-limits/medibank/medibank-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.medibank.com.au/)
- [Documentation](https://www.medibank.com.au/providers/)
- [Getting started](https://www.medibank.com.au/health-support/pregnancy/article/getting-started-breastfeeding/)
- [Sign up](https://www.medibank.com.au/health-insurance/join/)
- [Support](https://www.medibank.com.au/help/)
- [Blog](https://www.medibank.com.au/livebetter/newsroom/)
- [Terms of service](https://www.medibank.com.au/legal-information/)
- [Privacy policy](https://www.medibank.com.au/privacy/)
- [GitHub](https://github.com/Medibank)

## API Evangelist rating

**Kin Score 23.7** — emerging · rubric 0.24.0 · scored 2026-10-20

| Facet | Score |
|---|---|
| Discoverability | 55.4 |
| Contract quality | 0.0 |
| Contract governance | 4.5 |
| Operational transparency | 13.2 |
| Developer ergonomics | 45.2 |
| Access clarity | 34.2 |

**Agent readiness 5.6** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 16.7** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/medibank/](https://apis.io/providers/medibank/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Medibank: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/medibank/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
