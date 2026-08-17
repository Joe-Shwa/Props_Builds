# Props_Builds
Prototyping Form

A small app that reads prototype rows from a Google Sheet and lays each one out as a printable "prop tag" form — for handing off to the props/fabrication team.

One-time setup (you, before sending it to her)
Add her as a test user. The Google sign-in is still in Testing mode in Cloud Console, which means only pre-approved accounts can sign in.
Go to Google Cloud Console → your project → APIs & Services → OAuth consent screen → Audience/Test users
Add her Google account email
This takes effect immediately, no waiting period
Host the files. Upload these three files to the same folder in your joe-shwa.github.io repo:
prototype_tags.html
prototagicon192.png
prototagicon512.png
Give her the resulting URL, e.g. https://joe-shwa.github.io/prototype-tags/
Have her create the Google Sheet (see structure below), and a Drive folder for reference images. Share both links with yourself so you can sanity-check them, or just have her keep them handy for setup.
Setting up the Google Sheet

Row 1 must be headers (order doesn't matter — matching is case-insensitive):

Prototype Name	Category	Priority	Status	Description	Image	Fabricator	Created Date
Combs	Wood	Low	Completed	Replicate wooden comb in slightly different styles...	combs-photo	Joe Blog	17/8/2026
Category: Ceramics / Wood / Metal / Textile / Paper / Paint / 3D Print
Priority: High / Medium / Low
Status: Idea / In progress / Completed
Image: just needs to roughly match a filename in the image folder — doesn't need the file extension or to be an exact match (e.g. "Combs" will find combs-photo.jpg)
Completed Date is intentionally left off the sheet — it prints as a blank line on the form for the fabricator to fill in by hand

Tip: use Google Sheets' Data → Data validation to turn Category/Priority/Status into dropdowns, so entries stay consistent.

Setting up the image folder

Create a Drive folder and drop reference photos into it, named however makes sense (they just need to contain the text from the sheet's Image column somewhere in the filename).

First time opening the app
Tap Connect Google → sign in → grant access (read Sheets, read Drive files, and a private settings space)
Paste in the Sheet link and the image folder link
Tap Save & load prototypes

After that, opening the app just shows the list straight away.

Day to day
List view: every prototype, filterable by status, with colour-coded priority/status badges
Tap a row: opens the full printable tag — description, image, fabricator, dates
🖨 Print: opens the browser print dialog — print directly or "Save as PDF"
↻ (top right): pulls the latest data from the sheet (also happens automatically when reopening the app)
⚙ Settings: change badge colours, or update the connected sheet/folder
Colour customisation

Badge colours for Category, Priority, and Status are set in ⚙ Settings, with sensible defaults pre-filled. Changes are saved to her Google Drive automatically, so they carry across devices — no need to reset them up on the iPad vs the phone. A Reset colours to default button is included if needed.

Troubleshooting
"This app isn't verified" → her account hasn't been added as a test user yet (see step 1 above)
No image showing on a form → the Image column text doesn't match any filename in the folder closely enough — check spelling/spacing
Data looks out of date → tap ↻ to force a refresh
