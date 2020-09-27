---
date: 2020-09-28T11:53:00+13:00
title: On causal inference
---

> Note: This post was originally drafted on ~20 April 2020, but never published until now.
> I have finally decided to publish it five months later with an Epilogue ;)

"The Book of Why: The New Science of Cause and Effect" by [Judea Pearl](https://en.wikipedia.org/wiki/Judea_Pearl) and Dana Mackenzie was recommended to me by my partner over the weekend, and I was instantly hooked, if not questioning part of my life.
The topic is so exciting that the availability of the preprint copy of my first ever scientific paper - [DeepBedMap](https://doi.org/10.5194/tc-2020-74) - is taking an aside (nah kidding, I'm still really stoked)!

Reading that book, the language of [Causal inference](https://en.wikipedia.org/wiki/Causal_inference) is two steps up from the statistics mindset I was taught in high school/university, where "correlation does not equal causation".
What then do we use to determine causation, and how do we express it?
It might bode well with the [Buddhist philosophy of Dependent Origination](https://en.wikipedia.org/wiki/Causality#Buddhist_philosophy) I've been brought up with though.
The Chinese term used is 因果, literally 'cause' and 'fruit', or to put it better, the 'seed' and hence the 'fruit'.

So yes, I'm reading the book with a background in the ([Weak AI](https://en.wikipedia.org/wiki/Weak_AI)) 'Deep Learning' space , cautiously interested to see how [Strong AI](https://en.wikipedia.org/wiki/Strong_AI) would play out.
Also with the ongoing Covid-19 pandemic playing out, and the Economic uncertainty, it seems like a space to get my head around.

It is with language, and through imagination, that we make sense of our world.
Having just finished "Doughnut Economics: Seven Ways to Think Like a 21st-Century Economist" by [Kate Raworth](https://en.wikipedia.org/wiki/Kate_Raworth), I am acutely aware of how powerful a proper visualization can be, and language falls in the same category of mental 'models' we use to describe our world.

So yes, I've gone down a rabbit hole, and below are just a sprinkling on what I've read during the initial slide (in rough order of when I started):

Epidemiology/Economist view:

- [More on enconomists and epidemiologists](https://marginalrevolution.com/marginalrevolution/2020/04/more-on-economists-and-epidemiologists.html)
- [Are economists smarter than epidemiologists? (Comments on Imbens’s recent paper)](http://causality.cs.ucla.edu/blog/index.php/2014/10/27/are-economists-smarter-than-epidemiologists-comments-on-imbenss-recent-paper/)

Machine Learning view:

- [Causal vs Statistical Inference](https://towardsdatascience.com/causal-vs-statistical-inference-3f2c3e617220)
- [Why every data scientist shall read “The Book of Why” by Judea Pearl](https://towardsdatascience.com/why-every-data-scientist-shall-read-the-book-of-why-by-judea-pearl-e2dad84b3f9d)

Video format:

- [The Seven Tools of Causal Inference, with Reflections on Machine Learning](https://doi.org/10.1145/3241036)

[![The Seven Tools of Causal Inference with Reflections on Machine Learning video thumbnail image](https://img.youtube.com/vi/CsMV5o3hotY/0.jpg)](https://www.youtube.com/watch?v=CsMV5o3hotY "The Seven Tools of Causal Inference with Reflections on Machine Learning | Judea Pearl")
-

At risk of sounding creepy, wouldn't it be better, if you were served personalized ads of stuff that would actually help you, (e.g. medicine that would *cause* you to get better), instead of ads that seem to fit your profile (e.g. medicine that are *associated* with your past clicks/browser history).
This is about getting 100% of the way there.
As per the [Pareto principle](/climbing-the-pareto-curve) the first 80% has already been achieved with relative ease using 20% effort, now it's time to tackle the last 20% with all that we've got.

Minions beware?

## WhyNot do something?

About half a century ago, scientists from the [Club of Rome](https://en.wikipedia.org/wiki/Club_of_Rome) commissioned a computer model called [World3](https://en.wikipedia.org/wiki/World3) that analyzed the interactions between population, industrial activity, food production and limits in the ecosystems of the Earth.
The results were published in 1972 as [The Limits to Growth](https://en.wikipedia.org/wiki/The_Limits_to_Growth), and the trend [is not good](https://www.mnn.com/green-tech/computers/stories/MIT-computer-model-predicted-end-world-limits-of-growth).

Coincidentally perhaps, an earlier model dubbed World1 suggested that 2020 was the tipping point for civilization.
And with a little benefit of [hindsight](https://en.wikipedia.org/wiki/Hindsight_Bias) now, we all know what's happening.
Novel Coronavirus Pandemic takes over the world!
Crude oil prices collapse below negative!

So what do we do?

We model.

One of the key tricks we have as humans is that we can *imagine*.
We can *imagine* something that has not happened, or might not ever happen, yet we still do it anyway, why?

It might be hinting at the fact, that we understand cause and effect.
Maybe the Buddha was onto something.
Our brains were wired to figure out what would happen if we did something, or what would happen if we did not do something.

If correlation does not imply causation, if everything in the world only happens by chance, why would we have evolved the ability to imagine?
Sure, we could be off the track sometimes, things we imagine will happen might not actually happen, cue Murphy's Law.
Still, it goes back to the question of why it is that we possess this 'feature' if you will, to create mental representations of different realities?

[Models](https://en.wikipedia.org/wiki/Scientific_modelling), mathematical ones to be precise, are a way of formalizing what we know of some aspect of the world.
They often allow us to answer "What-if?" type questions, or interventions as some may describe it that way.

Models can mean different things to different people, so I thought I'd just provide some context on where I'm coming from.
I do my research in the "Earth science" field, of which climate models are the most prominent example in the public view.
The research centre I'm currently based at focuses on ice sheet models, which is a subset of the great "Earth System" modelling work out there.
Even then, you hear people talk about glacier flow models in glaciology, age-depth models in ice core studies, digital elevation models in remote sensing, etc.

...

Yet you may have heard of the phrase "All models are wrong, but some are useful".

There have been attempts in some of these fields to use an ensemble approach, a wisdom of the crowd if you will.
Where results mostly agree, we hope that this means each model is doing the right thing.
Where results don't match across models, it means something is up, and the physics might need fixing.

An alternative approach is to test, test and test.
The model could be encapsulated in a mysterious box for all intents and purposes, but if it produces valid results given known situations, we can trust it.
If the model is run outside of its tested domain, maybe we can't put so much faith in it.

Either way, being able to step back from those results and pinpoint what caused those errornous results in the first place is hard!

What is the true cause, and what is merely a symptom?

If you remove the symptom, will the cause still remain?

---

## Epilogue

As September 2020 ends, I wonder if I would wake up, and see the world become 'enlightened'.

No, not 'free', for what is freedom if you still need to be controlled by one's self.

No, not 'secure', for what is security but a false sense of grasping onto impermanence.

No, not 'better', for what is betterment but a relative comparison that has no end.

So wake up, wake up, wake up, and see the light.
