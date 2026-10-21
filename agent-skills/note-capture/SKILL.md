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

When a visual would clarify the note, put it first, before the prose. Then use a short opening paragraph to orient the reader and state the main point. For source-based notes, introduce the source and organize its key takeaways into a compact bulleted list when that improves scanability; follow with a short paragraph for a related distinction or implication. Keep the prose neutral and assistant-authored in English. Distinguish established evidence from inference, hypothesis, and uncertainty. Attribute a user proposal when needed rather than presenting it as an established fact.

After the key findings, add a **Resources** section when useful, then finish with a **Context** callout. Write Context in your voice, addressing the user directly, in one or two sentences that remind them why and when they asked for the note. Do not write a transcript, chronological thinking log, motivational commentary, or first-person text impersonating the user. Do not fill the word target with repetition.

### References for claims

Support factual, empirical, or technical claims with a source. Prefer a direct inline link on the claim; a short linked marker is also fine when it clearly maps to a numbered **Resources** entry. Do not leave bare, unresolved markers. In **Resources**, use concise linked titles and include author or publisher when useful; do not force dates or other metadata that add no value. Prefer primary and authoritative sources (papers, official docs, standards) over summaries. Keep inference, hypothesis, and user proposals visibly separate from sourced claims. Never invent or reconstruct a citation from memory: use only sources from the conversation, or ones opened and checked in this turn. Cite the specific material actually consulted; when only part of a source was read, describe that part rather than implying the whole source was reviewed. Keep citations concise and free of process commentary such as "not opened here" or "not independently verified." If a key claim has no available source, say so rather than omitting the gap.

### Visuals

Include a visual when it conveys the content better than prose, such as a relationship, process, comparison, or timeline. Choose the lightest form that works:

- A Mermaid diagram (code block, language `mermaid`) for flows, hierarchies, and relationships.
- A table for comparisons across several dimensions.
- An image embed only when its URL came from a source already in the conversation or one you opened, with a caption crediting the source. Never guess image URLs.

Use at most one visual per note, place it at the top, and skip it when prose is clear enough. A fetched Markdown page can confirm that the visual content was saved, but not that it renders in the Notion UI. Prefer a table when diagram rendering cannot be confirmed; if using Mermaid, verify the rendering in the Notion UI when available.

### Context callout

Finish with a Notion callout using the gray information icon and no explicit color, so it keeps the plain background. Put one or two sentences in your voice inside it, addressing the user directly and reminding them why and when they asked for the note (for example, “You wanted a test note to refine the note-writing skill with.”). Do not add a **Context** heading inside the callout or use generic archival language.

### Further reading

In the **Resources** section at the bottom, list the sources supporting claims and up to three useful further-reading links, each with a short phrase describing its value. Include the source used and any directly relevant resources surfaced while reading it; one quick search is allowed only to find a canonical reference for the core topic. Do not turn a capture request into a research task, and omit Resources if nothing credible is available. Place it after the prose and immediately before the final callout.

### Length

The 80–120 word target applies to the prose body. The visual and Resources section are additional, but keep the whole note a quick-scan reference. Reuse sources already available; open a cited source if its contents are needed to support the note.

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

Use the available Notion search, fetch, create-page, and update-page capabilities. Read `notion://docs/enhanced-markdown-spec` before writing if it has not already been loaded. Create a normal note under parent data_source_id `3fb6dbf3-8dc5-808f-85d9-000b9795cfbb`, with properties and body together. Keep the title in Name rather than repeating it in the body. Do not designate captured notes as skills, alter the database schema, change views, move existing pages, or change sharing.

Wait for any asynchronous creation task to succeed before proceeding. Fetch the created page and verify its body (including that the visual is first, Resources links are present, and the final Context is a callout), destination, and intended properties before confirming success. If a write times out or has an ambiguous result, check for the created page before retrying to avoid duplicates.

If tools or required schema options are unavailable, say briefly that the note was not saved and identify the blocker; preserve the drafted text in the reply if useful. Never claim a queued or failed write is complete.

## Reply

After a verified save, return only a brief confirmation and the page link, such as “Saved: [Title](page URL).” If the user also asked a substantive question, answer it in the same turn without requiring a detour into note review.
