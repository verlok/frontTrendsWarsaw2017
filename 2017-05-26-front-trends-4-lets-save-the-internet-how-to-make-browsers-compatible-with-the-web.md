---
layout: post
title: Let's save the internet, how to make browsers compatible with the web - Ola Gasidlo - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes]
---

These are my notes from Front-trends 2017 Warsaw conference.

> During the browser wars, compatibility was a mess and so was the web. Dirty hacks, a huge pile of frustration and enormous amount of time to test through every browser were a part of our everyday life.
> Times changed. Browser wars are finally over (right?!). But the web is still broken and browsers still work in different ways.
> In this talk, we’ll explore the reason for web (in)compatibility, how to fix it and how you as wcompats can help to save the world (wide web).

Ola is a web compatibility engineer & tech leader

What's web compatibility? 

- who experienced a bug
- who reported it
- who did a hack to get around it

Do you report web compat bug?

Why don't you? Too much hassle?

http://webcompat.com - they also have a bug reporting extension

You should be aware of how and WHY things work.

Some time ago we just needed to open an editor to make a change (no grunt / gulp tools to bundle things)

## Browser wars

WWW -> Nexus -> Mosaic -> Cello, Arena, Lynx, Mosaic

Mosaic was like to become the standard.

One of the Mosaic developer created Netscape Navigator - 1994. 
It improved Mosaic UX and reliability. Able to display pages as they loaded.

Netscape, IE. 1995. First browser war.

Netscape had Javascript. IE JScript. Blink and marquee. 

\1996. CSS Support. Opera.

Windows 1995 embedding IE. It became a dominant browser in 2002. 

First browser war won by IE.

And then 2003 released safari, in 2007 mobile safari.

Firefox released in 2004 and wow. 

In 2008 came Chrome, focused on developers. Then Firefox started to fall.

Chrome for android 4.

One thing we've learned during browser wars: things get better.

Browsers started to use the same engine (webkit, blink -- safari, opera, chrome)

Specs are a defined standard to what to implement in a browser.

Who does create the specs? 

The W3C decides. Because of browser wars causing incompatibility between browsers.

The community decides. (?)

The W3C decides what to implement but not how. 

You can become a member of the W3C, or you can join whatwg. Or contributing on Github.

Why should I care?

The CSSOM spec features all. Apple wrote a spec because they wanted it. If we anticipated it, that wouldn't be happened.

(_I kinda lost her here..._)

Prefix seemed a good idea to start a feature without breaking the others. Turned out it's not production ready. So they're moving away.

PWA

Make things backwards compatible, use a polyfill, test on saucelabs or browserstack, and selenium server, or webdriver.io, which has a visual regression service.

With all the tools set, produce good code.

You can become a Wompat, fight for the web. Feel the force, what you would like to contrib to. Go to webcompat.com, submit bugs.

Amazing community behind it.
















@webcompat @misprintedtype