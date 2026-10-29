# DSV

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

DSV A/S is a Danish transport and logistics group headquartered in Hedehusene, Denmark, and one of the world's largest freight forwarders — roughly 150,000 employees across more than 90 countries after its 2025 acquisition of Schenker from Deutsche Bahn. It sells air, sea, road, rail and parcel forwarding plus contract logistics and customs brokerage, sitting in the intermediation layer between shippers and the carriers, terminals and customs authorities it books capacity with. Its API posture is a real, publicly browsable Azure API Management developer portal at developer.dsv.com carrying 29 downloadable OpenAPI 3.0.1 contracts for booking, tracking, quoting, labels, documents, invoicing, customs, warehousing and webhooks — but every published product is a DEMO/test environment, production access is gated behind myDSV customer credentials and an 'apply to go live' step, and for a large part of DSV's customer base the real integration path is still EDIFACT D10B, ANSI X12 and DSV XML message packages moved over AS2, SFTP or HTTPS. The REST surface is entirely DSV-proprietary: no DCSA, IATA ONE Record, Cargo-XML or GS1 EPCIS conformance is claimed anywhere.

**Areas:** Logistics · Supply Chain · Denmark · Freight Forwarding · Air Cargo · Ocean Freight · Road Freight · Rail Freight · Parcel · Contract Logistics · Warehousing · Customs

## DSV on APIs.io

Everything profiled for DSV is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/dsv/](https://apis.io/providers/dsv/)** — or go straight to one of the APIs or properties below.

### APIs (32)

- [DSV Booking API](https://apis.io/apis/dsv/dsv-booking-api/) — Booking Api Service
- [DSV Bookings API](https://apis.io/apis/dsv/dsv-bookings-api/) — The Bookings API from DSV — 8 operation(s) for bookings.
- [DSV Booking Web Service API](https://apis.io/apis/dsv/dsv-bookingwebservice-api/) — The BookingWebService API from DSV — 1 operation(s) for bookingwebservice.
- [DSV BPO Inbound API](https://apis.io/apis/dsv/dsv-bpo-inbound-api/) — The BPO Inbound API from DSV — 3 operation(s) for bpo inbound.
- [DSV Declarations API](https://apis.io/apis/dsv/dsv-declarations-api/) — The Declarations API from DSV — 2 operation(s) for declarations.
- [DSV Delivery API](https://apis.io/apis/dsv/dsv-delivery-api/) — The Delivery API from DSV — 1 operation(s) for delivery.
- [DSV Draft API](https://apis.io/apis/dsv/dsv-draft-api/) — The Draft API from DSV — 4 operation(s) for draft.
- [DSV Events API](https://apis.io/apis/dsv/dsv-events-api/) — The Events API from DSV — 2 operation(s) for events.
- [DSV Inbound API](https://apis.io/apis/dsv/dsv-inbound-api/) — The Inbound API from DSV — 1 operation(s) for inbound.
- [DSV Inventory API](https://apis.io/apis/dsv/dsv-inventory-api/) — The Inventory API from DSV — 2 operation(s) for inventory.
- [DSV Invoices API](https://apis.io/apis/dsv/dsv-invoices-api/) — The Invoices API from DSV — 5 operation(s) for invoices.
- [DSV Label API](https://apis.io/apis/dsv/dsv-label-api/) — Printing API
- [DSV Load Plans API](https://apis.io/apis/dsv/dsv-loadplans-api/) — The LoadPlans API from DSV — 7 operation(s) for loadplans.
- [DSV Orders API](https://apis.io/apis/dsv/dsv-orders-api/) — The Orders API from DSV — 6 operation(s) for orders.
- [DSV Orders Async API](https://apis.io/apis/dsv/dsv-ordersasync-api/) — The OrdersAsync API from DSV — 1 operation(s) for ordersasync.
- [DSV Public API](https://apis.io/apis/dsv/dsv-public-api/) — The Public API from DSV — 5 operation(s) for public.
- [DSV Quote API](https://apis.io/apis/dsv/dsv-quote-api/) — The Quote API from DSV — 1 operation(s) for quote.
- [DSV Shipment API](https://apis.io/apis/dsv/dsv-shipment-api/) — The Shipment API from DSV — 1 operation(s) for shipment.
- [DSV Shipment details API](https://apis.io/apis/dsv/dsv-shipment-details-api/) — The Shipment details API from DSV — 4 operation(s) for shipment details.
- [DSV Shipment document API](https://apis.io/apis/dsv/dsv-shipment-document-api/) — The Shipment document API from DSV — 1 operation(s) for shipment document.
- [DSV Shipment documents API](https://apis.io/apis/dsv/dsv-shipment-documents-api/) — The Shipment documents API from DSV — 3 operation(s) for shipment documents.
- [DSV Shipment list API](https://apis.io/apis/dsv/dsv-shipment-list-api/) — The Shipment list API from DSV — 1 operation(s) for shipment list.
- [DSV Shipments API](https://apis.io/apis/dsv/dsv-shipments-api/) — The Shipments API from DSV — 1 operation(s) for shipments.
- [DSV Status API](https://apis.io/apis/dsv/dsv-status-api/) — The Status API from DSV — 2 operation(s) for status.
- [DSV Token API](https://apis.io/apis/dsv/dsv-token-api/) — The Token API from DSV — 1 operation(s) for token.
- [DSV Tracking API](https://apis.io/apis/dsv/dsv-tracking-api/) — The Tracking API from DSV — 3 operation(s) for tracking.
- [DSV Tracking Web Service V3 API](https://apis.io/apis/dsv/dsv-trackingwebservicev3-api/) — The TrackingWebServiceV3 API from DSV — 1 operation(s) for trackingwebservicev3.
- [DSV Upload attachment using Booking ID API](https://apis.io/apis/dsv/dsv-upload-attachment-using-booking-id-api/) — The Upload attachment using Booking ID API from DSV — 1 operation(s) for upload attachment using booking id.
- [DSV Upload attachment using Shipment Id API](https://apis.io/apis/dsv/dsv-upload-attachment-using-shipment-id-api/) — The Upload attachment using Shipment Id API from DSV — 1 operation(s) for upload attachment using shipment id.
- [DSV Webhook API](https://apis.io/apis/dsv/dsv-webhook-api/) — The Webhook API from DSV — 3 operation(s) for webhook.
- [DSV E Docs API](https://apis.io/apis/dsv/dsv-edocs-api/) — The EDocs API from DSV — 5 operation(s) for edocs.
- [DSV Product Data API](https://apis.io/apis/dsv/dsv-product-data-api/) — The Product Data API from DSV — 1 operation(s) for product data.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Collections (29)

Postman and Open Collection request collections.

- [Access Token (DEMO)](https://apis.io/collections/dsv/open-dsv-access-token-demo-v1/)
- [Connect Booking API (DEMO)](https://apis.io/collections/dsv/open-dsv-connect-api-booking-demo-v1/)
- [Connect Tracking API (DEMO)](https://apis.io/collections/dsv/open-dsv-connect-api-tracking-demo-v1/)
- [Customs (DEMO)](https://apis.io/collections/dsv/open-dsv-customs-ai-demo-v2/)
- [Booking - SCM](https://apis.io/collections/dsv/open-dsv-edc-booking-api-v2/)
- [eDOCS - SCM](https://apis.io/collections/dsv/open-dsv-edc-edocs-api-v2/)
- [Events - SCM](https://apis.io/collections/dsv/open-dsv-edc-events-api-v2/)
- [Loadplan - SCM](https://apis.io/collections/dsv/open-dsv-edc-loadplan-api-v2/)
- [Neom - eDC](https://apis.io/collections/dsv/open-dsv-edc-neom-api-v2/)
- [Orders - SCM](https://apis.io/collections/dsv/open-dsv-edc-public-api-v2/)
- [Shipments - SCM](https://apis.io/collections/dsv/open-dsv-edc-shipments-api-v2/)
- [QUOTE API DEMO](https://apis.io/collections/dsv/open-dsv-es-quote-demo-v1/)
- [Webhook (DEMO) - Air, Sea, Road(EU), Rail](https://apis.io/collections/dsv/open-dsv-es-webhook-demo-v1/)
- [Webhook API (INT)](https://apis.io/collections/dsv/open-dsv-es-webhook-int-v1/)
- [BOOKING (DEMO) - Air, Sea, Road (EU), Rail](https://apis.io/collections/dsv/open-dsv-generic-booking-demo-v2/)
- [DOWNLOAD (DEMO) - Air, Sea, Road (EU), Rail](https://apis.io/collections/dsv/open-dsv-generic-download-demo-v1/)
- [Invoice (DEMO) - Air, Sea, Rail](https://apis.io/collections/dsv/open-dsv-generic-invoice-demo-v1/)
- [Labels (DEMO) - Air, Sea, Road(EU), Rail](https://apis.io/collections/dsv/open-dsv-generic-labels-demo-v1/)
- [TRACKING (DEMO)- Air, Sea, Road (EU), Rail](https://apis.io/collections/dsv/open-dsv-generic-tracking-demo-v2/)
- [UPLOAD - Air, Sea, Road (EU), Rail (DEMO)](https://apis.io/collections/dsv/open-dsv-generic-upload-demo-v1/)
- [Visibility (DEMO) - Air, Sea, Rail, XPress](https://apis.io/collections/dsv/open-dsv-generic-visibilitydemo-v1/)
- [WMS Delivery Notification (DEMO)](https://apis.io/collections/dsv/open-dsv-warehousing-despatch-demo-v1/)
- [WMS Inventory (DEMO)](https://apis.io/collections/dsv/open-dsv-warehousing-inventory-demo-v1/)
- [WMS Inbound Notification (DEMO)](https://apis.io/collections/dsv/open-dsv-warehousing-preadvice-demo-v1/)
- [WMS Product Data (DEMO)](https://apis.io/collections/dsv/open-dsv-warehousing-productdata-demo-v1/)
- …and 4 more published on APIs.io

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.dsv.com/)
- [Documentation](https://developer.dsv.com/getting-started)
- [API reference](https://developer.dsv.com/apicatalogue)
- [Support](https://developer.dsv.com/support-contact)
- [Changelog](https://developer.dsv.com/release-notes)
- [Security](https://developer.dsv.com/edi-certificates)
- [Terms of service](https://developer.dsv.com/terms-and-conditions)
- [Privacy policy](https://www.dsv.com/en/about-dsv/corporate-responsibility/policies/data-privacy)

## API Evangelist rating

**Kin Score 38.9** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 67.9 |
| Contract quality | 47.3 |
| Contract governance | 0.0 |
| Operational transparency | 34.2 |
| Developer ergonomics | 47.6 |
| Access clarity | 23.7 |

**Agent readiness 31.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | unknown |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/dsv/](https://apis.io/providers/dsv/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for DSV: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/dsv/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
