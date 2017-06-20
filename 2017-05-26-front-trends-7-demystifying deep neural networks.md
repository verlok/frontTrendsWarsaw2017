---
layout: post
title: Demystifying Deep Neural Networks - Rosie Campbell - Front-trends Warsaw 2017
date: 2017-05-24 18:00:00 +01:00
categories:
- conferences
tags: [front-trends, notes, future of the web]
---

These are my notes from Front-trends 2017 Warsaw conference.

> Deep neural networks are the latest hot computing trend – but to most people they are still a bit of a mystery.
> With the release of libraries like Google’s Tensorflow and the open source ConvNetJS, there’s never been a better time for developers to start exploring deep learning. But I know from experience that wading through complex academic explanations can be pretty intimidating!
> That’s why I wrote a talk that starts from scratch and assumes no prior machine learning knowledge – but by the end of it, I aim for you to go away as excited about neural networks as I am, and knowledgeable enough to rave to your friends about them in the pub.
> We’ll look at what makes a neuron, how neurons become a network, how networks are trained and what the ‘Conv’ in ‘ConvNets’ means. We’ll see how ConvNets can produce weird and wonderful works of art, how they can turn your selfies into masterpieces, and look at some of the rather amusing ways they can go wrong!

Rosie works in R&D.

Why neural networks at a FE conf? 
- understand the hype, 
- you will interect with them at some point
- they are amazing
- not as hard as you might think

We'll make some simplifications.

History: 1940 cybernetics, XXXX connectionism, 2006 deep learning - good hardware, internet provides "big data"

Conventional computing to recognize acat takes a bunch of ifs

Neural network takes positive and negative examples

Neural networks because they are inspired by biological brains

Neural networks are good at things humans do, and bad ad things computer are good at

Trivial example - will the weather be nice, etc.

Should a go to a concert? (Score x importance) * N factors = > 25 ? I'll go

So we sum up things, check the activation function.

Activation functions are step, sigmoid, or the 3rd one which is polular these days

Isn't it all just simple arithmetics though? No :(

We need to train the network
- randomly initialize the network
- get a ton of labelled training data
for each piece of data
- check whetere the network get it right
- how wrong was that?
_(see slides)_

Go back to the network and re-train it

How do we know how much it was wrong? Using a error, energy or cost function. It's the difference between the desired and the actual output.
Minimising the loss function

**Tensorflow (google's open source learning platform) does it all for you!**

Convolutionar networks (convnets) are good for recognizing images

Images are a bunch of arrays of numbers.
The convolution operation is pasing an array of numbers and multiply ... (see slides)

Until 2011 we had 25% error, in 2012 convnets made it to 12%. Now they are similar to humans.

Inside a convnet, in the later layers, you can see better details.

Style vs content.

Google daydream examples.

Algorithimic bias - machines are neigher infallible nor objective, the network sees what's trained to see -> diversify your training data, and your engineerint teams

---

WOW.




















@RosieCampbell

