# LuoLinguaAI Progress Update

This report gives a short update on work completed and work still to do in Phase One and Phase Two.

## Phase One — Foundation

### Achieved

- **Database:** The Neon database is connected and running. This has been checked.
- **Website online:** The system is deployed on Vercel and opens from its web link. This has been checked.
- **Phone and laptop access:** The website can be installed from the browser. Its icon appears on the phone and laptop screens. This has been checked. It is an installable website, not yet a separate app from an app store.
- **Database design:** The code has places to store users, roles, Luo content, translations, pictures, transcripts, and information used by AI search.
- **First content sections:** Code is in place for the Dholuo dictionary, proverbs, riddles, and oral histories.
- **Login and admin roles:** Login, Google sign-in, user roles, and admin pages are present in the code.
- **AI starting features:** The code connects to Gemini and includes AI search, a chatbot, transcript summaries, and finding people, places, and clans in transcripts.

### Pending

- Add and review more dictionary words, proverbs, riddles, and oral histories. The sample files currently contain 5 dictionary entries, 3 proverbs, and 2 riddles.
- Add the approved transcript data to the live system. The data package has 26 prepared transcripts split into 2,708 text sections; this does not mean they are already loaded into the live database.
- Keep the source and permission details with each item when adding it. Some transcripts are marked for research or internal use, so they must not be made public or sent to an outside AI service without approval.
- Finish checking the upload and review process, including the required details about each file and its file-check information.
- Check that users can only see records, pictures, and transcripts they are allowed to see.
- Test AI search and chatbot answers using approved Luo content. Check that the answers use the right information.
- Check the transcript summaries and names found by AI against the original transcripts.
- Confirm that edits are recorded and earlier versions can be reviewed.
- Test that database backups and media can be restored.
- Finish basic instructions for adding content, managing accounts, and restoring a backup.

## Phase Two — More Content and Web System

### Achieved or started

- **Public website:** The web system is online on Vercel. Pages are present for several content sections.
- **Admin dashboard:** Admin pages are in the code for managing users, content, reviews, pictures, translations, and system settings.
- **Stories and songs:** Pages and data routes are present in the code.
- **Artifacts:** Artifact pages and picture upload are present. Some artifact pictures have been uploaded and are visible to users. This has been checked.
- **Heritage sites:** Pages, data routes, and map components are present in the code.
- **Installable website:** The system opens from an icon on a phone or laptop screen. This has been checked.

### Pending

- Add more approved stories, songs, artifacts, and heritage-site information.
- Add approved descriptions and pictures for the Luo museum collection. Some artifact pictures are already visible.
- Decide how the virtual museum should work. A picture collection, a map, 3D objects, and a virtual tour are different features.
- Add audio and video after the project team provides and approves the recordings. No audio or video files were found in the supplied data files reviewed for this report.
- Test the full admin process: add content, attach a picture, review it, approve it, publish it, and make a correction.
- Check the heritage-site locations and decide which location details can be shown publicly.
- Complete and check the reports and data exports needed by the project.

## Checks still to complete

The following have not been confirmed as tested yet:

- Restricted content is blocked for users without permission.
- Search results follow the user’s access rights.
- A file upload saves the required details and file-check information.
- Content reviews and changes are recorded correctly.
- A user can export only information they are allowed to receive.
- A database backup and sample pictures can be restored.
- The system works well on a slow internet connection and meets the project’s speed and availability needs.

## Summary

- **Phase One:** The database, online system, installable website, core page structures, and initial AI code are in place. More approved content, permission checks, full feature testing, and handover work remain.
- **Phase Two:** The public website, admin pages, pages for more content areas, and some visible artifact pictures are in place. More content, a complete museum collection, and full testing of the admin tools remain.

Only the database, website deployment, phone/laptop installation, and visible artifact pictures are marked as checked above. Other items are described as present in code until they have been tested in the working system.
