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
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Part one</span>
  <h1 class="talk-section-heading__title">A hobby</h1>
</div>

<!--
Most good indie projects do not start with market research. They start with irritation.
-->

---
class: timeline-slide
---

# Xcode projects at scale suck

- 2017: Frustrated with Xcode project conflicts at work
- Built `tuist/xcodeproj` as a Swift CRUD layer for Xcode projects
- XcodeGen emerged around the same time
- I wanted Swift manifests with compile-time safety
- Project generation became a way to **compress Xcode complexity**
- Shared it. People started using it.

<img src="/it-started-as-a-side-project.png" class="slide-right-img" style="top: auto; bottom: 4.75rem; transform: none; height: 82%;" />

<div class="talk-timeline" style="--timeline-orange-fill: 10%; --timeline-green-fill: 10%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span class="is-active">2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track"></div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This was not visionary. It was practical. I had pain, I built a fix, and other people had the same pain.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# It kept growing on the side

- It helped me get a job at Shopify as a mobile tooling engineer
- I also met Marek there, who later became my co-founder
- None of my employers ever used it
- Users, contributors, support, and feature requests kept growing
- It was still something I could manage in my spare time

<div class="talk-terminal-window">
  <div data-part="bar">
    <span data-part="language">CLI</span>
    <span data-part="hint">where most of the value lived</span>
  </div>
  <div data-part="code">
    <code>$ tuist generate</code>
  </div>
</div>

<div class="talk-timeline" style="--timeline-orange-fill: 10%; --timeline-green-fill: 30%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span class="is-active">2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track"></div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This was an important signal in retrospect. Tuist was valuable enough to shape my career, and even led me to meet Marek, who later became my co-founder, but not yet something I could dedicate myself to full-time. The load was growing, contributors were showing up, and the center of gravity was clearly the CLI and project generation. It was still survivable on nights and weekends.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# The hidden cost of "free" software

Software is cheap to copy. It is **not** cheap to maintain.

- Supporting weird setups
- Keeping up with every new Xcode release
- Reviewing PRs, triaging issues, adding features
- Carrying the emotional load when other teams depend on your weekends

See also: [Why We Can't Have Nice Software](https://andrewkelley.me/post/why-we-cant-have-nice-software.html). Software wants to be *finished*, but sustaining it never is.

<blockquote class="talk-pizza-callout">
  <p>🍕 Offering a slice is easy.</p>
  <p>Running the kitchen every night is the expensive part.</p>
</blockquote>

<div class="talk-timeline" style="--timeline-orange-fill: 10%; --timeline-green-fill: 40%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span class="is-active">2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track"></div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
Distribution is almost free. Maintenance is not. That's the cost open source maintainers feel first. Andrew Kelley's post makes a related point: software naturally tends toward completion, but the work of maintaining it is perpetual.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# We had already built something hard to replace

It had taken years and a lot of human capital to build:

- A community of users and contributors
- A strong brand built on openness
- Teams using us every day through the CLI
- Deep Xcode and project generation know-how

<div class="talk-timeline" style="--timeline-orange-fill: 10%; --timeline-green-fill: 50%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span class="is-active">2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track"></div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
By then, this was no longer just a side project repository. It was accumulated trust, accumulated know-how, and accumulated usage. That made the question less "should we keep doing this?" and more "how do we sustain something people already depend on?"
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Donations felt like the obvious answer

That made Tuist a valuable asset for established companies that couldn't figure out GTM around developer tools.

- We felt a gravitational pull toward a donation or sponsorship model
- It pairs nicely with low confidence in your ability to build a business
- The value exchange is deeply unbalanced
- We get peanuts; they get distribution, goodwill, and a "Company X supports Tuist" story

<div class="talk-message-window">
  <div data-part="bar">
    <span data-part="label">Sponsorship pitch</span>
  </div>
  <div data-part="body">
    <p>Hi,</p>
    <p>We thought you might be interested in doing a few posts a month about us. We can donate $50 a month.</p>
  </div>
</div>

<div class="talk-timeline" style="--timeline-orange-fill: 10%; --timeline-green-fill: 55%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span class="is-active">2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track"></div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
Once Tuist was clearly valuable, the easiest path to imagine was sponsorship. Established companies know how to justify donations and brand support internally. That path is seductive because it avoids the harder question of what the real product and value exchange should be. But it usually means they capture far more value than you do.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Part two</span>
  <h1 class="talk-section-heading__title">It can be a business</h1>
</div>

<!--
The transition from side project to business rarely happens in one dramatic moment. It usually looks like accumulating signals.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Taking the leap was scary

- Standing still meant either letting Tuist stagnate or paying for it with our nights and weekends
- We knew the donations model wouldn't work
- We didn't want to let the project die, or keep burning ourselves out to sustain it
- We still had no clear idea how to make the leap work

<div class="talk-timeline" style="--timeline-orange-fill: 10%; --timeline-green-fill: 60%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span class="is-active">2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track"></div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
At that point, the status quo no longer felt stable. We had already learned that donations were not a real answer, and doing nothing meant either letting Tuist decay or letting it consume more and more of our lives. The problem was that acting on that insight meant stepping into a kind of uncertainty we didn't yet feel prepared for.
-->

---
class: full-bleed-image
---

<div class="talk-article-shot">
  <div class="talk-article-shot__hero">
    <div class="talk-article-shot__nav">
      <div class="talk-article-shot__brand">
        <img src="/shopify.svg" alt="Shopify" />
        <span>shopify</span>
      </div>
      <div class="talk-article-shot__links">
        <span>All news</span>
        <span>Company</span>
        <span>Product</span>
        <span>POV</span>
        <span>Insights</span>
        <span>Press releases</span>
        <span>About us</span>
      </div>
      <div class="talk-article-shot__search">Search</div>
    </div>
    <div class="talk-article-shot__header">
      <p>COMPANY</p>
      <h1>Important team and business changes</h1>
      <span>May 4, 2023</span>
    </div>
  </div>
  <div class="talk-article-shot__body">
    <img src="/shopify-business-changes.jpg" class="talk-full-bleed-image" alt="Shopify business changes article image" />
  </div>
</div>

---
class: pizza-bottom timeline-slide wide-title
---

# We decided to build a company

By 2023, it was no longer a side project.

- We had signals companies would pay for new features
- I reached out to Marek, still at Shopify
- We had already decided to go for it
- Marek joined a bit later, after leaving Shopify

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 67.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This is the point where the story becomes deliberate. The slide should feel like a decision, not a framework.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Our business mental model

We needed a business model for companies building apps with Xcode at scale.

- Teams don't pay for CLIs. They pay for productivity infrastructure
- So we looked for server-backed problems like caching and build acceleration
- They had to build on the foundations we already had
- And they had to support a B2B sales motion

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 67.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This is the business filter: not abstract strategy, but the constraints that shaped what we could credibly sell.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Our openness model

We wanted to stay open, but we also needed time to move value capture toward infrastructure.

- The server would start under Fair Core
- A small CLI extension would be closed source too
- The plan was to move toward OSS as the market grew and value shifted to operational complexity
- We also wanted openness to shape how we built the product and company
- That also reduced early risks: competitors, self-hosting customers, and cloud vendors

<blockquote>
  <p>HashiCorp spent four years building the foundations of its open core model. We had one.</p>
</blockquote>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 67.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This was not ideological. It was a temporary way to stay open-minded about the long-term model while protecting enough value to survive the first year.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Why not just go closed source?

Because open source lets you capture less per user, but from a much larger market.

- Closed source would have made value capture simpler
- But open source gave us access to a much larger market
- And it made the product stronger through trust, adoption, and contribution
- So we wanted to capture value around operating it at scale

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 67.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This is the core tradeoff: capture less per user, but create more value through reach, trust, and contributions.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# We had demand, but not enough runway

We had already closed some enterprise customers. The problem was time.

- We had learned B2B deals can take months, sometimes a year, to close
- We'd need many more of them before we could pay ourselves a salary
- So the real question became how to buy enough time
- Savings were one option. Raising a round was the other

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This is the bridge into fundraising: demand existed, but enterprise sales alone were too slow to fund the leap.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# We pitched the upside, honestly

We came in with a vision, but kept our feet on the ground.

- **What sounded good:** we already had users and companies using Tuist
- **What sounded good:** we had shown we could build
- **What sounded good:** our solutions could go beyond the Apple ecosystem
- **What sounded good:** the long-term market was all software organizations
- **What we were honest about:** we weren't going to play the raise-for-the-sake-of-raising game
- **What we were honest about:** long-term, we wanted to be fully OSS
- **What we were honest about:** it was our first time founding a company

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
The pitch was intentionally balanced: enough ambition for investors to see upside, enough honesty that it still felt like us.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# A few things we learned

This was just our experience, but a few patterns showed up quickly.

- Some wanted a bigger swing: "don't you need more?"
- Social proof changed the room fast
- Some studied the market deeply. Others wanted a familiar category

<blockquote class="talk-signals-quote">
  <p class="talk-signals-quote__text">"The business is the envelope. The real thing is the letter inside."</p>
  <p class="talk-signals-quote__eyebrow">Jason Fried, 37signals</p>
  <p class="talk-signals-quote__body">That framing stayed with us: raise enough to keep building the product, but don't let the envelope become the point.</p>
  <p class="talk-signals-quote__source"><a href="https://www.youtube.com/watch?v=BdDCtMA1gSw" target="_blank" rel="noreferrer">Interview</a></p>
</blockquote>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This should land as observation, not judgment. Different investors play different games; this is just what became visible once we were in the room.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Our proposal

The ask itself was actually pretty simple.

- Raise enough to become profitable in two years
- Do it with a team of four people, around $1M in total
- Validate the model in the Apple ecosystem first
- Then expand into Android and Gradle
- Design and server expertise: Marek on tech, both on product, me on operations

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This should feel concrete and modest: not a moonshot deck, just a specific proposal to buy enough time to prove the model.
-->

---
class: pizza-bottom timeline-slide wide-title
---

# Binary caching

- Gradle's build cache already proved this is a viable business
- Project generation gave us the foundation to build on incrementally
- Carthage showed that distributing and consuming pre-built binaries works
- It works with both local targets and Swift packages

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span class="is-active">2023</span>
    <span>2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
Binary caching was the first product idea that felt like a real business. Gradle had already validated the model in the JVM world. We had project generation as a foundation, and Carthage had proven that pre-built binaries could work in the Apple ecosystem. The gap was Swift packages.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Part four</span>
  <h1 class="talk-section-heading__title">How we made it happen</h1>
</div>

<!--
This section shifts from the pitch itself to the concrete moves that made the business real.
-->

---

# Engineering

- We built the server in Elixir to get the most from a small team
- We shipped cache and insights for builds, tests, and bundles
- We dog-fooded everything: Tuist running on Tuist
- We moved the CLI, design system, server, and app into one monorepo

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 82.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span class="is-active">2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This is where the proposal becomes execution: choose a stack that compounds a small team, build the infrastructure, and use it ourselves first.
-->

---

# Product

- We went deep on Xcode internals and proprietary formats
- That know-how became a moat
- We made new features adoptable without generated projects, like insights
- We lowered adoption cost so teams could try things incrementally
- We let developers experience the product in public, not just watch demos
- The product stopped being "a CLI" and became a platform, with the CLI as one of the interfaces

<div class="talk-center-cta">
  <a href="https://tuist.dev/tuist/tuist" target="_blank" rel="noreferrer" class="noora-button talk-center-cta__button" data-variant="primary" data-size="medium"><span>Explore Tuist's features</span></a>
</div>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 82.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span class="is-active">2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

---

# Design

<div class="talk-split-slide">
<div>

- Design craft had to match the engineering quality
- Otherwise it would drag down perceived value
- We built Noora (`github.com/tuist/noora`) for the Elixir server and the Swift CLI
- Tuist could speak the same visual language everywhere
- And we could move faster with shared design-system blocks

</div>

<div class="talk-split-slide__media">
  <img src="/noora.png" alt="Noora design system" />
</div>
</div>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 82.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span class="is-active">2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

---
class: website-grid-slide
---

<div class="talk-website-grid">
  <figure class="talk-website-grid__item">
    <img src="/website-2018.png" alt="Tuist website in 2018" />
    <figcaption>2018</figcaption>
  </figure>
  <figure class="talk-website-grid__item">
    <img src="/website-2019.png" alt="Tuist website in 2019" />
    <figcaption>2019</figcaption>
  </figure>
  <figure class="talk-website-grid__item">
    <img src="/website-2021.png" alt="Tuist website in 2021" />
    <figcaption>2021</figcaption>
  </figure>
  <figure class="talk-website-grid__item">
    <img src="/website-2026.png" alt="Tuist website in 2026" />
    <figcaption>2026</figcaption>
  </figure>
</div>

---

# Marketing

- We explored ideas and shared what we learned
- In a noisy market, the content had to be memorable and useful
- That is how engineers build trust, like PSPDFKit did
- We could not afford clickbait or brute-force ad spend

<blockquote>
  <p>Hi Tuist team,</p>
  <p>We would like to exchange with you on the paid features of Tuist, in particular Dashboard and Remote Cache.</p>
  <p>Over the past months, we have fully migrated the <strong>██████ iOS app</strong> to Tuist. From our perspective, this decision has clearly paid off, especially in terms of project structure, scalability, and overall developer experience.</p>
</blockquote>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 82.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span class="is-active">2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

---

# Sales

- Developers pay with ideas, bug reports, contributions, and word of mouth. Employers pay with money
- We built a system to keep conversations warm while supporting adoption
- Some parts stayed slow: security reviews, procurement, and legal
- New systems like Gradle lowered adoption cost dramatically, it was just a plugin
- Adoption often started with one developer and ended in procurement

<div class="talk-terminal-window" style="width: min(100%, 32rem); margin-top: var(--noora-spacing-6);">
  <div data-part="bar">
    <span data-part="language">Gradle</span>
  </div>
  <div data-part="code">
    <pre><code>plugins {
  id("dev.tuist")
  version "0.1.0"
}</code></pre>
  </div>
</div>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 82.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span class="is-active">2024</span>
    <span>2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>


---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Part five</span>
  <h1 class="talk-section-heading__title">AI happened</h1>
</div>

<!--
This is where many developers get stuck. They think there is one "real" business model. There isn't.
-->

---
class: quote-bottom
---

# Inference getting faster pulls us into the stack

- Faster inference makes slow workflows feel broken.
- More and faster compute helps, but it is expensive and capped.
- We invested in the depth of build systems, where CI and compute companies often would not.
- That depth is becoming more valuable as agents need to know **what to build, test, and skip**.

<div class="talk-openai-quote">
  <p class="talk-openai-quote__text">"If it's 'oh god, I don't want to do this' and 'oh my god, this is hard,' that's a good spot to be in."</p>
  <div class="talk-openai-quote__meta">
    <div class="talk-openai-quote__source">
      <img src="/openai-logomark.svg" alt="OpenAI logo" class="talk-openai-quote__logo" />
      <span class="talk-openai-quote__cite">Peter Steinberger</span>
    </div>
    <a href="https://www.youtube.com/watch?v=8lF7HmQ_RgY" class="talk-openai-quote__link">The creator of Clawd: "I ship code I don't read"</a>
  </div>
</div>

<!--
As models get faster, the bottleneck becomes the software delivery system around them. We ended up investing in deep build-system knowledge that many CI and compute companies historically treated as too costly. That depth is now becoming strategically relevant because agents need guidance, selectivity, and confidence.
-->

---
class: timeline-slide
---

# AI made us more productive

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: var(--noora-spacing-8); align-items: center;">
<div>

We dog-food our own tools, so we're motivated to optimize developer workflows. AI agents let us ship faster with the same team.

- A concrete example: we rolled out Gradle support in **3 weeks**
- We ship without committees and stay close to customers
- AI does **not** replace taste, trust, or customer understanding. It multiplies everything else.

</div>
<div>
<img src="/tuist-commits.png" style="width: 100%; border-radius: var(--noora-radius-xlarge); box-shadow: var(--noora-border-light-default); padding: var(--noora-spacing-5); background: var(--noora-surface-background-primary);" />
</div>
</div>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 82.5%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span class="is-active">2025</span>
    <span>2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
The commit chart shows our velocity increasing dramatically. AI has been a real force multiplier for us. One concrete example is that we rolled out Gradle support in three weeks.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Part six</span>
  <h1 class="talk-section-heading__title">Today</h1>
</div>

---
class: timeline-slide
---

# The business is working

- Binary and action cache, build/test/bundle insights, test flakiness detection and sharding, MCP and REST APIs
- We are close to profitability
- Inbound from organizations keeps building momentum
- We'll grow the team soon
- We now have 3 big challenges ahead

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 100%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span class="is-active">2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
Momentum is finally visible in the business, not just the product. We are close to profitability, more organizations are finding us inbound, and that gives us room to grow the team. The next chapter is not survival, it is executing well against the three big challenges ahead.
-->

---
class: timeline-slide
---

# #1 Scale our cache infrastructure

<div class="talk-split-slide talk-split-slide--globe">
<div>

- We are building infrastructure that is fast, low-latency, and global by default
- It has to speed up workflows from developer laptops, CI, and agentic environments
- It also has to work in a multi-tenant setup with a fair distribution of resources

</div>

<div class="talk-split-slide__media">
  <div class="talk-globe-frame">
    <iframe src="/cobe-infrastructure-globe.html" class="talk-globe-frame__embed" title="Global low-latency infrastructure globe"></iframe>
  </div>
</div>
</div>

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 100%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span class="is-active">2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
This is one of the hard problems ahead. If developers, CI, and agents are all producing software continuously, then latency stops being a minor annoyance and becomes a product problem. The infrastructure has to be global so workflows stay fast wherever execution starts.
-->

---
class: timeline-slide
---

# #2 Bring compute capabilities

- Compete with CI providers that co-locate cache but don't distribute
- Enable agentic workflows that act on your project data
- Sandboxing is solved; managing it at scale is the challenge

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 100%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span class="is-active">2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
Compute is the natural next step. CI providers co-locate cache with build machines, which is fast but not distributed. We can flip that: distributed cache first, then bring compute to the edge. Agentic workflows — like automated test analysis or code suggestions — need access to project data, and that means running code in sandboxed environments we control.
-->

---
class: timeline-slide
---

# #3 GTM for new ecosystems

- Plugging our infrastructure into new ecosystems is low-cost thanks to AI
- Bazel is next; long-term we plan to integrate with every build system (<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 128 128" style="display:inline;height:1.2em;vertical-align:middle"><path fill="#76d275" d="m32 0 32 32-32 32L0 32Z"/><path fill="#43a047" d="M0 32v32l32 32V64Z"/><path fill="#76d275" d="m96 0 32 32-32 32-32-32Z"/><path fill="#43a047" d="M128 32v32L96 96V64Zm-64 0 32 32-32 32-32-32Z"/><path fill="#00701a" d="M64 96v32L32 96V64Z"/><path fill="#004300" d="m64 96 32-32v32l-32 32Z"/></svg>, <img src="/rust.svg" style="display:inline;height:1.2em;vertical-align:middle" />, <img src="/go.svg" style="display:inline;height:1.2em;vertical-align:middle" />, <img src="/elixir.svg" style="display:inline;height:1.2em;vertical-align:middle" />)
- GTM is still too costly with too much noise
- Betting on video-based storytelling (limited resources breed creativity)

<div class="talk-timeline talk-timeline--with-gray" style="--timeline-orange-fill: 10%; --timeline-green-fill: 65%; --timeline-gray-fill: 75%; --timeline-invested-fill: 100%;">
  <div class="talk-timeline__labels" aria-hidden="true">
    <span>2017</span>
    <span>2018</span>
    <span>2019</span>
    <span>2020</span>
    <span>2021</span>
    <span>2022</span>
    <span>2023</span>
    <span>2024</span>
    <span>2025</span>
    <span class="is-active">2026</span>
  </div>
  <div class="talk-timeline__track">
    <span class="talk-timeline__segment talk-timeline__segment--gray"></span>
    <span class="talk-timeline__segment talk-timeline__segment--invested"></span>
  </div>
  <div class="talk-timeline__events" aria-hidden="true">
    <span><img src="/soundcloud.svg" class="talk-timeline__logo soundcloud" alt="" /></span>
    <span><img src="/shopify.svg" class="talk-timeline__logo shopify" alt="" /></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span><img src="/german-government.svg" class="talk-timeline__logo government" alt="" /></span>
    <span><span class="talk-timeline__symbol invested">$</span></span>
    <span></span>
    <span></span>
  </div>
</div>

<!--
Expanding to new ecosystems is technically cheap now — AI helps us build integrations fast. But reaching developers in those ecosystems is expensive and noisy. We're leaning into video storytelling as our GTM lever because it lets a small team punch above its weight.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Part seven</span>
  <h1 class="talk-section-heading__title">Wrap up</h1>
</div>

<!--
Let's wrap up with the key takeaways from this journey.
-->

---

# Looking back, looking forward

- **Compound your assets.** Code, expertise, reputation, trust, word of mouth. Each layer is harder to build and harder to copy
- **Brand travels further than you think.** Tuist grew organically in South Korea 🇰🇷. Local devs gave talks, translated docs, and we closed our first customer there without a single sales call
- **Think about the business earlier.** "Great" doesn't pay rent
- **Be ready for competition.** Companies that used your OSS for brand recognition can pivot to compete against you
- **Charge earlier than feels comfortable.** The discomfort of asking for money fades. Running out of runway doesn't

<!--
Honest reflections after years of building. These are not regrets — just things we see more clearly now. Trust compounds but takes years. Do not trade it away cheaply.
-->

---
layout: section
class: section-glow
---

<iframe src="/tuist-glow-shader.html" class="section-shader"></iframe>

<div class="talk-section-heading">
  <span class="noora-badge talk-section-heading__part" data-size="large" data-style="light-fill" data-color="neutral">Most importantly</span>
  <h1 class="talk-section-heading__title">Be yourself</h1>
</div>

<!--
Authenticity is the one thing no competitor can copy. Stay true to who you are and why you started.
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
