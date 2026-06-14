# Ably GraphQL Schema

Conceptual GraphQL schema for the [Ably](https://ably.com/) realtime messaging platform.
Covers both the **Platform API** (`rest.ably.io`) and the **Control API** (`control.ably.net/v1`).

- REST API docs: <https://ably.com/docs/api/rest-api>
- Control API docs: <https://ably.com/docs/api/control-api>
- GitHub: <https://github.com/ably>

---

## Overview

Ably provides realtime pub/sub messaging, presence, push notifications, message history, and
account management via REST and WebSocket transports. This GraphQL schema provides a unified
query surface across both API surfaces.

---

## Schema file

See [`ably-schema.graphql`](./ably-schema.graphql) for the full schema.

---

## Type inventory

### Scalars
| Scalar | Purpose |
|--------|---------|
| `DateTime` | ISO-8601 timestamps |
| `JSON` | Arbitrary JSON payload |
| `Long` | 64-bit integers (timestamps in ms, byte counts) |

### Enums (9)
| Enum | Values |
|------|--------|
| `PresenceAction` | ABSENT, PRESENT, ENTER, LEAVE, UPDATE |
| `MessageEncoding` | UTF8, JSON, BASE64, CIPHER_PLUS_BASE64, CIPHER_PLUS_UTF8 |
| `DevicePlatform` | IOS, ANDROID, BROWSER |
| `PushState` | ACTIVE, FAILED, UNREGISTERED |
| `RuleType` | HTTP, AMQP, KINESIS, KAFKA, SQS, PULSAR, ZAPIER, CLOUDMATICS |
| `QueueRegion` | US_EAST_1, EU_WEST_1, AP_SOUTHEAST_1, AP_NORTHEAST_1 |
| `StatsInterval` | MINUTE, HOUR, DAY, MONTH |
| `ChannelState` | INITIALIZED, ATTACHING, ATTACHED, DETACHING, DETACHED, SUSPENDED, FAILED |
| `ConnectionState` | INITIALIZED, CONNECTING, CONNECTED, DISCONNECTED, SUSPENDED, CLOSING, CLOSED, FAILED |
| `KeyStatus` | ENABLED, REVOKED |
| `AppStatus` | ENABLED, DISABLED |

### Object types (65+)

#### App & Account
- `App` — top-level app resource; links to keys, stats, namespaces, queues, rules
- `AppDetails` — full app metadata including account ID, TLS-only flag, timestamps
- `AppKey` — API key attached to an app; carries capability and revocation info
- `AppStats` — inbound/outbound/persisted message stats and connection counts

#### Key
- `Key` — API key record
- `KeyDetails` — full key metadata including revocable-tokens flag
- `KeyCapability` — channel list and permission set for a key

#### Channel
- `Channel` — pub/sub channel with presence, occupancy, and history sub-fields
- `ChannelDetails` — channel metadata including global-master and region
- `ChannelStatus` — isActive flag plus current occupancy metrics
- `ChannelPresence` — list of present members with total count
- `ChannelMetadata` — channel metadata envelope used by the Ably Meta channels
- `ChannelOccupancy` — occupancy metrics wrapper
- `OccupancyMetrics` — connections, publishers, subscribers, presence counts

#### Message
- `Message` — a pub/sub message with name, data, encoding, extras, and timestamp
- `MessageDetails` — full message metadata
- `MessageName` — wrapper for a message event name string
- `MessageData` — raw string plus parsed JSON representation

#### Presence
- `PresenceMessage` — presence event with action, clientId, connectionId, data
- `PresenceDetails` — full presence event metadata
- `PresenceMember` — current presence state for a single client

#### History
- `History` — channel history wrapper
- `HistoryDetails` — parameters used to fetch history (start, end, limit, direction)
- `HistoryPage` — paginated history result with hasNext flag

#### Token & Auth
- `Token` — an Ably token with expiry and capability
- `TokenDetails` — full token metadata (issued/expires as Long ms)
- `TokenCapability` — raw JSON capability plus convenience channel/permission lists
- `TokenExpiry` — token expiry details including TTL
- `AuthRequest` — HMAC-signed token request
- `AuthDetails` — token request metadata

#### Queue
- `Queue` — AMQP/STOMP queue resource
- `QueueDetails` — full queue config including AMQP/STOMP endpoints and stats
- `QueueAmqpConfig` — AMQP URI and queue name
- `QueueStompConfig` — STOMP URI, host, and destination
- `QueueMessageStats` — ready/unacknowledged/total message counts
- `QueueStats` — publish, delivery, and acknowledgement rates
- `QueueMessage` — a message retrieved from a queue
- `QueueRule` — rule that links a channel filter to a queue

#### Rule (Integration)
- `Rule` — integration rule (HTTP, AMQP, Kinesis, etc.)
- `RuleDetails` — full rule metadata including timestamps
- `RuleSource` — channel filter and source type
- `RuleTarget` — URL, headers, signing key, envelope, and format
- `RuleHeader` — name/value header pair

#### Push Notifications
- `PushChannel` — channel with push subscriptions
- `PushTarget` — transport type and push details
- `PushPayload` — notification + data envelope for push delivery
- `PushNotification` — push notification content (title, body, icon, sound)
- `PushDetails` — registration/device token and recipient type
- `PushState` — per-device push state and error reason
- `PushChannelSubscription` — binding between a channel and a device/client

#### Device Registration
- `DeviceRegistration` — registered push device
- `DeviceDetails` — full device metadata including push state
- `DevicePushDetails` — recipient, state, and error for a device's push config

#### Stats
- `Stats` — stats record for a given interval
- `StatsDetails` — message count breakdown (all, presence)
- `MessageCount` — count and data (bytes) pair
- `Interval` — interval descriptor
- `IntervalDetails` — start/end timestamps for an interval

#### Connection
- `Connection` — Ably connection state
- `ConnectionDetails` — key, max sizes, TTL, idle interval, server ID

#### Namespace
- `Namespace` — channel namespace resource
- `NamespaceDetails` — full namespace config (persisted, authenticated, push-enabled, TLS-only)

#### API Key (Control API alias)
- `APIKey` — Control API view of an app key including revocable-tokens flag

#### Webhook
- `Webhook` — HTTP webhook integration
- `WebhookDetails` — full webhook metadata including timestamps
- `WebhookEvent` — event name and optional filter

#### Error
- `ErrorInfo` — Ably error envelope (code, statusCode, message, href)

---

## Query examples

### List channels in an app
```graphql
query {
  channels(appId: "my-app-id") {
    id
    name
    status {
      isActive
      occupancy {
        metrics {
          publishers
          subscribers
          presenceMembers
        }
      }
    }
  }
}
```

### Fetch recent history for a channel
```graphql
query {
  channelHistory(channelName: "my-channel", limit: 100, direction: "backwards") {
    items {
      id
      name { value }
      data { raw }
      timestamp
    }
    hasNext
  }
}
```

### Publish a message
```graphql
mutation {
  publishMessage(channelName: "my-channel", name: "update", data: { count: 42 }) {
    id
    timestamp
  }
}
```

### Create an app key (Control API)
```graphql
mutation {
  createAppKey(appId: "my-app-id", name: "backend-key", capability: { "*": ["publish", "subscribe"] }) {
    id
    key
    status
  }
}
```

### Subscribe to channel messages
```graphql
subscription {
  channelMessages(channelName: "my-channel") {
    id
    name { value }
    data { raw parsed }
    timestamp
    clientId
  }
}
```
