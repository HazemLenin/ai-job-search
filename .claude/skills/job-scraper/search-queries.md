# Search Queries for Job Scraper

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

**Language scope:** write every query category in every language listed in your CLAUDE.md Languages table (typically 1-2, sometimes more). A posting requiring a language you have *not* declared, as a job condition, is excluded before scoring; a posting requiring a *higher level* than you declared in a language you *do* work in is flagged for your own judgment, not excluded — see `04-job-evaluation.md`'s Language Gate, the single source of truth for this rule. Translate each category's keywords rather than machine-translating word-for-word (e.g. "Frontend Developer" -> "Desarrollador Frontend", not a literal word-for-word translation) if you work in more than one language.

## Search Sites

Primary:
- **linkedin.com/jobs** - LinkedIn job listings (filters: Egypt, Remote, Gulf, EU); also covered by `linkedin-search` CLI
- **wuzzuf.net** - largest Egyptian job board
- **remoteok.com** / **weworkremotely.com** - remote-first boards

Note: the built-in Danish portal CLIs (Jobindex, Jobnet, etc.) are not relevant for this market. Scaffold local portal integrations with `/add-portal` if needed.

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Write **each category in every language from your Languages table** (see Language scope above; currently just English). Combine each query with your location terms (Egypt, Remote, Gulf cities, EU) where the site supports it.

**Organize by function, not job title.** The same underlying work carries different titles across companies and markets (a "Data Scientist" role at one employer may be posted as "Insights Analyst" or "Data Consultant" at another). Name each priority category after the function it covers, and list several plausible job titles as query variants within that category rather than betting an entire priority tier on one exact title string.

### Priority 1: .NET / Backend

Strongest and most desired direction.

```
site:linkedin.com/jobs ".NET Developer" remote OR Egypt
site:linkedin.com/jobs ".NET Engineer" remote OR Egypt
site:linkedin.com/jobs "Backend Engineer" ".NET" remote
site:wuzzuf.net ".NET Developer"
site:wuzzuf.net "Backend Developer"
```

### Priority 2: Full Stack / Angular

Direct match for the Angular + .NET full-stack profile.

```
site:linkedin.com/jobs "Full Stack Developer" ".NET" Angular remote OR Egypt
site:linkedin.com/jobs "Angular Developer" remote OR Egypt
site:wuzzuf.net "Full Stack Developer"
site:wuzzuf.net "Angular Developer"
```

### Priority 3: Mobile / NestJS

Adjacent roles backed by real experience.

```
site:linkedin.com/jobs "Mobile Developer" Capacitor OR Ionic OR Angular remote OR Egypt
site:linkedin.com/jobs "NestJS" developer remote
site:wuzzuf.net "Mobile Developer"
```

### Priority 4: Broader Software Engineering

Wider net, including Gulf/EU relocation and tooling/lead-track roles.

```
site:linkedin.com/jobs "Software Engineer" ".NET" Dubai OR Riyadh OR Qatar
site:linkedin.com/jobs "Software Engineer" ".NET" relocation Europe
site:linkedin.com/jobs "Software Developer" remote Egypt
site:linkedin.com/jobs "developer tooling" OR "platform engineer" ".NET" OR TypeScript remote
```

## Location Filter

Acceptable locations, in order of preference:
- Remote (worldwide) - ideal
- Alexandria, Egypt (on-site/hybrid) - ideal
- Cairo, Egypt - acceptable if hybrid/flexible
- Gulf (UAE, Saudi Arabia, Qatar, Kuwait) with relocation package - acceptable
- EU with relocation/visa sponsorship - acceptable
- On-site elsewhere without relocation support - too far

Salary floor: 1300 USD/month minimum when based in Egypt (including remote roles). Flag postings below this.

## Language Filter

Your working languages and levels are in CLAUDE.md's Languages table. When filtering scraped results, apply `04-job-evaluation.md`'s Language Gate: a posting requiring a language you haven't declared at all is excluded; a posting requiring a higher level than you declared in a language you do work in is not excluded, flag it clearly instead (see `job-scraper/SKILL.md`'s Step 3 "Quick Fit Assessment" for how the flag surfaces in `/scrape` output). Postings simply *written* in a language you don't work in, that don't require it on the job, are fine.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
