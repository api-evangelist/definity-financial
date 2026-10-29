# Definity Financial

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

Definity Financial Corporation is a Canadian property and casualty insurance group headquartered in Waterloo, Ontario and listed on the Toronto Stock Exchange (DFY). It is the demutualized successor to Economical Mutual Insurance Company, founded in 1871 in Berlin (now Kitchener), Ontario; policyholders approved demutualization in May 2021 and the company completed its IPO in November 2021, renaming the operating carrier Definity Insurance Company. Definity underwrites personal and commercial property, automobile, farm, and pet lines across Canada through four brands: Economical (broker-distributed home, auto, farm and business insurance), Sonnet (described by the company as the largest fully digital direct-to-consumer insurance business in Canada), Family Insurance Solutions, and Petline/Petsecure (pet insurance). It is one of the Big Few Canadian P&C carriers and reported roughly $6.3B in gross written premiums on a trailing-twelve-month pro-forma basis including its Travelers Canada acquisition. Its API posture is partner-gated and honest to state plainly: Definity publishes no public, self-serve developer portal and no downloadable OpenAPI, Swagger, GraphQL, or AsyncAPI definition on any first-party host. Every developer-shaped subdomain of definityfinancial.com fails to resolve, an api.definity.com host exists behind Imperva but answers HTTP 404 with an empty body to every anonymous path including OAuth and OpenID discovery, and the only reachable broker surface, broker.economical.com, is a Docebo learning management system for broker training rather than an API reference. The gated API is nonetheless real and independently attested: CSIO, Canada's property-and-casualty data-standards body and the domestic counterpart to ACORD, certified Definity against its API Security Standards on 27 November 2024 — the industry's standard authentication and authorization API model for insurer-to-broker-management-system connectivity, requiring confirmed mitigation of 16 OAuth security concerns and 18 API endpoint concerns — and Definity is additionally CSIO eDocs Certified and Compliance Certified (all non-standard Z-Codes eliminated from broker data exchange). Its Vyne broker digital platform runs on Guidewire Cloud, which Definity was the first Canadian P&C insurer to adopt for its core insurance platform. Two brands, Sonnet and Economical, publish real hand-authored llms.txt documents with explicit AI-training, generation, summarization and crawling directives, including named directives for OpenAI, Google-DeepMind and Anthropic. All of this sits in a Canadian market where OSFI supervises prudentially, the provinces regulate conduct, and Consumer-Driven Banking excludes insurance entirely, so no open-insurance mandate forces a public API surface and standardization is industry-led through CSIO instead.

**Areas:** Insurance · Canada · Property and Casualty · Carrier · Underwriting · Claims · Pet Insurance · Direct to Consumer · CSIO · Insurtech

## Definity Financial on APIs.io

Everything profiled for Definity Financial is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/definity-financial/](https://apis.io/providers/definity-financial/)** — or go straight to one of the APIs or properties below.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Definity Financial Authentication](https://apis.io/security/definity-financial/definity-financial-authentication/)
- [Definity Financial Domain Security](https://apis.io/security/definity-financial/definity-financial-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.definityfinancial.com/)
- [Sign up](https://www.sonnet.ca/get-a-quote)
- [Support](https://www.economical.com/en/contact-us)
- [Blog](https://www.economical.com/en/blog)
- [Compliance](https://csio.com/csio-certification/certified-members)
- [Terms of service](https://www.economical.com/en/terms-of-use)
- [Privacy policy](https://www.economical.com/en/privacy)

## API Evangelist rating

**Kin Score 21.9** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 55.4 |
| Contract quality | 0.0 |
| Contract governance | 18.2 |
| Operational transparency | 0.0 |
| Developer ergonomics | 21.4 |
| Access clarity | 42.1 |

**Agent readiness 2.5** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
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

**Regulatory alignment 26.3** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/definity-financial/](https://apis.io/providers/definity-financial/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Definity Financial: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/definity-financial/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
