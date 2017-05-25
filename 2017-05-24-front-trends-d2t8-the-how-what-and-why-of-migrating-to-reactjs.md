---
layout: post
title: The How, What and Why of migrating to ReactJS - Jack Franklin - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, react]
---

These are my notes from Front-trends 2017 Warsaw conference.

> The application I look after at work is a large ticketing platform that was written using Angular 1 and has not been maintained. With the new release of Angular 2, we made the decision to migrate off Angular and onto React.
> In this talk I’ll discuss why we did this (without criticising Angular, it has served us well) and how we’re migrating in small chunks. A big rewrite was off the cards; this application is business critical and as such we can’t afford to not be able to fix existing bugs or quickly add features because we’re rewriting. Instead we’ve split the work down into many small pieces that we can tackle one at a time.
> I’ll go through some code examples and talk not only about the benefits but the negatives too, because it’s not all been plain sailing. We’ll see how React’s approach and characteristics make it very adaptable and we’ll look at how we updated tests as we went to ensure our migrations maintained feature parity.

It's about migrating complicated pieces of software. 

SongKick we sell tickets and find tunes you might like

The product it called "the store".

It started 2 y ago based on Angular 1.
It works very well, but changing it is VERY tricky.

It works on an older version on Angular 1, we have legacy code, we lack confidence in your system.

4 t's: Tech Test Team Talking

Chosen react because we're familiar with it already.

Big bang vs incremental. 

Big bang gives problems, the add value is only at the end.
The incremental add value immediately, and you keep adding more value.

Bit by bit makes you learn while doing... 

## The theory

Components (or directives in Angular) are organized in a tree. The outmost, then chidren.
So we started from the leaves of the tree. In theory it would work.

## The plan

..

(don't have time to write...)


## Tests

We can't break the store. 

Unit tests would need to be migrated too. But they are coupled with the code. We wanted to abstract from the code.

So acceptance tests. Automated tests decoupled from the code.

They are slow to run, though. We don't test every edge case but the most risky ones.

## Team

First time for me on long project. It's 9 month working on the same goal. How do we keep the team motivated and running. Momentum and prioritization. 

Pick work based on bugs and churn rate, not code quality. Churn * bugs == priority.
Churn rate = how a file is "hot" meaning you edit frequently.

Mix large tasks with small ones to keep people interested .

Break down large work into smaller cards and pull requests.
It also to make a better review work with your reviewer.

Release early and often, to make easy to react to bugs.

Always leave things better than you found them (the scout rule).

A migrated codebase is not a perfect code base.

Everytime you touch some code, you'll learn about it. So why make it perfect now?

Document code directly in the repository, using .md files.

**Metrics metrics metrics** Keeps the team happy to know they're heading in the right direction.

Migrations are a good excuse to upgrade your tools. Browserify to webpack; tests to jest.

The most important people to convince are not in your tech team.

He shows some sentences he tried to convince... nothing worked, until... ? he played it on maintainability and platform stability. 

Keep people in the loop. 

Deal with fire. Unfortunately things will go wrong in production. Explain what went wrong and what you did to prevent it from happening again.

## Takeaways

1. don't migrate for the sake of it
2. plan plan and plan again
3. cross business comms it more important than you think
4. prioritized based on (see above)
5. mix tasks
6. ?(_lost it_)
7. don't expect it to go perfectly on the first time

@jack_franklin