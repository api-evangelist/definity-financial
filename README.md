# Definity Financial (definity-financial)

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

### ACORD posture

**No ACORD reference found.** Canada's P&C data-standards body is **CSIO** (Centre for Study of Insurance Operations), not ACORD. CSIO maintains eDocs Standards, EDI Standards, XML Standards, XML Dataset Standards, JSON Standards, API Security Standards, Commercial Lines Data Standards, CSIOnet and My Proof of Insurance, and states that 9 of Canada's top 10 insurers are members. Definity/Economical membership or certification could not be confirmed on CSIO's publicly reachable pages, and no AL3, ACORD XML, NGDS, IVANS, Applied Epic or Vertafore reference was retrievable from Definity's own Imperva-walled sites.

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

## Links

- [Definity Financial](https://www.definityfinancial.com/)
- [Economical Insurance](https://www.economical.com/)
- [Sonnet Insurance](https://www.sonnet.ca/)
- [Petsecure](https://www.petsecure.com/)
- [Postman — Definity Insurance](https://www.postman.com/definity-insurance) (team exists, nothing published)
- [CSIO — Canadian P&C data standards](http://csio.com/)
