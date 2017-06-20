---
layout: post
title: The first meaningful paint - Patrick Hamann - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, performance]
---

These are my notes from Front-trends 2017 Warsaw conference.

> __abstract missing__

He's a web performance engineer at Fastly.

Why here? 
How fast is your website?
What does it mean to be fast?
It depends on the context - what your user is trying to do.

What is the metric we should optimize for? Should it exist? Probably not. UX is a moving target.

More interesting metrics today are speedindex, first meaningful paint, time to interaction, custom...

TTFMP - time to meaningful paint. FMP is the time when a page's primary content appeared on the screen. And it's ABOVE THE FOLD. And fonts have loaded, which can take up to 3 seconds.

Shows a timeline, frames of loading, guess what is the TTFMP? 5 (i'd say 4).

With Google Lighthouse you can measure it. It's also a CLI and a browser extension. **You can integrate this in your build process**

## Optimizing for TTFMP

Building real website for real users means having lots of resources.

Webpagetest allows you to test on real devices and slow connections (emergin markets 3G). You should test for your average devices and network conditions.

What is your average user profile?

- wher are your users bases
- what is their device landscape
- what context are they using your site?
- ...

Set a budget for performance. The TTFMP that you need to achieve.

## Baseline

It's an HTML file with a link to a single CSS.

Q: What about HTTP/2, wouldn't it be convenient to have more than 1 file so they're smaller?

(shows a webpagetest waterfall and explains it)

### Inline critical CSS

Shows a flowchart of render blogking things, renderer vs network.
There's a lot of idle time, we're wasting time during network requests. 

If you inline CSS, we'd save time and make the browser know what to render.

We must use loadCSS to make the loading of CSS async and not render blocking.

Pros and cons.
- causes reflow
- not cachable, invalidating milion of pages every time you change a CSS file
- hard to maintain
- hard to automate

## Preload

How can we prioritize resource.
What are your critical resources? The logo? The fonts? The hero image? 

Golden rule: **Check out the initial navigation blocking resources and remove them.** 

Fonts are critical!

Back to the flowchart, shows how the text blocks the render.

Fortunately we have a new API named Preload. 
It provides a **declarative fetch primitive** that initiates an early fetch and separates fetching from resources execution.

You can declare them as a LINK http header.

Just putting them in the HTTP header, we can move it above in the waterfall.

Pros: indicate hidden resources. Cons: easy to create contention; requires server logic.

## HTTP/2 server push

Traditionally, the CSS were requeted after the HTML was parsed.
The server can send them.

```
Link: <critical.css>; rel="preload"; as="style"
```

No "nopush" here.

There's a priority tree. HTML has a higher priority over CSS. 

**NOTE:** the critical css is still in a separate file at this point.

**Is indicating push via HTML response too late?**

## Async push

We really want to use the idle time at the beginning.
So we want to push the CSS before we even request for it.

We need to have access to the apache or NGNX server. We send them ASAP.

Pros and cons: _(lost them, see slides)_

### What about the repeat view

Google "PRPL pattern", it tries to solve this problem.

Shows a **comparison video** of the loading, wow.

It shows a network diagram with hints, what the browser needs (_and what it already have?_)

Waste of resources to push resources that the browser already have in cache.

## Closing

_(lost this)_

Keep testing always

---

Q: What about service workers?
Q: What about FOUT?