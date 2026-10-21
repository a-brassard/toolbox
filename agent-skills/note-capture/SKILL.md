---
name: note-capture
description: Save part of the current conversation as a concise Notion note when the user says "make a note of ___", "let's note this", or naturally asks to record something in Notion.
category: productivity
---

Use this skill when the user says “make a note of \_\_\_\_\_”, “let’s note this”, or naturally asks to save part of the current conversation as a Notion note. Treat the topic as a scope cue, not a required title. Do not require an @ mention or explicit skill name. Do not trigger on a quoted example, negation, or discussion of the trigger itself.

## Outcome and interaction

Create one concise, self-contained information packet directly in the user's Notes database during the current turn. The user has authorized direct saves and reviews AI entries later through Stack. Do not ask for draft approval, confirmation, immediate review, or an additional safeguard. Finish the write before reporting success; “background” means minimal interruption, not a promise of work after the turn ends.

## Resolve the scope

Use the requested topic and surrounding conversation to select the useful information. Carry forward corrections, qualifications, and unresolved questions. If the relevant conversation is unavailable, retrieve the specific prior context when possible. Ask one short scope question only if the subject cannot be recovered well enough to write a faithful note. Do not invent missing discussion or turn tentative ideas into conclusions.

## Write the note

Choose a descriptive, informative title independently of the rough topic wording. Aim for about 80–120 words in the body: a self-contained, roughly 30-second reference packet.

Start with a plain-language sentence orienting a future reader. Present the key findings or distinctions compactly, with useful source links when available. Use neutral, explanatory, assistant-authored prose in English. Distinguish established evidence from inference, hypothesis, and uncertainty. Attribute a user proposal when needed rather than presenting it as an established fact.

End with a short **Context** section of one or two descriptive sentences explaining why this information was retained. Do not write a transcript, chronological thinking log, motivational commentary, or first-person text impersonating the user. Do not fill the word target with repetition.

Reuse sources already available; open a cited source if its contents are needed to support the note. Do not invent citations or imply independent verification. Do not expand a capture request into unrelated research.

## Destination and properties

Use the current Notes database, not an older database with the same name:

- Database: https://app.notion.com/p/3fb6dbf38dc580bdbe18f8712f1d8012
- Database ID: `3fb6dbf3-8dc5-80bd-be18-f8712f1d8012`.
- Data source: `collection://3fb6dbf3-8dc5-808f-85d9-000b9795cfbb`.

Fetch this database or data source before each capture operation, unless its current schema was already fetched in the same turn. Treat the live schema as authoritative; do not recreate missing fields, invent options, or silently switch to another Notes database.

Set the following properties using the fetched schema:

- `Name`: descriptive title.
- `Type`: `Info (AI)`.
- `Status`: `Open`. This is the user's existing Stack review safeguard; do not close it after saving.
- `Author`: `Worker` for research and intellectual content; `Admin` for administrative processes; `Technician` for tools, systems, and workflows. These are role categories, not human authorship claims.
- `Folder`: omit by default. Choose an existing option only when it clearly applies. Use the exact live spelling; for example, `Notes & archives` for note-taking and archiving workflows. Do not classify all captured notes there merely because they are notes.
- `Created`: omit; Notion sets it automatically.

Author, Folder, and Type are select properties; Status is a status property; Name is the title.

## Save and verify

Use the available Notion search, fetch, and create-page capabilities. Read `notion://docs/enhanced-markdown-spec` before writing if it has not already been loaded. Create a normal note under parent data_source_id `3fb6dbf3-8dc5-808f-85d9-000b9795cfbb`, with properties and body together. Keep the title in Name rather than repeating it in the body. Do not designate captured notes as skills, alter the database schema, change views, move existing pages, or change sharing.

Wait for any asynchronous creation task to succeed before proceeding. Fetch the created page and verify its body, destination, and intended properties before confirming success. If a write times out or has an ambiguous result, check for the created page before retrying to avoid duplicates.

If tools or required schema options are unavailable, say briefly that the note was not saved and identify the blocker; preserve the drafted text in the reply if useful. Never claim a queued or failed write is complete.

## Reply

After a verified save, return only a brief confirmation and the page link, such as “Saved: [Title](page URL).” If the user also asked a substantive question, answer it in the same turn without requiring a detour into note review.
