---
layout: post
title: Components, patterns and sh*t it’s hard to deal with - Marco Cedaro - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, __category__]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Everyone has a pattern library or dreams about having one. We went through conversations and the codification of our visual dictionary and then we ended up with a beautiful living document.
> But what happens when we need to re-use our components and they don’t fit in the design? How do we re-use our patterns in slightly different use cases?
> We have all the tech to make a front end really modular, we have techniques and methodologies which enabled us avoiding the bad parts of the languages we use. Every part of the puzzle seems to be falling in the right place.
> Yet, sometimes we are struggling to handle the variations of our patterns in a reliable and maintainable way. Our codebase is getting filled with exceptions and overrides and refactoring of base patterns becomes impossible. This talk will explain some techniques to get back control and why the might work or not in the way we’d expect.

Modular architecture. Classes and compoents. Components and modifiers. And overrides. Or... the title.

Meaning is complex and ofter gets lost in translation. Everybody has is own mind model.

2015, Shazam. We were trying to build a modular system. We used Mustache, Akase, BEM. Struggling to make this as modular as it should be.

Atomic desigbby brad frost. Atoms, molecues, organisms, templates, pages.

Back again, web components in 2011. (undelivered?) We are eager to work with that because we want that modularization and componentization.

Triggering point was reactJS. We started to make things modular. It gave this change to us in how we perceive components.

## Where are we at, today?

It's not that simple. Like trying to fit squares in a hole. 

"A pattern library is a mix of minimup things that I can put together in a low definition mock." (_NDA_ kinda)

How do we manage patterns without making too rigit rules?

It's not about any specific tech stack.
It's about modularity at its core.
About ..

### Classname injection

I mean 

```jsx
<IconButton className="content-actions__button">
```

??? kinda lost him here -- too fast on this point

### Ad hoc BEM-like modifiers

```jsx
<Dialog ...
```

??? still too fast on this point, lost him, need to watch the video

### Predefined modifiers

...

## The issue

What are we trying to solve?

### Arrangement within parent components

(_nda_ I can't follow, do I read or do I listen to him?)

### Space in relation to other components

Inline defined space in classes. Like M40, P20. (_nda_ Really?)

## Does it get easier?

No. Yes. It get easier. Oh yeah? The more you know what you are and what you want, the less things upset you

I just don't know what I'm supposed to be

Instead of start coding right away, we need to get involved early, talk to people, we need to remember that we're not hopeless.

