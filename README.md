# DSV (dsv)

DSV A/S is a Danish transport and logistics group headquartered in Hedehusene, Denmark, and one of the world's largest freight forwarders — roughly 150,000 employees across more than 90 countries after its 2025 acquisition of Schenker from Deutsche Bahn. It sells air, sea, road, rail and parcel forwarding plus contract logistics and customs brokerage, sitting in the intermediation layer between shippers and the carriers, terminals and customs authorities it books capacity with. Its API posture is a real, publicly browsable Azure API Management developer portal at developer.dsv.com carrying 29 downloadable OpenAPI 3.0.1 contracts for booking, tracking, quoting, labels, documents, invoicing, customs, warehousing and webhooks — but every published product is a DEMO/test environment, production access is gated behind myDSV customer credentials and an 'apply to go live' step, and for a large part of DSV's customer base the real integration path is still EDIFACT D10B, ANSI X12 and DSV XML message packages moved over AS2, SFTP or HTTPS. The REST surface is entirely DSV-proprietary: no DCSA, IATA ONE Record, Cargo-XML or GS1 EPCIS conformance is claimed anywhere.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/dsv/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/dsv/refs/heads/main/apis.yml)

## Tags

- Logistics
- Supply Chain
- Denmark
- Freight Forwarding
- Air Cargo
- Ocean Freight
- Road Freight
- Rail Freight
- Parcel
- Contract Logistics
- Warehousing
- Customs
- Trade Compliance
- Track and Trace
- EDI

## Timestamps

- **Created:** 2026-07-30
- **Modified:** 2026-07-30

## APIs

### DSV Access Token API

OAuth 2.0 token endpoint for the DSV Generic APIs. Exchanges myDSV username/password (sent as client_id/client_secret with grant_type=client_credentials) plus a DSV-Subscription-Key for a 10-minute bearer access token and a 30-day refresh token. Mandatory for every Generic and Warehousing API since the 31 January 2026 migration deadline.

- **Human URL:** [https://developer.dsv.com/api-details#api=access-token-demo-v1](https://developer.dsv.com/api-details#api=access-token-demo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/oauth/v1`

#### Tags

- Authentication
- OAuth
- Tokens

#### Properties

- [OpenAPI](openapi/dsv-access-token-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-access-token-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-access-token-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=access-token-demo-v1)
- [Documentation](https://developer.dsv.com/oauth-guide)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Access%20Token%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Booking API (Air, Sea, Road EU, Rail)

Submits and updates shipment bookings to DSV across air, sea, European road and rail. Carries GS1 SSCC package tracking numbers (explicitly referenced to gs1.org/standards/id-keys/sscc), EORI numbers, HS/harmonised commodity codes, DSV MDM customer numbers and Incoterms. Returns a DSV bookingId that every other Generic API keys on.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-booking-demo-v2](https://developer.dsv.com/api-details#api=generic-booking-demo-v2)
- **Base URL:** `https://api.dsv.com/my-demo/booking/v2`

#### Tags

- Booking
- Air Freight
- Ocean Freight
- Road Freight
- Rail Freight

#### Properties

- [OpenAPI](openapi/dsv-generic-booking-demo-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-booking-demo-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-booking-demo-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-booking-demo-v2)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Booking%20V2%20-%20samples%20with%20Bearer%20Token).zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Tracking API (Air, Sea, Road EU, Rail)

Polling track-and-trace over DSV-moved shipments. Lookups by DSV bookingId, DSV TMS shipment id or customer reference; responses carry house and master bill of lading numbers, air waybill numbers, container numbers, UN/LOCODE locations, SSCC package numbers, carrier SCAC codes and a DSV-proprietary event vocabulary.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-tracking-demo-v2](https://developer.dsv.com/api-details#api=generic-tracking-demo-v2)
- **Base URL:** `https://api.dsv.com/my-demo/tracking/v2`

#### Tags

- Track and Trace
- Shipments
- Events

#### Properties

- [OpenAPI](openapi/dsv-generic-tracking-demo-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-tracking-demo-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-tracking-demo-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-tracking-demo-v2)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Tracking%20v2.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Label Print API

Prints package labels as PDF for bookings submitted through the DSV Booking API or myDSV, addressed by bookingId and GS1 SSCC package number.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-labels-demo-v1](https://developer.dsv.com/api-details#api=generic-labels-demo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/printing/v1`

#### Tags

- Labels
- Printing
- Documents

#### Properties

- [OpenAPI](openapi/dsv-generic-labels-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-labels-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-labels-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-labels-demo-v1)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Label%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Document Upload API

Uploads documents against an existing DSV booking or shipment for air, sea, European road and rail traffic.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-upload-demo-v1](https://developer.dsv.com/api-details#api=generic-upload-demo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/upload/v1`

#### Tags

- Documents
- Uploads

#### Properties

- [OpenAPI](openapi/dsv-generic-upload-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-upload-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-upload-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-upload-demo-v1)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Upload%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Document Download API

Downloads the documents DSV holds against a booking or shipment — proof of delivery, transport documents and customs paperwork — for air, sea, European road and rail traffic.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-download-demo-v1](https://developer.dsv.com/api-details#api=generic-download-demo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/download/v1`

#### Tags

- Documents
- Downloads

#### Properties

- [OpenAPI](openapi/dsv-generic-download-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-download-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-download-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-download-demo-v1)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Download%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Invoice API

Retrieves freight invoice detail for DSV air, sea and rail shipments, including carrier SCAC, master and house bill of lading references and UN/LOCODE locations.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-invoice-demo-v1](https://developer.dsv.com/api-details#api=generic-invoice-demo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/invoice/v1`

#### Tags

- Invoicing
- Billing
- Finance

#### Properties

- [OpenAPI](openapi/dsv-generic-invoice-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-invoice-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-invoice-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-invoice-demo-v1)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Visibility API

Returns live IoT device readings from DSV Visibility for air, sea, rail and XPress shipments, queried by search filter.

- **Human URL:** [https://developer.dsv.com/api-details#api=generic-visibilitydemo-v1](https://developer.dsv.com/api-details#api=generic-visibilitydemo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/visibility/v1`

#### Tags

- Visibility
- Telematics
- IoT
- Track and Trace

#### Properties

- [OpenAPI](openapi/dsv-generic-visibilitydemo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-generic-visibilitydemo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-generic-visibilitydemo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=generic-visibilitydemo-v1)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Visibility%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Quote API

Requests freight quotations from DSV. Origin and destination are expressed as 5-character UN/LOCODEs for both ports and airports — the spec explicitly rejects IATA 3-letter airport codes — alongside Incoterms and dangerous-goods flags.

- **Human URL:** [https://developer.dsv.com/api-details#api=es-quote-demo-v1](https://developer.dsv.com/api-details#api=es-quote-demo-v1)
- **Base URL:** `https://api.dsv.com/qs-demo/quote/v1`

#### Tags

- Quoting
- Rates
- Pricing

#### Properties

- [OpenAPI](openapi/dsv-es-quote-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-es-quote-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-es-quote-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=es-quote-demo-v1)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Quote%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Webhook API

Subscription API for DSV push notifications covering the Invoice, Visibility, Quote, Tracking, Warehousing, Customs and Downtime events. The subscriber supplies a push URL (validated with an OPTIONS then POST probe), basic or OAuth callback credentials, and a DSV MDM or WarehouseID customer scope. Event names are DSV-proprietary (TrackingShipmentDelivered, TrackingShipmentEstimatedDeliveryChanged, TrackingShipmentPodAvailable and similar) rather than DCSA or GS1 EPCIS event types.

- **Human URL:** [https://developer.dsv.com/api-details#api=es-webhook-demo-v1](https://developer.dsv.com/api-details#api=es-webhook-demo-v1)
- **Base URL:** `https://api.dsv.com/my-demo/webhook/v1`

#### Tags

- Webhooks
- Events
- Notifications
- Track and Trace

#### Properties

- [OpenAPI](openapi/dsv-es-webhook-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-es-webhook-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-es-webhook-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=es-webhook-demo-v1)
- [Documentation](https://developer.dsv.com/webhook-guide)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Webhook%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Webhook API (INT / Warehousing)

Integration-environment webhook subscription surface used for the Invoice and Visibility APIs and the Contract Logistics WMS events.

- **Human URL:** [https://developer.dsv.com/api-details#api=es-webhook-int-v1](https://developer.dsv.com/api-details#api=es-webhook-int-v1)
- **Base URL:** `https://api.dsv.com/my-int/webhook/v1`

#### Tags

- Webhooks
- Events
- Warehousing

#### Properties

- [OpenAPI](openapi/dsv-es-webhook-int-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-es-webhook-int-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-es-webhook-int-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=es-webhook-int-v1)
- [Documentation](https://developer.dsv.com/webhook-guide)
- [Documentation](https://developer.dsv.com/apicatalogue-cl)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(WMS%20Webhook%20V1.0%20INT%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Customs API

Transmits, updates and retrieves customs declarations through DSV Customs AI. Fields follow customs-authority vocabulary — HS commodity codes, EORI/importer/exporter registration codes, Incoterms with UN/LOCODE places, holder-of-authorization records, bill of lading package counts and container lists — but no reference to the WCO Data Model or to EU eFTI is published.

- **Human URL:** [https://developer.dsv.com/api-details#api=customs-ai-demo-v2](https://developer.dsv.com/api-details#api=customs-ai-demo-v2)
- **Base URL:** `https://api.dsv.com/csai-demo/v2`

#### Tags

- Customs
- Trade Compliance
- Declarations

#### Properties

- [OpenAPI](openapi/dsv-customs-ai-demo-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-customs-ai-demo-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-customs-ai-demo-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=customs-ai-demo-v2)
- [Documentation](https://developer.dsv.com/guide-mydsv)
- [Documentation](https://developer.dsv.com/apicatalogue-generic)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(Customs%20v2.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Connect Booking API (SOAP)

SOAP BookingWebService covering land, air and ocean (LCL/FCL) bookings. Inherited from the DB Schenker estate that DSV acquired in 2025 and fronted through the same Azure API Management gateway as the REST products; the OpenAPI export models a single SOAP pass-through operation.

- **Human URL:** [https://developer.dsv.com/api-details#api=connect-api-booking-demo-v1](https://developer.dsv.com/api-details#api=connect-api-booking-demo-v1)
- **Base URL:** `https://api.dsv.com/connect-demo/booking/v1`

#### Tags

- Booking
- SOAP
- Road Freight
- Ocean Freight

#### Properties

- [OpenAPI](openapi/dsv-connect-api-booking-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-connect-api-booking-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-connect-api-booking-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=connect-api-booking-demo-v1)
- [Documentation](https://developer.dsv.com/guide-road)
- [Documentation](https://developer.dsv.com/apicatalogue-road)
- [Postman Collection](https://developer.dsv.com/content/BookingWebService%20SOAP%20API%20v1.3.postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV Connect Tracking API (SOAP)

SOAP TrackingWebService, described in DSV's own API Management metadata as the 'DB Schenker Standard Tracking SOAP API' — the legacy tracking contract carried over from the Schenker acquisition and re-published on developer.dsv.com.

- **Human URL:** [https://developer.dsv.com/api-details#api=connect-api-tracking-demo-v1](https://developer.dsv.com/api-details#api=connect-api-tracking-demo-v1)
- **Base URL:** `https://api.dsv.com/connect-demo/tracking/v1`

#### Tags

- Track and Trace
- SOAP
- Shipments

#### Properties

- [OpenAPI](openapi/dsv-connect-api-tracking-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-connect-api-tracking-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-connect-api-tracking-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=connect-api-tracking-demo-v1)
- [Documentation](https://developer.dsv.com/guide-road)
- [Documentation](https://developer.dsv.com/apicatalogue-road)
- [Postman Collection](https://developer.dsv.com/content/TrackingWebService%20SOAP%20API%20v1.3.postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV XPress Booking API

Creates express/parcel shipments and retrieves package labels. Carries per-package air waybill numbers, underlying express carrier codes and carrier tracking numbers, plus ADR/IATA dangerous-goods proper shipping names.

- **Human URL:** [https://developer.dsv.com/api-details#api=xpress-booking-v2](https://developer.dsv.com/api-details#api=xpress-booking-v2)
- **Base URL:** `https://api.dsv.com/xp/booking/v2`

#### Tags

- Parcel
- Express
- Booking
- Labels

#### Properties

- [OpenAPI](openapi/dsv-xpress-booking-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-xpress-booking-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-xpress-booking-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=xpress-booking-v2)
- [Documentation](https://developer.dsv.com/guide-xpress)
- [Documentation](https://developer.dsv.com/apicatalogue-xpress)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API(XPress%20Booking%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV XPress Tracking API

Express/parcel track-and-trace. Shipments are addressable by DSV shipment id or by air waybill number (GET /shipments/awb/{awb}); responses carry the underlying express carrier's own tracking number and tracking URL.

- **Human URL:** [https://developer.dsv.com/api-details#api=xpress-tracking-v2](https://developer.dsv.com/api-details#api=xpress-tracking-v2)
- **Base URL:** `https://api.dsv.com/xp/tracking/v2`

#### Tags

- Parcel
- Express
- Track and Trace

#### Properties

- [OpenAPI](openapi/dsv-xpress-tracking-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-xpress-tracking-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-xpress-tracking-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=xpress-tracking-v2)
- [Documentation](https://developer.dsv.com/guide-xpress)
- [Documentation](https://developer.dsv.com/apicatalogue-xpress)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API(XPress%20Tracking%20V2.0).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV XPress Quote API

Compares services and rates for express/parcel shipments against the customer's agreed tariff, including ADR, ADR-LQ, IATA DGR and lithium-battery dangerous-goods service codes.

- **Human URL:** [https://developer.dsv.com/api-details#api=xpress-comparator-v2](https://developer.dsv.com/api-details#api=xpress-comparator-v2)
- **Base URL:** `https://api.dsv.com/xp/comparator/v2`

#### Tags

- Parcel
- Express
- Quoting
- Rates

#### Properties

- [OpenAPI](openapi/dsv-xpress-comparator-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-xpress-comparator-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-xpress-comparator-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=xpress-comparator-v2)
- [Documentation](https://developer.dsv.com/guide-xpress)
- [Documentation](https://developer.dsv.com/apicatalogue-xpress)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API(XPress%20Quote%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV SCM Orders API

Submits and updates purchase orders in DSV's Supply Chain Management (eDC) platform, the order-management layer that sits above the forwarding products. Order and shipment records carry carrier SCAC codes, master and house bill of lading numbers and container numbers.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-public-api-v2](https://developer.dsv.com/api-details#api=edc-public-api-v2)
- **Base URL:** `https://api.dsv.com/om/v2`

#### Tags

- Supply Chain
- Orders
- SCM

#### Properties

- [OpenAPI](openapi/dsv-edc-public-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-public-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-public-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-public-api-v2)
- [Documentation](https://developer.dsv.com/guide-scm)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(eDC%20Orders%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV SCM Booking API

Creates and searches bookings in the DSV SCM (eDC) platform, including original/copy bill of lading counts, carrier SCAC and carrier contract numbers.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-booking-api-v2](https://developer.dsv.com/api-details#api=edc-booking-api-v2)
- **Base URL:** `https://api.dsv.com/om/bookings/v2`

#### Tags

- Supply Chain
- Booking
- SCM

#### Properties

- [OpenAPI](openapi/dsv-edc-booking-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-booking-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-booking-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-booking-api-v2)
- [Documentation](https://developer.dsv.com/guide-scm)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(eDC%20Booking%20V2.0%20-samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV SCM Shipments API

Searches shipments in the DSV SCM (eDC) platform by criteria, returning carrier, bill of lading and container detail.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-shipments-api-v2](https://developer.dsv.com/api-details#api=edc-shipments-api-v2)
- **Base URL:** `https://api.dsv.com/om/shipments/v2`

#### Tags

- Supply Chain
- Shipments
- SCM

#### Properties

- [OpenAPI](openapi/dsv-edc-shipments-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-shipments-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-shipments-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-shipments-api-v2)
- [Documentation](https://developer.dsv.com/guide-scm)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(eDC%20Shipments%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV SCM Load Plan API

Creates and manages load plans in the DSV SCM (eDC) platform across transport legs, each leg carrying carrier code, carrier SCAC and DSV's internal Dakosky carrier code.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-loadplan-api-v2](https://developer.dsv.com/api-details#api=edc-loadplan-api-v2)
- **Base URL:** `https://api.dsv.com/om/loadplans/v2`

#### Tags

- Supply Chain
- Load Planning
- SCM

#### Properties

- [OpenAPI](openapi/dsv-edc-loadplan-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-loadplan-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-loadplan-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-loadplan-api-v2)
- [Documentation](https://developer.dsv.com/guide-scm)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(eDC%20Loadplans%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV SCM eDocs API

Adds and retrieves electronic documents against SCM orders, bookings and shipments in the DSV eDC platform.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-edocs-api-v2](https://developer.dsv.com/api-details#api=edc-edocs-api-v2)
- **Base URL:** `https://api.dsv.com/om/edocs/v2`

#### Tags

- Supply Chain
- Documents
- SCM

#### Properties

- [OpenAPI](openapi/dsv-edc-edocs-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-edocs-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-edocs-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-edocs-api-v2)
- [Documentation](https://developer.dsv.com/guide-scm)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(eDC%20eDocs%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV SCM Events API

Writes milestone events into the DSV SCM (eDC) platform. Notably exposes POST /event/ServiceProvider so a third-party service provider — not only the account owner — can post events into DSV's chain, the clearest multi-party write path DSV publishes.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-events-api-v2](https://developer.dsv.com/api-details#api=edc-events-api-v2)
- **Base URL:** `https://api.dsv.com/om/events/v2`

#### Tags

- Supply Chain
- Events
- SCM
- Track and Trace

#### Properties

- [OpenAPI](openapi/dsv-edc-events-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-events-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-events-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-events-api-v2)
- [Documentation](https://developer.dsv.com/guide-scm)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(eDC%20Events%20V2.0%20-%20samples).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV NEOM API (eDC)

Customer-specific eDC surface published for the NEOM programme, covering orders, containers, harmonised commodity codes and house bill of lading references.

- **Human URL:** [https://developer.dsv.com/api-details#api=edc-neom-api-v2](https://developer.dsv.com/api-details#api=edc-neom-api-v2)
- **Base URL:** `https://api.dsv.com/om/neom/v2`

#### Tags

- Supply Chain
- SCM
- Projects

#### Properties

- [OpenAPI](openapi/dsv-edc-neom-api-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-edc-neom-api-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-edc-neom-api-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=edc-neom-api-v2)
- [Documentation](https://developer.dsv.com/guide-neom)
- [Documentation](https://developer.dsv.com/apicatalogue-scm)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV WMS Product Data API

Creates and updates product master data records in DSV Contract Logistics warehouse management.

- **Human URL:** [https://developer.dsv.com/api-details#api=warehousing-productdata-demo-v1](https://developer.dsv.com/api-details#api=warehousing-productdata-demo-v1)
- **Base URL:** `https://api.dsv.com/cl-demo/productdata/v1`

#### Tags

- Warehousing
- Contract Logistics
- Master Data

#### Properties

- [OpenAPI](openapi/dsv-warehousing-productdata-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-warehousing-productdata-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-warehousing-productdata-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=warehousing-productdata-demo-v1)
- [Documentation](https://developer.dsv.com/guide-contract-logistics)
- [Documentation](https://developer.dsv.com/apicatalogue-cl)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(WMS%20Product%20Data%20v1.0%20-%20samples%20with%20Bearer%20token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV WMS Inbound Notification API

Creates and updates inbound (pre-advice) orders for DSV Contract Logistics warehouses, with GS1 SSCC pallet/carton codes and container numbers on the line items.

- **Human URL:** [https://developer.dsv.com/api-details#api=warehousing-preadvice-demo-v1](https://developer.dsv.com/api-details#api=warehousing-preadvice-demo-v1)
- **Base URL:** `https://api.dsv.com/cl-demo/inbound/v1`

#### Tags

- Warehousing
- Contract Logistics
- Inbound

#### Properties

- [OpenAPI](openapi/dsv-warehousing-preadvice-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-warehousing-preadvice-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-warehousing-preadvice-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=warehousing-preadvice-demo-v1)
- [Documentation](https://developer.dsv.com/guide-contract-logistics)
- [Documentation](https://developer.dsv.com/apicatalogue-cl)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(WMS%20Inbound%20Notification%20v1.0%20-%20samples%20with%20Bearer%20Token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV WMS Delivery Notification API

Creates and updates outbound delivery notification orders for DSV Contract Logistics warehouses.

- **Human URL:** [https://developer.dsv.com/api-details#api=warehousing-despatch-demo-v1](https://developer.dsv.com/api-details#api=warehousing-despatch-demo-v1)
- **Base URL:** `https://api.dsv.com/cl-demo/delivery/v1`

#### Tags

- Warehousing
- Contract Logistics
- Outbound

#### Properties

- [OpenAPI](openapi/dsv-warehousing-despatch-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-warehousing-despatch-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-warehousing-despatch-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=warehousing-despatch-demo-v1)
- [Documentation](https://developer.dsv.com/guide-contract-logistics)
- [Documentation](https://developer.dsv.com/apicatalogue-cl)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(WMS%20Delivery%20Notification%20v1.0%20-%20samples%20with%20Bearer%20token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV WMS Inventory API

Retrieves inventory positions from DSV Contract Logistics warehouses, per product id or as a full inventory request.

- **Human URL:** [https://developer.dsv.com/api-details#api=warehousing-inventory-demo-v1](https://developer.dsv.com/api-details#api=warehousing-inventory-demo-v1)
- **Base URL:** `https://api.dsv.com/cl-demo/inventory/v1`

#### Tags

- Warehousing
- Contract Logistics
- Inventory

#### Properties

- [OpenAPI](openapi/dsv-warehousing-inventory-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-warehousing-inventory-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-warehousing-inventory-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=warehousing-inventory-demo-v1)
- [Documentation](https://developer.dsv.com/guide-contract-logistics)
- [Documentation](https://developer.dsv.com/apicatalogue-cl)
- [Postman Collection](https://developer.dsv.com/content/DSV%20API%20(WMS%20Inventory%20v1.0%20-%20samples%20with%20Bearer%20token).postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

### DSV WMS Order Status API

Returns the current status of a specific delivery or inbound order in DSV Contract Logistics warehouse management.

- **Human URL:** [https://developer.dsv.com/api-details#api=warehousing-status-demo-v1](https://developer.dsv.com/api-details#api=warehousing-status-demo-v1)
- **Base URL:** `https://api.dsv.com/cl-demo/status/v1`

#### Tags

- Warehousing
- Contract Logistics
- Status

#### Properties

- [OpenAPI](openapi/dsv-warehousing-status-demo-v1-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dsv-warehousing-status-demo-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dsv-warehousing-status-demo-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [API Reference](https://developer.dsv.com/api-details#api=warehousing-status-demo-v1)
- [Documentation](https://developer.dsv.com/guide-contract-logistics)
- [Documentation](https://developer.dsv.com/apicatalogue-cl)
- [Postman Collection](https://developer.dsv.com/content/WMS%20Notification%20Status%20v1.0%20API.postman_collection.zip) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Authentication](https://developer.dsv.com/oauth-guide)

## Common Properties

- [Website](https://www.dsv.com/)
- [Portal](https://developer.dsv.com/)
- [Documentation](https://developer.dsv.com/getting-started)
- [API Reference](https://developer.dsv.com/apicatalogue)
- [Signup](https://developer.dsv.com/signup)
- [Sign In](https://developer.dsv.com/signin)
- [Authentication](https://developer.dsv.com/oauth-guide)
- [Changelog](https://developer.dsv.com/release-notes)
- [Webhooks](https://developer.dsv.com/webhook-guide)
- [E D I](https://developer.dsv.com/getting-started-with-edi)
- [Documentation](https://developer.dsv.com/editransport)
- [Security](https://developer.dsv.com/edi-certificates)
- [Partners](https://developer.dsv.com/partner-integrations-and-plugins1)
- [Plugins](https://developer.dsv.com/ecommerce-shopify)
- [F A Q](https://developer.dsv.com/api_faq)
- [Support](https://developer.dsv.com/support-contact)
- [Terms of Service](https://developer.dsv.com/terms-and-conditions)
- [Privacy Policy](https://www.dsv.com/en/about-dsv/corporate-responsibility/policies/data-privacy)
- [LinkedIn](https://www.linkedin.com/company/dsv)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
