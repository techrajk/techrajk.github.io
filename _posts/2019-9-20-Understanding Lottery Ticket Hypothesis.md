---
layout: post
title: Understanding Lottery Ticket Hypothesis 
comments: false
---

![lottery](/images/lottery.jpg "lottery")

On 7th of this month I attended a meetup at <a href="https://www.silversparrow.com">SilverSparrow</a>.The speaker Megh Makwana during his presentation on Mixed Precision Training made a reference to a paper titled "Lottery Ticket Hypothesis".The title and its relevance to theoritical understanding of deep learning pushed me to go through it.

Here my take on this paper.Just a disclaimer that this is my first hand account and by no means written by Phd. bent of mind. :)

## Background
Those who have some knowledge about Neural Networks understood the importance of Initilization(of weights) for sucessfully training a model. Sometimes your choice of weight vector would converge early and sometimes it don't no matter how long you train it.The question why they(Neural Network) behave in this manner is still baffling both the deep learning reseachers and coders.More on this in later half of the post,till then keep horses of your mind reined in.

## Why the name "Lottery Ticket" ? 

The authors of this paper Micheal J and Carbin of CSAIL,MIT tried to draw an analogy between initialisation of NN to buying a bag of lottery tickets and the **"winning ticket"** being the model that is successfully trained.
You bought a bag full of every possible ticket that has the chance of winning the lottery and only one of them is going to be the winning ticket.


## What the paper is trying to say or establish ?
Simply put it states that there exists a smaller sub-network within the larger network that is capable of being trained on new data to make predictions that doesn't departs too far from the original network, provided weights are reset (not reinitilised) to the state that the original network had when the training begins.
<br />

<br />
## Roadblocks
The paper used a brute-force approach to identify 'subnetworks' and doesn't provide a clear framework for identifying them in a larger network.  
Also some warmup strategy is to be used in large and deep networks.

## Future Directions

<br />
If you want to add something or could explain it better some other way , contact me at tech DOT rajk AT gmail.com, I would update this if found interesting.

<br />

<a href="https://twitter.com/share" class="twitter-share-button" data-size="large" data-text="Check out this AWESOME article" data-lang="en" data-show-count="false">Tweet</a><script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
