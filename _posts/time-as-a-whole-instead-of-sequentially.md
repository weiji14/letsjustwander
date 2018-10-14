---
date: 2018-10-14T23:47:00+13:00
title: Time as a whole instead of sequentially
---

Can you multi-task?
Is it possible to look at your whole life, basically everything, at once, instead of one by one?

I'd like to draw some parallels on the above two questions.
The first question can be thought of on a micro scale, running several things in parallel over the course of an hour or a day.
The second one appears to take your whole life into consideration, namely:
"Is there a way you can be intentional with how your whole life will play out?"

In fact, there probably doesn't need to be a distinction.
We could simplify things and say, yes, there is a simple app that is extremely efficient which can multi-task and handle everything all at once.

How so?

The answer lies in your brain.
More specifically perhaps, your mindset.

## The good ol' bad ol' for-loop

For many of us, we think, and therefore go through time in an orderly step by step manner.
First we do this, then we do those, finally we do that.

In learning programming, one of the first things we learn is how to construct a [for-loop](https://en.wikipedia.org/wiki/For_loop).
It is an ubiquitous tool, allowing a program to execute a task or a set of task in regular intervals, one after another until the loop is terminated.

Clasically in school or work, we tend to progress through ranks in a linear fashion too.
You start with basic tasks, and as you get more proficient, you are given harder and harder tasks to learn and do.
Well, at least up to a point.

When we build ice sheet or climate models in the university, there is also this concept of time baked in.
The models don't run in reverse, it has to run along a one way street, e.g. from the present to the future.
Hardly ever would you run your model from a future state to a past state (unless doing some sort of inverse modelling).

Why is it that these things are made to happen in sequence?

One word - **Dependency**.

I mentioned in the beginning that there is no reason things can't just happen in parallel.
The only thing stopping us from breaking the speed barrier, multi-tasking, progressing on with our life, etc, is that we are held back by a **dependent**.

Now think about it for a while.

Why would you need to depend on something to happen, before you can take the next step?
Is there a reason for that dependency to hold you back?

The key to progressing is to resolve your dependencies.
You could wait for the dependency to resolve itself, basically letting it run its course over time until it is over.
*Or*, you could realize that the dependency is irrelevant, that there is no reason B needs to be after A.

Ask yourself:
"Could you take a shortcut that sidesteps that dependency, such as by taking the bridge instead of kayaking through the river?"

In the examples listed above, the for-loop could be converted into a [vectorized loop](https://en.wikipedia.org/wiki/Automatic_vectorization).
Almost two weeks ago, I [refactored a part of my code](https://github.com/weiji14/deepbedmap/commit/061242a9e0437a9e98c9052223b7a63f88515878) that was taking minutes to an hour to run on a new set of data.
I was trying to find tiles (cropped boxes) of relevant parts of an image that had full data.

I looked into many ways to optimize the sequential for-loop by using spatial index queries and even trying out a parallel for-loop (that still had an element of sequential-ness to it).
In the end, I figured out a vectorized implementation, and was surprised to see it taking seconds to run instead of hours (though I never actually timed it for that long).
Granted, I probably had to trade off computer memory for this.

The power of being able to look at everything at once instead of one by one is incredible.
In my case, the dependency clearly did not need to be there, it did not matter if I looked at one area first before another.
In other cases, you might still think that there is a reason that dependency needs to exist, but have you truly looked hard enough?

## Dependency or Distraction?

The word 'dependent' can also be though of demographically (see [Dependency ratio](https://en.wikipedia.org/wiki/Dependency_ratio)) as those who are below the age of 15, and over the age of 64.
Basically kids and old folks.

Now the ages 15 and 64 are quite arbitrary, it is not to say that every kid under 15 and every retiree over 64 aren't making productive contributions to society.
While I do agree that newborn babies are very dependent individuals requiring lots of care, I'm not sure older kids are necessarily counted as dependents.

Sure, it varies from place to place, from generation to generation, and even people to people.
There is no hard and fast rule on when parents and guardians can say their kid is no longer their dependent.
While newborns require literally every one of their basic needs (food, water, shelter) to be served, you could argue that a teenager wouldn't want you shoving food or water into their mouths.
Mental needs on the other hand, that probably goes on for much longer into adulthood.

I have a lot of respect for parents and guardians who have to care for their young dependents.
But I'd still like for them to know that kids are not an excuse to distract them from their goals in life.

I know what I'm saying can be interpreted differently, so I'll try to get at the gist:

> At some point in your life, be it after your kids have grown up and moved on or **right now**, you will need to figure out your goal.

It is easy, I know, to fall into this trap of thinking "Oh, I'll decide after X happens".
X could be when your kids grow up, or when you graduate, or when you get enough experience for that promotion.

Then what?
Then what?!!

The art of looking at everything at once(TM), is to finish answering the "Then what?"
It is not merely an efficient means to the end, it is truly looking at the end game itself.
Those very *hard* existential-type questions you've been putting off for who-knows-how-long *needs* to be resolved at some point.

Would you rather start figuring them out now when there's plenty of time to craft out a good answer?
Or do you want to postpone/procrastinate until you've fixed that all-too-distracting [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell)?

## If time can be non-linear, so can you

Your health is not something you take care in the future when you're old.
Putting off your finances until you're nearing retirement isn't smart either.
Nor can you forever hide or run away from all the truly important things that needs attending to.

Looking at time as a whole instead of sequentially is to treat your future in much the same way as you would treat your present self.
It is not about sacrificing fun now so that you can enjoy it later.
Rather, it is more like spreading the fun across your whole lifetime so that you can have fun any time you want.

Last week, the IPCC released a [special report](https://ipcc.ch/report/sr15/) on the impacts of global warming 1.5°C can have on our planet.
One of the battles we have had and continue to rage is the way in which people discount the future.
But I'm not here to [rant about people discounting the future](https://thespinoff.co.nz/politics/11-10-2018/step-one-accept-people-dont-and-may-never-give-a-toss-about-climate-change/).
I'm here to reframe it.

Yes, there is no reason we have to care about the future when we seem to have trouble with the present.
You're right, in fact, everyone is right about every opinion they have.

But you are blind, in fact every person on this planet is blind, myself included.
We think A needs to happen before B, because well, time dependency.

What if A doesn't need to happen before B?
What if governments don't need to get their shit together before we can do something about climate change?
What if you don't need to win the lottery in order to live a rich and meaningful life?
What if that new health or exercise habit you want to get into doesn't require you to purchase some superfood or gym membership before you can get going?

Is A dependent on B, or is A just a wall you think you need to climb over in order to see B happen?

## Call to action

No, I'm not necessarily asking you to [hold two opposed ideas in mind at the same time and still retain the ability to function](https://en.wikiquote.org/wiki/Talk:F._Scott_Fitzgerald#Quotations).
You can spend a day, or maybe just a quiet night, reflecting on what it is that you need to do to reach your goal.
Don't think about it step by step, see it as it is, as a whole.

If kids today can have their phone, tablet and laptop open and work at them all at once, it speaks of the ability of the brain to look at more than one thing at a time.
Personally as a tutor, I do wonder about students that play on their phones constantly in class.
But is it necessarily a bad thing?
Or is it just the older generation being a tiny bit jealous that they were not wired to multi-task?

The way to accomplish something great in a short amount of time is not to look at things sequentially, but by breaking down dependencies that are mere distractions.
In other words, understand how to look at the 'whole', and find a way to do things all in one go.

Respect the future the same way you would treat the present, that means taking care of your personal health, finances, the planet, everything (!) **all at the same time**.
They are not pieces of a puzzle you put in one by one as you see fit, they are all related to the core problem that is an unsolved puzzle.

What is this puzzle?

Have you found a creative way to solve it?
