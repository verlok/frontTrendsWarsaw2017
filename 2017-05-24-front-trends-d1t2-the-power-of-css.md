---
layout: post
title: The Power of CSS - Una Kravetz - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, css]
---

These are my notes from Front-trends 2017 Warsaw conference.

> This talk will go over some of the superpowers of CSS. From fauxtoshop to recreating common UI elements, or querying for browser information via at-rules, CSS supertricks offer control and new capabilities. You’ll learn where to use these superpowers for good, and when (and why) they shouldn’t be used—all while keeping accessibility in mind along the way.

A talk about blending modes and filters.

She demoes live with a very colorful picture. In one textbox she writes the code to change the filter, in another the blend mode.

- blend-mode : color, she covers an image with linear gradient and uses it as blend mode. You can also use it with images, or videos, or iframes. 

CSS is a Turing Complete system. She demoed something.

Youmightnotneedjs.com contains examples, like
- the accordion example using checkbox, 
- tabbing group using radio buttons
- lightboxes -- two links, one for the thumbnail that links to the lightbox, the lightbox is then dispayed using :target
- modals -- similar technique, using opacity:1; visibility:visible
- tooltips -- uses `<span data-tip="I am a tooltip" tabindex="0">tooltip text</span>` e in css `content: attr(data-tip)` -- the triangle too is created in css only
- scroll progress bar -- this is a hack!, a gradient that takes the height of the page, ... didn't get that

## CSS Grids

You can check in your browser's CSS if it support things. Like CSS Grids.

## More things you can do with just css

You can create entire presentations in HTML+CSS, featuring keyboard support and access keys to specific slides. 

You can preate games, like whack-a-mole, tic tac toe (of course it's not adviced in production)

Create a big writing in 3D like transformed and skewed with animated text background.

## Conclusion

Don't do it in production. But CSS is awesome.