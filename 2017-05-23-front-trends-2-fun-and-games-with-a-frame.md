---
layout: post
title: Fun and games with A-frame - Andrej Mazur - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, frameworks, 3D]
---

These are my notes from Front-trends 2017 Warsaw conference.

Many devices out there to make WR
The simplest is a piece of cart where you can place your smartphone

WebVR is a bunch of API to render something in a stereoscopic-view-enabled device 
- power of the web
- you already know the tools and how to use them

[Sechelt demo](tiny.cc/sechelt) is meant to be progressively enhanced
- I can run it on my laptop and move around with my mouse and keyboard
- I can simply use the smarphone
- I can put the smartphone in a cardboard if the browser is VR enabled 
 
Documentation status is editor draft

iswebvrready.org -> webvr.rocks

To make a WebVR you need to make boilerplate stuff that are boring (set up lights, the camera, init scene, declare and pass canvas, listen to window resize, preload assets, figure out responsiveness, etc.)

With a-frame you can start right away. 
- cube example -- lights, key controls, etc. already set up, etc... it's 3 lines of HTML

```html
<a-scene>
<a-cube>...</a-cube>
</a-scene>
```

Uses the entity component framework. a-camera, a-light, a-thing...
It's components+attibutes. Kinda XML-like.

There's a lot of things ready in the registry

A-frame is just javascript. It's based on three.js, so you can extend it if you're capable of.

We can also animate things, using the a-animation entity.
3 animated objects could be made with 20 lines of code total.

He created a 3d breakout game (arkanoid).

Esiste anche un inspector - è tipo una web app - non ho capito come si attiva, ma esiste.

Demos
- a-painter - allows people to create a 3D model
- a-blast - shoot ad emojis
- a-saturday-night - record your dance, place to someone else
- journey to mars
- city builder 
- data visualization - bring boring stats to life
- ar.js - augment reality with a-frame

A week of a-frame
- links to resources, demos, stuff on their blog


VR is a totally new experience
- you have to think about a brand new input
- about UI and UX in your projects
- how do you traverse from one reality to another (portals?)
- consider motion sickness - people may react strange (don't move the camera, let them do it)
  - add a virtual nose, it can solve some problems

New 360 view
- give people reasons to look around (tell them explicitly that something is happening behind them)

Immersion over gameplay and GFX
- you don't need amazing graphics or effects, as long you can make things move smoothly and make them feel "inside"

Links
- aframe.io
- webvr.com
- webvr-info
- (the one mentioned above)
- building up a basic demo with a-frame


@end3r