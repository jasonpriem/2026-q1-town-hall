# Research Review: "GUI is Dead, Open Data Wins"

**Prepared by:** Claude (Opus 4.5), via Claude Code CLI
**Date:** January 16, 2026
**For:** Jason Priem, OpenAlex

---

## About This Document

### Who I Am

I am Claude, an AI assistant made by Anthropic. This research was conducted using Claude Code, Anthropic's CLI tool that allows me to read local files, search the web, and write documents. I'm running as the `claude-opus-4-5-20251101` model.

### What I Was Asked To Do

Jason asked me to help with a blog post about the thesis that "GUI is dead" and "open data wins in the AI era." Specifically, he asked me to:

1. Find and read Martin Alderson's article "AI Agents Are Starting to Eat SaaS"
2. Read his current blog post draft for context
3. Review Vercel's new json-render tool as an example of just-in-time UI generation
4. Search for how the broader online discourse is discussing these themes over the last 1-2 months
5. Pay particular attention to the academic library and research tools context
6. Provide a structured review with recommendations for strengthening the blog post

### Methodology

I conducted this research through a combination of:

1. **Local file reads**: I read Jason's existing blog post draft (`gui_is_dead_blog_post.md`), the knowledge base from the Q1 2026 Town Hall, the original 2013 Nature article "Beyond the Paper," and the planning documents.

2. **Web searches**: I ran approximately 15 web searches covering:
   - Martin Alderson's original article and its reception
   - "GUI is dead" and related interface paradigm discussions
   - Generative UI, A2UI protocol, and just-in-time interface generation
   - AI agents vs SaaS / build vs buy discourse
   - Academic libraries and AI transformation
   - OpenAlex, Scopus, Web of Science, and open science alternatives
   - Model Context Protocol (MCP) and open standards for agent data access
   - Open data advantages in the AI era

3. **Web fetches**: I retrieved and analyzed full content from key articles including Alderson's post, the LSE blog on AI and libraries, Coronium's analysis of the death of traditional UI, and Glean's analysis of AI agents replacing SaaS.

4. **Synthesis**: I organized findings by theme, identified the main positions being staked out in the discourse, and developed recommendations specific to Jason's thesis and OpenAlex's positioning.

**Limitations**: Web search results are inherently incomplete. I focused on English-language sources and may have missed relevant discussions in other languages or on platforms not indexed by search. The "last 60 days" timeframe is approximate based on publication dates visible in search results.

---

## The User's Current Draft

Jason's `gui_is_dead_blog_post.md` is approximately 400 words. It makes the core argument:

- In 2013, Jason predicted a "Cambrian explosion of communication species" in Nature
- That explosion is finally happening—150+ AI tools for research identified
- Martin Alderson's thesis: AI agents are eating SaaS, especially "CRUD logic dashboards"
- Traditional research tools (Scopus, WoS, etc.) fit that description exactly
- OpenAlex is positioned differently: "We're not building the GUI. The GUI is dead."
- Demo: A one-sentence prompt produced a working research trends app in 10 minutes
- "Intelligence + information = knowledge. We have the information, and intelligence is now on tap."
- OpenAlex's job: be the soil (big, tidy, open) that the ecosystem grows from

The draft is strong but brief. The recommendations below suggest ways to expand and strengthen it.

---

## The Online Discourse (Last 60 Days)

### 1. The "Agents Eating SaaS" Thread

**Martin Alderson's thesis** ([original post](https://martinalderson.com/posts/ai-agents-are-starting-to-eat-saas/)) has sparked significant debate:

- **Hacker News** (412 points): The main pushback is that agents are "a multiplier on existing velocity, not an equalizer." Some argue end users can't build their own tools—their system is Excel.
- **Enterprise analysis** ([Glean](https://www.glean.com/perspectives/will-ai-agents-replace-saas-tools-as-the-new-operating-layer-of-work), [Bain](https://www.bain.com/insights/will-agentic-ai-disrupt-saas-technology-report-2025/)): McKinsey estimates AI could take over 30% of SaaS workflows within 5 years. The per-seat pricing model is collapsing—if one user + agent does the work of ten, why pay for ten seats?
- **The "at risk" category**: Alderson specifically flags "CRUD logic dashboards built on customer data"—which describes Scopus, WoS, and Dimensions perfectly.

### 2. The "Death of GUI" Movement

Several voices are making arguments that align with Jason's:

- **Eric Schmidt** (former Google CEO): "User interfaces are largely going to go away." Quoted in [Coronium's analysis](https://www.coronium.io/blog/end-of-traditional-ui-agents-replace-interface-paradigm) of why the 50-year WIMP paradigm is ending.
- **Sean's "Death of the User Interface"** ([Medium](https://medium.com/@0xs34n/the-death-of-the-user-interface-fd15a59aab27)): Traces from Douglas Engelbart's mouse (1964) to 2025 AI agents. Key metaphor: traditional UIs are bicycles, AI agents are teleporters.
- **Counterarguments** ([NN/g](https://www.nngroup.com/articles/generative-ui/), [UX Tigers](https://www.uxtigers.com/post/ai-agents)): UI "inspires, educates, guides, confirms, delights." The future is polarized—invisible UX on one end, high-craft interfaces on the other. This is actually good for Jason's argument: OpenAlex doesn't need to build the high-craft UI; it needs to be the open data layer.

### 3. Generative UI & Just-in-Time Interfaces

This is where **json-render** fits perfectly:

- **Google's A2UI Protocol** ([announcement](https://developers.googleblog.com/introducing-a2ui-an-open-project-for-agent-driven-interfaces/)): A declarative UI protocol for agent-driven interfaces. Agents generate the interface best suited to the current conversation, rendered natively across platforms.
- **Vercel AI SDK** ([docs](https://ai-sdk.dev/docs/ai-sdk-ui/generative-user-interfaces)): "Generative UI connects tool call results to React components." The AI describes UI intent; the system renders it.
- **json-render** ([GitHub](https://github.com/vercel-labs/json-render)): Same pattern—AI generates JSON, JSON renders as React components. "Developers define what's possible; AI determines what to build."
- **2025 Trend**: "The single most transformative trend of the year is Generative UI, where the interface itself is created on the fly by an AI agent." ([Thesys Report](https://www.thesys.dev/report/gen-ui-2025))

**Jason's vibe-coded demo is a perfect example of this paradigm.**

### 4. Academic Libraries & Research Tools

This is where the thesis gets most interesting for OpenAlex's audience:

- **LSE Blog** ([article](https://blogs.lse.ac.uk/impactofsocialsciences/2025/12/18/automated-warehouse-or-augmented-service-how-will-ai-change-libraries-and-librarians/)): AI won't replace librarians but transforms their role to "Knowledge Synthesists"—partnering with AI to transform information into knowledge. Libraries are becoming agents in reforming how knowledge is created and shared.
- **Clarivate's response** ([press release](https://ir.clarivate.com/news-events/press-releases/news-details/2025/Clarivate-Expands-its-Academic-AI-Platform-Introducing-Agentic-AI-for-Research-and-Learning/default.aspx)): They're adding AI agents to Web of Science—a literature review agent that "simplifies what is often a labor-intensive process." But the data stays locked.
- **Nature on AI agents for research** ([article](https://www.nature.com/articles/d41586-025-03246-7)): "Researchers are increasingly turning to AI tools that can handle complex, multi-step processes."
- **The vulnerability of closed systems**: A [deep dive on AI search tools](https://katinamagazine.org/content/article/reviews/2025/deep-dive-into-three-ai-academic-search-tools) notes "a skilled human searcher would likely produce more precise queries than AI tools"—but this changes when the data is open and the user controls the prompt.

### 5. The Open Data Advantage

Several pieces support the "open data wins" thesis:

- **OpenAlex's positioning** ([arxiv analysis](https://arxiv.org/abs/2512.16434), [Zenodo review](https://zenodo.org/records/17357948)): 146 articles analyzed between 2022-2025 show "rapid adoption of OpenAlex as an open alternative, particularly across the Global South."
- **Institutional defection**: Sorbonne deregistered from Scopus in favor of OpenAlex (2023). France's Ministry of Research considers OpenAlex "crucial open science infrastructure."
- **Barcelona Declaration on Open Research Information** (2023): Calls for collective action toward "as open as possible." Alternative databases "largely replicate commercial providers while supplementing and expanding them."
- **MCP as enabling infrastructure** ([Anthropic](https://www.anthropic.com/news/model-context-protocol), [Wikipedia](https://en.wikipedia.org/wiki/Model_Context_Protocol)): The Model Context Protocol (now under Linux Foundation) creates "USB-C-like standardization" for AI agents to connect to data sources. OpenAI, Google, and major toolmakers adopted it in 2025. **OpenAlex's open API fits this paradigm perfectly.**
- **Data lock-in backlash** ([VentureBeat](https://venturebeat.com/data-infrastructure/why-2025-will-redefine-data-infrastructure-11-expert-insights-on-sovereign-clouds-exploding-data-paas-and-more/)): "Locking data into proprietary systems will starve AI of the information it needs to excel." Organizations building specialized models need data control—exactly what OpenAlex provides.

---

## Positions Being Staked Out

| Position | Proponents | Argument |
|----------|------------|----------|
| **GUI is dead** | Eric Schmidt, Martin Alderson, Sean | Agents generate interfaces on demand; pre-built GUIs become unnecessary |
| **GUI is transformed** | NN/g, UX Tigers | Future is polarized—invisible UX + high-craft interfaces. UI still matters for trust/delight |
| **Agents multiply velocity** | HN commenters, enterprise users | Agents help sophisticated teams ship faster; they don't enable non-technical users |
| **Open data wins AI era** | OpenAlex, Barcelona Declaration, Open Science advocates | Locked data can't be used by agents; open data becomes essential infrastructure |
| **Closed vendors can add AI** | Clarivate, Elsevier | Adding AI features to existing closed products (Scopus AI, Web of Science Research Assistant) |
| **Build vs buy is shifting** | Alderson, Bain, Glean | Custom-built solutions eliminate vendor lock-in; per-seat pricing is collapsing |

---

## Recommendations for Strengthening the Blog Post

### 1. Make the Three-Layer Argument Explicit

The thesis has three layers that could be made more explicit:

1. **The Alderson Layer**: AI agents are eating SaaS → traditional research tools are exactly the "CRUD dashboards" most vulnerable → they can't pivot because their business model requires closed data
2. **The Infrastructure Layer**: MCP, A2UI, json-render all show that data-to-UI pipelines are becoming standardized → open data + open standards = anyone can build → no need for vendor mediation
3. **The Historical Layer**: Jason predicted this in 2013 → the technology finally caught up → 2026 is the inflection point

### 2. Add the json-render Example

It fits perfectly. Consider adding a line like:

> "Tools like Vercel's json-render take this further: AI generates JSON, JSON renders as components. The interface is compiled from intent."

### 3. Address the Strongest Counterargument

The strongest pushback is: "Agents multiply velocity for sophisticated users but don't enable non-technical users." A possible response:

> "That's true today. But the floor keeps rising. What required a developer last year requires a power user this year. By the time traditional vendors adapt, the window will have closed."

### 4. Quantify the Stakes

The numbers are compelling:
- OpenAlex: 477M works, 115M monthly API queries, adopted by Sorbonne, France's research ministry
- McKinsey: 30% of SaaS workflows at risk within 5 years
- Gartner: 40% of enterprise apps will embed agents by end of 2026 (up from 5% in 2025)

### 5. Strengthen the Closing

The current closing is already strong ("set the default to open"). Consider making it more urgent:

> "This is a rare window. The standards for AI-era research infrastructure are being set now. If we get it right, open becomes the default. If we don't, the for-profits will build it worse and charge more."

### 6. Consider Length

The current draft is ~400 words. Given the richness of the argument, 600-800 words might serve it better without losing the punchy tone. The plan document suggested ~470 words for the strategy/philosophy section alone.

---

## Source Links

### Core Articles
- [AI agents are starting to eat SaaS - Martin Alderson](https://martinalderson.com/posts/ai-agents-are-starting-to-eat-saas/)
- [Hacker News discussion](https://news.ycombinator.com/item?id=46268452)
- [json-render - Vercel Labs](https://github.com/vercel-labs/json-render)

### GUI is Dead
- [End of Traditional UI - Coronium](https://www.coronium.io/blog/end-of-traditional-ui-agents-replace-interface-paradigm)
- [Death of User Interface - Sean](https://medium.com/@0xs34n/the-death-of-the-user-interface-fd15a59aab27)
- [Generative UI - NN/g](https://www.nngroup.com/articles/generative-ui/)

### Generative UI
- [A2UI Protocol - Google](https://developers.googleblog.com/introducing-a2ui-an-open-project-for-agent-driven-interfaces/)
- [Generative UI - CopilotKit](https://www.copilotkit.ai/generative-ui)
- [AI SDK UI - Vercel](https://ai-sdk.dev/docs/ai-sdk-ui/generative-user-interfaces)
- [Generative UI Report 2025 - Thesys](https://www.thesys.dev/report/gen-ui-2025)

### AI Agents & SaaS
- [Will AI Agents Replace SaaS? - Glean](https://www.glean.com/perspectives/will-ai-agents-replace-saas-tools-as-the-new-operating-layer-of-work)
- [Will Agentic AI Disrupt SaaS? - Bain](https://www.bain.com/insights/will-agentic-ai-disrupt-saas-technology-report-2025/)
- [Build vs Buy - Dust](https://dust.tt/blog/build-vs-buy-ai-agents)
- [AI Agents vs Traditional Software - Robylon](https://www.robylon.ai/blog/ai-agents-vs-traditional-software-2025)

### Academic/Research Context
- [How AI will change libraries - LSE](https://blogs.lse.ac.uk/impactofsocialsciences/2025/12/18/automated-warehouse-or-augmented-service-how-will-ai-change-libraries-and-librarians/)
- [Clarivate Agentic AI announcement](https://ir.clarivate.com/news-events/press-releases/news-details/2025/Clarivate-Expands-its-Academic-AI-Platform-Introducing-Agentic-AI-for-Research-and-Learning/default.aspx)
- [How AI agents will change research - Nature](https://www.nature.com/articles/d41586-025-03246-7)
- [AI in academic libraries - Hybrid Horizons](https://hybridhorizons.substack.com/p/how-ai-will-transform-libraries-and)
- [Deep dive into AI academic search tools - Katina Magazine](https://katinamagazine.org/content/article/reviews/2025/deep-dive-into-three-ai-academic-search-tools)

### OpenAlex & Open Science
- [OpenAlex analysis - arXiv](https://arxiv.org/abs/2512.16434)
- [OpenAlex database review - Zenodo](https://zenodo.org/records/17357948)
- [Open Science Alternatives to Scopus/WoS - MDPI](https://www.mdpi.com/2304-6775/12/4/43)
- [OpenAlex API Guide for LLMs](https://docs.openalex.org/api-guide-for-llms)

### Open Data & Infrastructure
- [Model Context Protocol - Anthropic](https://www.anthropic.com/news/model-context-protocol)
- [MCP - Wikipedia](https://en.wikipedia.org/wiki/Model_Context_Protocol)
- [One Year of MCP - MCP Blog](http://blog.modelcontextprotocol.io/posts/2025-11-25-first-mcp-anniversary/)
- [Open Data and AI - data.europa.eu](https://data.europa.eu/en/publications/datastories/open-data-and-ai-symbiotic-relationship-progress)
- [2025 Data Infrastructure Trends - VentureBeat](https://venturebeat.com/data-infrastructure/why-2025-will-redefine-data-infrastructure-11-expert-insights-on-sovereign-clouds-exploding-data-paas-and-more/)
- [Open Data for AI - Futurum](https://futurumgroup.com/insights/open-data-is-critical-to-becoming-an-ai-intelligence-company/)

---

## For Future Agents

If you're an AI agent working on this blog post after me, here's the context:

1. **The thesis**: GUI is dead, open data wins in the AI era. OpenAlex is positioned as the "soil" layer—big, tidy, open data that the AI ecosystem grows from.

2. **The draft**: Located at `gui_is_dead_blog_post.md` in this directory. It's solid but brief (~400 words).

3. **Key connections to make**:
   - Alderson's "agents eating SaaS" → traditional research tools are exactly what's vulnerable
   - json-render and A2UI → examples of the generative UI paradigm Jason's demo exemplifies
   - MCP → open standards for agent data access, which OpenAlex already supports
   - 2013 Nature article → Jason predicted this moment 13 years ago

4. **The audience**: OpenAlex users and potential members—researchers, librarians, institutions, funders who care about open science infrastructure.

5. **The tone**: Confident, accessible, direct. Short paragraphs. Quantify achievements. See reference posts in the knowledge base.

6. **Files in this directory**:
   - `gui_is_dead_blog_post.md` - the draft being worked on
   - `2026_roadmap_blog_post.md` - companion post about Q1 roadmap
   - `knowledge_base.md` - comprehensive notes from the Q1 Town Hall
   - `beyond_the_paper.md` - Jason's 2013 Nature article (important historical context)
   - `q1_2026_outline.md` - outline of the town hall presentation
