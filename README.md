 # Seo Skills

A library of **106 reusable SEO and project-documentation skills** for AI assistants. Each skill is a plain Markdown file that tells an assistant how to do one job well, such as writing a meta description, clustering keywords, checking a robots.txt file, or estimating the return on a keyword.

The skills contain instructions only. There is no application code, no crawler, and no API behind them, so everything an assistant produces comes from the text you supply.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## Table of contents

- [Why use this](#why-use-this)
- [What is in the repository](#what-is-in-the-repository)
- [Skill catalog](#skill-catalog)
- [Installation](#installation)
- [Usage](#usage)
- [Anatomy of a skill](#anatomy-of-a-skill)
- [Validation and tests](#validation-and-tests)
- [Adding or editing a skill](#adding-or-editing-a-skill)
- [Limitations](#limitations)
- [License](#license)

## Why use this

- **One task per skill.** Each file has a narrow job, a stated minimum input, and a defined deliverable, so the assistant stays on task.
- **Honest by design.** Skills tell the assistant to mark unknowns as unknown, never to invent metrics or sources, and never to claim a live crawl or official validation happened when it did not.
- **No form-filling.** You can paste plain text, a URL, or a few rows of data. Optional fields stay optional.
- **Safe with untrusted text.** Instructions found inside pasted page content are treated as data, not as new commands.
- **Testable.** Every skill carries scenario tests, and the registry includes a runnable documentation test suite.

## What is in the repository

```
Seo-Skills/
├── skill/
│   ├── registry.md                 # Router: pick the right skill from a plain-language goal
│   ├── projectdetail.md            # Project brief skill
│   ├── <skill-name>.md             # 105 SEO skills, one flat file each
│   └── skills/
│       └── <skill-name>/
│           └── SKILL.md            # The same 106 skills in folder form
├── LICENSE                         # MIT
└── README.md
```

Every skill exists in two forms with identical content:

| Form | Path | Use it when |
| ---- | ---- | ----------- |
| Flat file | `skill/<skill-name>.md` | You want to browse, link to, or paste a single file. |
| Folder | `skill/skills/<skill-name>/SKILL.md` | Your assistant loads skills from folders containing a `SKILL.md`. |

`skill/registry.md` is a routing guide, not a skill you install on its own. It maps common goals to the best starting skill and lists the full catalog.

## Skill catalog

106 skills across 12 categories. Click a skill to open it.

| Category | Skills |
| -------- | ------ |
| [AI-Powered SEO](#ai-powered-seo) | 11 |
| [Backlink & Link-Building](#backlink--link-building) | 9 |
| [Competitor Analysis](#competitor-analysis) | 9 |
| [Content SEO](#content-seo) | 12 |
| [Keyword Research](#keyword-research) | 10 |
| [Local SEO](#local-seo) | 8 |
| [On-Page Optimization](#on-page-optimization) | 12 |
| [Project Management](#project-management) | 1 |
| [SEO Performance](#seo-performance) | 10 |
| [SEO Utility](#seo-utility) | 11 |
| [Schema & Structured Data](#schema--structured-data) | 4 |
| [Technical SEO](#technical-seo) | 9 |

### AI-Powered SEO

| Skill | Start with |
| ----- | ---------- |
| [AI article length optimizer](skill/ai-article-length-optimizer.md) | Topic or draft |
| [AI blog intro writer](skill/ai-blog-intro-writer.md) | Topic and article angle, or article draft |
| [AI competitor title rewriter](skill/ai-competitor-title-rewriter.md) | Competitor title and your page topic |
| [AI content detector](skill/ai-content-detector.md) | Text to review |
| [AI content improver](skill/ai-content-improver.md) | Draft text |
| [AI content outline generator](skill/ai-content-outline-generator.md) | Topic or reader question |
| [AI FAQ creator](skill/ai-faq-creator.md) | Source content or topic |
| [AI keyword explainer](skill/ai-keyword-explainer.md) | Keyword or phrase |
| [AI meta tag writer](skill/ai-meta-tag-writer.md) | Page copy or factual page summary |
| [AI schema generator](skill/ai-schema-generator.md) | Visible page content and page URL |
| [AI snippet generator](skill/ai-snippet-generator.md) | Question and supporting source text |

### Backlink & Link-Building

| Skill | Start with |
| ----- | ---------- |
| [Anchor text analyzer](skill/anchor-text-analyzer.md) | Links with anchor text and destinations |
| [Backlink idea generator](skill/backlink-idea-generator.md) | Site topic and target audience |
| [Backlink tracking template generator](skill/backlink-tracking-template-generator.md) | Tracking goal; existing rows optional |
| [Domain authority simulator](skill/domain-authority-simulator.md) | Domain signals and an explicit scoring rubric |
| [Guest posting opportunity finder](skill/guest-posting-opportunity-finder.md) | Topic, audience and optional prospect list |
| [Link relevance evaluator](skill/link-relevance-evaluator.md) | Source page context and destination page context |
| [Link source categorizer](skill/link-source-categorizer.md) | Backlink rows with source URLs and optional page context |
| [Link toxicity checker](skill/link-toxicity-checker.md) | Backlink examples and available evidence |
| [Outreach email template generator](skill/outreach-email-template-generator.md) | Recipient context, outreach purpose and genuine offer |

### Competitor Analysis

| Skill | Start with |
| ----- | ---------- |
| [Competitor backlink idea generator](skill/competitor-backlink-idea-generator.md) | Your niche and competitor backlink examples or export |
| [Competitor gap analyzer](skill/competitor-gap-analyzer.md) | Your offering and at least one competitor profile |
| [Competitor keyword overlap checker](skill/competitor-keyword-overlap-checker.md) | Two labeled keyword sets |
| [Competitor summary report creator](skill/competitor-summary-report-creator.md) | Competitor names or URLs and evidence to summarize |
| [Content length comparator](skill/content-length-comparator.md) | Two or more labeled text samples |
| [Domain comparison report tool](skill/domain-comparison-report-tool.md) | Two or more domains with dated comparable metrics |
| [Keyword share estimator](skill/keyword-share-estimator.md) | Comparable visibility values for your domain and selected competitors |
| [Meta tag comparison tool](skill/meta-tag-comparison-tool.md) | HTML or extracted metadata from two or more labeled pages |
| [Ranking opportunity finder](skill/ranking-opportunity-finder.md) | Query/page performance export or dated ranking evidence |

### Content SEO

| Skill | Start with |
| ----- | ---------- |
| [Blog title generator](skill/blog-title-generator.md) | Topic or page summary |
| [Content freshness checker](skill/content-freshness-checker.md) | Content and known publication or update date if available |
| [Content gap finder](skill/content-gap-finder.md) | Existing content inventory and audience goal |
| [FAQ generator](skill/faq-generator.md) | Actual questions plus answer facts |
| [Featured snippet optimizer](skill/featured-snippet-optimizer.md) | Target question and existing passage |
| [Headline analyzer](skill/headline-analyzer.md) | Headline and intended article summary |
| [Keyword placement highlighter](skill/keyword-placement-highlighter.md) | Text and target keywords |
| [Meta description writer](skill/meta-description-writer.md) | Page content or factual summary |
| [Paragraph keyword optimizer](skill/paragraph-keyword-optimizer.md) | Paragraph and target keyword |
| [Product description generator](skill/product-description-generator.md) | Verified product features and intended buyer |
| [Readability enhancer](skill/readability-enhancer.md) | Text and optional reader level |
| [Tone of voice analyzer](skill/tone-of-voice-analyzer.md) | Text and optional brand voice sample |

### Keyword Research

| Skill | Start with |
| ----- | ---------- |
| [Keyword clustering tool](skill/keyword-clustering-tool.md) | Keyword list |
| [Keyword comparison tool](skill/keyword-comparison-tool.md) | Two or more keywords and optional metrics |
| [Keyword density checker](skill/keyword-density-checker.md) | Text and target word or phrase |
| [Keyword difficulty estimator](skill/keyword-difficulty-estimator.md) | Keyword plus supplied SERP or competitor evidence |
| [Keyword expansion tool](skill/keyword-expansion-tool.md) | Seed terms and optional industry |
| [Keyword gap finder](skill/keyword-gap-finder.md) | Your keyword set and competitor keyword sets |
| [Keyword intent identifier](skill/keyword-intent-identifier.md) | Keyword or query list |
| [Keyword suggestion tool](skill/keyword-suggestion-tool.md) | Seed topic |
| [Long tail keyword generator](skill/long-tail-keyword-generator.md) | Seed topic and optional audience or use case |
| [Trending keyword visualizer](skill/trending-keyword-visualizer.md) | Dated keyword interest or volume series with source |

### Local SEO

| Skill | Start with |
| ----- | ---------- |
| [Geo keyword expansion tool](skill/geo-keyword-expansion-tool.md) | Seed keyword and target locations |
| [GMB optimization helper](skill/gmb-optimization-helper.md) | Google Business Profile details or business facts |
| [Local citation finder](skill/local-citation-finder.md) | Business category and service location |
| [Local keyword generator](skill/local-keyword-generator.md) | Service or product and actual target location |
| [Local SEO audit checklist](skill/local-seo-audit-checklist.md) | Business type, location and profile or site details |
| [Location based content idea generator](skill/location-based-content-idea-generator.md) | Location, audience and business topic |
| [NAP consistency checker](skill/nap-consistency-checker.md) | Canonical business name, address and phone plus listing records |
| [Review response generator](skill/review-response-generator.md) | Review text and verified business context |

### On-Page Optimization

| Skill | Start with |
| ----- | ---------- |
| [Duplicate content checker](skill/duplicate-content-checker.md) | Two or more texts or accessible pages |
| [Heading analyzer](skill/heading-analyzer.md) | HTML, Markdown or extracted headings |
| [Image alt tag generator](skill/image-alt-tag-generator.md) | Image or accurate image description and page context |
| [Internal link suggestion tool](skill/internal-link-suggestion-tool.md) | Source text and available destination pages |
| [Internal linking planner](skill/internal-linking-planner.md) | Site page inventory and priority user journeys |
| [Meta description optimizer](skill/meta-description-optimizer.md) | Existing description and page content or summary |
| [Meta tag generator](skill/meta-tag-generator.md) | Page summary, URL and optional brand or social image |
| [On page SEO audit checker](skill/on-page-seo-audit-checker.md) | Page URL or HTML and target reader task |
| [Readability score calculator](skill/readability-score-calculator.md) | Text and language |
| [SEO content checker](skill/seo-content-checker.md) | Content and target query or reader task |
| [Title meta length counter](skill/title-meta-length-counter.md) | Title and/or meta description |
| [Word count structure checker](skill/word-count-structure-checker.md) | Text or structured article |

### Project Management

| Skill | Start with |
| ----- | ---------- |
| [Projectdetail](skill/projectdetail.md) | One sentence, rough notes or an existing project brief |

### SEO Performance

| Skill | Start with |
| ----- | ---------- |
| [Bounce rate estimator](skill/bounce-rate-estimator.md) | Sessions and bounced sessions, or sessions and engaged sessions with metric definition |
| [CTR predictor](skill/ctr-predictor.md) | Impressions and an explicitly supplied CTR assumption or historical benchmark |
| [Impression to click ratio calculator](skill/impression-to-click-ratio-calculator.md) | Clicks and impressions for the same scope |
| [Keyword ROI calculator](skill/keyword-roi-calculator.md) | Traffic estimate, conversion rate, value per conversion, margin and SEO cost for one period |
| [Organic growth forecast tool](skill/organic-growth-forecast-tool.md) | Dated traffic history or baseline with explicit growth assumptions |
| [Ranking progress tracker](skill/ranking-progress-tracker.md) | Dated keyword positions with engine, market and device |
| [SEO health score calculator](skill/seo-health-score-calculator.md) | Audit findings and a disclosed scoring rubric |
| [Site comparison report generator](skill/site-comparison-report-generator.md) | Two or more sites and the user's comparison goal |
| [Traffic potential calculator](skill/traffic-potential-calculator.md) | Search volume and explicit CTR assumptions for matching period and market |
| [Visibility index calculator](skill/visibility-index-calculator.md) | Keyword weights and rank-to-CTR mapping with rankings |

### SEO Utility

| Skill | Start with |
| ----- | ---------- |
| [Canonical URL builder](skill/canonical-url-builder.md) | Preferred page URL and duplicate URL variants |
| [OG tag generator](skill/og-tag-generator.md) | Page URL, title, description and optional public image URL |
| [Redirect 301 generator](skill/redirect-301-generator.md) | Source-to-destination mapping and deployment platform |
| [Reverse image search](skill/reverse-image-search.md) | Image or public image URL |
| [Robots.txt creator](skill/robots-txt-creator.md) | Site origin and desired crawl rules |
| [Search preview simulator](skill/search-preview-simulator.md) | Title, description and page URL |
| [SEO checklist generator](skill/seo-checklist-generator.md) | Site type and current goal |
| [Sitemap generator](skill/sitemap-generator.md) | Canonical public page URLs and optional real modification dates |
| [Text to HTML converter](skill/text-to-html-converter.md) | Plain text and optional structure preferences |
| [Text translator](skill/text-translator.md) | Source text and target language or locale |
| [URL slug generator](skill/url-slug-generator.md) | Page title and optional language or URL policy |

### Schema & Structured Data

| Skill | Start with |
| ----- | ---------- |
| [Featured tool schema generator](skill/featured-tool-schema-generator.md) | Tool page URL and visible tool capabilities |
| [Local schema builder](skill/local-schema-builder.md) | Business facts, page URL and actual address or service area |
| [Schema markup generator](skill/schema-markup-generator.md) | Entity type or page facts and canonical page URL |
| [Structured data validator](skill/structured-data-validator.md) | JSON-LD, Microdata or RDFa source |

### Technical SEO

| Skill | Start with |
| ----- | ---------- |
| [Broken link finder](skill/broken-link-finder.md) | Page URL, HTML or a list of links |
| [Canonical tag checker](skill/canonical-tag-checker.md) | HTML and page URL, or accessible page URL |
| [Hreflang tag generator](skill/hreflang-tag-generator.md) | Equivalent page URLs mapped to language and optional region |
| [HTTP status code tester](skill/http-status-code-tester.md) | One or more HTTP(S) URLs |
| [Mobile friendly test](skill/mobile-friendly-test.md) | Accessible page or supplied screenshots and HTML |
| [Page speed score simulator](skill/page-speed-score-simulator.md) | Performance report or explicit hypothetical performance inputs |
| [Redirect checker](skill/redirect-checker.md) | URL or recorded response chain |
| [Robots.txt validator](skill/robots-txt-validator.md) | Robots.txt text, crawler and URLs to test |
| [XML sitemap visualizer](skill/xml-sitemap-visualizer.md) | XML sitemap or sitemap index |

Not sure which one to pick? Describe your goal to the assistant and let it use the [skill registry](skill/registry.md), or read the registry's "Route by intent" table yourself.

## Installation

Clone the repository:

```bash
git clone https://github.com/WHOISABHISHEKADHIKARI/Seo-Skills.git
cd Seo-Skills
```

Copy the skill folders you want into your assistant's skills directory. The exact location depends on the tool; a `.claude/skills/` folder in your project or home directory is one common choice.

```bash
# One skill
cp -r skill/skills/meta-tag-generator ~/.claude/skills/

# Several skills
for s in keyword-clustering-tool keyword-intent-identifier robots-txt-validator; do
  cp -r "skill/skills/$s" ~/.claude/skills/
done

# Everything
cp -r skill/skills/* ~/.claude/skills/
```

If your tool does not use skill folders, open the flat file (for example `skill/meta-tag-generator.md`) and paste it into your project instructions or at the start of a chat.

Each skill links to `registry.md` in its "Related workflow" section. That link only resolves when `registry.md` sits next to the skill file, so keep the flat files together with the registry if you want the link to work.

## Usage

Once a skill is available, ask for the result in plain language and paste whatever you have. You do not need to name the skill.

```text
Write a title tag and meta description for this page. Keep the price.
URL: https://example.com/bike-repairs
Summary: Same-day bicycle repairs, starting at AUD 20.
```

```text
Group these keywords by search intent: [paste list]
```

```text
Calculate CTR: 25 clicks, 1,000 impressions.
```

Every skill also includes a copy-and-adapt prompt template:

```text
Help me with <skill name>.
Input: [paste the minimum input]
Goal: [optional desired outcome]
For: [optional audience, market or language]
Preferences: [optional tone, detail level, format or constraints]
```

Only the minimum input is required. If you send nothing, the assistant should ask for it rather than invent an analysis.

## Anatomy of a skill

Every skill file has the same shape.

**Frontmatter**

| Field | Meaning |
| ----- | ------- |
| `name` | Matches the file name (without `.md`) or the folder name. |
| `description` | When to use the skill and what it returns. |
| `category` | One of the catalog categories above. |
| `risk` | Currently `safe` for every skill. |
| `source`, `source_repo`, `source_type` | Provenance. All skills come from `WHOISABHISHEKADHIKARI/100seotools`. |
| `date_added` | When the skill was added. |
| `author` | Skill author. |
| `tags` | Free-form tags, such as `seo` or `tool`. |

**Body sections**

1. **Start here:** the minimum input and a copy-and-adapt prompt.
2. **Workflow and decisions:** four steps, with step 3 specific to the tool.
3. **Personalization and scenario handling:** how to treat follow-ups, locale, conflicts, batches, missing access, and uncertainty.
4. **Deliverable:** exactly what the assistant returns, plus rules for formats and calculations.
5. **Scenario tests:** eight acceptance cases (tool-specific regression, minimal input, empty input, personalization, conflicting requirements, unavailable evidence, mixed batch, embedded instruction).
6. **Related workflow:** a pointer back to the registry.

## Validation and tests

`skill/registry.md` contains a Python 3.9+ documentation test suite that uses only the standard library, writes no files, and makes no network calls. It checks that:

- every skill has valid frontmatter and a name that matches its file,
- all required sections and all eight scenario cases are present,
- every link resolves and no template placeholders remain,
- the registry links to every skill, and each skill's workflow is distinct,
- a set of arithmetic fixtures (CTR, bounce rate, traffic, ROI, forecast, keyword density, keyword overlap, rank change, SEO health score) produce the documented values.

Run it from the `skill/` directory by pasting the code block from the registry's "Runnable documentation unit tests" section into `python3`.

The registry also records an AI smoke check from 2026-10-23. It was run by the same model, with shared context and self-grading, on synthetic inputs, so treat it as a sanity check and not as proof of production reliability. The scenario tables in each skill are acceptance cases you should run yourself against the assistant you use.

## Adding or editing a skill

1. Create `skill/<skill-name>.md` with the frontmatter and sections described above.
2. Add the same content as `skill/skills/<skill-name>/SKILL.md`. The two copies are currently identical, so keep them in sync.
3. Add the skill to the matching category in `skill/registry.md`, using the format `- [name](./skill-name.md) — Start with ...`.
4. If the skill does arithmetic, add a `## Calculation fixture` section with a JSON block so the test suite can check it.
5. Update the expected document count in the registry's test suite if the total changes.
6. Run the documentation tests before opening a pull request.

## Limitations

- **No live data.** Skills do not crawl sites, call search engines, or query analytics. Where a skill needs rankings, search volume, or traffic, you supply the numbers or the assistant marks the result unknown.
- **Estimators are not forecasts.** The simulators and predictors (domain authority, page speed, CTR, difficulty) require explicit assumptions or a disclosed rubric and do not promise results.
- **No ranking guarantees.** No skill can guarantee a position in search results.
- **Drafts are not actions.** Generating text does not publish, send, or change anything on your behalf.

## License

Released under the [MIT License](LICENSE). Copyright (c) 2026 Abhishek Adhikari.

## Star History

<a href="https://www.star-history.com/?repos=whoisabhishekadhikari%2Fseo-skills&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=whoisabhishekadhikari/seo-skills&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=whoisabhishekadhikari/seo-skills&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=whoisabhishekadhikari/seo-skills&type=date&legend=top-left" />
 </picture>
</a>

## Author

Maintained by [Abhishek Adhikari](https://github.com/WHOISABHISHEKADHIKARI). Skills originate from the [100SEOTools](https://www.100seotools.com) project.
