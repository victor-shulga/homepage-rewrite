# homepage-rewrite

A **Claude Code skill** that rewrites the homepage of a B2B service company (agency,
outsourcing, consulting) on two tracks at once.

- **Clarity.** A visitor from your target market understands what you sell, to whom, and
  with what result from the first screen, in about five seconds.
- **Trust.** They believe it: every promise has a named case with a number next to it,
  logos and testimonials are real and attributed, and there is no "coming soon" anywhere.

Most service-company homepages do one of the two. Some read like a pitch nobody can check;
others are a wall of logos with no offer on top. The skill scores both, then writes copy you
can paste into the site.

## What you get

One markdown file, `<company>-homepage-rewrite-<date>.md`:

→ **proof bank**: every number, case, testimonial and review link the company actually has,
marked verified or not (unverified items never reach the copy)

→ **canvas**: one primary audience, the champion who pushes the deal, their situation, current
way, limitations, problems, and the capabilities, features and benefits that answer them

→ **diagnosis**: clarity 0–50 (five buyer questions + a 5-second test of the first screen),
trust 0–12 (six rules), and the three costliest gaps

→ **new copy per block**: hero with a trust line, logos, problem, solution with a case per
argument, lower-half sections; each block names the canvas cell and proof it uses, and blocks
that already work are marked "keep"

→ **remove list**: placeholders, unverified logos, anonymous quotes, numbers without a source,
links to empty pages

→ **pre-ship checklist** and **questions** only the company can answer (logo permission, the
source of a number, a missing timeframe)

## The trust rules

| Rule | What it checks |
|---|---|
| T1 | Every case: who, result as a number, timeframe |
| T2 | Logos = paying clients with permission; quotes with name, role, company; independent review links (Clutch, G2, LinkedIn recommendations) |
| T3 | No placeholders: "coming soon", empty cards, `0+` counters, links to empty sections |
| T4 | Proof sits in the same block as the promise it backs |
| T5 | Every promise links to a page where it can be checked |
| T6 | A human voice: no hype words, no AI tells |

The skill never invents a case, a number, a quote or a logo. If the proof is thin, the copy
says less and the questions list grows.

## Install

```bash
npx skills add victor-shulga/homepage-rewrite
```

Then in Claude: "rewrite the homepage of https://linear.app", "why doesn't our homepage
convert", "перепиши головну stripe.com".

## Requirements & integrations

| Integration | Used for | Required? | Auth / setup |
|---|---|---|---|
| Claude Code (or any client that loads skills) | running the skill | yes | claude.com/claude-code |
| A web fetch tool (built-in fetch, Firecrawl or similar) | reading the current homepage and the pages behind its cases | yes, unless you paste the copy | whatever the session already has |
| `anticopywriting-ai` skill | the final edit for AI tells | optional | `npx skills add victor-shulga/gtm-skills` |

No API keys, no accounts, no scripts.

## Works with

- [`website-audit`](https://github.com/victor-shulga/website-audit): technical and mobile audit of
  the same site, before and after the rewrite ships
- [`page-builder`](https://github.com/victor-shulga/page-builder): service, industry and case pages
  built from the same proof bank and canvas
- `website` in [`marketing-engine-skills`](https://github.com/victor-shulga/marketing-engine-skills):
  one flow from audit through this skill and page-builder to a second audit

## Credits

The homepage canvas and the idea of judging a homepage by the questions a buyer must be able to
answer are adapted from a published SaaS homepage messaging framework by two product-marketing
consultants. The trust track, the proof bank and the service-business adaptation are by Victor
Shulga.

Part of the GTM-system methodology by [Victor Shulga](https://victorshulga.com) (Fractional CRO).
Every skill in the stack: [CATALOG.md](https://github.com/victor-shulga/max/blob/main/CATALOG.md).

## License

MIT © Victor Shulga. See `LICENSE`.
