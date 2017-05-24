---
layout: post
title: Monsters, mailboxes and other nonsense - Niels Leenheer - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes]
---

These are my notes from Front-trends 2017 Warsaw conference.

> The Internet of Things can become quite boring pretty fast. Turning on the lights in your apartment with an app is a nice novelty, but it isn’t really very creative. And as developers we like to tinker and look under the hood, but manufacturers like their walled gardens. This talk is about combining sensors, switches and displays with different technologies to solve problems that don’t really exist and more importantly just to have fun with IoT and make geeky stuff. This talk contains monsters, and lots of them.

I'm gonna speak of my new house.
I'm far from the internet connection and I don't have a TV.

In NL there was a program called _the house of the future_. It had digital things, speech regognition, etc. 
Nowadays many of those things are in the house. 
- Radio controls switches
- Smart lights
- Wi-fi connected speakers
But still I miss something. 

IoT is incredibly boring.

Let's combine them to do things together. 
Use raspberry pi, combine things together to do something like... 

## A chicken thermostat!

I inherited 5 chickens, but I am lazy.
So I bought stuff and I combined together using a rfxcom.

If the temperature goes below zero, turn on the heater. It's just a switch on and off.

## The "s" in IoT stand for security

It's not secure, I can enable the fire alarm of my neighbor if I want.

## The fiery witch teggle

Do it yourself IoT.
We need a brain, or microcontrollers. 

We could use
- Arduino (big, limited)
- USP-01
- NodeMCU - very cheap, --- see specs in slides

NodeMCU you can use Lua SDK and write code in C.

Neopixel is a thing with 24 LEDs in a circle. (he shows the code to make a led go round)

He modified an IKEA lamp and made it glow like a fireplace (showed the picture and video)

You can talk to Siri to enable its sparkle.

## Pixel mosters

A ceiling light he brough in a store with an LED panel.
Modified it to display monsters.

Created a grid in a 3D printer, put it in an LED panel, tried different things, etc.

You can even draw your monster in an app for the smartphone. (showed the code to do that) The drawing goes to the connected devices. 

Live demo --> loaded the app in the phone, drawed in it, it was laggy, but it worked!

# The mistery of the haunted mailbox

I have a mail box, outside of my view. I didn't want to go out to check the mail.

Used magnetic contacts, managed by the rfxcom, to send a notification to the display and to his phone.

Some times lots of notifications arrived. It was the wind. It solved it with a "patch". :)

