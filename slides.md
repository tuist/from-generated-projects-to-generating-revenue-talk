---
theme: default
title: From Generating Projects to Generating Revenue
info: |
  A talk about turning Tuist from an open-source project into a business.
  Deep Dish Swift 2026
author: Pedro Piñera Buendía
keywords: tuist,open-source,business,swift,indie
---

<div class="talk-banner">
  <div class="talk-banner__eyebrow">
    <span class="noora-badge" data-size="large" data-style="light-fill" data-color="primary">Deep Dish Swift 2026</span>
    <span class="noora-badge" data-size="large" data-style="light-fill" data-color="secondary">Swift</span>
  </div>
  <h1>From Generating Projects to Generating Revenue</h1>
  <p class="talk-banner__subtitle">How a painful Xcode tool became sustainable work, one layer at a time.</p>
  <div class="talk-banner__footer">
    <span class="noora-tag"><span data-part="label">Pedro Piñera Buendía</span></span>
    <span class="noora-tag"><span data-part="label">@pepicrft</span></span>
  </div>
</div>

<!--
This talk is for Swift developers who have built something on nights and weekends and wondered whether it could become more than a hobby.
-->

---

# About me

- Building Tuist since 2017
- Previously at SoundCloud, Shopify, and other companies
- Now full-time CEO and co-founder of Tuist

<!--
Quick intro. I've spent most of my career as a Swift developer. Tuist started as a tool I needed, not as a startup idea.
-->

---

<div style="max-width: 55%;">

# What is Tuist?

<span style="color: var(--noora-font-color-primary)">A <strong>platform team as a service</strong>.</span>

<div class="talk-product-link">
  <img src="/brand-tuist.svg" alt="Tuist logo" />
  <a href="https://tuist.dev">tuist.dev</a>
</div>

- Started with Xcode project generation
- Expanded into caching, selective testing, and insights
- Becoming more relevant as agentic coding accelerates and build & test setups struggle to keep up

</div>

<img src="/what-is-tuist.png" class="slide-right-img" />

<!--
For anyone who does not know Tuist, this is the short version. The important part for this talk is not the product surface area. It's the path from painful tool to sustainable business.
-->

---
class: slide-with-bg
---

<img src="/why-this-story.png" class="slide-bg-img" />

# Why this story might matter to you

- 2017: weekend fix for `.pbxproj` pain
- 2023: went full-time on Tuist
- 2026: still a small team, now with paying customers
- You likely have a side project quietly baking already

<!--
I'm not here to say everyone should build a venture-backed company. I'm here to show that a painful developer problem can turn into something sustainable.
-->

---

# What "indie" means in this talk

- Not "must stay solo forever"
- Means **small, intentional, and close to customers**
- Can look like a paid app, niche SaaS, OSS business, or productized consulting
- The goal: buy back your time with something you own

<!--
I want to widen the definition. Indie is not an aesthetic. It's a way of building with tight feedback loops and fewer layers between you and the customer.
-->

---

# What we'll cover

1. **Start with a painful problem**
2. **Knowing when it's more than a hobby**
3. **Find what software companies would pay for**
4. **Pick a model you can live with**
5. **Selling to developers**
6. **Small is a feature**
7. **Protect what compounds**
8. **Looking back, looking forward**

<!--
A roadmap for the talk. Each section mixes Tuist's experience with takeaways you can apply to your own projects.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 1. Start with a painful problem

<!--
Most good indie projects do not start with market research. They start with irritation.
-->

---

# It started as a side project

- 2017: Frustrated with Xcode project conflicts at work
- XcodeGen emerged around the same time
- I wanted Swift manifests with compile-time safety
- Project generation became a way to **compress Xcode complexity**
- Shared it. People started using it.

**Sound familiar?**

Most of you have solved a problem like this at least once.

<img src="/it-started-as-a-side-project.png" class="slide-right-img" style="top: auto; bottom: 0; transform: none; height: 90%;" />

<!--
This was not visionary. It was practical. I had pain, I built a fix, and other people had the same pain.
-->

---

# Boring problems are underrated

> Do the **uninteresting, hard things** that nobody else wants to do.
> -- Peter Steinberger

Nobody wakes up excited about `.pbxproj` files.

But painful, repeated, boring problems are often where the money is.

<img src="/boring-problems.png" style="margin-top: var(--noora-spacing-6); max-height: 40%; width: auto; display: block; margin-inline: auto;" />

<!--
That quote has stayed with me for years. Glamorous ideas attract attention. Uninteresting hard problems attract grateful users.
-->

---

# The best ideas usually start like this

- A frustration you keep hitting at work
- A workaround you repeat every week
- A thing your team complains about in Slack
- A tool you made "just for yourself" that others keep asking for

That is often the first signal of an indie opportunity.

<!--
The early question is not "is this a billion-dollar business?" It's "does this pain happen often enough that people want relief?"
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 2. Knowing when it's more than a hobby

<!--
The transition from side project to business rarely happens in one dramatic moment. It usually looks like accumulating signals.
-->

---

# The hidden cost of "free" software

Software is cheap to copy. It is **not** cheap to maintain.

- Supporting weird setups
- Keeping up with every new Xcode release
- Reviewing PRs, triaging issues, adding features
- Carrying the emotional load when other teams depend on your weekends

<blockquote class="talk-pizza-callout">
  <p>🍕 Offering a slice is easy.</p>
  <p>Running the kitchen every night is the expensive part.</p>
</blockquote>

See also: [Why We Can't Have Nice Software](https://andrewkelley.me/post/why-we-cant-have-nice-software.html). Software wants to be *finished*, but sustaining it never is.

<!--
Distribution is almost free. Maintenance is not. That's the cost open source maintainers feel first. Andrew Kelley's post makes a related point: software naturally tends toward completion, but the work of maintaining it is perpetual.
-->

---

# Signals this might be a business

<ul class="talk-signal-list">
  <li>🧱 Users depend on it for real work</li>
  <li>🔒 Companies ask for reliability, security, or support</li>
  <li>🤝 Contributors show up without you recruiting them</li>
  <li>🪝 The roadmap gets pulled by demand, not pushed by your curiosity</li>
  <li style="color: var(--slidev-theme-primary); font-weight: var(--noora-font-weight-semibold);">⏳ The project consumes more time than you can give for free <img src="/brand-tuist.svg" style="display: inline; width: 1.2em; height: 1.2em; vertical-align: middle; margin-left: 0.3em; filter: invert(22%) sepia(85%) saturate(5000%) hue-rotate(252deg) brightness(92%) contrast(95%);" /></li>
  <li>💳 You hear some version of: "Can my company pay for this?"</li>
</ul>

When the work stops being random and starts being predictable, pay attention.


<!--
This is the slide I wish I'd seen earlier. These are the signals I would watch for in any side project today.
-->

---

# How we bought ourselves time

Going full-time means you need money to pay yourself first. There is no single "correct" bridge:

- Savings
- Consulting
- Early customers
- <span style="color: var(--slidev-theme-primary); font-weight: var(--noora-font-weight-semibold);">Grants or unemployment benefits <img src="/brand-tuist.svg" style="display: inline; width: 1.2em; height: 1.2em; vertical-align: middle; margin-left: 0.3em; filter: invert(22%) sepia(85%) saturate(5000%) hue-rotate(252deg) brightness(92%) contrast(95%);" /></span>
- Investors

Pick whatever buys you enough time to find your first paying customers.

> We had the signals, but enterprise sales are slow. Our customers are large companies. By the time deals close, you can run out of runway. We raised a small round to buy ourselves that time.

<!--
I wanted to keep this section because people are curious about funding, but the important point is optionality. There are many ways to create runway.
-->

---

# What raising a small round taught us

We only raised a small round. But even that was eye-opening:

- With a solid team and foundation, **it's less scary than it sounds**
- Storytelling matters. Investors buy the narrative, not just the metrics
- Investors have their own investors. They need you to fail fast or grow big
- Some founders optimize for raising, not building. That's a valid path, just know which game you're playing
- Reputation compounds. Every conversation is a reference check

> Our pitch: *not Google-scale*, *still Apple-focused*, *long-term returns*. Most investors stopped listening there. But developer productivity spend is growing, the market is unexplored, and our customers are large and sticky. Find investors who understand your timeline.

<!--
This slide is meant as a peek behind the curtain for developers who've never been in fundraising conversations. Not a warning against raising, just context.
-->

---

# Our market

<img src="/markets.png" style="max-height: 90%; width: auto; display: block; margin-inline: auto; margin-top: var(--noora-spacing-6);" />

<!--
TAM: any software company operating at scale. SAM: companies building native mobile apps at scale. SOM: companies working with Xcode at scale.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 3. Find what software companies would pay for

<!--
Before you can price anything, you need to find the right problem to monetize.
-->

---

# Finding what software companies would pay for

You need two things: **signals** that a business model works somewhere else, and **confidence** that you bring something unique to the space.

- Align with how companies already think about paying. If a solution needs a server, paying for it feels natural
- Look for proof in adjacent ecosystems. If someone else made it work, your version might too
- Don't invent a business model. Adapt one that's already validated

<!--
This is about finding the right shape for the paid product. Not everything can be monetized. The trick is finding the problem that requires infrastructure, not just code.
-->

---

# What software companies won't pay for

- **Local-only tools** (including CLIs). If it runs entirely on a developer's machine, they expect it to be free
- **Easy or interesting problems.** Their developers will build in-house solutions for the fun of it
- **Things AI is getting good at.** If a model can generate it, the perceived value drops fast

Know what sits outside the paywall so you can focus on what sits inside it.

<!--
This is about scoping your paid product. Not everything you build can be monetized. Focus on the parts that require infrastructure, trust, or ongoing maintenance.
-->

---

# Developers adopt. Companies pay.

In developer tooling, you have two customers:

- The **developer** who discovers and champions the tool internally
- The **company** that signs the contract and pays the invoice

Your job is to make the developer look good when they pitch it to their manager.

> The developer is your user. The company is your customer. Build for both.

<!--
This is the core dynamic of bottom-up developer sales. The developer is your distribution channel, the company is your revenue source.
-->

---

# This is what it looks like

> Hi Tuist team,
>
> We would like to exchange with you on the paid features of Tuist, in particular Dashboard and Remote Cache.
>
> Over the past months, we have fully migrated the **██████ iOS app** to Tuist. From our perspective, this decision has clearly paid off, especially in terms of project structure, scalability, and overall developer experience.

The developer championed it. The company is now ready to pay.

<!--
A real email, redacted. This is what bottom-up adoption looks like when it works.
-->

---

# Companies pay for not having to worry

We thought they were buying features. They were buying **certainty**.

- "Will this still work after the next Xcode update?"
- "Can we pass a security review with this in our stack?"
- "If something breaks at 2am, is someone accountable?"
- "Can a new hire be productive without tribal knowledge?"

The code is table stakes. What closes the deal is the answer to: **"Can we depend on this?"**

<!--
This was an important realization for us. Many customers are not paying for features alone. They're paying for certainty.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 4. Pick a model you can live with

<!--
This is where many developers get stuck. They think there is one "real" business model. There isn't.
-->

---

# Business models for developer tools

| Model | Good when | Trap |
|-------|-----------|------|
| **Paid app / subscription** | You solve an end-user problem | High churn pressure |
| **Consulting / productized service** | You already have demand and trust | You can become the bottleneck |
| **Courses / education** | Your expertise is teachable | You may build an audience business, not a product |
| **Open core** | Free adoption feeds paid upgrades | Feature-gating can create resentment |
| **Hosted / managed OSS** | Running it well is hard and valuable | Infra and support become the product |

<!--
The right model depends on what you want your day-to-day work to feel like.
-->

---

# What Tuist chose

- Free for indies and small startups
- Paid for large companies that need guarantees
- Value capture moved toward **infrastructure and accountability**
- The more value shifts to infra, the more client-side code we can open up

Indies pay us in a different currency too:

<ul class="talk-signal-list">
  <li>🐞 Bug reports</li>
  <li>💡 Feature requests</li>
  <li>🎤 Talks at conferences</li>
  <li>📣 Word of mouth</li>
  <li>🤝 Contributions</li>
</ul>

<!--
This is the model that fits us. It would be wrong for many products, which is exactly the point.
-->

---

<div style="max-width: 55%;">

# Pick the model that matches your constraints

Find the intersection of:

- **What you enjoy doing**
- **Who feels the pain enough to pay**
- **What they cannot easily reproduce themselves**

If you're building in public or in open source, add one more:

**How do I capture value without breaking trust?**

Not every good business needs to become a franchise.

</div>

<!-- TODO: Add drawing as /pick-model.png and uncomment -->
<!-- <img src="/pick-model.png" class="slide-right-img" /> -->

<!--
That last question matters a lot for developer audiences. Trust compounds slowly and is easy to destroy.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 5. Selling to developers

<!--
Your users are developers. Your go-to-market motion is weird in a very specific way.
-->

---

# Selling to developers is hard

- Cold outreach usually underperforms
- Flashy marketing rarely beats credibility
- "Book a demo" is a weak first touch
- Developers want to **discover, verify, and trust** a tool on their own

They are difficult customers. They are also your best distribution channel.

<blockquote class="talk-pizza-callout">
  <p>🍕 Developer tools spread more like trusted restaurant recommendations than ad campaigns.</p>
</blockquote>

<!--
Developers are skeptical, but in a healthy way. If they trust the tool, they will tell everyone.
-->

---

# What actually created inbound for us

- Shipping useful open source work consistently
- Writing docs and migration guides
- Speaking at conferences like this one
- Publishing blog posts around painful transitions
- Responding quickly when new Xcode releases broke people

Every artifact taught the market: **"When this hurts, Tuist is one place to look."**

> A great product is necessary, but not sufficient. Positioning, distribution, sales, pricing: treat them as skills to learn, not chores to avoid.

<!--
This is the practical GTM slide. No magic funnel. Just repeated acts of usefulness that build recall.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 6. Small is a feature

<!--
One of the best parts of staying small is that speed itself becomes part of the product.
-->

---

# AI makes small teams dangerous

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: var(--noora-spacing-8); align-items: center;">
<div>

We dog-food our own tools, so we're motivated to optimize developer workflows. AI agents let us ship more with fewer people.

AI does **not** replace taste, trust, or customer understanding. But it multiplies everything else.

</div>
<div>
<img src="/tuist-commits.png" style="width: 100%; border-radius: var(--noora-radius-xlarge); box-shadow: var(--noora-border-light-default); padding: var(--noora-spacing-5); background: var(--noora-surface-background-primary);" />
</div>
</div>

<!--
The commit chart shows our velocity increasing dramatically. AI is a real force multiplier for small teams.
-->

---

# Your size is an advantage

We rolled out our full feature set for Gradle support in **3 weeks**. A larger company would spend that time in planning meetings.

- Ship without committees
- Change direction quickly
- Stay close to customers
- Go deep on narrow, weird problems

Big companies have distribution. They also have bureaucracy and the innovator's dilemma. Use that.

<!--
If you're indie, you should not try to look big. You should exploit the advantages of being small.
-->

---

# You do not need a hot market

- Capital chases obvious categories
- Developers often find value in neglected corners
- A small painful niche can be enough
- Depth beats breadth when trust matters

For us, that meant going deeper into build systems instead of wider into adjacent markets.

<blockquote class="talk-pizza-callout">
  <p>🍕 You do not need to feed the whole city.</p>
  <p>You need the right table to come back again and again.</p>
</blockquote>

<!--
This is encouraging for indie builders because it means you do not need to win the trend cycle to win a real business.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 7. Protect what compounds

<!--
When your code is public or your audience is technical, your durable assets tend to live outside the repository.
-->

---

<div style="max-width: 55%;">

# Assets small teams can compound

1. **Code** (everyone starts here)
2. **Infrastructure expertise** (you know how to run it well)
3. **Reputation** (people associate you with the problem)
4. **Community trust** (people vouch for you unprompted)
5. **Word of mouth** (it scales without you)

Each layer is harder to build and harder to copy.

</div>

<!-- TODO: Add pyramid drawing as /compound-assets.png and uncomment -->
<!-- <img src="/compound-assets.png" class="slide-right-img" /> -->

<!--
This is the softer version of the moat argument. It lands better for technical audiences because it feels earned, not defensive.
-->

---

# Brand compounds in unexpected places

Tuist grew organically in South Korea. Developers gave talks at local meetups. The community translated our docs to Korean.

We closed our first customer there without a single sales call.

<blockquote class="talk-pizza-callout">
  <p>🍕 It's what makes someone say: "If we're in Chicago, that's the place."</p>
</blockquote>

That trust takes years to build. Do not trade it away cheaply.

<!--
Brand in this context is not logos and gradients. It is accumulated trust that travels further than you expect.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

# 8. Looking back, looking forward

<!--
Honest reflections after years of building Tuist.
-->

---

# What we'd do differently

- **Think about the business earlier.** We spent years building in the open without considering how to sustain it. The product was great, but "great" doesn't pay rent
- **Be ready for competition.** Once you enter business territory, companies that used your open-source work for brand recognition can pivot to compete against you. It happens
- **Charge earlier than feels comfortable.** The discomfort of asking for money fades. The cost of running out of runway doesn't

<!--
This is the honest slide. Not regrets, just things I see more clearly now.
-->

---

# Monday morning checklist

1. List three recurring pains you know firsthand
2. Pick the one that happens often and expensively
3. Talk to five people who have it
4. Build the smallest thing that removes real pain
5. Ask for money before polishing the brand story

**You do not need permission. You need evidence.**

<!--
If someone leaves with one actionable slide, I want it to be this one.
-->

---
layout: center
class: text-center
---

<div class="talk-outro">
  <div class="talk-outro__eyebrow">
    <span class="noora-badge" data-size="large" data-style="light-fill" data-color="primary">Thank you</span>
    <span class="noora-badge" data-size="large" data-style="light-fill" data-color="secondary">Deep Dish Swift</span>
  </div>
  <h1>From generating projects to generating revenue</h1>
  <p class="talk-outro__subtitle">The path from side project to sustainable work is shorter than it looks.</p>
  <div class="talk-outro__actions">
    <a class="noora-button" data-size="large" data-variant="primary" href="https://tuist.dev">
      <span>tuist.dev</span>
    </a>
    <a class="noora-button" data-size="large" data-variant="secondary" href="https://x.com/pepicrft">
      <span>@pepicrft</span>
    </a>
  </div>
</div>

<!--
Happy to chat after the talk if you're building something small, weird, and useful.
-->
