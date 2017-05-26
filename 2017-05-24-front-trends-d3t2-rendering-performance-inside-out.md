---
layout: post
title: Rendering performance inside out - Martin Splitt - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, performance]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Ever wondered why some things are "performant" and others aren’t?
> This talk looks at it from a Computer Graphics perspective - we will work our way up from pixels to DOM & CSS performance as well as shedding light on Canvas 2D and WebGL. You will learn tips and tricks along the way to get silky-smooth 60fps for your web app.

He engineers 3D and VR in the browser, ad Archilogic in Zurich.

Rendering performance. Your users will benefit, because they use your site to get things done. And also emotions, it's frustrating when nothing happens like for 10 seconds.

So agenda
1. computer graphics 101
2. browser rendering

## Computer graphics

Shows graphics diagrams and animations of pixels.

A pixel is a small box we can color! In the pixels there are 3 dots, RGB. To turn them on and off their intensity varies between 0 and 255. 2 digits of hex = 1 byte. FF = 255. So dots -> bytes. 

Talks about rendering. _(too fast to write down)_

This can get complex. To move the pixels. Write.

Sprite. Layer. Texture. They are the same concept. You take things out of the screen texture. Copy the entire array (sprite) to memory.

Rendering is copying sprite array to screen. 

Compositing is quickly copying memory over each other. It's a function. Input: screen memory (destination), sprite dto be added. Outpout: screen memory after (destination). How does it works? Doing an OR combination. 

Or we can multiply the colors. Or use a ton of equations. Blend functions! Blending. You could write your own. 

(shows formulas - the "screen" blend mode example - color = 1 - (1 - ...))

More compositing! Translate (move). Scale (2 pixel instead of 1). Rotate.

Compositing only: 
- rotate, translate, scale.
- blending -- only if it's in a separate layer
- filters -- only spearate layer, not all of them, not all browsers

Composite only filters - the browser does not repaint pixels for them (?)
- grayscale
- blur
- contrast
- hue-rotate
- invert
- opacity
- saturate
- sepia

CSS filters vs SVG filters. SVG causes repainting, which is worse.

- drop-shadow has a problem on Safari (causes lots of repaints)

Composoting -> shader = ... get a color

So back to the initial diagram: numbers, numbers, shader, image.

### Recap of part 1

Pixels are a bunch of numbers in mem

- useful to separate in sprites
- compositing = combining layers
- blending = how we combine
- compositing can be done concurrently

## Part 2 - browser rendering

Javascript, style, layout, paint, composite

> Performance is the art of avoiding work - paul lewis

Different paths - I can jump the layout, or jump the paint and only do the composite

Layout is a lot of work. Paint them. Then javascript goes "you know why? let's change" -> Nou! Re layout, repaint everything.

Why translateX 200 will repaint?

- Textures are expensive (intensive use of the memory)
- Entine relies on hints for layers, such as 
  - video and canvas
  - _3D_ transforms
  - _composite-only_ animations
  - will-change property (even if I change the LEFT property!)

### Browser rendering summary

- layout and paint is expensive
- compositing is only enabled then there'a layer
- layers hava cost
- signals in CSS lead to layer creation
- cheackout csstriggers (google it)

---

**MEASURE _THEN_ OPTIMIZE**

_(nda: wow that was an amazing talk!)_

@geekonaut