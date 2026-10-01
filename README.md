# Improvements Compared with `luolinguaai`

**Comparison date:** 2026-10-01  
**Scope:** Features and fixes in `luolinguaai_was being improved` compared with the `luolinguaai` reference project.

This document lists the improvements added to or expanded in the improved project. It describes code present in the repository; it does not claim that every item has completed deployment, user acceptance, external NRF validation, or production data migration. The reference project was used as a behavior and design baseline and was not modified.

## Preserved Reference Experience

- The root route keeps the reference login-first screen and its branded two-column auth layout.
- The login and registration pages, shared auth shell, colors, and form styling remain aligned with the reference.
- The public language home is available at `/luo`; Phase One additions do not replace the root login screen.
- Authenticated users retain role-aware routing, including the Master Super Admin dashboard.

## Consent, Governance, and Privacy

- Records, dictionary entries, media, and transcripts support shared consent and access-restriction metadata.
- New and existing content defaults to pending/internal until reviewed, rather than being treated as publicly releasable by default.
- Shared governance checks are applied to public pages, APIs, item details, approvals, media delivery, AI search/RAG, and embedding generation.
- Non-public material is excluded from public AI indexing; embeddings are removed when content loses eligibility.
- Oral-history publication requires explicit source-permission confirmation. Source-permission and attribution-preference flags can be carried into approved exports without exposing the full contribution payload.
- Editing a released record returns it to internal review and removes its AI index until it is approved again.
- Restricted records and media accessed through internal APIs generate audit events.

## Contribution and Editorial Workflow

- The public contribution flow opens structured, module-specific forms for dictionary entries, proverbs, riddles, and oral histories.
- Server-side validation enforces required content fields, including dictionary terms, proverb text and meaning, riddle question/answer/explanation, and oral-history transcript/title fields.
- Contributors can save private drafts; submission is limited to eligible draft or rejected states and uses a conditional transition to prevent duplicate or racing submissions.
- Contributors cannot publish directly. Authorized reviewers control approval and release.
- Elder contribution flows include source-permission and attribution controls, prevent submission when permission is denied, and support in-browser oral-history recording or audio upload.
- Content can store structured provenance: source type/name, date, location, collector, and notes. Revisions append source history instead of overwriting it.
- Bulk media uploads remain drafts until a reviewer makes the governance and release decision.

## Content and Language Features

- Dictionary entries support detailed meaning, origin, synonyms, antonyms, usage examples, pronunciation, grammar class, English meaning, and audio.
- Public dictionary search matches structured lexical content before pagination, and detail pages display the contributed lexical fields.
- Riddle explanations are required for submissions and displayed with the answer on public cards and detail pages.
- Translation updates require reviewer access for the target language and create audit records. Translated titles do not replace source-language titles.
- Language-home selection and switching preserve the selected language context; Dholuo and English module titles and contribution labels are supported.
- Public module cards now route to the actual implemented paths, including `muma`, `ngero`, `ngeche`, `sigana`, `sigana/folktales`, `wende`, `gik-luo`, and `piny-luo`. Modules without an implemented page are identified as “Soon” instead of linking to a missing route.
- Seed content uses explicit public governance settings rather than permissive defaults.

## Media, Transcripts, and AI

- Cloudinary uploads use authenticated upload authorization, and a server-side media proxy checks asset and parent-record access before streaming protected media.
- Anonymous public media requests can use the proxy, but still pass the same governance checks as API requests.
- Media and recording identifiers and storage paths follow stable, access-scoped and NRF-oriented conventions; transcript imports preserve source IDs and checksums.
- Transcript revisions have an authenticated curator API, increment versions, snapshot prior text, clear stale summaries/entities/embeddings, and return released records to review after edits.
- External transcript summarization/entity extraction is limited to curator-initiated work on published, explicitly public content. AI indexing, monitoring, and moderation endpoints are language-role restricted.

## NRF Interoperability and Corpus

- A role-restricted, audited `/api/nrf/export` endpoint supports metadata as JSON/CSV, authorized transcript text as JSONL, and image metadata/labels as CSV or COCO-style JSON.
- Exports check per-item consent and restrictions, use pagination cursors, and return no-store responses.
- A repeatable `npm run corpus:import` command preserves source/session/checksum metadata and imports the prepared corpus as `research_only` and `internal`; it does not publish or externally embed those records.
- The importer has not been run because destination authorization is still required. Export mappings and image annotation conventions still need review against the NRF technical contract.

## Reliability and Access Control

- Heritage-site maps load only in the browser, avoiding Leaflet server-rendering failures.
- Malformed language IDs return 404 rather than causing database validation errors.
- Public record totals and pagination are calculated after governance filtering, so hidden records do not affect visible counts.
- Master Super Admin login has a dedicated dashboard destination; middleware applies role checks to privileged routes and redirects signed-in users away from the auth entry screens.

## Remaining Gaps

- Dholuo/English interface localization is partial; many descriptions, validation messages, consent instructions, and admin controls still need reviewed translations.
- MFA for administrator and curator accounts is not implemented.
- Real-device acceptance for elder contribution and recording is still required.
- Existing public Cloudinary assets need a controlled migration/re-upload plan; the existing deployment has not been updated with the new governance code.
- The corpus import awaits explicit destination authorization, and NRF mappings/interoperability require external review.
- A successful real Google callback and successful password registration/login were not exercised during code-only verification.
- Mobile store apps, offline synchronization, speech/OCR/translation AI, image recognition, knowledge graph, full learning centre, 3D tours, and a full research portal remain outside the funded Phase One scope unless formally added.

## Verification Recorded

- `npx tsc --noEmit` and the production build passed after the UI-preservation and route fixes.
- Smoke checks returned HTTP 200 for the root login screen, `/luo`, `/login`, `/register`, and `/api/languages`; implemented public module routes also returned HTTP 200.
- The chatbot redirects signed-out users to login. Successful login and registration with real credentials were not tested.
