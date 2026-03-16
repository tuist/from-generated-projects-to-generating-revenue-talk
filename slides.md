---
theme: default
title: From Generating Projects to Generating Revenue
info: |
  A talk about turning Tuist from an open-source project into a business.
  Deep Dish Swift 2026
author: Pedro Piñera Buendía
keywords: tuist,open-source,business,swift
---

# From Generating Projects to Generating Revenue

Pedro Piñera Buendía

Deep Dish Swift 2026

<!--
Welcome everyone. This talk is about a journey that started with a side project and turned into a business. If you've ever built something in your free time and wondered "could this be more?", this talk is for you.
-->

---

# About me

- Building Tuist since 2017
- Previously at SoundCloud, Shopify, and other companies
- Now full-time founder

<!--
Quick intro. I've been an iOS/Swift developer for years, worked at various companies, and on the side I was building Tuist.
-->

---

# What is Tuist?

A platform that helps teams **scale their developer productivity** (Xcode and Gradle, for now).

- Build caching, selective testing, and insights
- Started with Xcode project generation, grew into much more
- Used by teams at scale worldwide

<!--
For those who don't know Tuist: it started as an Xcode project generation tool, but today it's a developer productivity platform. We support Xcode and Gradle, with features like build caching, selective testing, and build insights. The journey from "a tool that generates xcodeproj files" to "a platform that helps teams ship faster" is a big part of this talk.
-->

---
layout: section
---

# 1. You already have something valuable

<!--
Let's start with something I want you to internalize. If you have a side project that solves a real problem, you already have something valuable. You might not see it yet.
-->

---

# It started as a side project

- 2017: Frustrated with Xcode project conflicts at work
- XcodeGen emerged around the same time (I built `tuist/XcodeProj` to enable it)
- But I wanted Swift manifests with compile-time safety
- Project generation as a way to **conceptually compress** Xcode intricacies
- The goal: make managing Xcode projects a joy
- Shared it. People started using it.

**Sound familiar?**

Most of you have side projects. Some of you have users.

<!--
Tuist started the way a lot of your projects start. I had a problem at work, I built a thing on the weekend, I put it on GitHub, and people showed up. I didn't think of it as a business. It was a tool I needed.
-->

---

# Why did people show up?

> Do the **uninteresting, hard things** that nobody else wants to do.
> -- Peter Steinberger (OpenClaw)

Xcode project management is not glamorous. Nobody wakes up excited about `.pbxproj` files.

But every team at scale suffers from them. I didn't know it at the time, but **that's what business people call a market.**

<!--
So why did people show up? There's an insight from Peter Steinberger, the creator of OpenClaw, that I think about a lot. He said on the Pragmatic Podcast: do the uninteresting hard things that nobody else wants to do. Xcode project management is exactly that. It's boring, painful, and nobody wants to deal with it. But that's precisely what makes it a good place to build. If nobody wants to do it, and everyone needs it done, you have something that business people call a market. I didn't know that word at the time. I just knew people had a problem and I had a solution.
-->

---
layout: section
---

# 2. The moment it got real

<!--
For years Tuist was a side project. I maintained it in my free time. And then something happened that changed everything.
-->

---

# The hidden cost of "free" software

They say software has a **near-zero marginal cost**. One copy serves millions.

But there's another cost nobody talks about:

- Supporting users with unique setups
- Keeping up with every new Xcode version
- Reviewing PRs, triaging issues, adding features

You balance this with your full-time job, your family, your energy.

<!--
People say software has near-zero marginal cost. And that's true for distribution. But there's a cost nobody talks about: the maintenance cost. Supporting users, keeping up with Xcode updates, reviewing pull requests, fixing edge cases. You balance all of that with your day job and your personal life. And for a while, it works. You find the energy.
-->

---

# Some projects can be "done." Tuist couldn't.

Some side projects reach a point where you call them **complete**. That's fine.

Tuist was different. It kept growing. It kept demanding more.

Other maintainers in similar positions **burn out and walk away**.

We knew it wasn't sustainable, but making the leap felt too risky with a full-time job.

<!--
Some open source projects reach a natural stopping point and the maintainer can say "it's done." That wasn't the case for Tuist. The more people used it, the more they needed from it. We've all seen other projects where maintainers explicitly say "I'm burned out, I'm stepping away." We were heading in that direction. We felt we had to do something about it, but we didn't have the push to actually make a decision.
-->

---

# 2023: The push we needed

- Got laid off from Shopify during the tech downturn
- Tuist had real traction: contributors, users, companies depending on it
- For the first time, I had the space to make the call
- Pinged Marek, another core contributor still at Shopify. We knew each other from years of open source collaboration. We decided to build a company together.

**The signal:** when your project needs more than you can give for free, that's not a burden. That's an opportunity.

<!--
Then in 2023, I was laid off from Shopify, like many of you may have experienced during that wave. And suddenly I had something I never had before: the space to make a decision. So I pinged Marek, another core contributor who was still at Shopify at the time. We'd been collaborating on Tuist for years through open source, so we already knew how to work together. It felt like the right thing to throw ourselves into this journey together. We decided to build a company.
-->

---

# Something it took me a while to realize

# It's not a harder job. It's a different job.

As an engineer, you solve **technical problems**.

As a founder, you solve **people, market, and money problems**.

Different skills. Different anxieties. But not harder.

<!--
This is something it took me a while to realize. When you make the jump, you expect it to be harder. And some days it is. But mostly it's just different. Instead of debugging a compiler issue, you're debugging why a customer churned. Instead of writing tests, you're writing proposals. The anxiety is different, but the craft is the same: you're solving problems. Once I internalized that, it became a lot less scary.
-->

---

# Raising capital

- Germany was unofficially our first investor (unemployment benefits)
- But B2B large contracts take a **long time to close**
- We saw traction, but needed to **buy time** to build the momentum
- So we threw ourselves into raising capital

<!--
I want to be honest about this because people can be defensive about raising capital. Germany was unofficially our first investor, through unemployment benefits. That bought us some time. But we quickly realized that B2B sales with large enterprises take a long time to close. Months, sometimes. We had traction, the signals were there, but we needed to buy time to build the momentum. So we threw ourselves into raising capital.
-->

---

# What I learned about raising

- **Storytelling matters**. You can have something with no potential but a great story, and it works.
- Investors like **known and large markets**. They are driven by FOMO too.
- They want you to **die fast or grow fast**. Exits are failures to them -- they want you to go public.
- So it's possible you end up **playing a new game** you didn't sign up for.

We were honest: we wouldn't raise again if we don't see the value. We want Tuist to reach new corners, but **grow organically**, not artificially -- because that would compromise the product and our users.

<!--
Here's what I learned. Storytelling is everything in fundraising. You can have something with limited potential, but if the story is great, it works. Investors like known and large markets, and they're driven by FOMO just like everyone else. They want you to either die fast or grow fast. Exits are actually failures in their eyes -- they want you to go public. So you might end up playing a game you didn't sign up for. We were very honest with our investors: we wouldn't raise more unless we see real value in it. We want Tuist to reach new corners, but we'd rather grow organically than be forced to grow artificially. Because artificial growth compromises the product and the trust of our users and customers.
-->

---
layout: section
---

# 3. Understanding what you've actually built

<!--
Once I decided to go all in, I had to answer a question that sounds simple but isn't: what is my project actually worth? And how do I capture any of that worth?
-->

---

# Value created vs. value captured

Think of a restaurant:

- **Value created:** the meal, the experience, the atmosphere
- **Value captured:** the bill you pay

The ratio is healthy. You pay a fair share of the value you receive.

<!--
There's a concept from business that I find really useful. Every product creates value and captures value. A restaurant creates value through food and experience, and captures it through the bill. The ratio between those two is usually pretty healthy.
-->

---

# In open source, the ratio is broken

As [Penpot's team](https://penpot.app) brilliantly illustrated:

**Value captured / Value created ≈ 0.1%**

- Digital software operates at scale (one copy serves millions)
- Adoption is bottom-up (developers choose, companies benefit)
- Nobody gets a bill

<!--
In open source, this ratio is completely broken. Penpot's team showed this brilliantly: the value captured by open source projects is roughly 0.1% of the value they create. Your tool saves companies millions in developer time, and you get... GitHub stars. Maybe a sponsorship for 5 dollars a month. This is the fundamental problem.
-->

---

# Why is the ratio so broken?

Unlike a restaurant meal, software is **intangible**. It's hard to feel the value.

- Proprietary software captures ~10% of the value it creates
- Subscription models sneak past that (1%/month adds up)
- Open source? You're building on top of free, giving away free, and hoping a **tiny fraction** of users will pay for something extra

The result: people say "it's just a script", "we could build this ourselves", "why pay for something that's free?"

But your **expertise**, your **community trust**, and your **brand** are real assets -- and they're harder to replicate than code.

*Inspired by [Penpot's talk on open source business models](https://www.youtube.com/watch?v=STNomD9GUJY)*

<!--
The Penpot team explained this brilliantly. In a restaurant, you can feel the value: the meal, the atmosphere, the service. With software, it's intangible. Proprietary software has solved this by capturing around 10% of the value it creates. Subscriptions sneak past that by charging 1% per month, which adds up. But in open source, you're giving everything away and hoping a tiny fraction of users will pay for something extra. That gets you to about 0.1%. People say "it's just a script" or "we could build this ourselves." But what they can't replicate is the years of edge cases, the community trust, the expertise. Those are your real assets.
-->

---
layout: section
---

# 4. Choosing a model that fits you

<!--
So you know you have something valuable and the ratio is broken. Now the question is: how do you capture some of that value without destroying what makes your project great?
-->

---

# Open source business models

| Model | How it works | Risk |
|-------|-------------|------|
| **Donations** | Users contribute voluntarily | Unreliable, doesn't scale |
| **Support/Consulting** | Sell your time | Doesn't scale, burns you out |
| **Courses/Education** | Package your expertise | Scales better, but you're selling knowledge, not product |
| **Open Core** | Free core + paid premium features | Community resentment, feature gating |
| **SaaS / Managed** | Host it for them | Infra costs, AWS can clone you |
| **"Tax the controller"** | Charge for governance, not features | Requires enterprise market |

<!--
There are many models. Donations are nice but won't pay rent. Support and consulting sells your time, not your product. Open core is common but creates tension about what's free and what's not. SaaS works but you're competing with AWS. And then there's what Penpot calls "tax the controller", where the product stays fully open but you charge for enterprise governance.
-->

---

# What Tuist chose

Long-term, we align with **open core / "tax the controller"**. But we need value capturing in the **infrastructure**, not the software.

- We sell B2B to **large enterprises** where scaling development slows productivity down
- We built problems that need a server: **caching, insights**, and tackling **accidental complexity**
- Companies pay us for running Tuist **fast, reliably, and securely**. The software is the least important piece.
- Server uses a **source-available license** as a bridge -- as value shifts to infra, we open source more and more

<!--
We looked at all the models and realized we align most with open core or tax the controller. But to get there, we need to shift where we capture value from the software to the infrastructure. So we deliberately built features that need a server: caching, insights, and more recently tackling accidental complexity in build systems. Companies pay us not for the code, but for running it fast, reliably, and securely. We used a source-available license for the server as a bridge. As we shift value capturing to infrastructure, we keep releasing more pieces as open source.
-->

---

# No free trials. Different currencies.

- **Indies and small startups** use Tuist for free. Their currency: bug reports, feature requests, contributions.
- **Large companies** are our customers. They need SLAs, security, and someone to be liable.

<!--
We deliberately avoided the free trial model. Indie developers and small startups use Tuist for free, and they pay in a different currency: bug reports, feature requests, contributions. They make the product better. Large companies are our paying customers. They need uptime guarantees, security, and someone to call when things break. Both groups are valuable, just in different ways.
-->

---

# The right model depends on you

Find the intersection of:

- **What you enjoy doing** -- you'll be doing it for years
- **Who has the problem** -- your ICP (Ideal Customer Profile). Who suffers enough to pay?
- **What value you can capture** -- what's the thing they can't easily replicate or do themselves?

If you're open source, add a guiding principle: **how do I capture value without compromising the openness?**

<!--
There's no universal answer. You need to find the intersection of three things. First, what you enjoy doing, because you'll be doing it for a long time. Second, who has the problem. In business terms, that's your ICP, your Ideal Customer Profile. Who suffers enough from this problem to actually pay for a solution? And third, what value can you capture? What's the thing they can't easily replicate or do themselves? And if you're building in open source, you add one more guiding principle on top: how do I capture that value without compromising the openness of the project?
-->

---

# A great product is necessary, but not sufficient

As developers, we tend to believe that **if we build something good, people will come**.

That's not how it works. You also need to figure out:

- **Marketing** -- how do people discover you?
- **Go-to-market (GTM)** -- how do you reach your ICP?
- **Sales** -- how do you close deals?
- **Positioning** -- how do you explain what you do in 10 seconds?

Building the product is the part you already know. Everything else is the part you have to learn.

<!--
This is something I wish someone had told me earlier. As developers, we have this belief that if you build something good enough, people will just show up. And sometimes they do at first, through open source and word of mouth. But turning that into a business requires a whole set of skills you've never practiced: marketing, go-to-market strategy, sales, positioning. Building the product is the part you already know. Everything else is the part you have to learn. And honestly, it's where most of the work is.
-->

---
layout: section
---

# 5. Your users are developers (and that's weird)

<!--
Here's something nobody warns you about when you build developer tools: selling to developers is a completely different game.
-->

---

# Selling to developers is hard

- ❌ Cold outreach? They'll mass-block you.
- ❌ Flashy landing page? They'll view source.
- ❌ "Schedule a demo"? They'll close the tab.
- ✅ They **want to discover tools themselves**.

Developers are the worst customers... and the best marketers.

<!--
Developers hate being sold to. Cold emails? Straight to spam. Sales calls? They'd rather debug a memory leak. "Book a demo" buttons? They'll literally build a worse version of your tool just to avoid clicking it. But here's the flip side: when a developer genuinely likes your tool, they'll evangelize it harder than any sales team could.
-->

---

# Bottom-up adoption is your friend

1. A developer on a team discovers your tool
2. They try it, love it, introduce it to their team
3. The team adopts it, it becomes critical
4. Now the company needs support, SLAs, and **someone to be liable**

That's when the conversation about paying starts.

<!--
The sales motion for developer tools is bottom-up. One person finds it, introduces it to the team, the team depends on it, and eventually the company needs guarantees. That's when the conversation about paying starts. And here's the honest truth: companies often pay not because they love you, but because they need someone to be accountable. They pay so that when something breaks, it's your problem.
-->

---

# So how do you actually sell?

- We tried **cold outreach**. It doesn't work.
- What works is **inbound** -- but you have to lay the ground for it
- For us that means **building and sharing in public**: blog posts, talks, open source activity
- That's how you create the connection in developers' minds between **their pain** and **you solving it**

<!--
We tried cold outreach early on. It doesn't work with developers. So we shifted to inbound, but inbound doesn't happen by itself. You have to lay the ground for it. For us, that means building in public and sharing in public. Blog posts, conference talks, being active in the open source community. Every piece of content is a seed. When a developer eventually hits the pain point that Tuist solves, you want them to already know your name. That's how you create the connection between their problem and your solution. It's slow, but it compounds.
-->

---
layout: section
---

# 6. You don't need to be big

<!--
One of the biggest myths is that you need a big team to compete. That's less true today than it's ever been.
-->

---

# AI as the great equalizer

We're a tiny team. AI lets us:

- **Move fast across ecosystems** (added Gradle support in ~2 weeks)
- **Multiply output** without multiplying headcount
- **Jump into unfamiliar codebases** and be productive immediately

<!--
AI has fundamentally changed what a small team can do. We added Gradle build system support in roughly two weeks. Two weeks! That would have been months before. Coding agents let us jump into ecosystems we've never worked in and be productive almost immediately. This is a superpower for small companies.
-->

---

# Big companies have the innovation dilemma

Large companies struggle with:

- Internal politics and slow decision-making
- Legacy architecture they can't abandon
- Culture that punishes risk-taking

**You don't have those problems.** Your size is an advantage, not a limitation.

<!--
Meanwhile, big companies are stuck. They have the innovation dilemma: they can't cannibalize their existing products, they move slowly because of internal politics, and their culture punishes risk. You, with your side project and a laptop, can iterate faster than a team of 50 at a big company. Software efficiency, as Andrew Kelley from the Zig project writes about, is about doing more with less. That's your edge.
-->

---
layout: section
---

# 7. Protecting what you've built

<!--
Once you have something real, you need to think about protecting it. Not with lawyers necessarily, but with strategy.
-->

---

# Moats in open source

Your code is public. So what's your moat?

- **Community and trust** (takes years to build, seconds to lose)
- **Infrastructure** (hard to replicate, even if the code is open)
- **Brand and reputation** (people buy from people they trust)

Our strategy: shift the moat to infra, so we can **open source even more** of the client-side code.

<!--
In open source, your code is public by definition. So what protects you? Three things: community trust, which takes years to build. Infrastructure, which is genuinely hard to replicate even with the source code. And brand. Our strategy is deliberate: we're moving our moat deeper into infrastructure so that we can actually open source more of the surface-level code. The more we open source, the more trust we build. The more trust we build, the stronger the moat.
-->

---

# Your brand and how others see you

**Brand** is your hardest asset to build. In open source, it takes years: trust, community, word of mouth. Traditional companies throw money at it -- and when they see yours, they see a shortcut. It's the same playbook as influencer marketing: they offer peanuts for access to your reputation. **Know your worth.**

How other companies see you evolves:

1. **"Who are you?"** -- You're invisible.
2. **"Let's collaborate!"** -- They want your brand.
3. **"We're building that too."** -- You validated the market.
4. **"No comment."** -- You're a real threat.

If you get to stage 4, you're doing something right.

---

# You don't need to chase hot markets

- Heavily invested companies have **incentives to align** with where capital already flows
- Capital goes to **hot markets**, not necessarily new ones
- They constantly need to **increase captured value** or **expand into new markets** -- that's when they jump into new domains and become confusing to their own users
- Without that pressure, you can **innovate and untap new opportunities**

It feels uncomfortable. It seems like you're rowing against the trend. But you can find your cozy market and **make it yours**.

For us, that market is **plugging into every toolchain and helping it scale**. It's not attractive because it requires going deep into each build system. Other companies maximize the markets they can reach with a single solution. We go deep instead of wide.

<!--
Here's the thing about big companies and venture-backed startups: they have incentives to go where the money already is. Capital flows to hot markets, not to new ones. If you don't have that pressure, you can actually innovate in spaces nobody is paying attention to. It feels uncomfortable at first. You look around and nobody else is doing what you're doing, and you wonder if you're wrong. But that discomfort is actually a signal. You can find a market that's small enough that nobody else cares, but real enough that people will pay. And you can make it yours.
-->

---
layout: section
---

# 8. You can do this

<!--
Let me wrap up with something I genuinely believe.
-->

---

# What I've learned

- Your side project might be more valuable than you think
- The jump from engineer to founder is **different**, not harder
- You don't need permission, capital, or a big team to start
- AI has made small teams more powerful than ever
- Pick a model that lets you keep loving the work

<!--
If there's one thing I want you to take away, it's this: the barrier to doing this is lower than you think. You don't need venture capital. You don't need an MBA. You don't need a team of 20. You need a real problem, users who care, and the willingness to treat it as a different kind of engineering challenge.
-->

---
layout: center
class: text-center
---

# From generating projects to generating revenue

The path from side project to business is closer than you think.

**Thank you.**

@pepicrft

<!--
Thank you all. I'm happy to chat after the talk if any of you are thinking about making the jump. You can find me at pepicrft on most platforms.
-->
