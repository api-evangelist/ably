# Ably

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

Ably is a realtime messaging platform offering pub/sub, presence, push notifications, chat, LiveSync, and integrations over WebSocket and HTTP. Ably publishes its OpenAPI specifications publicly via the ably/open-specs GitHub repository, with separate specs for the Platform API (REST messaging surface) and the Control API (account, app, and key management).

**Areas:** Real-Time · WebSocket · Pub/Sub · Messaging · Streaming · Push Notifications · Chat · LiveSync

## Ably on APIs.io

Everything profiled for Ably is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/ably/](https://apis.io/providers/ably/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [Ably Apps API](https://apis.io/apis/ably/ably-apps-api/) — The apps API from Ably — 3 operation(s) for apps.
- [Ably Authentication API](https://apis.io/apis/ably/ably-authentication-api/) — The Authentication API from Ably — 1 operation(s) for authentication.
- [Ably History API](https://apis.io/apis/ably/ably-history-api/) — The History API from Ably — 2 operation(s) for history.
- [Ably Keys API](https://apis.io/apis/ably/ably-keys-api/) — The keys API from Ably — 3 operation(s) for keys.
- [Ably Namespaces API](https://apis.io/apis/ably/ably-namespaces-api/) — The namespaces API from Ably — 2 operation(s) for namespaces.
- [Ably Publishing API](https://apis.io/apis/ably/ably-publishing-api/) — The Publishing API from Ably — 1 operation(s) for publishing.
- [Ably Push API](https://apis.io/apis/ably/ably-push-api/) — The Push API from Ably — 6 operation(s) for push.
- [Ably Queues API](https://apis.io/apis/ably/ably-queues-api/) — The queues API from Ably — 2 operation(s) for queues.
- [Ably Rules API](https://apis.io/apis/ably/ably-rules-api/) — The rules API from Ably — 2 operation(s) for rules.
- [Ably Stats API](https://apis.io/apis/ably/ably-stats-api/) — The Stats API from Ably — 2 operation(s) for stats.
- [Ably Status API](https://apis.io/apis/ably/ably-status-api/) — The Status API from Ably — 3 operation(s) for status.
- [Ably Tokens API](https://apis.io/apis/ably/ably-tokens-api/) — The tokens API from Ably — 1 operation(s) for tokens.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Ably Realtime Protocol](https://apis.io/asyncapis/ably/ably-asyncapi/)

#### Event channels (3)

Individual events and webhooks the provider emits.

- [{channelName}](https://apis.io/channels/ably/channelname/)
- [/](https://apis.io/channels/ably/connection/)
- [/sse](https://apis.io/channels/ably/sse/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/ably/](https://apis.io/graphqls/ably/ably-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Ably Agentic Access](https://apis.io/agentic-access/ably/ably-agentic-access/)

#### JSON Schema (79)

The data models the API reads and writes.

- [amqp_external_rule_patch](https://apis.io/schemas/ably/ably-amqp-external-rule-patch/)
- [amqp_external_rule_post](https://apis.io/schemas/ably/ably-amqp-external-rule-post/)
- [amqp_external_rule_response](https://apis.io/schemas/ably/ably-amqp-external-rule-response/)
- [amqp_rule_patch](https://apis.io/schemas/ably/ably-amqp-rule-patch/)
- [amqp_rule_post](https://apis.io/schemas/ably/ably-amqp-rule-post/)
- [amqp_rule_response](https://apis.io/schemas/ably/ably-amqp-rule-response/)
- [app_patch](https://apis.io/schemas/ably/ably-app-patch/)
- [app_pkcs12](https://apis.io/schemas/ably/ably-app-pkcs12/)
- [app_post](https://apis.io/schemas/ably/ably-app-post/)
- [app_response](https://apis.io/schemas/ably/ably-app-response/)
- [aws_access_keys](https://apis.io/schemas/ably/ably-aws-access-keys/)
- [aws_access_keys_response](https://apis.io/schemas/ably/ably-aws-access-keys-response/)
- [aws_assume_role](https://apis.io/schemas/ably/ably-aws-assume-role/)
- [aws_kinesis_rule_patch](https://apis.io/schemas/ably/ably-aws-kinesis-rule-patch/)
- [aws_kinesis_rule_post](https://apis.io/schemas/ably/ably-aws-kinesis-rule-post/)
- [aws_kinesis_rule_response](https://apis.io/schemas/ably/ably-aws-kinesis-rule-response/)
- [aws_lambda_rule_patch](https://apis.io/schemas/ably/ably-aws-lambda-rule-patch/)
- [aws_lambda_rule_post](https://apis.io/schemas/ably/ably-aws-lambda-rule-post/)
- [aws_lambda_rule_response](https://apis.io/schemas/ably/ably-aws-lambda-rule-response/)
- [aws_sqs_rule_patch](https://apis.io/schemas/ably/ably-aws-sqs-rule-patch/)
- [aws_sqs_rule_post](https://apis.io/schemas/ably/ably-aws-sqs-rule-post/)
- [aws_sqs_rule_response](https://apis.io/schemas/ably/ably-aws-sqs-rule-response/)
- [azure_function_rule_patch](https://apis.io/schemas/ably/ably-azure-function-rule-patch/)
- [azure_function_rule_post](https://apis.io/schemas/ably/ably-azure-function-rule-post/)
- [azure_function_rule_response](https://apis.io/schemas/ably/ably-azure-function-rule-response/)
- …and 54 more published on APIs.io

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Ably Structure](https://apis.io/json-structure/ably/ably-structure/)

#### Examples (2)

Example requests and responses.

- [Ably Requestaccesstoken Example](https://apis.io/examples/ably/ably-requestaccesstoken-example/)
- [Ably Subscribepushdevicetochannel Example](https://apis.io/examples/ably/ably-subscribepushdevicetochannel-example/)

#### Collections (14)

Postman and Open Collection request collections.

- [Control API v1 apps API](https://apis.io/collections/ably/open-ably-apps-api/)
- [Control API v1 apps Authentication API](https://apis.io/collections/ably/open-ably-authentication-api/)
- [Control API v1](https://apis.io/collections/ably/open-ably-control-api/)
- [Control API v1 apps History API](https://apis.io/collections/ably/open-ably-history-api/)
- [Control API v1 apps keys API](https://apis.io/collections/ably/open-ably-keys-api/)
- [Control API v1 apps namespaces API](https://apis.io/collections/ably/open-ably-namespaces-api/)
- [Platform API](https://apis.io/collections/ably/open-ably-platform-api/)
- [Control API v1 apps Publishing API](https://apis.io/collections/ably/open-ably-publishing-api/)
- [Control API v1 apps Push API](https://apis.io/collections/ably/open-ably-push-api/)
- [Control API v1 apps queues API](https://apis.io/collections/ably/open-ably-queues-api/)
- [Control API v1 apps rules API](https://apis.io/collections/ably/open-ably-rules-api/)
- [Control API v1 apps Stats API](https://apis.io/collections/ably/open-ably-stats-api/)
- [Control API v1 apps Status API](https://apis.io/collections/ably/open-ably-status-api/)
- [Control API v1 apps tokens API](https://apis.io/collections/ably/open-ably-tokens-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Ably — asyncapi rules](https://apis.io/rules/ably/ably-asyncapi-spectral-rules/)
- [Ably — jsonschema rules](https://apis.io/rules/ably/ably-jsonschema-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Ably Authentication](https://apis.io/security/ably/ably-authentication/)
- [Ably Domain Security](https://apis.io/security/ably/ably-domain-security/)
- [Ably Trust Center](https://apis.io/security/ably/ably-trust-center/)
- [Ably Vulnerability Disclosure](https://apis.io/security/ably/ably-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Ably Plans Pricing](https://apis.io/plans/ably/ably-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Ably Rate Limits](https://apis.io/rate-limits/ably/ably-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Ably Finops](https://apis.io/finops/ably/ably-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.ably.com/)
- [Documentation](https://ably.com/docs)
- [Pricing](https://ably.com/pricing)
- [Blog](https://voltaire.ably.com/blog/rss.xml)
- [Status](https://status.ably.com/)

## API Evangelist rating

**Kin Score 42.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 57.8 |
| Contract governance | 13.6 |
| Operational transparency | 39.5 |
| Developer ergonomics | 33.3 |
| Access clarity | 26.3 |

**Agent readiness 26.8** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 22.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/ably/](https://apis.io/providers/ably/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Ably: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/ably/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
