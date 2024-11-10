---
date: 2024-11-11T12:29:00+13:00
title: Foundational infrastructure to be serviced
---

I've done a lot of travelling this year, more than I probably should have.
They were mostly for 'work', some were conferences, others were team-bonding meetups.
Guilty as I already am, I've tried my best to combine some trips back-to-back, resulting in some unconventional layovers, probably worsening my carbon footprint as a result...

For some reason, the stops tend to be capital cities - Washington, Vienna, Lisbon, Singapore...
There was one main exception - Seattle which I've blogged [here](https://weiji14.xyz/blog/engaging-in-the-2024-uw-hackweek/).
That is sort of the impetus for this blog post, because of a conversation I had with an ex-colleague, whom I had a day before the actual Hackweek.

I won't bore you with all the geeky geospatial tech details we caught up on, there was one sentence really that summed it up:

> It feels as though we [*as a community*] are rushing ahead with [*AI*] Foundation Models, without developing the underlying standards first.

I've almost certainly butchered the exact sentence (because, old age memory), but the gist was there.
Put another way, most of the attention has been on the race in building the 'first' or 'best' model (possibly on some [sub-optimal metric](/on-falling-down-the-optimal-rabbit-hole)).
Only a few are spending time on standardizing things like the [MLM extension](https://github.com/stac-extensions/mlm) my friend has been spearheading (it is not a multi-level marketing scheme, promise).

For a naive few months last year, I did volunteer to help on that standardization initiative, but my efforts have since been sucked up battling another front.
Specifically, keeping the software or tools of the geospatial data science sector up-to-date (in the [conda-forge](https://conda-forge.org) ecosystem), and meagerly helping out where I am able to on efficient libraries (re-)written in Rust.
At the very least, I've gotten somewhat good at figuring out how to compile packages with CUDA and/or Rust dependencies.

Even with interoperable standards-based schemas and efficient libraries, that doesn't mean we're all set.
You may have heard of how policy and copyright law isn't able to keep up with advancements in Artificial Intelligence (AI).
Or how society as a whole, will need to figure out how it [educates its young, ensures careers for the able, and tends to the old](/three-box-carts-in-one).
I won't go into that because I'm neither a lawyer nor a social anthropologist.

What I am keeping an eye on is the [Hardware Lottery](https://doi.org/10.48550/arXiv.2009.06489).
This is rather eloquently described in a blog post series that ended on - [The Wall & The Machine: Accelerated hardware](https://voltrondata.com/codex/accelerated-hardware).
The risk is, that the way we've been designing software for the CPU these past few decades, might become moot as accelerated hardware such as GPUs (and eventually, quantum computers) become more common.

My secondary school math teacher summed it up real well: quick fish eats slow fish.

---

## What we need as a whole

> We forgot transportation as a whole.
> We only looked at the automobiles.
> Because of that, today, when we need them again, the road beds, the railroads are falling apart
>
>...
>
> Now as we come to the world of the micro-computer, ...
> I'm afraid we will continue to buy pieces of hardware, and then put programs on them,
> when what we should be doing is looking at the underlying thing,
> which is the total flow of information.
>
> ~<cite> Grace Hopper on [Future Possibilities: Data, Hardware, Software, and People (Part One, 1982)](https://archive.org/details/youtube-si9iqF5uTFk)</cite>

[![Thumbnail of Grace Hopper giving a lecture](https://img.youtube.com/vi/si9iqF5uTFk/0.jpg)](https://archive.org/details/youtube-si9iqF5uTFk "Capt. Grace Hopper on Future Possibilities: Data, Hardware, Software, and People (Part One, 1982)")

As we enter a world of accelerated AI, enabled by accelerated hardware, created by humans with an accelerated attention-span, we can't lose sight of what we are missing as a whole.

On information, are we improving on the signal-to-noise ratio as we soak in more stuff, or is it just more noise?
There is a running joke in the Numerical Weather Prediction (NWP) sphere that we are trying to get higher precision forecasts using low-precision numbers in AI/ML models.
The need for speed is in-part, leading to lower precision math, but are we sacrificing anything in this process of approximation?

On accelerated computing, are we so hyper-focused on the hardware and software, that we had forgotten about the electricity required to run it?
We simply cannot scale up on non-renewable energy anymore.
People have called out proof-of-work cryptocurrency's impact on the energy grid years ago, there is some, but less pushback on how training and running billion-parameter Transformer-based AI models is a huge energy drain too, presumably because it is seen as more 'useful' work.
AI is the new electricity, but are we regulating and managing it as such?

Going back to capital cities, you might know that I live in one, and we've been having this issue with water pipes bursting a few years now.
Many of these water pipes date back to the early 1900s, and are long past their intended use-by date.
It's a classic case of infrastructure being an after-thought, it is easier to sell something 'new', rather than selling a 'maintenance' service.

The water pipes have been hidden underground for ages, out of sight and mind, working more or less as they should be.
Until a series of strong earthquakes rocked the city a few years ago, causing micro-fractures in the pipes.
Small leaks gradually become worse, I see them practically every time I walk into the city, they emerge on pedestrian sidewalks, sometimes literally in front of stores or apartment buildings.
A reminder of the fragility of the ground we walk on.

I see some parallels here.
As we engineer the infrastructure for accelerated AI, will there be an 'earthquake' in the future that will cause the pipes to 'burst'?

Are we designing for resiliency and repairability?
If it becomes critical infrastructure, are there fallbacks or substitutes in place?

Do we focus on the can-haves, or think about the could-lose?

You can pay for the feature now, but what of the service later?
