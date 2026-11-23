# AI-style cleanup (English)

Patterns that make English text read as machine-written, with fixes. The categories follow [epoko77-ai/im-not-ai](https://github.com/epoko77-ai/im-not-ai) (MIT), which covers Korean. The English entries here were written for business documents. For Korean, read `ai-tells.ko.md`.

## Hold these lines first

- Never change numbers, dates, units, proper nouns, product names, or quotations.
- Do not add metaphors, flourishes, or jokes the original did not have.
- Keep the level of formality. A report must not turn into a blog post.
- When editing existing text, change only what is needed. If more than half changed, you overdid it. Go back.

## 1. Stock phrases

| Pattern | Fix |
|---|---|
| In conclusion, To summarize, Overall | Delete. The conclusion is already in the heading and first line |
| It is worth noting that, It is important to note | Delete and state the point |
| plays a crucial role, is a testament to | Say what it does, with a number |
| Moving forward, Going forward | Delete or give the date |
| At the end of the day, When it comes to | Delete |
| Let's dive in, Let's break it down, Here's the thing | Delete |
| In today's fast-paced world, In the ever-evolving landscape | Delete the whole opener |
| I hope this helps, Feel free to reach out | Delete in documents. In email keep one closing line at most |

## 2. Hype and filler vocabulary

| Pattern | Fix |
|---|---|
| groundbreaking, game-changing, cutting-edge, revolutionary | Replace with the measured result |
| robust, seamless, comprehensive, holistic | Say what it covers or handles |
| leverage, utilize, harness | use |
| delve into, navigate, unpack | look at, handle, explain, or delete |
| unlock, empower, elevate, foster | State the concrete effect |
| crucial, pivotal, vital, key (repeated) | Keep one at most. Show importance with impact |
| landscape, realm, tapestry, journey | Name the actual market, field, or process |
| very, really, truly, incredibly, extremely | Delete or replace with a number |

## 3. Connectives and signposting

- Delete sentence-opening "Additionally", "Furthermore", "Moreover", "In addition". Bullets and numbering already show order.
- Limit "However" and "That said" to places with a real reversal.
- Do not start sentences with "This" or "This means" when the referent is vague. Name the subject.
- Do not announce what you are about to say ("Here are three reasons"). Give the reasons.

## 4. Hedging

| Pattern | Fix |
|---|---|
| may potentially, could possibly, might perhaps | One modal at most. If confirmed, state it |
| it seems that, it appears that, arguably | State it if confirmed. Otherwise label it an estimate |
| somewhat, relatively, fairly, to some extent | Delete or give the number |
| While X, it is important to consider Y | Write the judgment : which one wins and why |
| There are pros and cons | List them once, then decide |
| Further review is needed | Say who reviews what by when |

Removing hedges does not mean asserting things without evidence. State what is confirmed, label what is not as "estimate" or "unconfirmed", and cut only the blur in between.

## 5. Sentence templates

- "It's not X, it's Y" and "not just X, but Y" : say Y directly.
- Lists of exactly three adjectives or phrases, repeatedly : use as many as there are.
- Rhetorical question followed by its own answer ("The result? A 20% lift.") : state the result.
- "Whether you're A or B" openers : delete.
- A short punchy sentence closing every paragraph : keep it only where it adds information.
- "From X to Y" used as a sweep ("from startups to enterprises") : name the actual scope.

## 6. Wordy constructions

| Pattern | Fix |
|---|---|
| in order to | to |
| due to the fact that | because |
| at this point in time | now |
| a number of, a variety of | the number, or "several" |
| the implementation of the plan | implementing the plan |
| make a decision, conduct an analysis | decide, analyze |
| is able to, has the ability to | can |
| It was decided that (no actor) | Name who decided |
| with regard to, regarding, in terms of | about, on, for, or restructure |

## 7. Decoration

- No emoji. If a status marker is needed, use the tool's status element or a word ("Done", "In progress").
- No quotation marks for emphasis. Quotes are for quotations and names.
- One bold line per block.
- No mid-line dashes (—, –). Use ` : ` as the separator. The leading `-` of a bullet stays.
- Do not start every bullet with a bold label followed by a restatement.
- No Title Case In Every Heading. Use sentence case.
- No "(1), (2), (3)" inside a sentence. Use a list.

## 8. Rhythm

- Bullets that all have the same length and the same shape look mechanical. Short content gets a short bullet.
- Do not pad or trim a list to reach three items.
- Do not restate the heading in the first sentence under it.
- Do not end sections with a summary of what the section just said.

## Before and after

```
Before:
In conclusion, this redesign has the potential to be a game-changer for
the customer experience. Additionally, it's worth noting that the data
suggests a positive impact with regard to return visits, which is a
testament to the team's robust approach.

After:
- Return visits rose after the redesign : extend to all customers
  - Return visit rate 18% → 24%
  - Based on 1,200 customers on the new design, observed for 4 weeks
```
