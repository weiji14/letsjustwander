---
date: 2018-09-10T11:10:00+12:00
title: On falling down the optimal rabbit hole
---

What are we optimizing for?

Is the act of optimizing actually a distraction?

Here's why we need to be careful about systems that have an optimizing effect.

Back when I was in my corporate job, we had this tool called time tracker.
The names speaks for itself I guess, it tracks the time we spent on our project(s).
We're meant to complete it by the end of each month, ideally every end of week or everyday if possible.

When I first started on it, record-freak me thought:
"Yay, I can jot down notes on what I'm doing everyday!"
The enthusiasm died off after a couple of months though.
In fact, you could say that almost everyone hated it even though it was a necessary evil.

Why?
Well, the hours we record down translates to the hours we charge our clients.

The developers amongst us used to have a running joke that we have this random generator that can automatically fill in time tracker for us.
Middle management would remind us to keep it up to date at the end of each month.
It's the last thing on Friday afternoon lying between my office hours and personal time.

Just before I left, the new management team had this order that we should fill in **everything** that happens during our office hours.
Sure, we used to have to include meetings, but even our lunch time now?
And then there's leave - we now had to record down the time when we're not even in the office!
Sick leave, annual leave, ...
You go away to rest and come back having to fill up those time slots.
A colleague lamented how they'll probably want our toilet hours next.

It could be worse.
We could have used [punch clocks](https://en.wikipedia.org/wiki/Time_clock).

Minor annoyances aside, the thing that really bothered me was what the time tracking system rewarded - time [spend/wasted].
Say person A takes 3 hours to do one task, and person B takes 5 hours, does that mean we get to charge the client more by using person B?

The system doesn't reward efficiency.
Yes, it makes it 'easy' to invoice the clients, but there's no inherent push to modernize the way we do things.
I could have an automated script that takes 3 days instead of 2 weeks to run something, but there's no real motivation for me to do so other than the fact that it's boring stuff that should be automated anyway.

So what metric should we have gone by?
Number of git commits?
Lines of codes written?
Bugs/problems resolved?

Well, no matter what you pick, a system with an optimizing effect will have unintended consequences.
But how can we bill people if we don't even have some hard numbers you say?!

The simplest way is to not have clients.

The more intricate way is to be in a quantum indifferent state.
Your client exists and does not exist, so how do you invoice and not invoice?

Set a fixed price?
If there's a client, they pay; if there's no client, the price is not paid.
If we finish the job early, we gain; if we take too long, the client gains.
How do you make an estimate for a big project?
Is it true that this project has a big scope or was it just overthinking?

You see, there's an infinite number of solutions.
You can pick one and be done with it.
Time tracker might not have been the perfect solution, but it is *a* solution.

Or, you can perform a meta analysis.
An optimizer for the optimizer.
Out of the many solutions out there, is there a higher level system that can optimize us to the right one?

---

When you look at an online shopping catalogue, you'll often find the items sorted into categories.
You might spend a second or two thinking about the category for the item you're trying to find.
Then you'll spend a while fumbling to reconcile the category you thought up and the category that online shop actually sorts its items by.

Categorization in a sense is a distraction.
Some view it as a necessary evil, but I like to see it with an extremely shortlived purpose.
It is like wrapping paper to a present - a layer often simply discarded to get to the exciting thing inside.
Do you remember the color or design of the wrapping around your last birthday present?
Probably not.

What you'll usually end up doing in the online shopping problem is to just input the name into the search bar and be done with it.
Or you might have just used that name in the search engine and that would take you directly to the page too.

There's a whole art dedicated to it actually, called [Search engine optimization](https://en.wikipedia.org/wiki/Search_engine_optimization).

Is that the quickest way though?
No!
If you're good, you'll just type the whole website out.
If you're legendary, you'll figure out the exact IP address and bypass the DNS!

Once again, [the art of] optimization isn't *it*.
Say you're trying to get somewhere, or help someone to get there.
You could labour over deciding which search term he/she should use, what technique best suits so and so personality, or create a treatment plan that solves this and this symptom.

Yet you're not dealing with the root cause are you now?
Why [treat the symptom instead of the cause](https://rationalwiki.org/wiki/Treat_the_cause,_not_the_symptom)?

If finding the true cause helps you to solve the problem.
Do you:

- A) Find each and every way to arrive at that root cause, perhaps categorizing each technique while you're at it in case a similar problem pops up in the future.
- B) Just focus on the ultimate root.

---

I'll be honest here, this post is just me procrastinating from my actual research :P

In [mathematical optimization](https://en.wikipedia.org/wiki/Mathematical_optimization), there is a problem of falling into a local minimum rather than the global minimum.
Basically, you slide down the wrong [rabbit hole](https://en.wikipedia.org/wiki/Alice%27s_Adventures_in_Wonderland) and can't climb back up to get into the right one (the deepest rabbit hole).

Theoretically, there is one global minimum.
Think of it as the one rabbit hole that you want to fall into, because it gives you the most satisfying Alice in Wonderland-type experience.

Getting there can be done.
Sometimes you'll accidentally get stuck in local minima because the rabbit hole happened to be very enchanting.
Try to realize as soon as possible that it's not what you're after.

I'm working on a model, and there is a saying that:

> "All models are wrong; the practical question is how wrong do they have to be to not be useful."
> 
> ~<cite>[George Box](https://en.wikipedia.org/wiki/All_models_are_wrong)</cite>

Specifically, it's to do with my Geography PhD project.
The thing about the models we use in geography, or earth sciences in general, is how they can be tuned to be accurate for a region but not for another region.
In technical terms, you could optimize a model into a local minima in the parameter space (and make it work well for your geographical domain).

To use an analogy, think about weather forecasting models.
You could take a model that works (nearly) perfectly in one part of the world, but throw that model into a different hemisphere, maybe a different continent, and it won't be as accurate.

Fundamentally, you would think that the laws of physics are the same right?
It's not as though physics works differently in the North compared to the South.

In practice, one of the reason we do this is because of something called 'good enough'.
If we only need a tropical cyclone forecast for the Southern Hemisphere, do we need a model that states that cyclones rotate the other way in the Northern Hemisphere?

On one hand, it sounds like cheating.
On the other hand, you could also call it optimizing, albeit for a local minima in the parameter space.

I could be working on solving a problem on one area in the [Amundsen Sea](https://en.wikipedia.org/wiki/Amundsen_Sea) sector, but that might not work for the [Weddell Sea](https://en.wikipedia.org/wiki/Weddell_Sea) sector because of some different geology, different ice density, different [boundary conditions](https://en.wikipedia.org/wiki/Boundary_value_problem).
Again, the physics ought to be the same, why shouldn't the model be too then?

Can we take all [the data] that we have, and throw it into a [Universal function approximater](https://en.wikipedia.org/wiki/Universal_approximation_theorem) to simply get at the underlying gist?

---

Be wary about what it is you're optimizing, be it for maximum income, fame, quality of life.
Also, be careful of the optimizing tool you may be consciously or unconsciously using, be it some mathematical model, a computer app, or some system you're in.
Trust me, you don't want to fall down the wrong rabbit hole and be stuck there for too long.

> Far better an approximate answer to the right question, which is often vague, than an exact answer to the wrong question, which can always be made precise.
>
> ~<cite>[John Tukey](https://en.wikiquote.org/wiki/John_Tukey)</cite>

Now let's start optimizing, correctly.