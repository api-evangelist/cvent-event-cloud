---
name: cvent-register-attendee
description: Register a contact as an attendee on a Cvent event, choosing the correct registration path and type, then confirm the registration landed.
generated: '2026-08-13'
method: generated
source: openapi/_original/cvent-rest-apis-openapi.yaml
api: Cvent REST APIs
base_url: https://api-platform.cvent.com/ea
operations:
  - oauth2Token
  - getEvents
  - listRegistrationPaths
  - listRegistrationTypes
  - listContacts
  - createContacts
  - createAttendee
  - getAttendeeById
scopes:
  - event/events:read
  - event/attendees:read
  - event/attendees:write
  - event/contacts:read
  - event/contacts:write
---

# Register an attendee on a Cvent event

Every operationId below is verbatim from Cvent's published OpenAPI. Do not invent operations.

## 0. Pick the right host

`https://api-platform.cvent.com/ea` for North American accounts,
`https://api-platform-eur.cvent.com/ea` for European ones. There is no cross-region read — using
the wrong host returns 404 for records that exist.

## 1. Get a token

`oauth2Token` — `POST /oauth2/token`

Send `Authorization: Basic base64(client_id:client_secret)`,
`Content-Type: application/x-www-form-urlencoded`, body `grant_type=client_credentials`.
The token is a Bearer token valid for 3600 seconds. Cache it; do not fetch one per request.

## 2. Find the event

`getEvents` — `GET /events?filter=...`

Filter syntax is `filter='field' comparisonType 'value'`, e.g. `filter=eventName eq "Annual Summit"`.
Wrap the value in double quotes when it contains an apostrophe. Page with `limit` and `token`;
read `paging.nextToken` and stop when it is absent.

For a large or complex filter use `getEventsPostFilters` — `POST /events/filter` — which takes the
same predicate in a body instead of a query string.

## 3. Resolve the registration path and type

`listRegistrationPaths` — `GET /events/{id}/registration-paths`
`listRegistrationTypes` — `GET /events/{id}/registration-types`

An attendee cannot be created without a valid registration path for that event. Resolve both before
writing anything.

## 4. Find or create the contact

`listContacts` — `GET /contacts?filter=email eq "person@example.com"`

If nothing comes back, `createContacts` — `POST /contacts`. Cvent's contact record is
account-level and reused across events; creating a duplicate contact is the most common mistake in
this flow. Search by email first, always.

## 5. Create the attendee

`createAttendee` — `POST /attendees`

Reference the event, the contact, the registration path and the registration type resolved above.

**There is no idempotency key on this API.** `POST /attendees` is not safe to blind-retry: a retry
after a timeout can create a second registration. If a create times out, re-query with
`listAttendees` filtered on the contact and event before retrying.

## 6. Confirm

`getAttendeeById` — `GET /attendees/{id}`

## Error handling

| Status | Meaning | Do |
| --- | --- | --- |
| 400 | Invalid filter or body | Read `details[]`; fix the input. Never retry unchanged. |
| 401 | Token missing or expired (3600s) | Re-run step 1, retry once. |
| 403 | Scope or entitlement missing | Stop. Fix the application's scopes in the Cvent console. |
| 404 | Wrong id, or wrong regional host | Check the host before the id. |
| 429 | Rate limit or daily quota | See below. |

On 429, read the message. "Limit Exceeded" means the daily quota is gone — stop until after
midnight UTC; retrying burns quota because rejected requests still count. "Too Many Requests" means
the per-second rate — wait 2 seconds plus 1–1000 ms of jitter, double each attempt to a 16-second
ceiling, give up after five. There is no `Retry-After` header; use `X-RateLimit-Reset`.

Errors are `application/json` shaped `{code, message, target, details[]}` — not RFC 9457
problem+json.
