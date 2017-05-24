---
layout: post
title: Watch your back, Browser! You're being observed. - Stefan Judis - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, browsers, apis]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Web development can be tough. DOM APIs are known to be not convenient, and often we build the same things over and over again. Thanks to rolling releases by the browser vendors that changed. The development of the web as a platform has speed like never before. New APIs land in Browsers with every release. There is also this new term of “reactive programming” and new Observer/Observable APIs.
> Looking for a way to detect DOM changes to update a different part of the page? MutationObserver got you covered. Want to get notified when elements enter the viewport to load assets? IntersectionObserver is your friend. You’re dealing with sequences of events over time and want to save some headaches? Observables will make your life way easier.
> This talk we’ll cover the use cases of Observer/Observable APIs, go over the implementation details, and teach you what you need to know to use them in production.

Organizer of a meetup in Berlin, and teacher at "CSS Classes". Works at Contentful.

I'm really excited about conferences. You can learn, make new friends, have excellent time.

4 years ago I was entering the world of web.

The web platform evolves fast. Staying up to date is part of our job. 

Browser APIs adapt to common use cases. We're moving from pull towards push.

Let's celebrate the 4 years! He took the 2013 website and implemented the same lazy loading effect. He was looking how to do that and found that el.getBoundingClientRect() could be very slow cause could force layout / reflow!

Also window.addEventListener('scroll') is slow. We should debounce that function. And do the less operations possible there.

He went to the browser and checked the frame rate (slowing CPU down). Whi so slow? Get boundingClient Rect it's slow!!! -> 8 frames per second.

So what?

## Intersection observer

How wo I use it? 
- Define options (like threshold: 1.0)
- Then define the observer (see slides)
  - entries.forEach

It went to the browser again, and it was now 18 fps.

With the threshold > 0, intersecting is still true when something is out.

Support: IEdge, Chrome, Opera, Firefox coming..., Safari not pervenuto.

We can polyfill though. Check if supported, then polyfill in case.

How can we know that the effect occured?

## Mutation observer

I watch the elements and check for changes. I count the effects. And I disconnect the mutation observer.

We can observe childre, attribtues, and more!

Support: everywhere.

## Measure perfs

Ways to measure performance.

Real User Metrics (RUM)

windows.performance.timing gets us really details information about performance

## Recource timing API

`windows.performance.getEntriesByType('resource')` gets lot of information about a resource.

## User timing API

```js
performance.mark('')...
performance.get...
```

see slides

And then comes the cache.

## Performance observer

You initialize it and then define what metrics you want to observe.
It's the new encouraging things to use.

We can observe paint metrics, for example.

Performance observer shipped in Chrome, Opera, Moz behind a flag. NOT polyfillable.

## Resize observer

I can set up a resizing observer, which is perfect for managing resizing related calculations. 

Available only in Chrome and behind a flag.

## Observables

They only exists in specs now.

It's a collection that arrives over time.

We can use map and reduce on them.

(He's using Rx.js to do it)

Collection superpowers!

Good example! See slides.

## Wrap up

- Intersection, Mutation, Performance, Resize observer.
- Observables.

4 years ago, no clue.
After 4 years, web dev still exciting!

---

@stefanjudis on Twitter