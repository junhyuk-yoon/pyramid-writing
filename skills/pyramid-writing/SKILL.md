---
name: pyramid-writing
description: Write and edit business documents with the Pyramid Principle (So What, Why So, MECE). Use for reports, weekly updates, meeting notes, plans, proposals, analysis write-ups, wiki pages, memos, and work email, in any tool (Confluence, Google Docs, Notion, Word, Apple Notes, Markdown, Slack, email) and any language. Use it whenever the user says things like "write a report", "status update", "executive summary", "conclusion first", "tighten this doc", "make it MECE", "보고서 써줘", "문서 정리해줘", "회의록 정리", "개조식으로", "결론부터", "두괄식으로", "피라미드 구조로", "이 글 다듬어줘", or shares a document link or pasted text and asks to fix or review it, even if they never name the principles. Do not use for fiction, essays, ad copy, or code comments.
---

# Writing with The Pyramid Principle

Readers of business documents are busy and rarely read to the end. So put the conclusion on top and stack the evidence below it. Check the pyramid with three questions.

- **So What** (bottom to top) : what is the conclusion, and what should we do
- **Why So** (top to bottom) : why can we say that
- **MECE** (same level) : is anything missing or duplicated

A document works when a reader who skims only the headings and bold lines gets the conclusion, and a skeptical reader finds the evidence right below.

## Language

Write the document in the language the user is writing in, or the language of the source document.

- Korean : read `references/korean.md` first. It holds the Korean phrasing conventions and Korean examples for every rule here.
- AI-style cleanup : read `references/ai-tells.ko.md` for Korean, `references/ai-tells.en.md` for English. For other languages, apply the same categories in that language.

## Workflow

1. **Fix the reader and the purpose.** You cannot pick a conclusion without knowing who reads this and what they decide. If the conversation does not tell you and you cannot infer it, ask once.
2. **Extract the conclusions first.** Before writing the body, write one line for the document's conclusion and one line per section. If no conclusion comes out, the material is thin or the thinking is unfinished. Tell the user so.
3. **Build the structure.** Split sections so they do not overlap, and number them.
4. **Fill in the evidence.** Put numbers and sources right below each conclusion.
5. **Cut.** Run the "What to cut" list below.
6. **Remove AI style.** Run the "AI-style cleanup" section below.
7. **Format for the tool.** The structure stays the same and only formatting changes. If the target tool is known, read its entry in `references/tools.md`.

## When given a link or pasted text

If the user gives only a link or text with no further instruction, treat it as a request to revise it by these principles.

1. **Read the document.** Use whatever is connected for that tool (connector, MCP, browser). Do not try to fetch a login-protected document with a plain web request. If you cannot read it, ask the user to paste the text.
2. **Report a short diagnosis first.** One or two lines per axis (So What, Why So, MECE) on the biggest problem. Write "no issue" for an axis that is fine.
3. **Write the revision.** Do not change facts, numbers, or proper nouns. Do not invent evidence the original lacks. Mark it "evidence needed".
4. **Do not overwrite the original.** Show the revision in the conversation or create a new document. Edit the original in place only when asked, and then follow "Editing an existing document" below.
5. **Return it in the same tool's formatting.** A linked document will be pasted back into that tool, so follow its entry in `references/tools.md`.

## 1. So What : conclusion first, in one line

- **The heading is `keyword : conclusion`.** Open every section heading with a short topic keyword, then state the conclusion after ` : `. The keyword tells the reader where they are, and the conclusion tells them what to take away. A topic alone says nothing, and a conclusion alone is hard to scan and to point at in a meeting. The table of contents alone should tell the story.
  - Topic only : `3. Repurchase rate status`
  - Conclusion only : `3. Customers leave within 30 days of first purchase, so the repurchase rate is falling`
  - Keyword : conclusion : `3. Repurchase rate : falling, customers leave within 30 days of first purchase`
  - Keep the keyword a noun label of a few words (`Comparison by type`, `Purchase path`, `Legal review`), and reuse the label a reader would search for.
  - Keep the conclusion to one short point. The rest goes to the first bullet.
  - Subheadings follow the same shape : `3-1. Entry path : 57% arrive from a list search`
- **A first-level bullet is one conclusion line.** Keep it short and declarative. Drop spoken filler such as "we are pleased to share" or "as you can see".
- **One bold line per block.** Bold only the line that carries the judgment or decision. When several lines are bold, nothing stands out.
- **Connect data to action with an arrow.** Do not stop at the number. Attach what to do.
  - `62% of repeat buyers have notifications on → prompt for notification consent right after first purchase`
- **List only actions you can take.** Things you can only watch are monitoring, not actions.
- **No caveats in a decision heading.** Move limits and conditions to sub-bullets. A parenthetical caveat in the heading leaves the reader unsure whether a decision was made.
  - With caveat : `Free shipping : effective (though long-term effect needs more validation)`
  - Without : `Free shipping : judged effective, roll out to all stores next month`

## 2. Why So : evidence right below every conclusion

- **A second-level bullet is evidence.** Numbers and facts sit directly under the conclusion. Table cells follow the same order : conclusion, evidence, supporting detail.
- **Keep unconfirmed causes out of the summary.** Causes in a summary must be confirmed by data. Put guesses in the body or Notes and label them "estimate". When guesses mix into a summary, readers take everything as fact.
- **Cite the source.** Put the link to the supporting document in the first sub-bullet of a decision. State the period, basis, and exclusions for numbers above the table or in a note.
- **Record decisions as evidence → conclusion → follow-up.** State the follow-up trigger as a number, with both a ratio and an absolute value.
  - `Review again if refunds reach 200% of the prior 3-month average (over 90 per month)`
- **Name the specific cause.** Not "weak performance" or "lower volume". Say which stage dropped (visits, conversion, order value).
- **Do not assert causation.** Two things moving together is not proof that one caused the other.

## 3. MECE : no overlaps, no gaps

- **One metric per bullet.** Do not chain several metrics on one line with commas or dots. Keep only the grouping label on the parent bullet and give each metric its own sub-bullet. With several numbers on one line, the reader cannot tell which one matters.

  ```
  Bad  : Participating stores revenue 1.9x, orders 1.8x, conversion 6.4% → 9.8%

  Good : Participating stores
           - Revenue 1.9x
           - Orders 1.8x
           - Conversion 6.4% → 9.8%
  ```

- **The summary covers exactly what the table covers.** If the table covers a subset, limit the summary to that subset and state the basis in the subheading (`Revenue by region : year over year, app only`).
- **Put each item where it belongs.** A sub-decision goes under its parent topic. If the same content appears in two sections, merge it into one.
- **Split sections on one axis.** Within one level, use a single classification axis (if by region, by region throughout). Mixed axes create overlaps and gaps.
- **Fix the structure with numbering.** Use `1.` → `1-1` → `1-1-1`. Numbers let people point to "see 2-3" in a meeting.
- **Do not drop unfavorable information.** Items with zero samples, estimates, numbers on different bases, and warning signs go in a "Caveats" or "Notes" section. Removing them to look clean makes the whole document untrustworthy.

## 4. Expression

- **The separator is ` : `, always.** Use a colon with one space on each side to split a label from its content and to attach a supporting note, in headings and bullets alike. Replace only mid-line dashes (—, –) used as separators. The hyphen that starts a bullet line is a list marker and stays. One fixed separator lets readers parse "label : content" at a glance, and repeated dashes make text read as machine-written.
  - Dash : `1. Definition — a joint promotion of up to one month with top stores`
  - Colon : `1. Definition : a joint promotion of up to one month with top stores`
  - Bullets stay : in `- Long-term effect unconfirmed : recheck in 4 weeks` the leading `-` stays and only a mid-line dash would change.
  - The arrow (→) is not a separator. Use it only for "data to action" and "old value to new value".
- **One term per thing.** Use one official name for each metric and program. Mixing "price", "order value", and "ASP" for the same thing makes readers see three different metrics.
- **Names, not internal IDs.** Readers remember names, not numbers.
- **No slang for numbers.** Write "fell sharply" with the figure, not "tanked" or "cratered".
- **Units on every number.** Thousands separators for amounts and counts, % for ratios. In a table, state the unit once above the table or in the header.
- **Do not promise what is not confirmed.** Write "decide after a feasibility review", not "launching next year".
- **Use tables freely.** Comparisons, schedules, before and after, and ownership read faster in a table than in sentences.
  - Cells hold short phrases or up to three bullets, not sentences.
  - No bold inside tables. Emphasize in the sentences outside.
  - Item columns are noun labels (`1. Refund rate trend`), not questions or sentences.
  - Data tables end with a total row.
- **Mark unfinished items with `TBD` and an expected date.** `TBD (second draft due next week)`

## 5. What to cut

After drafting, delete anything below. Words that can go without changing the meaning cost the reader time.

- Tails that repeat the conclusion : `: all targets met`
- Comparison parentheses unrelated to the point : `(60.9% the day before)`
- Double markers for the same state : adding "(unconfirmed)" to "under discussion"
- Schedules everyone knows, obvious background
- Statistical terms with no explanation : if one is needed, add a plain one-line gloss
- Long histories of resolved issues : shorten to `Shipping delay impact ended`
- Self-corrections inside the document : write only what is true now, not "earlier we said A, now B"

## 6. AI-style cleanup

Good structure does not save a document whose sentences read as machine-written. Readers start doubting the content. After drafting, remove the patterns below. The full lists with fixes are in `references/ai-tells.en.md` and `references/ai-tells.ko.md`. Read the one for your output language when the document has many full sentences (summary paragraphs, background, email).

- **Stock phrases** : "in conclusion", "it is worth noting", "plays a crucial role", "moving forward". Delete them or write the specific point.
- **Hype words** : "groundbreaking", "robust", "seamless", "game-changing". Replace with numbers and facts.
- **Sentence-opening connectives** : "Additionally", "Furthermore", "Moreover". Delete. Order and numbering already show the flow.
- **Hedging** : "may potentially", "it seems that", "could possibly". State what is confirmed. Label what is not as an estimate.
- **False balance** : do not end on "there are pros and cons". Write the judgment.
- **Decoration** : no emoji, no scare quotes for emphasis, no scattered bold, no mid-line dashes.
- **Uniform rhythm** : bullets that all share one length and one ending look mechanical. Let length follow content.

Hold three lines while cleaning. Never change numbers, dates, proper nouns, or quotations. Do not add metaphors or flourishes the original did not have. Keep the original level of formality.

## Editing an existing document

- **Change only what was requested.** Leave other sections, wording, and tables exactly as they are.
- **Never revert the user's own edits.** Their changes win even when they differ from this skill's rules.
- **Follow the document's existing conventions.** Match its heading levels, numbering, and table shapes.
- When asked to proofread, do not rewrite everything. Say briefly what changed and why.

## Priority

If the user or their team has set a template, vocabulary, or tone, that comes before this skill. This skill is the default when nothing else is set.

## Final check

- Is every heading a `keyword : conclusion` pair, and do the headings alone convey the conclusion
- Does every conclusion have evidence right below it
- Is the summary free of guesses
- Does each number lead to an action where one is needed
- Does any line hold more than one metric
- Does the same content appear in two places
- Are unfavorable facts and limits kept in Notes
- Is there at most one bold line per block
- Is ` : ` the only separator, with no mid-line dashes left
- Are stock phrases, hype words, and sentence-opening connectives gone

## Example

**Before**

```
2. Promotion results

In conclusion, the free shipping promotion we ran last week delivered
strong results overall. Participating stores saw revenue up 1.9x, orders
up 1.8x, and conversion from 6.4% to 9.8%, a major recovery after last
month tanked (5.1% the month before). That said, further validation may
be needed regarding the long-term effect, and stock issues could
potentially have played a role.
```

**After**

```
2. Promotion results : free shipping judged effective, roll out to all stores next month

- **Participating store revenue up 1.9x → roll out to all stores**
  - Source : promotion results sheet (link)
  - Revenue 1.9x
  - Orders 1.8x
  - Conversion 6.4% → 9.8%
- Follow-up
  - Review again if 4-week conversion after rollout falls below 8%

Notes
- Long-term effect unconfirmed : recheck with repurchase rate in 4 weeks
- Stock shortage impact is an estimate, no data yet
```
