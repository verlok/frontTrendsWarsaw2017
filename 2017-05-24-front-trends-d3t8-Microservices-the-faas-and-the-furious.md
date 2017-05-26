---
layout: post
title: Microservices - The FAAS and the Furious - Phil Hawksworth - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Recent years have seen a shift in technical architectures. Building complex services for the web used to be just that – complex. Projects might have demanded a broad range of specialist skills which could stretch even the fullest of full-stack developers. These days we have a growing number of options for how we design, build and maintain the systems which keep our web sites and applications alive.
> This talk will look at ways to make use of readily available microservices to unlock functionality​ and opportunity in otherwise simple technical stacks. We’ll talk about the benefits in keeping your stack simple, and in leaning on the expertise of others.

Me all the way down :D

I work at R/GA. We make stuff for clients. I'm a dream crusher. The evil.

Context. 
- Excessive enhancement -> be careful what you send in the browser.
- I can smell your CMS -> 
- Static sites go all hollywood -> solve the things that were wrong
- Fhe FAAS and the furious

Empowerment and responsibility for front-end developers

Make making things simple -> less complex

It's hard to achieve simplicity

"Functions as a service" - FAAS

A web site was simple, now there might be routing, view, app logig, database, cacing, wrapped in a server, say N servers behind a load balancer, CMS, DAMS, other services (pricing, tax, fulfillment). To try and find someone who can maintain all these, you're looking for a very particular people.

So I'm going static more often.  Bake, don't fry.

Static sites are limite, though. 
However, the ceiling is far higher than you think.

People think they are very limited.

JAM stack = javascript, api and markup

Think that you cant
-  have a site search (yes)
- Have forms (yes you can)
- comments (yes)
- have content management (yes)

Netlify -- google it

Build tools -> A web site (see slides) -> api endpoints -> automation. += Microservices 

We can have comments, live tweets

Considerations
- we could have a client-side twitter javascrip twidget
- ..
- we want it as part of the HTML mrakup -- without a server?

I can replicate the static architecture on Netlify. But twitter? Another source of data. So how we trigger the build? With IFTTT (if this than that) - I can create watchers that make request to an endpoint.

If @verlok tweets, call this endpoint.

But we need more power. And more control. 

So we need server-side logic, in a static web site. Routing somewhere else. You can do that invisibly. 

You can create a single function (lambda, like) that makes the magic happen to keep the service alive.

AWS lambda, ms azure, more ...

How do we route if we run a static website?
On netlify there's the _redirects 
- you can redirect /home to / --> 301
- /journal to /blog --> 301
- based on the country
- manage wildcards and :splashes
- can do proxying /api/* to https://api.foo.com/ ..

So static files + functions

Services
- serverless
- webstack
- stdlib

## Takeaways

- There's great power in avoiding responsibility :D - we need to choose what to be responsible for
- Don't be afraid to start small
- Don't be intimidated, tooling is coming
- Complexity can be a barrier, simplicity can be an enabler
- Simplifiyng is not dumbing down

---

What else have we learned

- it's hard to teach all abut neural networks in 30 minutes :D (rosie)
- transparency - a hallmark of our industry (vitaly) - UX in the center
- the browser can do more than you think (sam)
- consider the audience, the users (adam)
- we have to decide what the web can be (mihai)
- what we learn at this conf is futile (maciej) - the rate of change
- the power of animations (val)
- patrick + more about performance
- we drive and push forward
- hacking or experimenting we create our own path

--

Thanks!















@philhawksworth







