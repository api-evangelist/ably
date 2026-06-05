# Ably (ably)

Ably is a realtime messaging platform offering pub/sub, presence, push notifications, chat, LiveSync, and integrations over WebSocket and HTTP. Ably publishes its OpenAPI specifications publicly via the ably/open-specs GitHub repository, with separate specs for the Platform API (REST messaging surface) and the Control API (account, app, and key management).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ably/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ably/refs/heads/main/apis.yml)

## Tags

- Realtime
- WebSockets
- Pub/Sub
- Messaging
- Streaming
- Push Notifications
- Chat
- LiveSync

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-29

## APIs

### Ably Platform API

The Ably Platform API exposes pub/sub messaging, presence, history, push notifications, and channel/stats endpoints over REST and WebSocket. WebSocket realtime connections use realtime.ably.io. Authentication via Basic auth (key) or token-based.

- **Human URL:** [https://ably.com/docs/api/rest-api](https://ably.com/docs/api/rest-api)
- **Base URL:** `https://rest.ably.io`

#### Tags

- Pub/Sub
- Messaging
- WebSockets
- REST
- Streaming

#### Properties

- [Documentation](https://ably.com/docs/api/rest-api)
- [OpenAPI](openapi/ably-platform-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ably-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ably-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/ably-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Web Socket](wss://realtime.ably.io)

### Ably Control API

The Ably Control API manages accounts, apps, API keys, namespaces, queues, integration rules, and webhooks. Used to provision and operate Ably resources programmatically. Authentication via personal access token (PAT).

- **Human URL:** [https://ably.com/docs/api/control-api](https://ably.com/docs/api/control-api)
- **Base URL:** `https://control.ably.net/v1`

#### Tags

- Account Management
- Apps
- Keys
- Namespaces
- Integrations

#### Properties

- [Documentation](https://ably.com/docs/api/control-api)
- [OpenAPI](openapi/ably-control-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ably-control-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ably-control-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/ably-realtime)
- [Portal](https://ably.com/)
- [Documentation](https://ably.com/docs)
- [Pricing](https://ably.com/pricing)
- [Git Hub](https://github.com/ably)
- [Status Page](https://status.ably.com/)
- [Plans](plans/ably-plans-pricing.yml)
- [Rate Limits](rate-limits/ably-rate-limits.yml)
- [Fin Ops](finops/ably-finops.yml)
- [L L Ms Txt](https://ably.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
