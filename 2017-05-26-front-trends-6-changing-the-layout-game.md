---
layout: post
title: Changing the layout game - Chris Wright - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, html, css]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Our demand for layout on the web has changed, we’ve moved from building a series of pages, to building interfaces out of libraries of components that we compose together. Our tools for creating layout in the past have been an exercise in hacks, magic numbers, and workarounds.
> The tools we had weren’t designed for the challenge, but we made them work. Today, we have game changers like Grid, Columns, Flexbox, and Calc. With these powerful features we’re capable of creating beautiful, flexible layouts with much more simplified code, and build out components that can independently adapt to the space in which they exist.
> In this talk, we’ll discover the possibilities these features create. We’ll explore the ResizeObserver and the first steps toward the Container Query, creating smarter components with Flexbox, managing complex layout with Grid, and using CSS Variables to help us simplify managing the layout.

Goes through the ways we changed the layout in time. Tables, floats and clearfix, bla bla.

We create the craziest hacks.

Hacks are the path we want to walk.

Some hacks are brilliant, some are not.

Brittiant:

- Intrinsic ratio, quantity queries

Bad:

- Browser isolation 
- Using comments to prevent inline block to have a space

Flexbox grid (35 lines of code, wtf!) became the css grid (3 lines of code).

Fraction unit. Repeat. Minmax. Start at the 2nd column. Column span: N. 

And we can break out of the grid, using z-index.

Use the span property to do complex grids.

And you can make it flexible. Auto-fit make them responsive by default.

Auto rows.

Simplerwith variables. Define how colums spans. Combine it with repeat to be a 1 liner.

_Creating offset is not yet possible but it would be great to have._

Quantity queries can be used with grids - depending on how many items you have, change their size.

## Moving towards components

Large, small - breakpoint.

On the most famous websites I found 264 media queries. They are restricted to viewports and media types.

Media queries aren't flexible enough. The dream would be to have them auto-flexible elements in the grid (see slides)

Container queries would be the solution.

But problems: 
- infinite loops are possible. 
- css is parsed in such a way...

Flex can solve it? --> media query-less layout

Flex-grow: 9999 variant (flex-grow: 1, flex-grow: 9999)

Multi columns

column-width: 600px, if you don't specify the number of columns they are automatically generated

Combine multi columns with flex grow 9999 and you get the layout

### Component based imagery

SVG has its own space

You can embed `picture` inside an SVG, to use SVG as the container

### Component text

Resizing and make text react to the size of the component would be good

Container based fluid typography - how does it work? JS -> Resize observer -> setVariable on the container to set the element width and height

In the browser, it works

---

Shape your own path

