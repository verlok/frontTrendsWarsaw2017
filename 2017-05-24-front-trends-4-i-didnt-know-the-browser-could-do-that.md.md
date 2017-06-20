---
layout: post
title: I didn't know the browser could do that! - Sam Bellen - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, browsers, apis]
---

These are my notes from Front-trends 2017 Warsaw conference.

> The times when a browser simply had to parse and show some markup are long gone. These days they are full of interesting api’s exposing various information and behaviour to web developers. This talk will walk you through a few of these api’s, some of which you might know, some maybe not.

@Sambego

## Speech API

A browser can also talk! Text to speech. And you can choose the voice.
Chrome and Firefox 

```js
const synth = window.speechSynthesis;
const utterThis = new SpeechSynthesisUtterace('Hi everybody!');
synth.speak(utterThis);

utterThis.voice = // voices can be found and used -- More code in the sides.
```

Also works in reverse, speech to text.

You need to be connected to the internet to make this work.

```js
const recognition = new SpeechRecognition();
recognition.lang = 'en-US';
recognition.interimResults... // see slides for more code
```

## Geolocation API

Can define user's location.

```js
navigator.geolocation.getCurrentPosition(); 
// more code in the slides. aka 
```

## Notification API

It's easy, but you need to ask for permission first.

```js
Notification.requestPermission(permission => {
    if (permission === 'granted) {
        //yay!
    }
})
```

Then

```js
const notification ? new Notification("Im the title", {
    body: //... see slides
})
```

## Push notifications

It comes from a server vs the others only exists in the front-end.

This is recent, until service workers arrived.

You need a service worker, and SSL.

```js
if ('serviceWorker' in navigator) {
    // register it
}
```

```js
serviceWorkerRegistration.pushManager.getSub...
sendSubscriptionToPushServer(subscription);
```

And you need to self.subscribe to those notifications and do something.


## Battery API

```js
navigator.getBattery().then(battery => {
    //battery.charging
    //battery.level
    //..

    //battery.addEventListener('levelChange')...
    //more events in the slides
});
```

## Media something API

```js
navigator.mediaDevices.getUserMedia({
    video: true, // we want video
    audio: true // and audio
}).then(stream => {
    // we have access to the stream
})
```

## All together now

A personal assistant!

Conversational. Asks for the weather at this location. Battery level. Adds cats ears to his face through image face detection.





