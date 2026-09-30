# LuoLinguaAI Progress Report: Phase One and Phase Two

**Prepared for:** Project lecturer  
**Date:** 30 September 2026  
**Progress is based on:** the PRD, the funding request, Activity 3.1.1 technical requirements, a review of the project code, and tests reported by the developer.

## Phase plan used in this report

The funding request sets out four phases of 16 weeks each. This report covers only the first two:

- **Phase One — Foundation:** database and security setup, the first four content areas (Dictionary, Proverbs, Riddles, and Oral History), and the designs for the system pages.
- **Phase Two — Content and Web:** more content areas (Folktales, Songs, Artifacts, and Heritage Sites), the public web portal, and the admin dashboard.

The one-week period discussed in the WhatsApp messages was for an early version to review. It was not the full Phase One period.

## Phase One — Foundation

### Achieved

| Work | Progress and evidence |
|---|---|
| Database setup | The Neon database is running and connected to the system. This was checked by the developer. The code has tables for users, roles, languages, cultural records, dictionary entries, media, transcripts, translations, AI search, consent, and audit history. |
| System available online | The website has been deployed on Vercel and opens from its web link. This was checked by the developer. |
| Phone and computer access | The website can be installed from the browser. The developer tested it on a phone and a laptop and confirmed the app icon appears on each screen. |
| Login and roles | The code includes account sign-in, Google sign-in, admin roles, and protected admin pages. These features are present in the code. Full role and security checks listed in Activity 3.1.1 are still pending below. |
| First four content areas | The code includes pages and data routes for Dictionary, Proverbs, Riddles, and Oral History. Small sample files are present for the dictionary (5 entries), proverbs (3), and riddles (2). |
| Search and AI foundation | The code connects to Gemini and includes semantic search and a chatbot that can retrieve information from the system. The code also includes transcript summaries and extraction of people, places, and clans. These AI paths still need the checks listed below before they can be counted as accepted. |

### Pending

| Work | What remains |
|---|---|
| Add the agreed Phase One content | Add enough reviewed Luo words, proverbs, riddles, and oral histories for the lecturer to judge the four areas. The sample files are only a starting point. |
| Add the supplied transcript data safely | The data package contains 26 prepared transcripts split into 2,708 text sections. They are not all shown to be loaded in the live system. Keep the source name, county/site, speaker details, consent, and access level when importing them. |
| Finish the data upload process | Activity 3.1.1 requires upload, required information about each item, a file check, and a review path from raw material to approved and published material. The code has upload and review pieces; the complete process and the required file checks still need an end-to-end check. |
| Apply access rules to every item | The technical annex requires access to depend on a person’s role, consent, and restriction level. It also requires separate rules for a record, its image/video/audio, and its transcript. The code has roles and consent-related data structures, but full checks for these rules are still pending. |
| Check login safety | The annex calls for protected staff sign-in, extra security for admin accounts, and rules for ending inactive sessions. The code has login and roles; the added security checks have not been confirmed. |
| Test AI using approved Luo material | Load approved records, build the search index, try real Dholuo and English questions, and check that answers use the right records. Do not send research-only or restricted material to public pages or an outside AI service without permission. |
| Check summaries and name extraction | Compare the AI summaries and extracted people, places, and clans with the original transcripts. Have a knowledgeable reviewer correct mistakes. |
| Protect participant information | The annex calls for hiding personal details where needed, protecting consent forms, and limiting exact location details where the community requires it. These steps still need confirmation in the working system. |
| Check change history | The database has places to store who changed a record and its earlier versions. Confirm that edits actually save this history and can be reviewed. |
| Test search and filters | Check that word search, filters, and AI search show only information the current user is allowed to see. |
| Test backup and restore | Backup code and data structures exist. The annex requires a test restore of the database and sample media. That restore test is still pending. |
| Prepare Phase One handover | Write short instructions for staff to add and approve content, manage accounts, and restore a backup. Confirm the agreed Phase One acceptance list with the lecturer. |

## Phase Two — More content and web system

### Achieved or started early

| Work | Progress and evidence |
|---|---|
| Public web portal | The web system is deployed on Vercel and has public pages for several content areas. The developer confirmed that it opens online. |
| Admin dashboard | Admin and super-admin pages are present in the code for users, content, review, media, translations, analytics, and system settings. The full admin process still needs to be checked with the lecturer. |
| Folktales and Songs | Pages and data routes exist in the code. Complete collections and all PRD features are not yet confirmed. |
| Artifacts | Artifact pages and media upload support are present. The developer uploaded artifact pictures and confirmed that users can see them. |
| Heritage sites | Heritage-site pages, data routes, and map components exist in the code. Full site information and virtual tours are not yet confirmed. |
| Phone-friendly install | The deployed website can be installed from the phone browser, and the icon appears on the phone screen. This supports access to the web system; it does not mean separate Android and iOS store apps are complete. |

### Pending

| Work | What remains |
|---|---|
| Fill the expanded content areas | Add reviewed stories, songs, artifacts, and heritage sites with enough approved information and images for users to explore. |
| Complete the Luo museum collection | Some artifact pictures are already visible. Add the approved descriptions and more items, and agree what the lecturer means by “virtual museum.” A picture collection, a map, a 3D model, and a full virtual tour are different amounts of work. |
| Add audio and video | The supplied archives reviewed for this report contained images but no audio or video files. The project team needs to provide and approve any recordings to be displayed. |
| Finish admin tasks | Test that an admin can add an item, attach media, send it for review, approve it, publish it, and correct it later. |
| Finish maps and site details | Check location information and decide whether exact coordinates can be shared for each site. |
| Test the complete website | Check the main public and admin tasks using a phone and a computer, including slow connections and failed uploads. |
| Complete reporting and records | Confirm the needed reports, data exports, and content history for the university’s research team. |

## Technical checks required by Activity 3.1.1

The developer has confirmed four working checks: the Vercel website opens, Neon is running, uploaded artifact pictures are visible to users, and the installable website icon appears on phone and laptop screens. Other checks below are still pending unless the development team has separate test records:

- A restricted record and its media cannot be opened by a user without permission.
- Search results respect the user’s role, consent level, and content restrictions.
- A file upload saves its checksum and required information about the file.
- A reviewer can approve, request a change, or restrict an item, and the action is recorded.
- Earlier versions and the person who changed an item can be viewed.
- A data export leaves out records and personal details that the user is not allowed to receive.
- A database backup and sample media can be restored successfully.
- The system meets the response-time and availability targets in the technical annex.

## Phase Two groundwork already in the code

Some early building blocks for later features are already present: phone-browser installation, starter language settings, learning and games placeholders, and AI transcript tools. These are foundations only. They do not mean that native mobile apps, full lessons and games, offline use, or a complete AI language tutor are finished.

## Important data and AI note

The prepared transcript package labels its records for research or internal use by default. Confirm permission for each item before making it public or sending it to an outside AI service. The AI features use Gemini to search and work with stored information; this is not the same as training a new Luo language model.

## Progress summary

- **Phase One:** database, deployment, phone/laptop installation, core page structures, and early AI code are in place. Content population, permission checks, full feature testing, and handover remain.
- **Phase Two:** the web portal, admin pages, several expanded content pages, and visible artifact pictures have already been started. More approved content, complete admin checks, and a clear museum experience remain.

The progress statements marked as tested above are based on the developer’s reported checks. Items described as present in code have not been marked as tested unless a working test was confirmed.
