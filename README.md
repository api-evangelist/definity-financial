# Definity Financial (definity-financial)

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

Definity Financial Corporation is a Canadian property and casualty insurance group headquartered in Waterloo, Ontario and listed on the Toronto Stock Exchange (DFY). It is the demutualized successor to Economical Mutual Insurance Company, founded in 1871 in Berlin (now Kitchener), Ontario; policyholders approved demutualization in May 2021, the IPO closed in November 2021, and the operating carrier was renamed Definity Insurance Company that December. Definity underwrites personal and commercial property, automobile, farm and pet lines across Canada through four brands — Economical (broker-distributed home, auto, farm and business insurance), Sonnet (the company's direct-to-consumer digital carrier), Family Insurance Solutions, and Petline/Petsecure — and is one of the Big Few Canadian P&C carriers, reporting roughly $6.3B in gross written premiums on a trailing-twelve-month pro-forma basis including its Travelers Canada acquisition.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/definity-financial/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/definity-financial/refs/heads/main/apis.yml)

## API Posture

Definity Financial publishes **no public, self-serve developer portal and no downloadable API definition**. This profile records that absence deliberately and accurately.

- Every developer-shaped subdomain of the primary domain fails to resolve: `developer.`, `developers.`, `docs.` and `api.definityfinancial.com` all return no connection.
- The first-party paths `/developers`, `/api`, `/developer`, `/partners` and `/integrations` return HTTP 403 behind an Imperva edge, and a rendered fetch of the homepage shows no developer, API, or partner-technology links anywhere in the site navigation.
- A real gateway host exists but is entirely non-public: `api.definity.com` resolves behind Imperva and answers HTTP 404 with an empty body to every anonymous path, including `/openapi.json`, `/swagger.json`, `/api-docs`, `/graphql`, `/.well-known/openid-configuration` and `/.well-known/oauth-authorization-server`.
- The only reachable broker-facing host, `broker.economical.com` (HTTP 200, redirects to `/learn`), is a **Docebo learning management system** serving broker training courseware — a login wall, not an API reference.
- **Vyne**, Definity's broker digital platform named in its own investor material, has no public documentation host. `vyne.economical.ca` returns HTTP 200 but serves a third-party "domain for sale" parking page and is not a Definity property.
- **Sonnet** (`sonnet.ca`) runs a public consumer quote-and-buy web flow but publishes no developer documentation (`/openapi.json`, `/api-docs`, `/.well-known/openid-configuration` all 404).
- No GitHub organization exists. Corporate Postman teams exist (`definity-insurance`, `definity-5429`, `economicaldefinity`) but publish zero public collections or workspaces.

### ACORD / CSIO posture

**No ACORD reference found.** Canada's P&C data-standards body is **CSIO** (Centre for Study of Insurance Operations), not ACORD. No AL3, ACORD XML, NGDS, IVANS, Applied Epic or Vertafore reference was retrievable from Definity's own Imperva-walled sites.

**Definity is CSIO certified — confirmed.** The first round of this profile recorded CSIO certification as unconfirmed; the 2026-07-25 enrichment round confirmed it on CSIO's own certified-members register:

| Certification | Awarded | What it attests |
|---|---|---|
| **API Security Standards Certification** (Insurer) | 2024-11-27 | CSIO's standard authentication and authorization API model for insurer-to-Broker-Management-System connectivity. Built by CSIO's INNOTECH Advisory Committee and its API Security Working Group; the standard addresses **OAuth 2.1** security concerns, and certification requires confirmed prevention of **16 OAuth security concerns and 18 API endpoint concerns**. |
| **eDocs Certification** (Insurer) | 2025-05-21 | Updated CSIO eDocs Standards deployed to production; standardized codes and descriptions transmitted to Broker Management Systems. |
| **Compliance Certification** | 2025-05-21 | All **Z-Codes** (non-standard coverage codes) eliminated from broker data exchange. |

Definity is **not** listed under CSIO's *JSON API Standards Certified* or *CL Data Standards Certified* categories.

This is the meaningful finding for a carrier with no public API: **the broker API surface is real and independently attested, it is simply never documented publicly.** The certification does not make any endpoint, scope, or schema available.

### Core platform

Definity became the **first Canadian P&C insurer to transition its core insurance platform to Guidewire Cloud** (September 2022). Sonnet and Vyne were Guidewire Innovation Award winners in 2016 and 2018 respectively. Guidewire Cloud exposes licensed platform APIs, not Definity-published developer contracts.

### AI access posture (llms.txt)

Two brands publish real, hand-authored **llms.txt** documents at their site roots — saved verbatim in `llms/`:

- [`sonnet.ca/llms.txt`](https://www.sonnet.ca/llms.txt) (5,836 bytes)
- [`economical.com/llms.txt`](https://www.economical.com/llms.txt) (37,448 bytes)

Both set `AI-Training: Allow`, `AI-Generation: Allow`, `AI-Summarization: Allow` and `AI-Crawling: Allow` for `*`, with **named per-vendor directives for OpenAI, Google-DeepMind and Anthropic**, plus a curated reference site map for AI indexing. `petsecure.com/llms.txt` and `definityfinancial.com/.well-known/security.txt` return HTTP 200 but are **false positives** (site HTML shell and the string `Invalid key` respectively).

### Quote / bind / issue / FNOL

None of the four insurance verbs are exposed through a documented public API. Quoting and binding happen through the gated Vyne broker platform or the Sonnet consumer web flow; policy issuance and FNOL have no public API surface. The integration audience is **partner-only**.

This is consistent with the Canadian market seam: OSFI supervises federally-regulated insurers prudentially while the provinces regulate market conduct (FSRA in Ontario, AMF in Quebec), there is no open-insurance mandate, and Consumer-Driven Banking excludes insurance entirely — so nothing forces a public API surface.

## Tags

- Insurance
- Canada
- Property and Casualty
- Carrier
- Underwriting
- Claims
- Broker
- Pet Insurance
- Direct to Consumer
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None. No public, documented, self-serve API is published by Definity Financial or any of its brands. See [`review.yml`](review.yml) for the full probe log and provenance.

## Artifacts

| Artifact | File | Method |
|---|---|---|
| Conformance / CSIO certifications | [`conformance/definity-financial-conformance.yml`](conformance/definity-financial-conformance.yml) | searched |
| Authentication posture | [`authentication/definity-financial-authentication.yml`](authentication/definity-financial-authentication.yml) | searched |
| Lifecycle (versioning / deprecation / SLA / status) | [`lifecycle/definity-financial-lifecycle.yml`](lifecycle/definity-financial-lifecycle.yml) | searched |
| Well-known + site-root discovery index | [`well-known/definity-financial-well-known.yml`](well-known/definity-financial-well-known.yml) | searched |
| Domain security (TLS/HSTS/DNSSEC/CAA/SPF/DMARC) | [`security/definity-financial-domain-security.yml`](security/definity-financial-domain-security.yml) | probed |
| Sonnet llms.txt (verbatim) | [`llms/definity-financial-sonnet-llms.txt`](llms/definity-financial-sonnet-llms.txt) | searched |
| Economical llms.txt (verbatim) | [`llms/definity-financial-economical-llms.txt`](llms/definity-financial-economical-llms.txt) | searched |
| Definity Financial llms.txt | [`llms/definity-financial-llms.txt`](llms/definity-financial-llms.txt) | generated |

**Not present, and correctly so:** no `openapi/`, `asyncapi/`, `graphql/`, `grpc/`, `mcp/`, `skills/`, `arazzo/`, `packages/`, `sandbox/`, `errors/`, `scopes/`, `conventions/`, `changelog/`, `cli/`, `components/` or `data-model/` artifacts — there is no machine-readable contract to derive them from, and none were fabricated. No vulnerability-disclosure program or trust center was found: `trust.`, `security.` and `status.` subdomains do not resolve, and no `security.txt` exists on any host.

### Domain security summary

All six probed hosts (`www.definityfinancial.com`, `www.economical.com`, `www.sonnet.ca`, `www.petsecure.com`, `api.definity.com`, `broker.economical.com`) serve **TLS 1.3 with HSTS**; only `broker.economical.com` sets `includeSubDomains`. Across all five registrable domains: **no DNSSEC, no CAA**, SPF everywhere with a `-all` hard fail, and DMARC published everywhere but at `p=none` on four of five — only `petsecure.com` enforces (`p=quarantine`). None reach `p=reject`.

## Links

- [Definity Financial](https://www.definityfinancial.com/)
- [Economical Insurance](https://www.economical.com/)
- [Sonnet Insurance](https://www.sonnet.ca/)
- [Petsecure](https://www.petsecure.com/)
- [Postman — Definity Insurance](https://www.postman.com/definity-insurance) (team exists, nothing published)
- [CSIO — Canadian P&C data standards](http://csio.com/)
