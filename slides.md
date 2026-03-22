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
- Now full-time founder

<!--
Quick intro. I've spent most of my career as a Swift developer. Tuist started as a tool I needed, not as a startup idea.
-->

---

# What is Tuist?

A platform that helps teams **scale developer productivity**.

<div class="talk-product-link">
  <img src="/brand-tuist.svg" alt="Tuist logo" />
  <a href="https://tuist.dev">tuist.dev</a>
</div>

- Started with Xcode project generation
- Expanded into caching, selective testing, and insights
- Built for teams whose build systems get slower as they grow

<!--
For anyone who does not know Tuist, this is the short version. The important part for this talk is not the product surface area. It's the path from painful tool to sustainable business.
-->

---

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
layout: section
---

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

<!--
This was not visionary. It was practical. I had pain, I built a fix, and other people had the same pain.
-->

---

# Boring problems are underrated

> Do the **uninteresting, hard things** that nobody else wants to do.
> -- Peter Steinberger

Nobody wakes up excited about `.pbxproj` files.

But painful, repeated, boring problems are often where the money is.

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
---

# 2. Knowing when it's more than a hobby

<!--
The transition from side project to business rarely happens in one dramatic moment. It usually looks like accumulating signals.
-->

---

# The hidden cost of "free" software

Software is cheap to copy.

It is **not** cheap to maintain.

- Supporting weird setups
- Keeping up with every new Xcode release
- Reviewing PRs, triaging issues, adding features
- Carrying the emotional load when other teams depend on your weekends

<blockquote class="talk-pizza-callout">
  <p>🍕 Offering a slice is easy.</p>
  <p>Running the kitchen every night is the expensive part.</p>
</blockquote>

<!--
Distribution is almost free. Maintenance is not. That's the cost open source maintainers feel first.
-->

---

# Signals this might be a business

<ul class="talk-signal-list">
  <li>🧱 Users depend on it for real work</li>
  <li>🔒 Companies ask for reliability, security, or support</li>
  <li>🤝 Contributors show up without you recruiting them</li>
  <li>🪝 The roadmap gets pulled by demand, not pushed by your curiosity</li>
  <li>💳 You hear some version of: "Can my company pay for this?"</li>
</ul>

When the work stops being random and starts being predictable, pay attention.

<!--
This is the slide I wish I'd seen earlier. These are the signals I would watch for in any side project today.
-->

---

# It's not a harder job. It's a different job.

<div class="talk-contrast">
  <div class="talk-contrast__cards">
    <div class="noora-card__section">
      <p class="talk-contrast__label">🛠️ Engineer</p>
      <p>You solve <strong>technical problems</strong>.</p>
    </div>
    <div class="noora-card__section">
      <p class="talk-contrast__label">🧭 Founder</p>
      <p>You solve <strong>people, market, and money problems</strong>.</p>
    </div>
  </div>
  <p class="talk-contrast__summary">Different skills. Different anxieties. Same underlying craft:</p>
  <p class="talk-contrast__thesis">Find the constraint, reduce the uncertainty, keep moving.</p>
</div>

<!--
This mindset shift matters. If you frame "business" as magic, you'll avoid it. If you frame it as a new problem space, you can learn it.
-->

---

# How we bought ourselves time

There is no single "correct" bridge to full-time:

- Savings
- Consulting
- Early customers
- Grants or unemployment benefits
- Investors

We chose capital because enterprise sales cycles are slow.

The lesson is simpler: pick financing that matches your reality, not your ego.

<!--
I wanted to keep this section because people are curious about funding, but the important point is optionality. There are many ways to create runway.
-->

---
layout: section
---

# 3. Put a price on the pain

<!--
Developers often underprice their work because they think in implementation effort instead of business value.
-->

---

# Usage is not the same as revenue

Developer products often have a strange shape:

- One developer adopts the tool
- A whole team gets the benefit
- Sometimes the budget owner is not the adopter
- You still carry the maintenance burden

Usage is proof of relevance, not a business model.

<blockquote class="talk-pizza-callout">
  <p>🍕 Enjoying a slice is not the same as funding the restaurant.</p>
</blockquote>

<!--
This is the value-capture problem in more concrete terms. Adoption can compound faster than revenue unless you design for capture.
-->

---

# Developer math, not startup math

If a tool saves:

- 15 minutes per developer per day
- for a team of 20
- across ~220 workdays

That is **1,100 hours per year**.

Now multiply by loaded engineering cost.

That is what companies are actually budgeting against.

<!--
This framing tends to land better with technical audiences than abstract business language. You're not selling software. You're selling recovered time and reduced friction.
-->

---

# What companies actually pay for

- Reliability on weird setups
- Fast updates when Apple changes something
- Better onboarding and fewer tribal workflows
- Security reviews, SLAs, and accountability

The code matters.

But the **risk reduction** often matters more.

<!--
This was an important realization for us. Many customers are not paying for features alone. They're paying for certainty.
-->

---
layout: section
---

# 4. Pick a model you can live with

<!--
This is where many developers get stuck. They think there is one "real" business model. There isn't.
-->

---

# Indie business models for developers

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

# Pick the model that matches your constraints

Find the intersection of:

- **What you enjoy doing**
- **Who feels the pain enough to pay**
- **What they cannot easily reproduce themselves**

If you're building in public or in open source, add one more:

**How do I capture value without breaking trust?**

Not every good business needs to become a franchise.

<!--
That last question matters a lot for developer audiences. Trust compounds slowly and is easy to destroy.
-->

---

# This generalizes beyond devtools

- Building a Swift app? Charge for a recurring problem people want gone
- Building a library or package? Adoption comes first; the money usually sits around it
- Doing client work? Productize the repeated part
- Running an OSS project? The paid layer is often hosting, guarantees, or team workflows

Different wrapper. Same underlying playbook.

<!--
I want app developers in the room to hear that this is not only a devtools talk. The form changes, the logic does not.
-->

---
layout: section
---

# 5. Developers do not want to be sold to

<!--
If your users are developers, your go-to-market motion is weird in a very specific way.
-->

---

# Selling to developers is hard

- Cold outreach usually underperforms
- Flashy marketing rarely beats credibility
- "Book a demo" is a weak first touch
- Developers want to **discover, verify, and trust** a tool on their own

They are difficult customers.

They are also your best distribution channel.

<blockquote class="talk-pizza-callout">
  <p>🍕 Developer tools spread more like trusted restaurant recommendations than ad campaigns.</p>
</blockquote>

<!--
Developers are skeptical, but in a healthy way. If they trust the tool, they will tell everyone.
-->

---

# Bottom-up adoption is your friend

1. One developer discovers your tool
2. They try it and bring it to the team
3. The team depends on it
4. The company eventually needs support, SLAs, or accountability

That is often when money enters the conversation.

<!--
This is how many developer products spread. You do not start with procurement. You earn your way there.
-->

---

# What actually created inbound for us

- Shipping useful open source work consistently
- Writing docs and migration guides
- Speaking at conferences like this one
- Publishing blog posts around painful transitions
- Responding quickly when new Xcode releases broke people

Every artifact taught the market:

**"When this hurts, Tuist is one place to look."**

<!--
This is the practical GTM slide. No magic funnel. Just repeated acts of usefulness that build recall.
-->

---

# A great product is necessary, not sufficient

You still need to learn:

- Positioning
- Distribution
- Sales
- Pricing

Building the product is familiar.

Learning how people find it, trust it, and pay for it is the second half of the work.

<!--
This is the part many engineers underestimate, including me.
-->

---
layout: section
---

# 6. Small is a feature

<!--
One of the best parts of staying small is that speed itself becomes part of the product.
-->

---

# AI is leverage, not magic

For a small team, AI is useful for:

- First drafts in unfamiliar ecosystems
- Faster prototyping and refactoring
- Support, documentation, and research
- Stretching a tiny team across more surface area

It does **not** replace taste, trust, or customer understanding.

<!--
I wanted to keep the AI point, but make it more grounded. The leverage is real. The replacement story is not.
-->

---

# Your size is an advantage

Small teams can:

- Ship without committees
- Change direction quickly
- Stay close to customers
- Go deep on narrow, weird problems

Big companies are better at distribution.

They are usually worse at focus.

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
---

# 7. Protect what compounds

<!--
When your code is public or your audience is technical, your durable assets tend to live outside the repository.
-->

---

# Assets small teams can compound

- Community trust
- Word of mouth
- Reputation for solving a specific pain well
- Infrastructure or workflow expertise
- A clear point of view

Code is important.

But these assets are usually harder to copy.

<!--
This is the softer version of the moat argument. It lands better for technical audiences because it feels earned, not defensive.
-->

---

# Brand is not vanity

In developer products, brand means:

- People know your name when the pain appears
- They assume you understand the edge cases
- They trust that you will still be around when it matters

That trust takes years to build.

<blockquote class="talk-pizza-callout">
  <p>🍕 It's what makes someone say: "If we're in Chicago, that's the place."</p>
</blockquote>

Do not trade it away cheaply.

<!--
Brand in this context is not logos and gradients. It is accumulated trust.
-->

---
layout: section
---

# 8. If you're considering indie

<!--
I want to end on actions, not inspiration alone.
-->

---

# My advice, condensed

- Start with a pain you understand deeply
- Look for signals before writing a grand plan
- Charge earlier than feels comfortable
- Pick a model that fits your life, not someone else's timeline
- Use AI for leverage, not validation

<!--
This is the summary I want people to remember.
-->

---

# Monday morning checklist

<div class="noora-card talk-checklist">
  <div class="noora-card__section">
    <div class="talk-inline-tags">
      <span class="noora-badge" data-size="large" data-style="light-fill" data-color="primary">Monday morning</span>
      <span class="noora-badge" data-size="large" data-style="light-fill" data-color="information">Actionable</span>
    </div>
<ol>
  <li>List three recurring pains you know firsthand</li>
  <li>Pick the one that happens often and expensively</li>
  <li>Talk to five people who have it</li>
  <li>Build the smallest thing that removes real pain</li>
  <li>Ask for money before polishing the brand story</li>
</ol>
<div class="noora-line-divider">
  <span data-part="line"></span>
  <span data-part="text">The punchline</span>
  <span data-part="line"></span>
</div>
<p class="talk-checklist__summary">You do not need permission. You need evidence.</p>
  </div>
</div>

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
