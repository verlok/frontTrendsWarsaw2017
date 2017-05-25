---
layout: post
title: I'm in IoT - Vadim Makeev - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, apis, internet of things]
---

These are my notes from Front-trends 2017 Warsaw conference.

> The Web has stepped down from virtual screens to the reality that you can touch: Bluetooth, beacons, blinking LEDs and flying robots! It’s there, but all tails are still leading us back to the new browser APIs. Stop pushing around screen pixels, let’s play with hardware in the Internet of Things!

He presented himself and the things he does, bla bla.

Talked about chemistry and gunpower and acids, still have 10 fingers.

Then life happened. Started to explore photography, design, then came to the web. It was a brand new world. New opportunities to express himself. 

But he lost the physical presence of things he did, though. Oh what a beautiful site I did! Best thing in my life! Then it gets a redesign and it's wiped away. 

The digital world is too fragile. We're not eternal though, but digital products are way to short. So I wanted to do something in my real life.

## Bluetooth 

B. is the best technology to transfer data, it unites protocols under the same standard. It also unites people, it's popular! In some places there's no wi-fi. In some villages it's used to exchange files.

Bluetooth 2 in 2004 and EDR (enhanced data rate) - it was fast enough to be usable, it has permanent connection. It works on short distance up to 10m, then it became 40m. Also 5.0 bluetooth.

Used in headphones, but it's expensive, so they're charging most of the time.

Bluetooth LE (stands for low energy). Low energy, 4.0 in 2010, short connections, long distances up to 100m. Slow speed (up to 1 megabit). But good use cases, like beacons. 

Beacons are small cheap boxes. In a conference they gave away 200 of them. Everybody was trying to connect to their own and you couldn't find your own, so I rubbed it (temperature sensor)

Bluetooth smart is the marketing name.

The bluetooth beacon transmits all the time. GATT server. There are applications able to connecto to those things. 

There are lots of devices in this room. I'm trying to connect... I did it. To a MI Band 2. I can easily connect to devices, explore their services, etc.

Services have unic ids (UUIDs), standard services are battery, blood pressure, weigh scale, etc. Standarc characteristics are battery\_level, waist\_circumferense, sport\_type\_bla\_bla. You can read properties, write properties, an subscribe to them.

LAMP demo. There's an app to control them, but it' ugly. Let's see if we can do something... I'm scanning the bluetooth devices in the room, found it, connected to it, there's an xFF08 service, and a characteristic called FFC. Let's try to write it... oh, it changed color!

## Web bluetooth

There's a web bluetooth spec, which allows you to control bluetooth devices. 
It connected it, now the button in the browser glows of the same color.
The bulb returns a promise and it contains the color.

Now it demoes and shows that changing an input text in the browser changes the lamp color at runtime. :) 

The app does a color validation using a Regex before sending it to the lamp. 

They have built in programs in this lamp. Like "rainbow" which changes color constantly. I can enable this program via bluetooth. I had to do reverse engineering to figure out what it did, bla bla.

DRONE!

It connected to a drone, it tries to make it fly. It has 2 buttons, take off and landing. 

The demo kinda failed, but the drone flied in the end... wasn't him! :)

webdr.one is an app to control a drone. I copied the code from there to make my drone fly.

Web bluetooth is enabled by default in Chrome.

Bluetooth 5.0 will bring more use cases in this area, because of longer distances, battery things, etc.

More links on the slides

@pepelsbey