# Contributing

Thanks for helping keep this list sharp. It is a curated list of resources that save human attention, not a directory of useful tools. Most submissions are declined, and that is the point.

## Inclusion criteria (hard gate)

A resource must pass **all three** checks:

1. **It makes people read less, watch less, click less, or wait less.** If the main effect is "accomplish more, faster", it belongs on a productivity list instead.
2. **You can name the attention it saves in one sentence.** For example: "Turns a 30-minute doc read into a ranked five-item brief."
3. **It can be evaluated without friction.** The link opens without an account, or a free account is enough to see what it actually does.

If you cannot write that one sentence, the resource does not belong here yet.

## What we do not list

- General productivity, note-taking, or task-management apps with no attention-specific mechanism.
- AI wrappers that only put a chat box in front of an existing product.
- Closed-source services you must register for before you can verify anything.
- Dead links, abandoned projects, and pages that now redirect somewhere else.
- Marketing pages, waitlists, and "coming soon" landing pages.
- Duplicates of a resource already listed.

## Entry format

```markdown
- [Name](https://example.com) - Sentence-case description ending with a period.
```

Rules:

- One line per entry, description on the same line.
- The description is sentence case, ends with a period, and starts with a capital letter.
- Descriptions must not begin with "A", "An", or "The".
- Use the resource's official name. Do not invent a shortened or translated name.
- URLs have no trailing slash and no tracking parameters.
- At most **3 new entries per pull request**, so each can be reviewed properly.
- Change **one category per pull request**. Put anything else in a separate PR.

## Categories

| # | Category |
|---|---|
| 1 | Foundations & Reading |
| 2 | Awesome Lists & Meta |
| 3 | Distill: Docs to Answers |
| 4 | Triage: Rank, Dedupe, Batch |
| 5 | Maps & Progressive Disclosure |
| 6 | Calm & Focus |
| 7 | Attention-Saving Dev Workflow |
| 8 | Anti-Patterns & Research |
| 9 | Organization & Life |

New categories need an issue first. Open an issue explaining which resources do not fit the nine existing categories and why the new one is not a rename of an old one. Do not add a category in a PR.

## Local checks

Run these before opening a pull request:

```bash
npx awesome-lint
node scripts/sync-catalog.mjs --check
```

If the catalog check fails, regenerate it and commit the result:

```bash
npm run sync
```

## Skills and generated files

`skills/attention-engineering/references/catalog.md` is generated from `README.md` by `scripts/sync-catalog.mjs`. Never edit it by hand. If your change touches list entries or skill references, run `npm run sync` and include the regenerated file in the same commit.

## Review

A maintainer checks the inclusion criteria, the link, and the formatting. Expect edits to your description: concise, factual phrasing wins over marketing language.
