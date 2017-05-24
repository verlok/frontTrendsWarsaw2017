---
layout: post
title: Big Bang Redesign: Smashing Magazine’s 2017 Relaunch - Vitaly Friedman - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, __category__]
---

These are my notes from Front-trends 2017 Warsaw conference.

> You’ve been there: big bang redesigns are usually a very, very bad idea. Redesigning and rebuilding an existing website from scratch is risky and unpredictable, and in many cases the level of complexity is highly underrated and underestimated. In mid-2016, Smashing Magazine has decided to make a big switch from the existing WordPress setup to an entirely new design, entirely new architecture (JAM Stack) and an entirely new, GitHub-based, editorial workflow.
> In this talk, Vitaly will share some of the insights into Smashing Magazine’s Relaunch in 2017 — with decisions made, failures, successes, lessons learned and shady’n’dirty techniques used along the way. Among other things, you’ll learn how Smashing Magazine uses HTTP/2, service workers and server-less architecture with static site generators to boost performance, with a dash of React, Flexbox, CSS and the peek into the new GitHub-based editorial workflow here and there. Beware: the session will contain at least 27 illustrations of cats!

## Ad-blockers

Use one, but serve a fallback message.
Avertising wasn't working... we need to rethink revenue. 
- Replaced ads. 
- Brought focus to products. 
- Full transparency and reporting how we spent the money.

## Unified platform

## Team

- Exploration
- Design
- Front-end
- Illustrator
- IA, UX
- ...

## Browsers

- Chrome
- Firefox
- Safari
- Edge
- Safari mob
- Chrome mob
- IE11 1.8%
- IE10 0.2
- IE8 0.002
- IE666 - 1 person

## Visual design - Personality

- Explorartion of typefaces
- That typeface, Mija

## Find the right angle

- 11 degrees tilt everywhere

...shows lots of screenshots of the new smashing mag...

# Front-end

Don't like media queries, because there will always be points where things break. (?) We can't be sure they cover every width.

# Tools

Trello, Slack
Github, Sass, BEM
PSD, HTML
...

## Layout problem

We should highlight authors. But... it was complicated. Sara finally managed it, floating things around. 2 sections to the right, the 3rd up with negatie margin, the orange down again, then adding a pseudosection and float it right again...

## Flexible, responsive type

They fixed a minimum and a maximum and scaled all in between.
Lots of math here, and calc.
At the end there is a simple line. 
```css
font-size: calc(16px + (24-16) * (100vw - 400px) / 800-400)); // they're not magic numbers, see slides.
```
Same for `line-height`.

That can be turned off in specific containers, or on again.

## Open beta now

To dos:
- clean up stuff
- tweak performance - moved from wordpress to static (jam stack? gem stack?)
- nail functionalities
- migration issues
- consistent new look

# Wrapping up

Unsatisfying compilation video :D

