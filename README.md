# Cvent Event Cloud

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

Cvent Event Cloud is the event management product line of the Cvent Platform. It supports the full event lifecycle: event creation, registration, marketing, agenda and session management, mobile event apps, onsite check-in, virtual and hybrid event delivery via the Attendee Hub, surveys, and analytics. Cvent publishes its own OpenAPI specification in public git at github.com/cvent/rest-sdks (cvent-public-spec/openapi.yaml) — 346 paths, 458 operations, 1,302 schemas — and generates its first-party TypeScript, .NET and Java SDKs from it with Speakeasy, applying five published OpenAPI Overlay 1.0.0 documents in the process. Access is OAuth 2.0, client credentials for server-to-server and authorization code for planner administrators, with the token endpoint at api-platform.cvent.com/ea/oauth2/token and 235 declared scopes. Regional bases split North America (api-platform.cvent.com/ea) from Europe (api-platform-eur.cvent.com/ea) with no cross-region read. Cvent also runs a live remote MCP server at mcp.cvent.com/mcp secured with OAuth 2.1 and PKCE, publishes a dated biweekly changelog, a 40-message webhook catalogue, SCIM 2.0 user provisioning, and a Custom Widgets browser SDK for embedding components in Cvent-hosted event pages.

**Areas:** Attendee Hub · Attendees · Bulk · Contacts · Event Cloud · Event Management · Event Marketing · Event · Exhibitors · Hybrid Events · MCP · Authentication

## Cvent Event Cloud on APIs.io

Everything profiled for Cvent Event Cloud is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cvent-event-cloud/](https://apis.io/providers/cvent-event-cloud/)** — or go straight to one of the APIs or properties below.

### APIs (55)

- [Cvent Platform REST API (Event Cloud)](https://apis.io/apis/cvent-event-cloud/rest-api/) — RESTful API for managing events, contacts, registrations, attendees, sessions, speakers, exhibitors, surveys, webhooks, and Attendee Hub data. Uses OAuth…
- [Cvent Event Cloud Attendees API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-attendees-api/) — Event registrations and attendees
- [Cvent Event Cloud Contacts API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-contacts-api/) — Contact/address book
- [Cvent Event Cloud Events API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-events-api/) — Event lifecycle and configuration
- [Cvent Event Cloud Sessions API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-sessions-api/) — Agenda sessions
- [Cvent Event Cloud Appointments API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-appointments-api/) — An appointment is a meeting scheduled between two or more parties. These APIs allow you to get information about your Cvent Appointments: appointment…
- [Cvent Event Cloud Attendee Activities API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-attendee-activities-api/) — The Attendee Activities API gives valuable insight into your customer's experience at your Cvent event. Now, you can get a fuller picture of your customer's…
- [Cvent Event Cloud Attendee Insights API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-attendee-insights-api/) — The Attendee Insights feature provides valuable information about your event attendees. It assists planners, marketers, and exhibitors in targeting…
- [Cvent Event Cloud Attendee Messages API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-attendee-messages-api/) — These APIs retrieve and manage attendee messages—communications exchanged between attendees within channels. Channels are virtual spaces created for…
- [Cvent Event Cloud Audience Segments API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-audience-segments-api/) — Audience Segments allow planners to segment their attendees into groups and better manage the attendee experience based on their defined segments. Audience…
- [Cvent Event Cloud Authentication API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-authentication-api/) — Endpoints for obtaining, refreshing, and validating OAuth2 access tokens.
- [Cvent Event Cloud Badge Print Job API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-badge-print-job-api/) — Badge print jobs can be scheduled to a printer pool, so a printer in the printer pool can consume the job and print the badge.
- [Cvent Event Cloud Badge Printer Pools API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-badge-printer-pools-api/) — Badge printer pools are set up from Cvent UI. You can use this API to retrieve badge printer pools.
- [Cvent Event Cloud Budget API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-budget-api/) — Budget is an event feature used to organize spending and track [allocations](https://support.cvent.com/s/communityarticle/Setting-Up-Budget-Allocations).…
- [Cvent Event Cloud Bulk API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-bulk-api/) — The Bulk API provides a simple interface to upload large amounts of data into Cvent. The API processes the uploaded data asynchronously making API calls on…
- [Cvent Event Cloud Campaigns API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-campaigns-api/) — Planners use eMarketing campaigns to contact an audience, such as newsletters, press releases, or product updates. Campaign emails are used as newsletters,…
- [Cvent Event Cloud Card Tokens API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-card-tokens-api/) — **Card Tokenization**: Tokenization is the process Cvent uses to collect sensitive card details and personally identifiable information (PII), directly from…
- [Cvent Event Cloud Compliance API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-compliance-api/) — These API's provide compliance support for regulated industries. **Communication Compliance** lets you view communication activities across your account.…
- [Cvent Event Cloud Custom Fields API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-custom-fields-api/) — Custom Fields are created by event planners to track important information about specific objects like events, contacts, or sessions. Use these APIs to…
- [Cvent Event Cloud Discounts API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-discounts-api/) — Discounts provide a way to reduce the cost of event registration items. Use these APIs to manage event discounts, including creating, updating, and linking…
- [Cvent Event Cloud Emails API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-emails-api/) — Event planners use emails to invite registrants, market their events and request feedback from attendees. Use these APIs to get historical data about your…
- [Cvent Event Cloud Event Credits API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-event-credits-api/) — Event Credits reward attendees for participating in your events. Planners can award credits for the entire event, specific sessions, or both. You can also…
- [Cvent Event Cloud Event Features API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-event-features-api/) — EventFeatures related APIs
- [Cvent Event Cloud Event Role API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-event-role-api/) — Event roles are event specific permission sets for your organization's users. Use these APIs to retrieve, create, update, and delete event role assignments…
- [Cvent Event Cloud Event Travel API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-event-travel-api/) — Event travel lets planners capture air & hotel requests from attendees and track air actuals, hotel reservations and alternate travel answers at your event.…
- [Cvent Event Cloud Events+ Hub API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-events-hub-api/) — An Events+ Hub persists basic information needed to assign an owner and optionally customize the public presentation.
- [Cvent Event Cloud Exhibitor API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-exhibitor-api/) — * **Exhibitor -** An exhibitor is an organization that is sponsoring or exhibiting at your event. This API allows you to get information about your…
- [Cvent Event Cloud Exhibitor Content API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-exhibitor-content-api/) — Exhibitor Content operations for an exhibitor. This API allows you to upload & get exhibitor content data such as files, weblinks.
- [Cvent Event Cloud Exhibitor Team API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-exhibitor-team-api/) — * **Exhibitor Admin -** Exhibitor Admins are administrators that have access to the exhibitor portal. In the portal, they are able to complete pre-event…
- [Cvent Event Cloud File API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-file-api/) — Allows you to upload files and get file location using the file ID. File ID can be used with other APIs to associate the file to an entity. For example: *…
- [Cvent Event Cloud Hooks API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-hooks-api/) — These APIs allow you to create hooks. When triggered, a hook sends a request to your service to get updated data related to the related Cvent object. For…
- [Cvent Event Cloud Leads API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-leads-api/) — * **Leads -** Leads include leads gathered by LeadCapture, Appointments, and Inbound Leads. Use this API to get information for the lead and how it was…
- [Cvent Event Cloud Process Form API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-process-form-api/) — Process forms automate data collection and notifications related to planning and executing events. Process form submissions are responses to a specific…
- [Cvent Event Cloud Seating API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-seating-api/) — Seating lets you plan seating at your events by configuring tables and assigning seats to your attendees. The seating APIs allow you to create, update, and…
- [Cvent Event Cloud Signatures API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-signatures-api/) — Retrieves Check-In & Check-Out Signatures Of Attendees
- [Cvent Event Cloud Speakers API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-speakers-api/) — Speakers are individuals presenting at your event's session(s). Use Speaker APIs to read existing speaker data, create new speakers or update existing…
- [Cvent Event Cloud Surveys API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-surveys-api/) — Surveys are lists of questions deployed to your contacts. Surveys can be standalone or can be associated to a Cvent event. Use these APIs to search for…
- [Cvent Event Cloud Usage API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-usage-api/) — Use these APIs view your REST API usage and limits metrics. For more details on limits - [Rate Limits](#section/Getting-Started/Rate-Limits)
- [Cvent Event Cloud User SCIM API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-user-scim-api/) — The [SCIM](https://www.simplecloud.info/) standard allows for easier cross-domain identity management. This API allows you to manage your account users and…
- [Cvent Event Cloud Users API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-users-api/) — Operations for managing account users and user groups, including creation, retrieval, update, and deletion. Use these endpoints to administer user access…
- [Cvent Event Cloud Video API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-video-api/) — Videos can be added to Cvent events with renditions at various resolutions, audio files, reactions tracks, and text tracks. Attendee viewership is tracked…
- [Cvent Event Cloud Webcasts API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-webcasts-api/) — Webcasts are virtual or livestreaming components of your Cvent events. Use these APIs to integrate your virtual events from outside sources into your Cvent…
- [Cvent Event Cloud Housing API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-housing-api/) — RegLink APIs allow you to exchange data with Cvent Passkey events and hotel reservation-booking engines. Generally, there are four primary categories of…
- [Cvent Event Cloud Housing Hotels API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-housing-hotels-api/) — APIs for managing hotel-related operations.
- [Cvent Event Cloud Meeting Request API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-meeting-request-api/) — When planning an event, meeting request forms are customizable online questionnaires to capture information about the event and facilitate the approval of…
- [Cvent Event Cloud Proposal Draft API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-proposal-draft-api/) — Beta - All APIs are in Beta. Proposal Drafts are editable copies of proposals. This API allows you to edit proposal data privately before publishing.
- [Cvent Event Cloud RFP Additional Details API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-rfp-additional-details-api/) — RFP additional details APIs for managing past event references and other miscellaneous RFP operations.
- [Cvent Event Cloud RFP Management API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-rfp-management-api/) — RFP (Request for Proposal) management APIs for core RFP operations including CRUD operations for base RFPs.
- [Cvent Event Cloud RFP Requirements API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-rfp-requirements-api/) — RFP requirements APIs for managing RFP-specific requirements including guest rooms, meeting rooms, custom questions, custom fields, and attachments (CRUD…
- [Cvent Event Cloud RFP Suppliers API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-rfp-suppliers-api/) — Suppliers are the venues and service providers that receive and respond to RFPs. Use these APIs to manage supplier associations, view recipient history, and…
- [Cvent Event Cloud Travel Accounts API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-travel-accounts-api/) — The travel account, or corporation that represents the demand-side of travel RFPs.
- [Cvent Event Cloud Travel RFPs API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-travel-rfps-api/) — The Travel RFP APIs provide access to travel programs and proposals. A travel program represents a request for proposal (RFP) that defines the specific…
- [Cvent Event Cloud Travel Suppliers API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-travel-suppliers-api/) — The Travel Supplier APIs provide access to Cvent data related to hotels, apartments, and other travel providers. This includes information related to…
- [Cvent Event Cloud Venue Meeting Rooms API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-venue-meeting-rooms-api/) — Manage meeting rooms for a venue, including creating and updating room details, configuring capacities and amenities, and associating images.
- [Cvent Event Cloud Venue Profiles API](https://apis.io/apis/cvent-event-cloud/cvent-event-cloud-venue-profiles-api/) — Manage venue profile details including type, contact information, address, and other venue properties.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (1)

Multi-step workflows that chain operations into a business task.

- [Test Suite](https://apis.io/arazzos/cvent-event-cloud/cvent-event-cloud-sdk-tests.arazzo/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Cvent Event Cloud Webhooks](https://apis.io/asyncapis/cvent-event-cloud/cvent-event-cloud-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Cvent MCP Server](https://apis.io/servers/cvent-event-cloud/cvent-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cvent Event Cloud Agentic Access](https://apis.io/agentic-access/cvent-event-cloud/cvent-event-cloud-agentic-access/)

#### Collections (41)

Postman and Open Collection request collections.

- [Cvent REST APIs — Event Cloud Appointments API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-appointments-api/)
- [Cvent REST APIs — Event Cloud Attendee Activities API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-attendee-activities-api/)
- [Cvent REST APIs — Event Cloud Attendee Insights API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-attendee-insights-api/)
- [Cvent REST APIs — Event Cloud Attendee Messages API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-attendee-messages-api/)
- [Cvent REST APIs — Event Cloud Attendees API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-attendees-api/)
- [Cvent REST APIs — Event Cloud Audience Segments API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-audience-segments-api/)
- [Cvent REST APIs — Event Cloud Authentication API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-authentication-api/)
- [Cvent REST APIs — Event Cloud Badge Print Job API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-badge-print-job-api/)
- [Cvent REST APIs — Event Cloud Badge Printer Pools API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-badge-printer-pools-api/)
- [Cvent REST APIs — Event Cloud Budget API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-budget-api/)
- [Cvent REST APIs — Event Cloud Bulk API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-bulk-api/)
- [Cvent REST APIs — Event Cloud Campaigns API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-campaigns-api/)
- [Cvent REST APIs — Event Cloud Card Tokens API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-card-tokens-api/)
- [Cvent REST APIs — Event Cloud Compliance API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-compliance-api/)
- [Cvent REST APIs — Event Cloud Contacts API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-contacts-api/)
- [Cvent REST APIs — Event Cloud Custom Fields API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-custom-fields-api/)
- [Cvent REST APIs — Event Cloud Discounts API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-discounts-api/)
- [Cvent REST APIs — Event Cloud Emails API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-emails-api/)
- [Cvent REST APIs — Event Cloud Event Credits API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-event-credits-api/)
- [Cvent REST APIs — Event Cloud Event Features API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-event-features-api/)
- [Cvent REST APIs — Event Cloud Event Role API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-event-role-api/)
- [Cvent REST APIs — Event Cloud Event Travel API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-event-travel-api/)
- [Cvent REST APIs — Event Cloud Events API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-events-api/)
- [Cvent REST APIs — Event Cloud Events+ Hub API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-events-hub-api/)
- [Cvent REST APIs — Event Cloud Exhibitor API](https://apis.io/collections/cvent-event-cloud/open-cvent-event-cloud-exhibitor-api/)
- …and 16 more published on APIs.io

#### Overlays (60)

OpenAPI overlays, including conversational phrasing for each operation.

- [Cvent Event Cloud Appointments Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-appointments-api-phrasing-overlay/)
- [Cvent Event Cloud Attendee Activities Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-attendee-activities-api-phrasing-overlay/)
- [Cvent Event Cloud Attendee Insights Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-attendee-insights-api-phrasing-overlay/)
- [Cvent Event Cloud Attendee Messages Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-attendee-messages-api-phrasing-overlay/)
- [Cvent Event Cloud Attendees Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-attendees-api-phrasing-overlay/)
- [Cvent Event Cloud Audience Segments Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-audience-segments-api-phrasing-overlay/)
- [Cvent Event Cloud Authentication Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-authentication-api-phrasing-overlay/)
- [Cvent Event Cloud Badge Print Job Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-badge-print-job-api-phrasing-overlay/)
- [Cvent Event Cloud Badge Printer Pools Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-badge-printer-pools-api-phrasing-overlay/)
- [Cvent Event Cloud Budget Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-budget-api-phrasing-overlay/)
- [Cvent Event Cloud Bulk Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-bulk-api-phrasing-overlay/)
- [Cvent Event Cloud Campaigns Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-campaigns-api-phrasing-overlay/)
- [Cvent Event Cloud Card Tokens Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-card-tokens-api-phrasing-overlay/)
- [Cvent Event Cloud Compliance Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-compliance-api-phrasing-overlay/)
- [Cvent Event Cloud Contacts Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-contacts-api-phrasing-overlay/)
- [Cvent Event Cloud Custom Fields Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-custom-fields-api-phrasing-overlay/)
- [Cvent Event Cloud Description Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-description-overlay/)
- [Cvent Event Cloud Discounts Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-discounts-api-phrasing-overlay/)
- [Cvent Event Cloud Emails Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-emails-api-phrasing-overlay/)
- [Cvent Event Cloud Event Credits Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-event-credits-api-phrasing-overlay/)
- [Cvent Event Cloud Event Features Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-event-features-api-phrasing-overlay/)
- [Cvent Event Cloud Event Role Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-event-role-api-phrasing-overlay/)
- [Cvent Event Cloud Event Travel Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-event-travel-api-phrasing-overlay/)
- [Cvent Event Cloud Events Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-events-api-phrasing-overlay/)
- [Cvent Event Cloud Events Hub Api Phrasing Overlay](https://apis.io/overlays/cvent-event-cloud/cvent-event-cloud-events-hub-api-phrasing-overlay/)
- …and 35 more published on APIs.io

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Cvent Event Cloud Authentication](https://apis.io/security/cvent-event-cloud/cvent-event-cloud-authentication/)
- [Cvent Event Cloud Domain Security](https://apis.io/security/cvent-event-cloud/cvent-event-cloud-domain-security/)
- [Cvent Event Cloud Trust Center](https://apis.io/security/cvent-event-cloud/cvent-event-cloud-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Cvent Event Cloud Scopes](https://apis.io/scopes/cvent-event-cloud/cvent-event-cloud-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cvent Event Cloud Plans Pricing](https://apis.io/plans/cvent-event-cloud/cvent-event-cloud-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cvent Event Cloud Rate Limits](https://apis.io/rate-limits/cvent-event-cloud/cvent-event-cloud-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Cvent Event Cloud Finops](https://apis.io/finops/cvent-event-cloud/cvent-event-cloud-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cvent.com/en/event-management-software)
- [Documentation](https://developers.cvent.com/docs/rest-api/overview)
- [Getting started](https://developers.cvent.com/docs/rest-api/tutorials/developer-quickstart)
- [API reference](https://developers.cvent.com/docs/rest-api/overview)
- [Pricing](https://www.cvent.com/en/event-management-software/cvent-pricing)
- [Sign up](https://developers.cvent.com/applications)
- [Support](https://support.cvent.com/)
- [Blog](https://www.cvent.com/blog)
- [Terms of service](https://www.cvent.com/en/cvent-general-terms-of-use)
- [Privacy policy](https://www.cvent.com/en/privacy-policy)
- [GitHub](https://github.com/cvent)
- [Status](https://status.cvent.com/)

## API Evangelist rating

**Kin Score 70.9** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 65.5 |
| Contract governance | 4.5 |
| Operational transparency | 81.6 |
| Developer ergonomics | 67.3 |
| Access clarity | 92.1 |

**Agent readiness 48.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | documented (partial credit) |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | mostly |

**Regulatory alignment 39.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cvent-event-cloud/](https://apis.io/providers/cvent-event-cloud/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cvent Event Cloud: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cvent-event-cloud/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
