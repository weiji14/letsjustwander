---
date: 2018-10-06T21:11:00+13:00
title: Throw it into the trash icon
---

> Data is my sutra
>
> Algorithms are my perceptual understanding [of *it*]
>
> If the data changes, so does the algorithm's parameters
>
> What then can I not fake?

I've talked about [falling down rabbit holes](/on-falling-down-the-optimal-rabbit-hole/), and I've talked about [climbing steep curves](/climbing-the-pareto-curve/).
I've mentioned how [struggles are personal](/the-struggle-that-is-personal/), and that you're better off [telling someone about it](/you-know-what-to-do-so-tell-me/) to clarify your thoughts.
I've also told you the [fallacy of taking it step by step](/three-box-carts-in-one/), and how shitty it is to have to well, [deal with shit](/giving-people-shit-to-step-on/).

Now let me tell you to disregard all of that by throwing everything away.

Do you think you know what you're writing?

[Throw](https://github.com/weiji14/cryospheric-data-lakes/commit/df48c3ac9df2bbbc83d6a638aac547f293a5ddce) [it](https://github.com/weiji14/cryospheric-data-lakes/commit/e0e6cf502c03ec9f6965538c327fead3cedf4f3f) [all](https://github.com/weiji14/cryospheric-data-lakes/commit/c1a2f58a914779d6139e58cfb220dd9ac8fa6fc5) [away](https://github.com/weiji14/cryospheric-data-lakes/commit/8985ee01edc6fb6d67a7bd8f058c6e7b9d1806ff).

Do you think your $100k or $1 million is a lot?

[It doesn't matter](https://halflifetheory.com/the-fire-hamster-wheel-the-sad-truth-about-pursuing-financial-independence/).

Do you think you know reality?

[Question it](https://arstechnica.com/science/2018/10/ars-on-your-lunch-break-have-you-ever-questioned-the-nature-of-your-reality/) and [dump it](https://arstechnica.com/science/2018/10/ars-on-your-lunch-break-nothing-is-real-except-for-object-impermanence/).

Seriously, it may *feel* hard to let go of some object in your possession, some literary work you've written, or some understanding you've gained from a subject.
But **throw it** into the trash can anyway.

It could be some medal of honour, a life changing book, or it could be some pride from an achievement.
That however, still does not mean you're better than most everyone else, smarter than average, or deserving of some lofty title.

There is this story which Master Hsing Yun tells of his ordination ceremony.

---

When I received full ordination at the age of fifteen, I got a taste of what it means to have to take the inhumane as humane, and the unreasonable as reasonable.
My ordination master asked me whether I had killed any living beings.
I answered, "No!"

Suddenly, a large willow branch struck me on the head.

"Am I to understand that you haven’t killed any mosquitoes or ants?"

I quickly changed my answer, "Yes, I have."

Suddenly, the willow branch struck me again, because killing living beings is wrong.
The ordination master then asked me whether my teacher had told me to come to the ordination ceremony.
I answered, "I came on my own."

I was struck a third time.

"Your teacher didn’t tell you to come? So you decide things all on your own? That deserves punishment!"

I accepted the reprimand with humility, and then answered, "It was my teacher who told me to come."

"So if he didn’t tell you to come, you wouldn’t have done so?"

Then I was struck for a fourth time.

...

If I gave a reason, I would get three whacks, but even if I gave no reason I would get three whacks.
The willow branch had beaten away all pride and obstinacy and transformed me into a person who could act without a "self." When we think that we clearly understand something, know it in our heart, and that we’ve realized the Way, we end up with fixed ideas and preconceived notions about everything.
We start to compare our knowledge and our practice with others, trying to see who comes out on top.
This is when knowledge becomes an obstacle for us.

---

You can read the full story from the source [here](https://web.archive.org/web/3/https://hsingyun.org/prajna-lifes-secret-ingredient/), though try not to dwell on it.

I do not know how many of you have ever experienced the pain of 'throwing away'.
I'm not talking about the rubbish you throw away every once in a while.
It's something that lies closer to your heart.

For almost eight months this year, I was writing my PhD project [proposal](https://github.com/weiji14/cryospheric-data-lakes/blob/doc_proposal/docs/project_proposal.pdf), and experienced something akin to the beating described above, albeit in a mental form.
There were pages of material I would spent weeks writing, only for my supervisor to cross it all out.

The first time was perhaps the most painful, I was told that ~2 A4 pages 'could perhaps go into the appendix'.
Actually, I didn't bother with the appendix, I just deleted them all.

The second time was still painful, as I thought I had what was an exciting research question that would be groundbreaking.
Again, my supervisor told me to leave out that entire ~1 A4 page section, saying it might be better for a postdoc.

Going into the final few drafts, there was a notable quote/sentence I resisted discarding, and also other rough edges, but I was used to the 'pain' by then.
Yes I could argue (and I should!), yes I could hold on to my pride, but at the end of the day, it doesn't matter.

I'm not even going to say why it doesn't matter.

All I know is that I started off like a cube, and as I roll along in life, my sharp corners gradually get worn down.
The resistance I feel are the sharp corners bumping against the ground.
I want to roll, I don't want to just stay where I was, and yet I foolishly hold on to those sharp corners thinking they are a part of me.
They're **not**.
In fact, the cube isn't the 'me' I wanted to be, I need to be a sphere that can roll smoothly along life.

You might think that surely there are right and wrong answers.
Or at the very least, answers that are more right or more wrong than others.

Yesterday morning, my supervisor and his students were discussing the stuff we've been doing this week over coffee.
I've been working on this [issue](https://github.com/weiji14/deepbedmap/issues/21) of pulling in a fairly big radar dataset and was seeing these crazy elevation surfaces from doing an ordinary [inverse distance weighted](https://en.wikipedia.org/wiki/Inverse_distance_weighting) [spatial interpolation](https://en.wikipedia.org/wiki/Multivariate_interpolation).
My supervisor recommended me to do a [spline interpolation](https://en.wikipedia.org/wiki/Spline_interpolation), which would require modifying my pipeline to use a different piece of software since the current one I had was fairly basic.

In other words, I was meant to throw out a good part of what I've designed up until now for the sake of getting a 'better' answer.
\#science.

For about two hours, I actually seriously considered that thought, to redesign/throw out what I had done!
I looked up the recommended software (which I've used before, just a newer version now), and figured out a way to swap out the interpolation component.
Already, I was so used to tearing things down and going back to the drawing board that I didn't really feel the pain.

Before I did that system redesign though, I decided to check the interpolated elevation surface one more time.
I changed the colour scheme to match a reference surface, and instead of getting negative numbers (bedrock elevation), I saw positive numbers.
It turns out I [missed out on a simple calculation](https://github.com/weiji14/deepbedmap/commit/ebcb85a7193d010dfdd974aa312f08ba91fa85e5)...

So crisis averted for now, but I do think I'll need to revisit the fancier interpolation scheme at some point in the future.

Wait, isn't this counter to the 'throwing out' mantra I've just been preaching?

No!
I was going to throw out my original design, so I thought up of a new one.
But then I realize the new framework wasn't necessary (yet), so I threw that new framework away too.

It sounds like I haven't changed anything, but in fact, I've 'thrown away' twice!

That's absurd!
Yes!
No!
Who cares?!!

It's all in the mind, it is the mind that is playing with you.

It is said that [reality isn't](https://after-on.com/episodes/026).
Taking something seriously doesn't mean you have to take it literally.
We evolved evolutionarily to simplify reality.
The trash icon on our desktop doesn't mean there's a literal trash can inside our computer.
Think of the app world, all the services we have one icon click away, all of them are abstractions.

To transcend reality, you have to look past simplification, look past your biases.
Think hard about what *is*.
Throw it away, then think, then throw it away again.
Repeat for n times until you finally get *it*.

Seeing the real truth costs energy as it is going against the grain.
You are sacrificing mental energy now for enlightenment later.

Do you want to be stuck in a cycle, or do you want to break away from the cycle?
Do you believe in science, or do you believe in yourself?

In a [Thin Ice](https://en.wikipedia.org/wiki/Thin_Ice_(2013_film)) film panel yesterday after the coffee meeting, there were a few questions on dealing with climate deniers
People who latch on to little factoids instead of full facts.

It's easy to tell so and so someone that they are wrong.
But it is harder, painful even, to round the rough edges that we have on ourselves.

Enough convincing, enough resisting.

Just throw it all and set fire to it all!
