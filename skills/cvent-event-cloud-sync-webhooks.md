---
name: cvent-sync-webhooks
description: Keep a downstream system in sync with Cvent — subscribe to contact hooks, handle the callback, and reconcile with the Bulk API and change history when events are missed.
generated: '2026-08-13'
method: generated
source: openapi/_original/cvent-rest-apis-openapi.yaml
api: Cvent REST APIs
base_url: https://api-platform.cvent.com/ea
operations:
  - oauth2Token
  - createContactHook
  - ListContactHooks
  - updateContactHook
  - deleteContactHook
  - getChangeHistoryForASpecificContact
  - createBulkJob
  - uploadBulkJobData
  - runBulkJob
  - getBulkJobById
  - listBulkJobResult
  - getUsage
  - getUsageTier
scopes:
  - event/contacts:read
  - event/contacts:write
---

# Keep a downstream system in sync with Cvent

## 1. Understand what is machine-readable

Cvent documents **40 webhook message types** across attendees, attendee emails, contacts, events,
sessions, speakers, meeting requests and manual sync — see
`asyncapi/cvent-event-cloud-webhooks.yml`. Only **one** of them has a payload contract in the
OpenAPI: the callback declared on `POST /contacts/hooks`. There is no AsyncAPI document. For every
other message type you must read the docs page and code defensively against the payload.

## 2. Subscribe

`createContactHook` — `POST /contacts/hooks`
`ListContactHooks` — `GET /contacts/hooks`
`updateContactHook` — `PUT /contacts/hooks/{id}`
`deleteContactHook` — `DELETE /contacts/hooks/{id}`

Your callback endpoint declares how Cvent should authenticate to *you*, using one of two schemes
from the spec:

- `CallbackApiKeyAuth` — Cvent sends an `Authorization` header carrying your API key.
- `CallbackBasicAuth` — Cvent sends HTTP Basic.

Both are for Cvent calling you. Neither can be used to call Cvent.

## 3. Handle the callback

Return 2xx quickly and process asynchronously. Assume at-least-once delivery: de-duplicate on the
record id plus the modification timestamp, because Cvent provides no delivery-id you can key on.

## 4. Reconcile — do not trust the stream alone

Webhooks drop. Two published recovery paths:

**Change history** — `getChangeHistoryForASpecificContact` — `GET /contacts/{contactId}/history`
for a targeted repair of one record.

**Manual sync** — an operator can re-emit a record from the Cvent UI
(`manual-event`, `manual-session`, `manual-speaker`, `manual-attendee`,
`manual-attendee-abandoned`). This is a human action, not an API call.

**Bulk API** — for a full re-baseline:

1. `createBulkJob` — `POST /bulk-jobs`
2. `uploadBulkJobData` — `POST /bulk-jobs/{id}/data`
3. `runBulkJob` — `POST /bulk-jobs/{id}/run`
4. `getBulkJobById` — `GET /bulk-jobs/{id}` until terminal
5. `listBulkJobResult` — `GET /bulk-jobs/{id}/results`

**Read this before trusting bulk results.** Cvent documents that when the target operation returns
`207 Multi-Status`, the `failed` flag on the result record reflects only the top-level HTTP status
and will be `false` even when individual items failed. You must inspect each result record's `data`
field yourself. A sync that branches on `failed` alone will silently lose rows.

Two bulk-specific errors exist: `JobLimitExceeded` (too many concurrent jobs) and
`DataLimitExceeded` (too many data records in one job).

## 5. Watch your budget

`getUsageTier` — `GET /usage/tier` — read your account's tier rather than hard-coding it; Cvent
states limits may change.
`getUsage` — `GET /usage` — poll consumption.

A reconciliation sweep is the fastest way to burn a daily quota. On the Free tier that is 1,000
calls per day, at 2 calls per second. Check `X-RateLimit-Remaining` on every response and stop
before you hit the wall, because every rejected request still counts against the quota.
