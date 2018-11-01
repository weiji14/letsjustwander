---
date: 2018-10-23T16:43:00+13:00
title: Developing behaviours by starting with why
---

> In order to warn everyone about catastrophic sea level rise,
>
> As a scientist,
>
> I want to openly share a better map of what lies below Antarctica.

So I've been rambling on in my last few posts in a Zen/[Chan](https://en.wikipedia.org/wiki/Chan_Buddhism)-like trance, on **suddenness**.
Indeed, people really [shouldn't take it a step at a time](/three-box-carts-in-one), because [it's all in the mind](/throw-it-into-the-trash-icon) and there are [better ways to look at things](/time-as-a-whole-instead-of-sequentially).

Yet Chan is not just about emptiness, it is also about **balance**.

So today we'll take a step back, looking at the individual steps you can take to reach the holy grail.

Note that this is the culmination of the things I've been going through in the past two weeks or so.
There is a saying that doing a PhD is like running your own little company.
A PhD student is like the founder nurturing the initial spark of an idea, the worker who turns it into a tangible thing, and also the salesperson selling the benefits to humankind.

Let's first start with the biggest question - Why?

## Why why why

Go watch this great video on the [Golden circle](https://www.ted.com/talks/simon_sinek_how_great_leaders_inspire_action):

[![IMAGE ALT TEXT](https://img.youtube.com/vi/qp0HIF3SfI4/0.jpg)](https://www.youtube.com/watch?v=qp0HIF3SfI4 "How great leaders inspire action | Simon Sinek")

In the video, Simon Sinek tells us to start with the "Why?"
It is a compelling argument, driven not by psychology he says, but biology.
Starting with "Why" taps into the limbic part of the brain, and is said to overcome our modern neocortex.

It is not just a business thing though, I went to a workshop on producing an effective PhD thesis two weeks ago.
In it, one of the points made was to put all the good bits in the beginning of the sentence, at the start of the abstract, the first few chapters of your thesis!
Don't leave all the juicy parts to the end of the text, people want to know **why** your work is original.

It is almost a running joke in academia that you just need to skim the abstract and conclusions of a paper to get at the core idea being put forward.
Really though, you don't want to lose a reader by putting all your effort in the conclusion and writing your abstract at the last minute.
Capture the audience, put your best foot forward - in the beginning!

Besides business and writing, you also apply this line of thought to other fields!
In the personal finance world I sometimes blog about, you are often told to come up with a goal first.
Yes, set a goal before coming up with a budget or finding a financial advisor!

Not just any goal though, you need to think hard about **Why** you want to reach that goal.
The **How** you do it is simply maths and grit, and the **What** is the reason behind the dopamine rush when you reach that goal.

Did you know that there's even a formalized way to write it out?
I discovered this as I started creating unit tests and fell down a rabbit hole to...

## How - With a language called Gherkin

[Gherkin](https://en.wikipedia.org/wiki/Pickled_cucumber#Gherkin) - a pickled cucumber.
It is typically used for getting people on the same page.
Well, the [Gherkin language](https://en.wikipedia.org/wiki/Cucumber_(software)#Gherkin_language) rather, not the cucumber.

As a domain specific language ([translated to over 70 languages](https://docs.cucumber.io/gherkin/reference/#spoken-languages)), Gherkin is used for writing behaviour scenarios in '.feature' files with an intuitive syntax.
These '.feature' files are codified templates that can be understood by non-technical people, and used by technical people to guide their coding in [Behaviour-driven development](https://en.wikipedia.org/wiki/Behavior-driven_development).
See also [BDD101](https://automationpanda.com/2017/01/25/bdd-101-introducing-bdd/)(Python-orientated).

This is an example I came up with this morning for my current project:

```gherkin
    # language: en
    Feature: High Resolution Bed Elevation Model of Antarctica
      In order to have a better map of Antarctica's bed
      As a glaciologist,
      We want a model that learns from many open datasets  

      Scenario: See high resolution bed
        Given low and high resolution images of a bed
         When the user selects some view of Antarctica
         Then a high resolution bed elevation map is returned
```

The brilliant thing about this feature file is that it is high-level **and** spells out what needs to be done!

The 'Feature:' is basically the title.
Under it is context.
You will see that I've used something akin to the Golden Circle by starting with the **Why**.
Unlike the Golden Circle though, I put in the **Who** next, a hint at the importance of user-centric design.
Finally the **What** is spelt out, which is either a model, an app, a fancy function, or ... you get the idea.

The 'Scenario:' lays out **How** the feature works.
Under it is a Given-When-Then statement, a form of [Specification by example](https://en.wikipedia.org/wiki/Specification_by_example).
One way I think of it is as an input-processing-output pipeline.
*Given* some body of data or knowledge, *When* you are faced with something (the app has to act on this), *Then* an output is returned.

Take this as an opinionated starting template:

```gherkin
    # language: en
    Feature: <title>
      In order to ... <Why>
      As a ... <Who>
      I/We want ... <What>

      Scenario: <example>
        Given ... <input>
         When ... <something happens>
         Then ... <output>
```

If you want more examples, I find that the Python [behave tutorial](https://behave.readthedocs.io/en/latest/tutorial.html#feature-files) is one of the funnier ones, with ninjas!
It goes to show how people can use this in so many different ways besides its original use in Behavioural-Driven Development.
Why not make a few cards for a new habit you want to take up?

```gherkin
    # language: en
    Feature: Healthy Eating
      In order to live longer
      As a healthy person,
      I want to eat a balanced diet

      Scenario: Eating fruit
        Given a fruit bowl full of juicy fruit
         When the healthy person hasn't been any fruit eaten today
         Then there should be less fruit in the fruit bowl
          And some fruit in the healthy person's tummy
```

Alright, I am sort of (ab)using gherkin for purposes it wasn't designed for, and maybe breaking some standards to boot!
Go and read [how to write good gherkin](https://automationpanda.com/2017/01/30/bdd-101-writing-good-gherkin/) with proper grammar (e.g. the link recommends writing in third person instead of first person).
Or maybe follow some [good gherkin examples](https://automationpanda.com/2017/01/27/bdd-101-gherkin-by-example/).

We've now ran through a method of formally writing down something we want to do using Gherkin language.
So now what?

Did I hear "what's in it for **me**" you say?

## What's in it for me

It's easy to for anyone to argue on how to do things (implementation).
But it is much harder to argue about the why (principles).

By starting with the core **Why**, you deliberately make things as vulnerable/awkward as you possible could.
If it's a strong why, it stays.
If it's not good, people realize it immediately and you can correct the most fundamental problem before it's buried in layers and layers of subjective matter.

The **Why** should be made as clear as possible.
Over time, different people will have different interpretations on **What** it means and **How** we can use the message laid out by the why.
The use cases will change, technology will change, but a good **Why** should withstand the test of time.

For example, I went to a workshop on managing documents and data last Wednesday.

They started off with the **Why** of backing up - so that you don't lose your work in the event of some unexpected event like an earthquake.
This is something I've covered in my [geographical diversification](/geographical-diversification) post.

The **How** is the implementation.
Here already, we differ on opinion.
The workshop people recommended a particular cloud storage provider that is quite 'reliable', whereas I prefer something like git which is not tied to a provider.

The **What** is the benefits of using a proper backup solution, things like peace of mind, ensuring your work lives on, etc etc.

As I write this paragraph, the place where I publish my work (Github) is experiencing some [login issues](https://status.github.com/messages/2018-10-22) and people are fretting out about potential data loss.
Yes it's annoying but I'm not too fussed because I've got my continuity plans in place.
With two local copies of my work, I am able sync it to any other git provider if necessary due to git's [fungible](https://en.wikipedia.org/wiki/Fungibility) nature.

If I used what the people at the university recommended, and that provider were to fail, or if I graduate and get kicked out of the university system...
Yes I might still have my two local copies, but I'd have lost my version control, and it would take lots of time and effort to find another backup provider that does the trick.
During that time, who knows what might happen to your personal computer?!
With fungible git, I can simply add a new remote and push it up in a minute like nothing has happened.

By starting with the "**Why**", you get to know the fundamental reason.
"How" things are done can change, "Who" your users are can change, "What" they think about your idea/product can change, but if you have a compelling "Why", those differences won't matter.

Maybe ten years down the road, there will be an even better solution, a better **How** to do things.
Yet the **Why** of having a peace of mind with backups won't really change.
It might even be the case that **What** the new solution offers is even more comprehensive, more foolproof, something that would seem like magic to us today.

So who stands to benefit from this?
Is this just some propaganda to change all of our language into a strict monotonous template of Gherkin-like syntax?

## Who cares

### Hackers

I'll be honest with you, I'm a guy who likes a good howto article that gets into the nuts and bolts.
A blog post might have a **How**-What-Why structure and I won't bat an eye.
Like, just tell me how it works already!!
Perhaps the developers and engineers reading this will feel the same.

You could be a great engineer, or developer, or some hacker that brings a vision to life.
There is however, a possibility of over-engineering something.
You could go from bug-driven development to test-driven development to behavioural-driven development, and so on, but was all of that necessary?
Could you have designed something much more simpler and easier to maintain that [covers 80% of the use cases](/climbing-the-pareto-curve)?

### Testers

Strangely enough, the Gherkin syntax was borne from Behaviour Driven Development (BDD), itself an extension of Test Driven Development (TDD).
Testers are akin to users, they are effectively the ones using the product, discovering **What** it does.

You could be so user-centric, focused on your customer, at the expense of losing your sanity.
Sure, the customer is always right, but that doesn't mean the customer can call all the shots and break the law to get what they want!
I've worked in the service industry, and you do realize that there are some privileged customers who can feel so entitled as to wreak havoc on your day.
[They might not be satisfied](/from-first-world-problems-to-surviving-an-apocalypse) with what you offer, and you'll need to accept that.

### Visionaries

Doesn't this **Why**-first syntax seem like some push from business orientated folk with an agenda?
Why should we believe in their vision?
Sure, come up with a vision and have us all adhere to that, building your empire and using your goods.

For the businessman, or teacher, or whatever inspirational leader out there.
Sure, maybe it *is* too much of an ask for you to write in (good) Gherkin.
It's all too easy to send out a tweet or have a witty one-liner quote sent out, while your minions scramble to work on it.
I don't know what to say really.
Perhaps be careful of the ideals you are bestowing on the world, because [taking it to the extreme](/on-falling-down-the-optimal-rabbit-hole) can be dangerous.

### Hustle on!!!

It's easy to specialize into your own silos, I know.
Although you get some great people who can cover all three, or maybe two out of the three questions (Why-How-What) in detail, it's a rarity.

As an individual, I do find it tricky to balance all three.

Coming back to my PhD...
Some days or weeks I would just get so engrossed in coding, implementing cool bleeding edge stuff that few people on the planet have done before.
When it comes to writing, it can be scary to go deep into the "Why?" question, because it means a lot of soul searching.
Further down the track, I'll need to explain myself too, what I've done over my PhD, what it means for our world!

As I mentioned at the start, it's all about balance.

To strike that balance, you need communication.
Be it communication between your team members, or communication with the different parts of your brain that does different things, we all need to figure out how to join the dots.

At the end of the day, you need to get to the same page.
Start with the **Why**.
Hopefully you find the gherkin spec helpful in formalizing your thoughts.
As for what comes next, that's up to you to discover!

Get going!
