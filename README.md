# LuoLinguaAI: Phase One Progress Report

**Prepared for:** Project lecturer  
**Prepared by:** Developer  
**Date:** 30 September 2026

## 1. Purpose of this report

This report explains what has been built for LuoLinguaAI, what still needs to be done, and what belongs to Phase Two.

The PRD describes a large system with 15 main modules. The project discussion set a six-week period for Phase One. The one-week period was for an early version that the lecturer could see and review. It was not the full six-week Phase One.

The report uses the PRD, the project files, and the current system. The lecturer can open the deployed system and review the work.

## 2. Overall progress

The first working version of the web system has been built and deployed. The database is running. Users can open the system on a phone or computer, and some Luo artifact pictures have been added and can be seen by users.

This is real progress toward Phase One. It does not mean that every part of the PRD is complete. The main work still needed is to add and check more approved Luo content, complete the agreed Phase One features, and test the main tasks with the lecturer.

## 3. Phase One achievements

| Area | What has been achieved |
|---|---|
| Web system | The web system has been built and deployed using Vercel. It can be opened through a web link. |
| Phone and computer access | The system can be installed from the browser. It was tested on a phone and on a laptop, and its app icon appears on both screens. This makes the website easy to open like an app. |
| Database | The Neon database is running and connected to the system. It stores the system’s information, such as users and cultural records. |
| System design | The database has places for language settings, user roles, cultural information, dictionary entries, translations, pictures and other media, transcripts, and AI search information. |
| Public pages | The system has pages for key content areas, including the dictionary, proverbs, riddles, oral histories, stories, songs, artifacts, and heritage sites. |
| Admin tools | Admin pages and tools have been built for managing users and content, reviewing submissions, managing media, and viewing system information. |
| User access | Login and account features, including admin roles, have been built into the system. The public Google sign-in has been configured for the current version. |
| Artifact pictures | Some artifact pictures have been uploaded. Users can see them in the system. |
| AI search and chatbot | The system is connected to Gemini. It has code for semantic search and a chatbot that can use information stored in the system to help answer questions. This is called RAG: in simple terms, the system looks for useful information first, then gives it to the chatbot to help form an answer. |
| Transcript tools | The system has code that can make a short summary of a transcript and identify names of people, places, and clans. These results still need to be checked against approved Luo source material. |

### Phone installation: what it means

The phone and laptop installation is an important achievement. It is an installable web app: the browser puts an icon on the screen and opens the website in an app-like window. It is not yet a separate Android or iOS app published through Google Play or Apple’s App Store.

## 4. Phase One work still to complete

| Work still needed | Why it matters |
|---|---|
| Add more approved Luo content | The current sample content is small. The source archive has many transcripts, reports, and pictures, but they have not all been added to the live system. The lecturer needs enough real content to review the main sections. |
| Finish the selected Phase One sections | The pages exist for several modules, but each needs enough checked content and a complete user experience. The lecturer and developer should agree which modules are required for the six-week Phase One. |
| Complete the virtual Luo museum | Artifact pictures are visible, which is a start. More approved artifact and heritage-site records, descriptions, and pictures are needed. A full 3D or virtual-tour experience is a larger feature and needs a separate decision. |
| Add and check available media | The current source files include pictures, but no audio or video files were found in the supplied archives. Audio and video features need the project team to provide the files and confirm that they can be shared. |
| Test the main tasks | Check that users can view and search content, that admins can add and approve content, and that uploaded pictures work on phones and computers. Check the live AI search and chatbot using real, approved records. |
| Check AI answers | The chatbot should give answers based on the approved Luo content and show which records it used. People who know the culture should review the answers for accuracy. |
| Add the rest of the approved data | The prepared transcript data needs to be carefully moved into the system with its source and access information. Having a file in the project folder does not automatically put it into the live database. |
| Review access and consent | Some transcript data is marked for research use or internal use. Before it is shown publicly or sent to an outside AI service, the project team must confirm that this use is allowed. |
| Complete the final handover | Prepare simple instructions for using the system, managing content, backing up the database, and reporting problems. |

The supplied NLP package describes 26 prepared transcripts divided into 2,708 text sections. This is useful source material. It is not proof that all these sections are already in the live system or approved for public use.

## 5. Phase One modules from the PRD

The PRD names 15 modules. The system has pages or database support for several of them, but a page alone does not mean the whole module is complete. The following is the current status:

| PRD area | Current status |
|---|---|
| Dholuo dictionary | The page and database support are present. A small sample is available; more checked words and examples are needed. |
| Proverbs | The page and database support are present. A small sample is available; more proverbs, meanings, and examples are needed. |
| Riddles | The page and a quiz feature are present. A small sample is available; more riddles and explanations are needed. |
| Oral histories | The system has pages and transcript support. More approved transcripts and related information need to be added and checked. |
| Folktales and stories | Pages are present. The collection and story details need to be expanded. |
| Songs | Pages are present. More lyrics and approved sound recordings are needed. |
| Artifacts and Luo museum | Artifact pages and some visible pictures are present. More records and descriptions are needed. |
| Heritage sites | Pages and map components are present. Site information, pictures, and map details need to be checked and added. |
| AI chatbot | The system has chatbot and RAG code. It needs testing with enough approved records. |
| AI language tutor | This is not complete. |
| Games and learning centre | Some basic quiz work exists, but the full learning and games features are not complete. |
| Cultural calendar | A database module is listed, but a complete calendar with approved events is not demonstrated. |
| Audio-visual library | Media upload tools exist, but a complete library with approved audio and video is not available yet. |
| Research portal | Database support exists, but a complete portal for researchers is not available yet. |

The PRD also lists content such as traditional food, medicine, ceremonies, clan history, fishing, farming, names, weather knowledge, and governance. These topics need to be selected with the lecturer and added as checked records. They should not be claimed as complete just because they appear in a transcript or analysis report.

## 6. Phase Two: later work

Phase Two should begin after the agreed Phase One work has been reviewed. The following PRD features are not complete in the current system:

- Separate Android and iOS apps for the app stores.
- Use without an internet connection and automatic syncing when the connection returns.
- Speech-to-text and text-to-speech.
- Pronunciation practice and the full AI language tutor.
- OCR, which reads words from pictures or scanned pages.
- Automatic translation between languages.
- Image recognition and a cultural knowledge graph.
- Full lessons, learning progress, and larger games or multiplayer activities.
- 3D artifact models, story animation, and full virtual tours.
- A complete research portal and the full audio-visual library.
- Full support for more languages. Kikuyu is listed in the system design but is not active as a complete language service.
- Moving the system to the university data centre, if the university confirms the technical needs and schedule.

### Phase Two groundwork already present

Some early pieces are already in the code. The phone-install feature is in place, but it is not a native app or offline mode. The system has early transcript summary and name-finding tools, but they need approved data and careful review. The database also has starter entries for future learning, games, research, and additional languages. These are starting points, not completed Phase Two features.

## 7. Important note about AI

The current AI features use Gemini to work with information in the system. The system has not trained a new Luo language model. Making text vectors helps the system find related information; it does not train a new model.

The AI should only use information that the project team has approved for that purpose. Its answers and transcript summaries should be reviewed by people who understand Dholuo and Luo culture.

## 8. Recommended next steps for Phase One

1. The lecturer confirms which content sections must be ready for the Phase One review.
2. The project team confirms which transcripts, pictures, and other media can be shown to the public and used with AI.
3. Add a useful set of approved content to the selected sections, including the artifact collection.
4. Test the main public, admin, media, and AI tasks on the deployed site using a phone and a computer.
5. Record the lecturer’s feedback and agree which remaining tasks belong to Phase One and which move to Phase Two.

## 9. Closing statement

Phase One has made clear progress: the web system is deployed, the Neon database is running, the system can be installed from a phone and laptop browser, admin and content features have been built, some artifact pictures are visible, and the first AI tools are in place.

The main unfinished work is to add more approved content and media, complete and test the selected Phase One features, and review the system with the lecturer. The broader mobile apps and advanced AI features belong to Phase Two unless the project team formally changes the agreed scope.
