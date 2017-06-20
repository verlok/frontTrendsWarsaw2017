---
layout: post
title: WebCartoon about webassembly - Lin Clark - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, technologies]
---

These are my notes from Front-trends 2017 Warsaw conference.

Lin Clark is a web cartoon maker and she works for Mozilla

Web assemply is a way to
- Make _other programming languages_ run in the browser
- Improve performance 
  - (first there wasn't JIT, then JIT, then JS used for everything)
  - we want to do the timeshorter

What is JIT
- Goal: human to speak machine language (viceversa)
  - interpreter (runtime compilation - slower) vs compiler
  - browsers implemented the "monitor" which looks as the code as it runs - if i.g. the same function is iterated many times, it tries and optimize it - but it's hard to do it because the assumptions it made could be wrong, and if they are it needs to throw it all away. If it tried too many times, it stops trying.

Dynamic types though made JS successful, so we don't throw it away
We don't need to throw away any of JS to use webassembly, but... we need to use modules

WA makes possible for library and framework makers to optimize them - without changing API

CPU has
- registers (short memory)
- ALU (arithmentic and logic unit)
- RAM (external)

There is a 1 to 1 relation between machine code and assembly code
Different languages x human, different for machines (N to M) - too slow
- introduction of IR - intermediate representation
  - front-end C, C++, Rust
  - back-end ARM, x86
- web assembly is in middle from back to front (to ARM, x86)

LLVM project
- tipo un compilatore? (mi son perso)

Caricare un modello WASM è come caricare un modello JS, ma ci si lavora in modo divero.
Devi usare un js object che simula l'heap (un array)
Va wrappato tutto in un modulo?

Much faster (lost the announcement)
No garbage collection required

Browers are allied (edge, chrome, ff, webkit)

Status:
- currently working on how to make it interact with the dom
- integration with Garbage Collection

Questions:
- will it come to mobile? -> depends on apple and google
- how will we debug it? -> sourcemaps, probably
- why do we need to use an array buffer? -> because it's garbage collected as soon as the wasm is dismissed



@linclark @codecartoons