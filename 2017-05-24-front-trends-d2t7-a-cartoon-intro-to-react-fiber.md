---
layout: post
title: A Cartoon Intro to React Fiber - Lin Clark - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, performance, react]
---

These are my notes from Front-trends 2017 Warsaw conference.

> React will be getting a new core algorithm soon with Fiber. This new algorithm improves perceived performance for complex pages. But to make that happen, the architecture had to be reconsidered from the ground up. In this talk, I’ll break down the new concepts and explain what makes it seem faster.

She works at mozilla.

What react fiber app does. It removes the jank, so it's more fluid.

It improved the perceived performance

It the new reconciliation algorithm. When react came, killer feature was Virtual DOM. React figures out to handle changes and update things.

If React would able to handle changes for something else? Renderers are pluggable. 

So what fibers does.

There are different triangles, each one containing smaller ones until the smaller portion which is a dot.

Fiber breaks the main thread in smaller pieces so it can return to the outer stack call, allowing the browser to re-render.

It does it in 2 phases:
1. render/reconciliation -- interruptible
2. commit -- not interruptible

## requestIdleCallback

Fiber asks the main thread for spare time, and main thread answers "go, you have 13 milliseconds", like. And it checks if its deadline has expired. Also it tags what it's changed and what's not. The stk of changes is called "effect list".

In the meantime the user can push a button like "aA" to increase font size. 

The tasks are prioritised, so high priority are executed before.

If a bunch of high priority arrives (starvation!) ... _nda: I didn't get this_

## cooperative scheduling

...