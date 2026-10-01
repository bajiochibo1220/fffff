# Whole System Test Guide

Use this guide to check the website from start to finish. Write **Pass** or **Fail** beside each number. If a check fails, write down what you saw and the page you were on.

## Before You Start

1. Use a test copy of the website and test information. Do not use real people's private information.
2. Make a backup before testing delete buttons or changing account access.
3. Start the website and make sure the home page opens at `http://localhost:3000`.
4. Make sure the website can reach its saved data and that the Google sign-in settings include `http://localhost:3000/api/auth/callback/google`.
5. Prepare one Google account already linked to a website account, one Google email with no website account, and one new Google account for sign-up.
6. Prepare one normal email-and-password account, one account waiting for approval, one suspended test account, one language admin, one super admin, and one master super admin.
7. Use a test language that is turned on, such as Luo. Make a note of its public page address.
8. When checking public content, use material marked for public sharing. A record kept private or for study only must stay off the public pages.

## Sign In And Sign Up

9. Open the sign-in page. **Expected:** The email, password, Google, and create-account choices are visible.
10. Sign in with the right email and password. **Expected:** The account opens its correct home page.
11. Sign in with a wrong password. **Expected:** The account does not open and a clear error appears.
12. Leave the email or password empty and try to sign in. **Expected:** The page asks for the missing detail.
13. Sign in with a Google account already linked to a website account. **Expected:** The account opens without an access-denied page.
14. Sign in with a Google account already linked to an admin account. **Expected:** The account opens the admin area, not the member area.
15. Sign in with the Google email of an existing password account that has not yet been linked. **Expected:** The same account opens; a second account is not made.
16. Sign out, then use the linked Google account again. **Expected:** It still opens the same account.
17. On the sign-in page, choose Google with an email that has no website account. **Expected:** You return to sign-in and see that no account was found, with a link to create one.
18. Use the link in that message. **Expected:** The create-account page opens.
19. On the create-account page, try Google sign-up before accepting the terms. **Expected:** Google sign-up cannot start.
20. Accept the terms, then choose Google sign-up with a new Google account. **Expected:** Google opens and returns you to the page for finishing account setup.
21. Try to finish Google sign-up without a name, birth date, or language. **Expected:** The missing detail is requested and no incomplete account is accepted.
22. Enter a date that does not exist, such as 31 February. **Expected:** The date is rejected.
23. Enter a date that makes the person younger than five or older than 120. **Expected:** The website does not finish account setup.
24. Choose a language, enter a real date and name, accept the terms, and finish Google sign-up. **Expected:** The account opens the member home page.
25. Sign out and sign in with that new Google account. **Expected:** It opens the same account and does not ask for the sign-up details again.
26. Try Google sign-up using the email of an existing account. **Expected:** The existing account opens; no duplicate account is made.
27. Use the normal create-account form with valid details. **Expected:** The account is made and can sign in.
28. Try the normal create-account form with an email already in use. **Expected:** The website explains that the email is already registered.
29. Try a password shorter than eight characters. **Expected:** The website does not create the account.
30. Try to create an account without accepting the terms. **Expected:** The website does not create the account.
31. Sign in with an account waiting for approval. **Expected:** It cannot use member or admin pages until approved.
32. Sign in with a suspended account using both password and Google. **Expected:** Access is refused with a clear message.
33. Cancel Google sign-in, return to the site, and then choose Google sign-in again. **Expected:** The second try follows the choice made on the current page.
34. Open a protected page while signed out. **Expected:** The website sends you to sign-in; it does not show private information.
35. Sign out and press the browser Back button. **Expected:** Private pages do not become usable again.

## Public Pages And Content

36. Open the public language home page. **Expected:** The page opens and shows its language and content areas.
37. Open each public area: dictionary, proverbs, riddles, oral histories, folktales, songs, artifacts, and heritage sites. **Expected:** Each page opens without an error.
38. Open each area when it has no public records. **Expected:** A clear empty message appears.
39. Open an area that has publicly released records. **Expected:** Its released records appear.
40. Open a public record from its list. **Expected:** The correct title and details appear.
41. Check that a private draft does not appear on a public page. **Expected:** It stays hidden.
42. Check that a record waiting for review does not appear on a public page. **Expected:** It stays hidden.
43. Check that a record kept for study, teaching, or community use does not appear as public. **Expected:** It stays hidden from people who are not allowed to see it.
44. Check that a record with public consent but a private restriction does not appear publicly. **Expected:** It stays hidden.
45. Check a public record with an embargo that has not ended. **Expected:** It stays hidden until the end date.
46. Check the same record after its embargo ends. **Expected:** It can appear if it is approved for public release.
47. Check an oral history without confirmed source permission. **Expected:** It stays off public pages.
48. Check an oral history with confirmed source permission and public access settings. **Expected:** It appears after public approval.
49. Change the public language page between Luo and English. **Expected:** The page shows content for the chosen language or culture setting.
50. Open a public link for a record that is not public. **Expected:** The record is not shown.
51. Use the public search box with a word that exists. **Expected:** Matching public records appear.
52. Search for a word that does not exist. **Expected:** A clear “no results” message appears.
53. Open the dictionary. **Expected:** Public dictionary words and approved dictionary records appear together.
54. If there are more than 50 public dictionary entries, choose “Show more entries.” **Expected:** More entries appear without repeating earlier entries.
55. Keep loading dictionary entries until the end. **Expected:** Every public entry can be reached.
56. Search the dictionary in Luo, English, or Kiswahili. **Expected:** Matching public entries appear.
57. Open a dictionary entry with audio. **Expected:** The audio can be played.
58. Open a public record with an image. **Expected:** The image loads and matches the record.
59. Open a public record with audio or video. **Expected:** The media plays and has working controls.
60. Open a public record with a transcript or document. **Expected:** The file opens or downloads correctly.
61. Open the public home page after publishing a record. **Expected:** It may show the record in the featured area when it is among the latest three public records.
62. Check that old or private content is not shown as featured. **Expected:** Only eligible public records appear there.

## Upload, Review, And Public Release

63. Sign in as a normal member and open a contribution form. **Expected:** You can enter a contribution but cannot publish it yourself.
64. Try to submit a contribution with required details missing. **Expected:** The missing details are named and it is not submitted.
65. Save a contribution as a draft. **Expected:** It appears in your drafts and not on public pages.
66. Submit a complete contribution for review. **Expected:** It appears in your submissions and the review list.
67. Add an image to a contribution and save it. **Expected:** The image is attached to the right record.
68. Add audio, video, and a transcript in separate test records. **Expected:** Each file is attached and can be opened by an allowed reviewer.
69. Try to upload an unsupported or too-large file. **Expected:** The website explains the problem and keeps the record safe.
70. Sign in as a reviewer and open the review list. **Expected:** You can see records for the language you manage.
71. Try to open a record from a language you do not manage. **Expected:** Access is refused.
72. Approve a record with public consent, a public restriction, and any required source permission. **Expected:** Its state says published and it appears in the correct public area.
73. Approve a record without public consent or with a private restriction. **Expected:** It says curated, explains that it was not published, and stays off public pages.
74. Open the curated filter in the admin content list. **Expected:** Internally curated records can be found there.
75. Correct the access settings on a curated record, then approve it again. **Expected:** It becomes published only after it meets the public rules.
76. Try to publish an oral history without confirmed source permission. **Expected:** It does not become public and the reason is clear.
77. Approve a record with a future embargo date. **Expected:** It does not appear publicly until the embargo ends.
78. Reject a contribution and add a note. **Expected:** It is marked rejected and the note is saved.
79. Send a contribution back for changes. **Expected:** The contributor can see that it needs changes.
80. Edit a published record. **Expected:** It is removed from public pages until it is approved again.
81. Approve the edited record again after checking its details. **Expected:** It returns to public pages if it still meets the public rules.
82. Try to approve incomplete required content. **Expected:** The website asks for the missing details and does not publish it.
83. Try to approve a record in a language you cannot review. **Expected:** The website refuses the action.
84. Refresh the public page after approval. **Expected:** The newly released record appears without needing a server restart.

## Admin And Master Admin Pages

85. Sign in as a language admin. **Expected:** The language admin home page opens.
86. Check that the language admin can review only allowed languages. **Expected:** Other languages cannot be changed.
87. Sign in as a super admin. **Expected:** The super admin pages open.
88. Change the selected language in the super admin area. **Expected:** The lists show the chosen language.
89. Sign in as a master super admin. **Expected:** The master super admin pages open.
90. Try to open a master super admin page as a normal member. **Expected:** Access is refused.
91. Add a test user through the admin tools. **Expected:** The user gets only the access chosen by the admin.
92. Change a test user's status or role. **Expected:** The new access takes effect after the user signs in again.
93. Open the admin content list and filter by draft, submitted, curated, and published. **Expected:** Each filter shows the right records.
94. Delete a test record after confirming the warning. **Expected:** It is removed and no longer appears in lists.
95. Cancel a delete warning. **Expected:** The record remains.
96. Open the activity history after a review action. **Expected:** The action, record, and reviewer are shown.
97. Open the reports and totals pages. **Expected:** They load and show sensible totals for the test data.
98. Change an admin setting, save it, and reload the page. **Expected:** The saved setting remains.
99. Try an admin action with a normal member account. **Expected:** The action is refused and nothing changes.
100. Open the site on a phone-sized screen. **Expected:** Text and buttons fit and the main pages can be used.
101. Open the site on a wide screen. **Expected:** Menus and page content do not cover each other.
102. Use keyboard Tab to reach sign-in, sign-up, search, and review buttons. **Expected:** Each control can be reached and used.
103. Refresh a page while signed in. **Expected:** You stay signed in and the page still works.
104. Stop and restart the website, then sign in and open a public record. **Expected:** Saved accounts and published records are still there.

## Finish The Test

105. Sign out of every test account and remove any test records that should not remain.
106. Write down every failed number, the account used, the page address, and what you expected to happen.
107. Do not mark a failed check as passed just because another page works.
108. A record counts as public only when it has passed review and is allowed for public sharing. A record kept private must remain private.
