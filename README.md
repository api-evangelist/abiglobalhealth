# Abi Global Health

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

Abi Global Health Ltd. (AGH) is an AI-native healthcare navigation, virtual care orchestration and
clinical cost management company founded in Dublin, Ireland in 2016. It sells to health insurers,
employee benefits providers, TPAs, assistance companies, digital health organisations,
pharmaceutical companies and public health programmes — not direct to consumers — and delivers
text, voice and video consultations, mental-health screening, form-based prescriptions and the Abi
Navigator AI triage assistant through chat apps, an embeddable widget, a hosted web app and a
partner REST API.

- Website: https://www.abiglobalhealth.com/
- API reference: https://docs.abi.ai/
- GitHub: https://github.com/abiglobalhealth
- LinkedIn: https://www.linkedin.com/company/abi-global-health

## What this profile found

The Abi API is documented publicly at **docs.abi.ai** — a client-side React application titled
"Abi API Reference" whose entire contents ship inside one JavaScript bundle. It documents **39
operations** across users, subscriptions, consultations, form-based prescriptions, Health Navigator
conversations and webhooks, **three regional base URLs**
(`https://client-api.abi.ai`, `https://ape1.api.abi.ai` for Hong Kong, and
`https://client-api.abiglobalhealth.cn` for China), a partner-API-key-for-Bearer-token
authentication flow, a seven-entry status-code table, a 23-term glossary and a **19-event webhook
catalog**.

**No machine-readable contract is published.** `/openapi.json`, `/openapi.yaml`, `/swagger.json`,
`/api-docs`, `/redoc`, `/v1/openapi.json` and `/graphql` were probed on both live API hosts and on
the docs host (2026-09-06): the API hosts return clean JSON 404s and the docs host returns its SPA
shell with HTTP 200 for every path. There is no OpenAPI, no AsyncAPI, no GraphQL SDL, no Postman
collection and no `.proto` or WSDL anywhere on the public surface, and no OpenAPI has been generated
here from the documentation — that would be fabrication.

Abi does publish a genuine, substantial **`/llms.txt`** (7.8 KB, saved verbatim in `llms/`), which
is unusual for a company of this size and is the strongest agent-facing signal in the profile.

### Notable gaps

- **No FHIR, HL7v2, X12 or SMART-on-FHIR anywhere in the contract.** For a company selling into
  insurers and health systems, this is the clearest interoperability gap: every integration needs a
  bespoke connector.
- **No pricing, no terms of service, no status page, no changelog, no deprecation policy, no
  documented rate limits.** Each was probed and recorded as an honest zero.
- **No MCP server and no A2A agent card**, despite the product itself being an LLM assistant whose
  own message format already carries a typed action/resource union.
- The only first-party package, `@abiglobalhealth/goapp-react-native`, last shipped **2025-02-27**
  and its source repository now returns 404.
- The company's own `llms.txt` links `https://www.abiglobalhealth.com/abi-navigator`, which returns
  **404**, and the API reference links `https://pro.abi.ai/join`, which serves a Squarespace
  "Domain Not Claimed" page.

### Compliance claims

The site footer and `llms.txt` claim **ISO/IEC 27001:2022, ISO/IEC 27701, ISO/IEC 42001:2023**,
HIPAA-aligned safeguards and GDPR compliance, certified via INTERCERT with the programme managed in
Sprinto. No trust centre, certificate number or audit report is published, so these are recorded as
published claims rather than verified attestations.

## Artifacts in this repository

| Path | What it holds |
|---|---|
| `llms/` | The provider's own `llms.txt`, saved verbatim |
| `authentication/` | The API-key → Bearer token flow, sub-partner authentication |
| `conventions/` | REST style, regional bases, idempotency verdict, reversibility grading |
| `errors/` | The published status-code catalog and error envelope |
| `asyncapi/` | The 19-event webhook catalog and subscription management surface |
| `vocabulary/` | The provider's 23-term published glossary |
| `data-model/` | Eight entities and eleven relationships read from the published object reference |
| `conformance/` | Certification claims and technical/domain-standard conformance |
| `lifecycle/` | Versioning, deprecation, status, SLA, support |
| `packages/` | The single npm package, with dated release evidence |
| `components/` | Chatbot, widget, web app and API interface inventory |
| `sandbox/` | The test partner account model |
| `plans/`, `rate-limits/` | Honest zeros, with the probes behind them |
| `security/` | TLS/HSTS/DNSSEC/CAA/SPF/DMARC probe results |
| `well-known/` | An eleven-host `.well-known` probe, all misses, with SPA false positives flagged |
| `mcp/` | A candidate tool mapping — **no MCP server exists** |
