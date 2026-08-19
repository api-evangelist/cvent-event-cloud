---
name: cvent-build-agenda
description: Build an event agenda in Cvent — create sessions, categorise them, attach speakers and session documents, then read enrollment and attendance back.
generated: '2026-08-13'
method: generated
source: openapi/_original/cvent-rest-apis-openapi.yaml
api: Cvent REST APIs
base_url: https://api-platform.cvent.com/ea
operations:
  - oauth2Token
  - listSessionsCategories
  - createSessionCategory
  - createSession
  - listSessions
  - getSessionById
  - updateSession
  - addSessionLocation
  - createSpeaker
  - listSpeakers
  - addSpeakerToSession
  - listSessionSpeakers
  - addSessionDoc
  - listSessionDocs
  - createSessionEnrollment
  - listSessionsEnrollment
  - sessionCheckIn
  - listSessionsAttendance
scopes:
  - event/sessions:read
  - event/sessions:write
  - event/speakers:read
  - event/speakers:write
---

# Build and run a Cvent event agenda

Every operationId is verbatim from Cvent's published OpenAPI.

## 1. Token

`oauth2Token` — `POST /oauth2/token`, HTTP Basic client credentials, `grant_type=client_credentials`.
Valid 3600 seconds.

## 2. Categories first

`listSessionsCategories` — `GET /session-categories`
`createSessionCategory` — `POST /session-categories`

Categories are account-level and reused across events. Look before you create.

## 3. Create sessions

`createSession` — `POST /sessions`
`listSessions` — `GET /sessions?filter=...`
`getSessionById` — `GET /sessions/{id}`
`updateSession` — `PUT /sessions/{id}`

For bulk reads with a long predicate use `listSessionsPostFilters` — `POST /sessions/filter`.

## 4. Locations

`getSessionLocation` — `GET /events/{id}/session-locations`
`addSessionLocation` — `POST /events/{id}/session-locations`

Note the shape change: locations are addressed under the **event**, not under the session.

## 5. Speakers

`listSpeakers` — `GET /speakers?filter=...` (search before creating — speakers are account-level)
`createSpeaker` — `POST /speakers`
`addSpeakerToSession` — `PUT /sessions/{id}/speakers/{speakerId}`
`listSessionSpeakers` — `GET /sessions/{id}/speakers`
`listSpeakerSessions` — `GET /speakers/{id}/sessions` (the reverse lookup)

`addSpeakerToSession` is a `PUT` on a composite key, so it **is** safely retryable — unlike the
`POST` creates in this flow, which have no idempotency key.

## 6. Session documents

`addSessionDoc` — `PUT /sessions/{id}/docs/{fileId}`
`listSessionDocs` — `GET /sessions/{id}/docs`
`getSessionDoc` — `GET /sessions/{id}/docs/{fileId}`

Upload the file through the File surface first, then relate it by `fileId`. Again a `PUT` on a
composite key: retry-safe.

## 7. Enrollment and attendance

Enrollment is intent; attendance is fact. They are separate.

`createSessionEnrollment` — `POST /sessions/{id}/enrollment/{attendeeId}`
`listSessionsEnrollment` — `GET /sessions/enrollment`
`sessionCheckIn` — `POST /sessions/{id}/check-in`
`listSessionsAttendance` — `GET /sessions/attendance`
`deleteSessionAttendance` — `DELETE /sessions/{id}/attendance/{attendeeId}`

## Conventions that apply throughout

- Page with `limit` + `token`; follow `paging.nextToken` until absent, and tolerate a final empty
  `data` array — Cvent documents that it happens when the total divides evenly by the limit.
- All timestamps are ISO 8601 UTC with a `Z` offset.
- 456 of 458 operations declare a 429. Back off per
  `rate-limits/cvent-event-cloud-rate-limits.yml`; there is no `Retry-After` header.
- No `Idempotency-Key` exists anywhere in this API. Treat every `POST` as at-least-once and
  re-query before retrying one.
