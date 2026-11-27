# Writing with The Pyramid Principle

English | [한국어](README.ko.md)

**A Claude skill that writes and edits business documents so the conclusion is readable from the headings alone.**

Give it a document link or pasted text. It diagnoses the document with three questions (So What, Why So, MECE) and returns a revised version. The same principles apply to Confluence, Google Docs, Notion, Word, Apple Notes, Markdown, Slack, and email. Only the formatting changes per tool.

## 1. Effect : the same content now opens with the conclusion and the next action

Before

```
2. Promotion results

In conclusion, the free shipping promotion we ran last week delivered
strong results overall. Participating stores saw revenue up 1.9x, orders
up 1.8x, and conversion from 6.4% to 9.8%, a major recovery after last
month tanked. That said, further validation may be needed regarding the
long-term effect.
```

After

```
2. Promotion results : free shipping judged effective, roll out to all stores next month

- **Participating store revenue up 1.9x → roll out to all stores**
  - Revenue 1.9x
  - Orders 1.8x
  - Conversion 6.4% → 9.8%
- Follow-up
  - Review again if 4-week conversion after rollout falls below 8%

Notes
- Long-term effect unconfirmed : recheck with repurchase rate in 4 weeks
```

| What changed | Principle applied |
|---|---|
| Topic heading → `keyword : conclusion` heading | So What |
| "Strong results" → numbers and a next action | So What, Why So |
| Three metrics on one line → one per line | MECE |
| Caveat buried in a sentence → moved to Notes | MECE |
| "In conclusion", "regarding", "tanked" removed | AI-style cleanup |

No number changed. Only the order and the structure did.

## 2. Principle : put the conclusion on top and stack the evidence below

Readers of business documents are busy and rarely read to the end. With the conclusion on top, a reader who stops at the first line still leaves with the conclusion.

```
                  Conclusion
        ┌─────────────┼─────────────┐
    Evidence 1    Evidence 2    Evidence 3
        │             │             │
     numbers       numbers       numbers
     sources       sources       sources

  Bottom → top   So What : what does this mean
  Top → bottom   Why So  : why is that true
  Same level     MECE    : no overlaps, no gaps
```

| Principle | Direction | Question | Typical rule |
|---|---|---|---|
| So What | Bottom → top | What is the conclusion | Headings read `keyword : conclusion`, numbers lead to an action with an arrow |
| Why So | Top → bottom | Why can we say that | Numbers and sources sit right below each conclusion, guesses stay out of the summary |
| MECE | Same level | Is anything missing or duplicated | One metric per bullet, unfavorable facts stay in Notes |

Two sentence-level rules sit on top of the three principles.

- One separator : write `1. Definition : content`, not `1. Definition — content`
- AI-style cleanup : translationese, stock closing phrases, hype words, sentence-opening connectives

The pyramid structure comes from Barbara Minto's *The Pyramid Principle*. *Logical Thinking* by Hanako Teruya and Keiko Okada grouped So What, Why So, and MECE into one set. This skill turns the principles of both books into rules you can apply to a working document.

## 3. Scope : every business document, no creative writing

- Use it for
  - Reports, weekly updates, meeting notes
  - Plans, proposals, analysis write-ups
  - Wiki pages, memos, work email
- Do not use it for
  - Fiction, essays, ad copy
  - Code comments

You do not need to name the principles. Saying "conclusion first", "make this tighter", or just sharing a document link triggers the skill.

## 4. How it works : diagnosis first, original untouched

1. Reader and purpose : it identifies who reads the document and what they decide. If unclear, it asks once.
2. Diagnosis : it reports the biggest problem on each axis (So What, Why So, MECE) in a line or two.
3. Revision : it keeps every fact, number, and proper noun from the original.
4. Tool-ready output : it returns the result in the formatting of the tool the document came from.

It holds three lines.

- Conclusions without evidence are marked "evidence needed", never invented
- The original document is not overwritten : the revision is delivered separately
- When asked to edit in place, it changes only the requested part

## 5. Install : two commands, entered one at a time

Install as a plugin in Claude Code. Enter the commands one at a time. Pasting both lines together runs them as one command and fails.

```
/plugin marketplace add junhyuk-yoon/pyramid-writing
```

Then install the plugin.

```
/plugin install pyramid-writing@pyramid-writing
```

Or copy the folder without the plugin system.

```bash
git clone https://github.com/junhyuk-yoon/pyramid-writing.git
cp -r pyramid-writing/skills/pyramid-writing ~/.claude/skills/
```

For the Claude apps (claude.ai, desktop), upload a zip.

1. Download this repository.
2. Zip the `skills/pyramid-writing` folder.
3. Upload the zip in the Skills menu under Settings.

## 6. Usage : a link or pasted text is enough

```
Rewrite this document with the pyramid principle : <document link>
```

```
Turn these meeting notes into a weekly update. I will paste it into Notion.
<notes>
```

```
Point out only the places in this draft where the So What is weak.
```

To read a linked document, Claude needs the connector for that tool (Atlassian, Google Drive, Notion, and so on). Without a connector, paste the text.

## 7. Output per tool : same structure, different formatting

| Tool | What it adapts |
|---|---|
| Confluence | Heading levels, date and status elements, bullets inside cells |
| Google Docs | Heading styles, list levels 1 → a → i |
| Notion | Callouts, toggles, databases for repeating items |
| Word | Heading styles, repeating table header row |
| Apple Notes | Two bullet levels, simple tables of up to three columns |
| Markdown | Short phrases in cells in place of bullets |
| Slack, email | Conclusion on the first line, long content behind a link |

In tools without headings or tables, it builds the same structure from one bold line and bullets.

## 8. Self-check : it verifies the output before returning it

- Is every heading a `keyword : conclusion` pair, and do the headings alone convey the conclusion
- Does every conclusion have evidence right below it
- Is the summary free of guesses
- Does any line hold more than one metric
- Does the same content appear in two places
- Are unfavorable facts and limits kept in Notes
- Is there at most one bold line per block
- Is ` : ` the only separator
- Are translationese and stock closing phrases gone

## 9. Files : one rule file and four references

```
skills/pyramid-writing/
├── SKILL.md              all rules and the workflow
└── references/
    ├── ai-tells.en.md    AI-style patterns to remove (English)
    ├── ai-tells.ko.md    AI-style patterns to remove (Korean)
    ├── korean.md         Korean phrasing rules and Korean examples
    └── tools.md          formatting per tool
```

## 10. Language : English and Korean documents are both supported

- The document is written in the language the user writes in
- English : applies the English AI-style list
- Korean : applies Korean phrasing rules and the Korean AI-style list
- Other languages : the structural rules apply as they are, and the tone follows that language's concise report style

## 11. Priority : your team's conventions come first

- If your team or you have a set template or vocabulary, the skill follows that
- Edits you made yourself are never reverted, even when they differ from the skill's rules

## 12. References : two books and one skill

- Barbara Minto, *The Pyramid Principle: Logic in Writing and Thinking* : the source of the pyramid structure and MECE
- Hanako Teruya and Keiko Okada, *Logical Thinking* : the So What, Why So, MECE set
- [epoko77-ai/im-not-ai](https://github.com/epoko77-ai/im-not-ai) (MIT) : the taxonomy behind the Korean AI-style list, trimmed for business documents

This is a personal project with no affiliation with the authors or publishers above. For polishing long-form prose in Korean, use im-not-ai alongside this skill.

## 13. License : MIT

---

This README was written with this skill. Every heading is a "name : conclusion" pair, ` : ` is the only separator, and the single bold line in the body is the one at the top.
