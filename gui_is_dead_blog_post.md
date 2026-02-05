# The GUI is Dead. Long Live the Ecosystem.

In 2012, my co-author and I published a paper called "Decoupling the Scholarly Journal." The argument was simple: journals bundle together functions that should be separate. Archiving, registration, dissemination, certification—all fused into 25,000 isolated silos. This tight coupling stifles innovation. You can't experiment with peer review without creating a whole new journal.

We proposed the "decoupled journal": unbundle these functions into independent services. Let them compete. Let them evolve. Authors would pick services à la carte—one for archiving, another for peer review, another for discovery. A marketplace, not a monolith.

In 2013, I wrote in Nature that we'd see "a dramatic dieback in journals and a Cambrian explosion of communication species."

It took longer than I expected. But it's finally happening—and in a form I didn't fully anticipate.

## Two revolutions, happening at once

What I'm seeing in 2026 is actually two related shifts:

**First: the decoupled journal is materializing.** AI-powered tools are taking over individual journal functions. Peer review bots. Literature discovery agents. Research integrity checkers. Hypothesis generators. We've catalogued over 150 of these tools. Each one picks off a piece of what journals used to do, and does it better.

**Second: the GUI is dying.** Not just for scholarly tools—everywhere. Martin Alderson recently wrote about how [AI agents are starting to eat SaaS](https://martinalderson.com/posts/ai-agents-are-starting-to-eat-saas/). The most vulnerable products, he argues, are "CRUD logic dashboards"—analytics tools built on customer data.

That description fits traditional research discovery tools exactly. Scopus, Web of Science, Dimensions—they're GUI-based products built on locked-down data. Their business model requires keeping data proprietary.

And here's where the two revolutions connect: **the new ecosystem of decoupled services doesn't need traditional GUIs at all.**

## Prompt is app

During our recent [Q1 town hall](https://www.youtube.com/watch?v=q9KF_eARJaY), I demoed what I mean. I opened Claude Desktop—not a coding tool, just the regular chat interface—and typed this:

> Make me an app that works on a single local HTML page, no dependencies. It graphs works per year of different universities. Inspo: Google Trends. I can pick up to 8 unis. I can also narrow topic using title search. Use OpenAlex API. When I click a data point, it takes me to the OpenAlex website showing those works.

Ten minutes later: [a working research trends app](https://vibe-coding-examples.vercel.app/research-trends.html). Compare universities, filter by topic, click any data point to see the actual works. No hallucination worries—you can verify every result.

This isn't science fiction. This is Claude Desktop, today. Anyone can do this right now.

## The horseless carriage mistake

Some people see "vibe coding" and think: now anyone can build a SaaS app! I think they're building horseless carriages.

The insight isn't that you can build your own GUI. It's that you don't need a GUI at all.

People aren't going to log into your app and navigate your interface. They're going to ask their agent—Claude, ChatGPT, Gemini, whatever they trust—a question. That agent will reach out to open data, synthesize an answer, and if visualization helps, generate one on the fly. These aren't applications. They're data visualizations, compiled from intent.

Over time, users might collect the visualizations they find useful into dashboards. When the dashboards get cluttered, they'll throw some widgets away. Why not? They took ten minutes to make.

This is what I mean when I say "prompt is app." The interface is ephemeral. The data is what matters.

## And the data must be open

This is where traditional vendors can't follow.

If your business model requires locking data behind a paywall, your data can't be accessed by the user's agent. You're invisible to the new ecosystem. You can bolt an AI chatbot onto your product, but that's backwards. People don't want to come to *your* agent. They want their agent to come to *your data*—except they can't, because it's closed.

OpenAlex is different. We're CC0. We're API-first. Our data is designed to be consumed by agents. When someone asks Claude a question about scholarly literature, Claude can query OpenAlex directly. No login. No interface. No friction.

The closed vendors are trying to add AI features to their GUIs. We're trying to be the open data layer that makes GUIs obsolete.

## The scholarly web, take two

Here's what excites me most about this moment.

The World Wide Web was invented at CERN as a scholarly communication tool. It got co-opted. Publishers built walled gardens using the technology. The open promise never materialized for research.

We have a chance to do it right this time.

What we're building with OpenAlex is something like the WWW for scholarship: a lightweight set of protocols and open data, maintained by a nonprofit, that enables an entire ecosystem. The web itself doesn't make much money—but it enables trillions of dollars of value. That's how I see OpenAlex: cheap but essential infrastructure.

And there's plenty of money to be made on top of it. The POSI principles put it well: **make money on services, not data.** Peer review services. Curation services. Analytics services. All the functions of the decoupled journal—these are real businesses, with real revenue, with authors and readers willing to pay.

We're not against profits. We're against profits built on balkanizing the scholarly record. That's shortsighted and destructive to scholarship, which by its nature requires openness and sharing.

## Big. Tidy. Open.

Our job in 2026 is to be the soil that the ecosystem grows from.

- **Big:** 477 million works and counting. We're world-leading here, and still growing.
- **Tidy:** Connected, deduplicated, trusted. We have room to improve—and in 2026, we will.
- **Open:** CC0, API-first, agent-friendly. This is our moat. The incumbents can't follow us here.

The standards for AI-era research infrastructure are being set right now. If we get it right, open becomes the default. If we don't, the for-profits will build it worse, and charge more.

This is the year. Let's build it open.

---

[Watch the full town hall](https://www.youtube.com/watch?v=q9KF_eARJaY) · [Try the vibe-coded demo](https://vibe-coding-examples.vercel.app/research-trends.html) · [Read the 2012 paper](https://doi.org/10.3389/fncom.2012.00019)
