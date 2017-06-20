---
layout: post
title: Alternative Reality DevTools - Konrad Dzwinel - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Eleven years after the first release of Firebug, all browsers now have excellent developer tools of their own. One thing that always bothered me though, is how very similar these tools became to one another. What’s more, some of the original Firebug’s ideas can still be found in today’s devtools in an almost unchanged form!
> With a strong belief that we should revisit those ideas, I started looking for an inspiration on how the alternative versions of devtools could look like. I talked with Android developers, designers, architects and electrical engineers about the tools they are using. I introduced people unfamiliar with how the Internet works to devtools and collected their thoughts and expectations. Finally, I had countless discussions with Front-End engineers about the way they are using them today.
> This research gave a unique perspective on devtools and allowed me to build some interesting prototypes. In this talk I’d like to share both, the conclusions and the demos, with you.

Programmers prefer to spend time writing a regex rather than spending the same time doing manual work :)

He uses devtools and reports bugs -> sees the discussion between the developers.

Then started to do pull requests. Added caret-color, then cookie editing.

On each browser there are dev tools teams and designers -> competition

All major devtools show ? in them. Where does it come from? Some think it started from firebug, but it started with jdebugger, then javascript debugger by netscape (had a console, a cal lstack, etc). 

These tools were separate from the browser. 

Microsoft released InterDev. Outline, css editing, - but it was meant for asp develpment and it wasn't free.

So we started with the `alert()` method.

In 2002 firefox started and in 2004 it had a console to evaluate expression, see errors, but no way to console.log from your scripts. -> So bookmarklets, extensions, the developer toolbar!

2006 Firebug was created. And console.log. First version was only the console, but you could inspect elements (to the console). Many devs went to firefox then! 

Safari released web inspector as stand alone tool for inspecting html and css. And standalone js debugger. Then progressive impressive development. 

Chrome was created as fork for webkit so inherited the devtools.

Firebug was then deprecated because it was native in FF.

IE then had the F12 tool.

And that brings us to today.

---

Now self mad tooling. 

An architect, Kasha, showed me some of the tools she uses. Like Autocad (complicated paint app). Infinite canvas where you can put things. Huge customizable space. Color coding made by herself. 

Bolko is a photograher, has a camera he uses to photograph sport. He uses a video editing tool. It has different environments to edit audo, clips, etc. I liked you can go back and forth in time.

Electronic engineer uses labview. Canvas. You can group pieces into components. And declare vaues.

Jakob game programmer. Unity, vistuual studio, unreal engine. Unity is super customizable, you can put the panels wherever, close them, etc. The inspevtor changes depending ton the context you're inspecting. Building for block to create behaviour diagram.

Patrizia is a graphic designer, from icons to big layouts. Uses Adobe tools. And Sketch, that have an infinite canvas and allows to create components, and have a library of them, and also manipulate them in place.

These were the highlights from the interviews I made.

---

I started creating prototypes and mocks (fake!).

## Context aware inspector

Meta tag inspector.
Inline SVG editor. 

## Concentrate

If you need to scroll up and down...

Change the tool so it can concentrate on a single element (inspect it like "edit group in place" in Adobe Flash). And switch between them. And reload them singolarmente.

## Timeline

Interacting with your application then going back in time like with CTRL-Z.

This actually came out in Opera Dragonfly, the dev who did it now works in the Edge team. Let's see.

## Infinite canvas

Emulating a single device is cool, but it would be cool to have emulation of more of them together, and maybe group them to interact simultaneously. And maybe multiple pages in canvas.

---

How do we make them a reality?

Most of them are open source, the FF ones are on Github, written in react and have a super community behind it.





