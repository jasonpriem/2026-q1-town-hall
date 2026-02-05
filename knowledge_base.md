# OpenAlex Q1 2026 Knowledge Base

> Source: Q1 2026 Town Hall presentation by Jason Priem, CEO of OpenAlex. January 15, 2026.

---

## Q4 2025 Retrospective

Q4 had three main goals: improve funder/awards coverage (the Wellcome Trust grant work), launch Walden (complete system rewrite), and improve revenue sustainability.

### Funder/Awards Coverage

**Awards as first-class entity.** Awards now exist alongside Works, Funders, Institutions, and other entities. Visit openalex.org/awards to see millions of ingested awards with varying metadata quality.

**PDF parsing for funder links.** Extracted 27 million work→funder links from fulltext. The goal is to build the most complete database of funder-to-award links ever created—every work, all its funding from every funder, eventually including specific award numbers.

**Partner integrations.** Added 15 new funders, pulling directly from their websites. Over 1 million new awards added. Each funder has their own format, so OpenAlex reconciles everything into a unified format.

### Walden Launch

**Why we did a full rewrite.** Walden was a complete, soup-to-nuts rewrite migrating from the hacky launch system to a modern Databricks infrastructure. "Everybody says don't do that. There's a reason why they say don't do that." But there was no choice—the old system couldn't scale. It took all year but enables faster feature shipping, better maintenance, and more responsiveness.

**477 million works.** This includes 192 million "xpac" (expansion pack) works—content from DataCite and repositories added during the Walden migration. OpenAlex is now "the largest repository of scholarly works connected together...ever published, that anyone's ever had access to in history." Living up to the Library of Alexandria namesake.

**Xpac sources (192M works):**
- DataCite integration
- Repository content
- Improved language detection (finding papers in languages with no previous coverage)
- Improved retraction tracking

**Institutional affiliations.** Fixed many missing affiliations affecting 2024-25 works. This is ongoing—about half fixed. The bug particularly affected Elsevier articles (not their fault, just how it happened). Expect full fix within a month.

**OREO (OpenAlex Rewrite Eval Overview).** Compared legacy OpenAlex with Walden—showed high fidelity, generally within a few percentage points. Now decommissioned.

**CUI v2 (Curation UI).** Didn't launch in Q4 as planned. Launches early February 2026.

### Revenue Blitz

**Quarterly snapshots.** Moved from monthly to quarterly to control costs. Done.

**Premium features status:**
- Vector search: Not done, likely Q1. Looking for launch partners willing to pay—it's expensive to implement.
- PDF downloads: Launches late January 2026. Endpoint to download PDFs directly from OpenAlex.
- Better diff format: Researched, launching late Q1. A better way for API users to get daily changes.

**Bespoke GUIs.** Decided not to build them. "The GUI is dead."

### Bonus Achievements (Not on Roadmap)

**Everyone has an API key.** No more anonymous access. Log into OpenAlex, go to settings, find your API key. Better tracking, limits, and service.

**Unpaywall alignment.** Unpaywall is now perfectly aligned with OpenAlex—same system, different format.

**Million-row CSV downloads.** Can download up to 1 million rows via the OpenAlex UI. Takes ~16 hours but is very reliable.

---

## 2026 Strategy

### The AI Transformation

**"Everything changes this year."** Jason has been predicting this since 2013 (Nature article "Beyond the Paper"):

> "The Web opens the workshop windows to disseminate scholarship as it happens, erasing the artificial distinction between process and product."

> "The next decade will see a dramatic dieback in journals and a Cambrian explosion of communication species."

**The tools are finally here.** We can now cash the checks written with Open Science. People said "make it open, they'll build amazing things"—and now they're actually building them. Claude Code identified 150+ AI-powered tools building on open science, spanning:

- Autonomous research agents
- AI peer review
- Research integrity tools
- Literature discovery
- Paper summarization
- Scientific writing assistants
- Lab automation
- Drug discovery
- Protein prediction
- Hypothesis generation
- And many more categories

### The Three-Layer Model

OpenAlex's strategic view of the open science ecosystem:

**1. Ecosystem (top layer).** Where intelligence lives. Innovation, vibrancy, life. "Used to be journal monoculture—like a tree farm or cornfield. Now increasingly a messy, biodiverse, energetic rainforest." All those AI tools will eventually replace journals—not next year, but eventually. In the meantime, they're replacing other scholarly workflow tools.

**2. Bedrock (bottom layer).** Solid, dependable, the source of nutrients. The community has built these for decades: Crossref, DataCite, ORCID, institutional repositories, arXiv, ROR. Essential infrastructure everything feeds off.

**3. Soil (middle layer).** Homogeneous, digestible, constantly available, always connected. Trees can't grow straight out of bedrock—you need soil. OpenAlex is the soil.

**ARIOSO:** All Research Information in One Spot, Openly. A matrix for biodiversity to grow from. Something dependable that digests all that bedrock (otherwise it's hard to connect all those different services yourself).

### The GUI is Dead

**The core thesis.** People won't need pre-built GUIs anymore. With intelligence on tap plus open information, anyone can create knowledge on demand.

**Demo 1: Vibe data science.** Prompt: "Graph AI papers from UF vs UGA, 2000-2025. Use title search, OpenAlex API." Result: A working chart in minutes, querying the API directly. No hallucination issue because data comes straight from OpenAlex—you can verify every data point.

**Demo 2: Vibe coding.** Prompt: "Make me an app that works on a single local HTML page, no dependencies. It graphs works per year of different universities. Inspo: Google Trends. I can pick up to 8 unis. I can also narrow topic using title search. Use OpenAlex API. When I click a data point, it takes me to the OpenAlex website showing those works."

Result: A fully functional app built in ~10 minutes. Filter by university, add search terms, click data points to see actual works in OpenAlex. No coding required—just a prompt.

**Live example:** https://vibe-coding-examples.vercel.app/research-trends.html

**"Prompt is app."** Our agency frontier extends. No mediator needed. This isn't incidental to OpenAlex—it's the whole point. "Intelligence plus information equals knowledge. We've got the information. The intelligence is on tap now."

**Implications for competitors.** Traditional vendors (Google Scholar, Scopus, Web of Science) can't follow because they're not open. With OpenAlex, you can always show your work—no hallucination concerns because you can click through to verify.

### What OpenAlex Needs to Be "Soil" in 2026

**Big.** Already the world's largest. Keep adding millions of works and new funding sources. Prioritize community-requested sources.

**Tidy.** Connected, deduplicated, trusted. This needs the most improvement. Two approaches:
1. Improve internally (including with coding and QA agents)
2. Work with community to fund and do curation

**Open.** Always CC0 data and code. New focus: AX (Agent Experience)—making the API easy for AI agents to consume. "We're an API company now."

**Sustainable.** Convince the community of value so they fund us.
- Enterprise: tie value to API usage
- Edu/Gov: tie value to community representation

**The stakes.** "If we want open science, we have to pay for it. We have to work together. Otherwise the for-profits will do it worse, and more expensive." This is a rare chance to set the norms for the AI era—"set the default to open."

---

## Q1 2026 Roadmap

### Wellcome Project (Funder/Awards)

**Funder ingestion.** Ingest awards from top 100 funders. Link works→funders via PDF fulltext parsing.

**Funder community.** Build relationships with funders, including an in-person meeting this quarter.

### Enterprise Features

**Better sync service.** Download all updated records for the day in one big chunk. No more polling the API through millions of updated works. Was supposed to be Q4, now targeting Q1.

**New API endpoints:**
- Content download (PDFs): Late January. All 50M PDFs, kept up to date.
- Vector search: Looking for launch partners who will pay. Expensive to implement, needs demonstrated demand.

**Credit-based API pricing.** Launching January 2026. Different API calls cost different amounts—shouldn't treat them as homogeneous.

| Call Type | Credits | Example |
|-----------|---------|---------|
| Singleton | 1 | Get one work |
| List | 10 | Get a list of works |
| Content | 100 | Download a PDF |
| Vector | 1,000 | Vector search query |

Roughly 10,000 credits = $1. Up to 10x bulk discount available.

**API subscriptions:**
- Free tier: Daily credits (probably fewer than currently)
- Pro tier: $120–3,000/year. For well-funded individuals or less well-funded organizations.
- Enterprise tier: $5–10k/year. Similar to current enterprise offerings.

**Data products:**
- Data sync subscription: $5–10k/year
- API credit pack (one-time): $50k for 500M credits (90% discount). For users who want to download 50 million PDFs in one shot.

### Government & Education Features

**Affiliation matching curation.** Members can edit the algorithm OpenAlex uses to match affiliation strings to institutions. Launches February for members.

How it works:
1. View unlinked affiliation strings containing your institution name
2. Tick strings that should match your institution
3. Changes reflect in API within one day
4. Affects the dataset and snapshots for everyone, permanently
5. Can also unlink incorrect matches

**Author name disambiguation (AND).** Complete rewrite by end of Q1. "This is probably the hardest job in this space, always has been. But with today's tech, with AI, we can actually build the best one ever built." Author profile curation will launch with AND—they're too tightly integrated to separate.

**Note:** Curating your own author profile will always be free. "People's data belongs to them."

**Relentless data quality.** Building agents to automate quality improvements. Walden infrastructure makes iteration fast.

### Membership Tiers

**$5k/year member tier:**
- Curate your affiliation string matching
- Unsub subscription included ($3k value)
- Members roundtable (monthly or quarterly meetings)
- Nominate advisory board members

**$20k/year member tier (everything in $5k plus):**
- 5 power user API keys (1M calls/day each)
- Dashboards: user management, repository ingest tracking
- 5 hours training/consulting (highest-value item per feedback)
- Email support

**Possible $10k tier:** Considering an in-between tier based on interest.

**Gov/Consortium tier:**
- Variable cost
- Everything above plus custom feature development (~one small feature/year)
- Active now—contact OpenAlex if interested

---

## Q&A Clarifications

### Technical/Data Questions

**Bulk download via API?** Currently UI only (creates async job that runs for hours). Could launch API version if there's demand—let the team know.

**Works with 100+ authors.** Authors were capped at 100 during Walden launch but should expand soon. Fix may be in current or next snapshot.

**Author profile curation status.** Currently dormant. Will launch with the new AND system because they're too tightly integrated to separate. AND launch targeted for late Q1.

**Keywords/aboutness endpoint.** Not currently working and not highest priority. If it's important to you and you have budget to help fund it, contact the team.

**Curation corrections as open dataset?** Yes, can make available. Organizations like ROR could benefit.

### Pricing/Membership Questions

**Consortia discounts?** Yes, working with consortia. Contact the team.

**Funder subscription tier?** Funders go in Gov/Edu tier. For custom metadata, that's part of the Wellcome grant—contact Kyle to discuss (no resources needed from funders to ingest grant metadata).

**Credit system for AI-demonstrated use?** Yes, just tell the AI your API key.

### Process/Philosophy Questions

**Vibe coding in production?** Used extensively for development and QA. Agents find inconsistencies, flag for manual inspection, then team writes code and automated tests. But the OpenAlex pipeline itself is fully deterministic—no stochastic models in production. Source code is fully open and forkable.

**Dependency on AI models?** No production dependency. Development workflow uses AI, but the actual system runs on regular Python. "English is the new coding language" but OpenAlex code remains traditional, deterministic, auditable.

**Provenance for member-curated data?** Membership is considered proxy for trust. Will track edit history (like Wikipedia) to identify controversial edits. Training provided before using curation tools. Can moderate or revert if issues arise.

---

## Key Themes for Communications

**For blog posts/social:**
- "The GUI is dead" / "Prompt is app"
- OpenAlex as "the soil" in the three-layer model
- Intelligence + Information = Knowledge
- "Set the default to open"
- Largest scholarly works repository ever published
- ARIOSO: All Research Information in One Spot, Openly

**For enterprise/sales:**
- Credit-based pricing aligns cost with value
- 50M PDFs available via API
- Sync service eliminates polling
- Vector search coming (needs launch partners)

**For edu/gov:**
- Affiliation curation empowers institutions
- Best-ever AND system coming Q1
- Membership = partnership in building the dataset
- Training/consulting included at $20k tier

**Historical context:**
- 2013 Nature article predicted this moment
- "Dramatic dieback in journals and Cambrian explosion of communication species"
- 2026 is when it actually happens
