# do Q1 town hall

Assignee: Jason Priem
Status: Working
Created time: January 13, 2026 7:25 PM
Last edited time: January 15, 2026 7:59 AM

# Q4 retro

- goal: funder/awards coverage launch
    - create awards entity: done. first-class citizen next to works, funders, institutions, etc
    - parse awards+funders from fulltext: done for funders. 27M work→funder links extracted from fulltext (more coming!)
    - add awards direct from partners: in progress! TODO how many funders, how many awards added from them.
- goal: walden launch (full rewrite and migration to databricks)
    - 400M+ works, datacite, repositories: done!  437M works, added 176M
    - fix languages, retractions: done! language info much more accurate. finds many new papers in non english-languages, including many languages we had no coverage of at all before.
    - faster fixes for authors and institutions later: on it! fixed many missing institutional affiliations affecting recent (2024-25) works, with more fixes soon to come.
    - user curations: waiting till new author name disambiguation, end of Q1
    - OREO (OpenAlex rewrite eval overview): launched! showed walden has high fidelity to old system, generally within a few percentage points and now decomissioned.
    - CUI (Curation UI) v2: very close!…launches early february. live demo later in the preso.
- goal: revenue blitz (improve revenue stream)
    - quarterly snapshots (down from monthly): done
    - better premium value:
        - vector search: not done. valuable but expensive. likely Q1
        - download PDFs, raw and parsed: not done, launches in two weeks (late jan)
        - better diff format: not done, launches late Q1.
    - better institutional value
        - bespoke features and dashboards: not going to do...GUI is dead (more on that later in the preso!)
        - consulting and curation: curation launches in february. consulting is part of new institutions plan structure (more later in preso!)
- bonus (not planned)
    - everyone has an API key now
    - unpaywall now always perfectly aligned with openalex, since the come from same system. unpaywall is actually a format change on the openalex data.

# 2026 strategy

- everything changes this year.
    - i’ve been saying this since 2013 (screenshot of nature paper, pull quotes…paper is in an md file this repo, called “beyond the paper”)
    - but now we have intelligence on tap.
    - example apps (pull diverse set of really cool apps from the folder.
        - peer review
        - research integrity
        - hypothesis generation
        - lit reviews
        - etc
        - etc
- the three layers of the new knowledge world
    - ecosystem. characterized by interaction, innnovation, vibrancy. life. key feature: intelligence
        - examples: see above. used to be just journal monoculture, now increasingly a messy, biodiverse, energetic rainforest.
    - bedrock: characterized by solidity, dependability, essence. nutrient source. key feature: information.
        - examples: crossref, datacite, orcid, institutional repositories, arxiv and siblings, ror
    - between: soil. characterized by homogeneity, digestibility, availability. matrix. key feature: connection
        - ARIOSO (acronym: all research information in one spot, openly). openalex. we are the soil.
- the gui is dead
    - vibe data science (live demo, share screen)
    - vibe code (live demo, share screen)
    - prompt is app. example prompts:
    - our agency frontier extends, no mediator needed. access to big, tidy, open info is the only limit.
- what do we need to be soil in 2026: big, tidy, open, sustainable.
    - big: adding millions of new works, new funding. already biggest in world. keep pushing. keep prioritizing community-requested sources
    - tidy: connected, deduplicated, trusted. much work to do here. two approaches:
        - improve internally (including with coding and QA agents), and
        - work with community to fund and do curation.
    - open: always open, CC0 data and code. but also, to make meaningfully open, focus on AX (agent experience). great api, great (machine-readable) docs. gui is dead. we’re an api company. show gov, academia, and biz how they can connect directly with data via ai.
    - sustainable: convince community of value to fund:
        - enterprise: tie value to api
        - edu/gov: tie value to community representation
        - we want open science, we have to pay for it. we have to work together. otherwise the for-profits are going to come in and do it worse, and more expensive. the future is about to happen—we have a rare chance in 2026 to push it in the right direction: toward open not closed, connection not constriction, equity not industry. if we do it right, right now, we set the norms for the rest of the ai era.

# Q1 roadmap

- wellcome project (improve funder/awards coverage)
    - ingest awards from top 100 funders
    - link works→funders via PDF fulltext
    - build funder community, including at in-person meeting
- enterprise
    - better sync service: download all updated records for the day in one big chunk, no more polling API through millions of updated works
    - New API endpoints:
        - download content (eg pdfs) in late jan. can download all 50M of our PDFs that way, and keep it up to date.
        - vector search (looking for launch partners!)
    - Credit-based API pricing (jan). numbers all SUPER approximate, still gathering data, feedback welcome!
        - auth limits and pricing by credit, not call…allows us to charge/limit based on resource use.
        - can buy one-time credit pack or subscription for daily credits.
        - volume discounts
        - free daily credits for all, but probably fewer then now. most users won’t notice.
        - rough cost/credit: 10,000 credits for $1. Up to 10x discount on bulk purchases.
        - *rough* credit costs breakdown:
            - **Singleton** (eg /works/w123): 1 credit
            - **List** (eg /works?filter=foo:bar): 10 credits
            - **Content** (new, download pdfs): 100 credits
            - Vector search (new): 1,000 credits
    - sustainability clearer plans with up-front pricing
        - api subscriptions
            - free: daily credits, probably fewer than now but few will notice.
            - pro: individual/startup, $120-3,000/yr
            - enterprise: SLA, 1-3M/day, $5-10k/yr
        - data sync subscription: $5-10k/yr
        - api credit pack (one-time): $50k for 500k credits (90% discount)
- gov/edu
    - affiliation matching curation (you can edit the algo that OpenAlex uses to match certain affiliation strings to your institution). launches february for members. (live demo, share screen)
    - Author name disambiguation (AND) rewrite (end of Q1). this is a hard one! but with today’s tech we can build the most accurate AND system ever made, and we’re going to.
    - relentless data-quality improvement across the whole dataset. we’re building agents to automate this, and walden infra makes it super fast.
    - New support mode
        - $5k member:
            - curate your affiliation string matching to improve coverage and accuracy
            - unsub subcription ($3k value)
            - members roundtable, nominate advisory board member
        - $20k member. everything in $5k, plus:
            - 5 power user API keys (1M/day each)
            - dashboards: user management, repository ingest
            - 5hrs training/consulting
            - email support
        - gov/consortium (variable cost).
            - custom feature development
        - these are ready to roll…talk to us today if you’re interested! we might also have a $10k one, still working on that.
- If we want open science, we have to pay for it. we have to work together. otherwise the for-profits are going to come in and do it worse, and more expensive. the future is about to happen—we have a rare chance in 2026 to push it in the right direction: toward open not closed, connection not constriction, equity not industry. if we do it right, right now, we set the