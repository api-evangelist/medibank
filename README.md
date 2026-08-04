# Medibank (medibank)

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

Medibank Private Limited (ASX: MPL) is Australia's largest private health insurer, headquartered in Melbourne and operating two retail brands, Medibank and ahm, alongside the Amplar Health services arm. Founded in 1976 as a government-owned fund and privatised through an ASX listing in 2014, it underwrites hospital, extras and ambulance cover for Australian residents, Overseas Student Health Cover and Overseas Visitors Health Cover, and distributes travel, pet, life, income protection and accident cover alongside its core private health insurance book. Its API posture is fully partner-gated: there is no public API and no developer portal.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/medibank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/medibank/refs/heads/main/apis.yml)

## Tags

- Insurance
- Australia
- Health Insurance
- Private Health Insurance
- Life and Health
- Carrier
- Claims
- Policy Administration
- Travel Insurance
- Pet Insurance
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None. Medibank publishes no public, self-serve API.

Every conventional developer host and path was probed on 2026-07-25. The `developer`, `developers`, `docs` and `apis` subdomains of `medibank.com.au` return no DNS answer. `api.medibank.com.au` resolves to 203.37.77.144 but does not accept a public TCP connection on port 443. `/developers`, `/api`, `/developer`, `/partners` and `/integrations` all return HTTP 404 on `www.medibank.com.au`, whose own sitemap — 1,364 URLs — contains no developer, API, SDK or integration page.

The only first-party integration surfaces are login walls and email-gated onboarding:

- **[Medibank Provider Self Service](https://providers.medibank.com.au/)** (linked from the provider hub as "Provider Central (ESP)") — HTTP 200, but a React single-page application with catch-all routing that serves the same shell for every path, including `/.well-known/openid-configuration`. No API catalog is readable anonymously.
- **portal.medibank.com.au** — a Palo Alto Networks GlobalProtect corporate VPN.
- **HCP Portal** — hospitals submit Hospital Casemix Protocol data after emailing `hcp@medibank.com.au` for access; the specification itself is published by the Australian Department of Health and Aged Care.

## How Medibank actually integrates

The real machine-to-machine rails are third-party and government-operated rather than Medibank-published:

- **ECLIPSE** — the Services Australia (Medicare Australia) in-patient online claiming system. Medibank accepts hospital claims and 25% Fund Gap medical claims from Simplified Billing Agents under claim type "MB", and ECLIPSE serves the Online Eligibility Check (OEC) with Presenting Illness (PIL) codes. Registration is with Services Australia, not Medibank.
- **ECFWeb** and **THELMA** — alternative eligibility-check channels named for providers without ECLIPSE OEC access.
- **HICAPS** and **iSOFT** — practice terminals carrying ancillary (extras) claiming.
- **MPPA billing channel** — pathology and diagnostic imaging, onboarded by phone and email.
- **HCP** — Hospital Casemix Protocol file submission.

## ACORD posture

**No ACORD reference found.** No occurrence of ACORD, AL3, ACORD XML or NGDS appears anywhere on Medibank's public estate. This is the expected result rather than a gap: ACORD's standards serve property-and-casualty and life carriers and their agency management systems, while Australian private health insurance runs on ECLIPSE, the Hospital Casemix Protocol and the Medicare Benefits Schedule. ECLIPSE and HCP are the local analogue of an ACORD posture, and neither is a Medibank publication.

## Quote / bind / issue / FNOL

None of the four insurance API verbs is exposed to unauthenticated developers. Quoting is a web funnel, binding and issuance are web and call-centre only, and claims intake — which is genuinely electronic — travels over ECLIPSE, HICAPS and iSOFT rather than any documented Medibank API.

## Market context

Australia has the legal machinery for open insurance and no live obligation. APRA supervises prudentially and the Private Health Insurance Ombudsman handles conduct, but the Consumer Data Right that opened banking and energy was designated to extend to general insurance and then deferred and de-prioritised — and would not have reached private health insurance in any case. There is no forcing function that would put a Medibank API in front of an outside developer.

## Links

- [Website](https://www.medibank.com.au/)
- [Newsroom](https://www.medibank.com.au/livebetter/newsroom/)
- [Provider hub](https://www.medibank.com.au/providers/)
- [Provider claims](https://www.medibank.com.au/providers/claims/)
- [MPPA billing channel](https://www.medibank.com.au/providers/medical/mppa/)
- [Hospital provider information (ECLIPSE, OEC, HCP)](https://www.medibank.com.au/providers/hospital/)
- [Information for Simplified Billing Agents](https://www.medibank.com.au/providers/information-for-simplified-billing-agents/)
- [Provider Self Service (Provider Central / ESP)](https://providers.medibank.com.au/)
- [GitHub organization](https://github.com/Medibank) — 12 public repositories, all recruitment exercises or AEM tooling forks
- [LinkedIn](https://www.linkedin.com/company/medibank)
- [Investor centre](https://www.medibank.com.au/about/investor-centre/)
- [Privacy policy](https://www.medibank.com.au/privacy/)
- [Legal information](https://www.medibank.com.au/legal-information/)
- [Security and privacy](https://www.medibank.com.au/help/security-and-privacy/)
