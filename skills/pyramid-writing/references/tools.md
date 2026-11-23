# Formatting per tool

The principles and the structure do not depend on the tool. This file only maps the same structure onto each tool's features. Read only the entry for your target tool.

When a tool lacks a feature, do not imitate it. Fall back to the simpler form in "When a feature is missing".

## Contents

- Common mapping
- Confluence (Atlassian)
- Google Docs
- Notion
- Microsoft Word
- Apple Notes
- Markdown (GitHub, terminal)
- Slack and chat
- Email
- When a feature is missing

## Common mapping

| Element | Role |
|---|---|
| Document title | Topic and status in one line |
| Top summary | Conclusion in one or two sentences (analysis, proposal, review) |
| Section heading | Number plus conclusion |
| First-level bullet | Conclusion |
| Second-level bullet | Evidence, numbers, source |
| Table | Comparison, schedule, before and after, ownership |
| Notes | Limits, estimates, differences in basis |

## Confluence (Atlassian)

- Use Heading 2 for sections and Heading 3 and 4 below. A divider under each section heading helps in long pages.
- Use the date element, mentions, status lozenges, and smart links for dates, people, status, and links. They are searchable, trigger notifications, and are easy to update. Keep rough expressions ("the 5th of every month", "next week") as text.
- Use one color rule for status across the page (one color each for done, in progress, not started).
- Info panels are optional. Skip them when tables and numbering already make the point.
- Cells can hold bullets, so write up to three bullets per cell.
- Updating a page through the API overwrites the whole body. Fetch the latest body right before saving, replace only the requested part, and save the rest unchanged.

## Google Docs

- Use heading styles (Heading 1 to 4). Text that is only enlarged does not appear in the outline or table of contents.
- Numbered list levels default to 1 → a → i. Type section numbers (`2-1`) directly in the heading text.
- Smart chips (type @) work for dates, people, and files.
- Cells can hold bullets. Fit table width to the page.
- When pasting from elsewhere, check that heading styles and list levels survived.

## Notion

- Use Heading 1 to 3. Put anything deeper into toggles or sub-pages.
- Use a callout for the top summary and for warnings.
- For tables of repeating items with status, owner, and date (trackers, schedules), use a database, not a simple table. Use select for status, date for dates, person for owners.
- Simple table cells cannot hold bullets. Write short phrases and use line breaks inside the cell when needed.
- Insert dates and people with @ mentions.

## Microsoft Word

- Use heading styles (Heading 1 to 3). The automatic table of contents and navigation pane read them.
- Number sections either by linking a multilevel list to heading styles or by typing numbers in the heading. Do not mix both in one document.
- Mark the first table row as a header row so it repeats across pages.
- Put the top summary in the first paragraph, bold, one or two sentences.
- The document may be printed or exported to PDF, so link the text and also write the name of key sources.

## Apple Notes

The feature set is small, so keep the structure simple.

- The first line becomes the note title. Put the conclusion in it.
- Styles are limited to Title, Heading, Subheading, and Body. Use Heading for sections and Subheading below, and type numbers as text.
- Use two bullet levels at most (conclusion, evidence).
- Tables are plain rows and columns, and cells cannot hold bullets. Use short tables of up to three columns. Turn anything more complex into bullets.
- Use checklists for to-dos.
- Type dates and owners as text.

## Markdown (GitHub, terminal)

- Use `##` for sections and `###`, `####` below.
- Table cells cannot hold bullets or line breaks. Write short phrases and attach supporting notes with ` : `. HTML tags (`<br>`, `<ul>`) show up as literal text in a terminal, so do not use them. If content does not fit a cell, split the table or use bullets.
- Put code, queries, and config values in code blocks, with the source and basis in a comment at the top.

## Slack and chat

- Put the conclusion on the first line. Notification previews show only that.
- There are no headings, so use one bold line as a subheading.
- Use two bullet levels at most.
- Tables break on narrow screens. Keep them to three columns or use bullets. Leave a blank line after a table and put interpretation outside it.
- For long content, write the summary in the message and move the rest to a thread or a linked document.

## Email

- Put the conclusion or the ask in the subject line (`[Decision needed] Roll out free shipping to all stores : reply by Friday`).
- Put the conclusion and what you need from the reader in the first paragraph.
- Formatting can disappear in the recipient's client, so build structure with numbers and line breaks that survive as plain text.
- One line each for greeting and sign-off.

## When a feature is missing

| Missing feature | Use instead |
|---|---|
| Heading styles | One bold line plus a number |
| Bullets in cells | Short phrases joined with ` : `, or turn the table into bullets |
| Date, person, status elements | Plain text (full dates such as `2025-03-14`) |
| Toggles | A separate "Details" section at the end |
| Callouts, panels | One or two bold sentences at the top |
| Tables | Bullets per item (item name, then attributes below) |
| Three or more indent levels | Split into subsections |
