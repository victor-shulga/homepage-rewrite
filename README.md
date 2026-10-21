# homepage-rewrite

A Claude Code skill that rewrites the homepage of a B2B service company (agency, outsourcing,
consulting) on two tracks.

- **Clarity**: a visitor from your target market understands what you sell, to whom and with what
  result from the first screen alone.
- **Trust**: they believe it, because every promise has a named case with a number next to it,
  logos are real clients, testimonials have names, and there are no "coming soon" placeholders.

It builds a proof bank from what is already on your site before writing a word, and never invents
a case, a number, a quote or a logo.

## What you get

One markdown file:

0. **Proof bank and canvas**: every case, number and testimonial found on your site, with its
   source, plus the copy canvas. Inner pages reuse them.
1. **Diagnosis**: clarity score 0-50, trust score 0-12 (rules T1-T6), the three costliest gaps.
2. **New copy per block**: hero, logos, problem, solution, lower-half sections. Each block has a
   one-line rationale saying which proof it uses.
3. **Remove list**: placeholders, unverified logos, numbers without a source.
4. **Pre-ship checklist** with "now" and "after" columns.
5. **Questions** only the company can answer (permission for a logo, the source of a number).

## Install

```bash
npx skills add victor-shulga/homepage-rewrite/skills/homepage-rewrite
```

Add `-g` to make it available in every project. Then in Claude Code:

```
/homepage-rewrite https://your-site.com
```

## Requirements & integrations

| Integration | Used for | Required? | Auth/setup |
|---|---|---|---|
| Claude Code (or Claude with skills) | runs the skill | Yes | none |
| A web fetch tool (built-in WebFetch, Firecrawl or similar) | reading the current homepage and case pages | Yes, or paste the text | none for WebFetch |
| `anticopywriting-ai` skill | the anti-AI-tell edit of the new copy | Optional | `npx skills add victor-shulga/gtm-skills/anticopywriting-ai` |
| Google Drive connector | saving the result as a Google Doc | Optional | connector in your Claude settings |

## Works with

- [`website-audit`](https://github.com/victor-shulga/website-audit): technical and mobile audit of
  the same site. Run it after the rewrite ships.
- [`page-builder`](https://github.com/victor-shulga/page-builder): service, industry and case
  pages from the same proof bank.
- `website` in [`marketing-engine-skills`](https://github.com/victor-shulga/marketing-engine-skills):
  one flow: a baseline audit, then homepage-rewrite, then page-builder, then the audit again.

## License

MIT. Method by Victor Shulga, [victorshulga.com](https://victorshulga.com). Credits for the
underlying homepage canvas are in `SKILL.md`.
