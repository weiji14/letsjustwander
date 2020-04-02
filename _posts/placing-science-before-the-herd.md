---
date: 2020-04-03T00:10:00+13:00
title: Placing science before the herd
---

> It ain't what you don't know that gets you into trouble.
> It's what you know for sure that just ain't so
>
> <cite>[Mark Twain](https://en.wikipedia.org/wiki/Mark_Twain)</cite>

Yes I'm alive, and so is this [disaster proof blog](/on-your-markdown-hypertext-now!) (which after re-reading it, seems *so* apt in this [covid-19 pandemic](https://en.wikipedia.org/wiki/Coronavirus_disease_2019) era).
The past three months has been historical to say the least, and while I've been fascinated by how it's all played out, I've also taken my sweet time before adding my perspective into all the noise the world is generating.

For background though, here are a couple of rabbit hole articles worth a read:
- [The Hammer and the Dance](https://medium.com/@tomaspueyo/coronavirus-the-hammer-and-the-dance-be9337092b56) ~ by [Tomas Pueyo](https://medium.com/@tomaspueyo)
- [Smarter COVID-19 Decision-Making](https://towardsdatascience.com/smarter-covid-19-decision-making-39dbff2ab2ba) ~ by [Cassie Kozyrkov](https://towardsdatascience.com/@kozyrkov)

It's also interesting how, as more information comes in and is acted upon, the language we use as a progressive society to describe some matters has evolved.
Great to see the [WHO](https://en.wikipedia.org/wiki/World_Health_Organization) taking a stance on 'proper' naming, e.g. [from 2019-nCoV to SARS-CoV-2/Covid-19](https://en.wikipedia.org/wiki/Coronavirus_disease_2019#Terminology).
Some might say that names, and the subjective meaning behind certain words, have an influence on people's perception, which has resulted in shifts:
- From [#FlattenTheCurve](https://thespinoff.co.nz/society/09-03-2020/the-three-phases-of-covid-19-and-how-we-can-make-it-manageable) to [#StopTheSpread](https://thespinoff.co.nz/society/14-03-2020/after-flatten-the-curve-we-must-now-stop-the-spread-heres-what-that-means/), to ... #StampItOut?
- From [social distancing](https://en.wikipedia.org/wiki/Social_distancing) to [physical distancing](https://www.who.int/docs/default-source/coronaviruse/transcripts/who-audio-emergencies-coronavirus-press-conference-full-20mar2020.pdf?sfvrsn=1eafbff_0) to emphasize the need to physically stay out of people's [bubbles](https://thespinoff.co.nz/covid-19/01-04-2020/siouxsie-wiles-toby-morris-why-those-bubbles-are-so-important)!

![Stay in your bubble, keep others safe](https://thespinoff.co.nz/wp-content/uploads/2020/03/Covid-19-Bubble-spread-02-1.gif)

I'm not an epidemiologist, nor an expert in any field of health science.
The problem is, most of you reading this aren't either (but if you are, big shout out for all your hard work! Remember to wash your hands after using your phone, and go on forth to save some lives!).

Yet somehow, you're still reading this, and probably trying to relate to it, getting some comfort out of the fact that:
"Hey, there's another random person on the internet who doesn't know what's going on, I can relate to that!".

Erm, well, do you, do you really?

It takes a lot of energy to fact check things, and I can see why a lot of people don't bother unless they have a strong stake at hand.
In many cases, we'll make do with:
"A trusted source says *x*, so *x* should be true".
Pardon the pun(s), but trust in this type of system relies on a reliable chain of transmission, and while it's easy for things to go viral nowadays, it's crucial that we can trace the link back to the source.

Wouldn't it be great if we could find patient zero, and establish a link from him/her to every other close contact to identify possible infected candidates?
Similarly, is it to hard of an ask, for people to link back to the official source of information (e.g. the Ministry of Health, some scientific paper), so that we couch surfers can do some fact checking?

I tried to do a bit of a fact checking myself the other day, looking at a published [white paper on the covid-19 modelling used to determine the potential worse case scenario in New Zealand as of 24 March 2020](https://www.health.govt.nz/system/files/documents/publications/report_for_chief_science_advisor_-_health_-_24_march_final.pdf).
Maybe I was expecting too much, but there was only one figure with a single blue line showing a peak, and a table of parameters fed into the 'model'.
To be honest, I was slightly disappointed, expecting some error bars or multiple scenarios being plotted, but I guess it was just meant for policy makers that are after the 'worst' case.

So I did some digging today for this blog post, and it took me a few minutes to find a slightly better [preprint article](https://doi.org/10.1101/2020.03.20.20039776) by the same University of Otago team.
Also managed to track down the model used, called CovidSIM (which you can interact with [here](http://covidsim.eu)).
The source code for it is hosted on GitLab [here](https://gitlab.com/exploratory-systems/covidsim), and I think I'll stop at that and call it a day.

Phew.

Sure, it didn't seem like a lot of effort to do a bit of a [DuckDuckGo](https://ddg.gg) search.
But the point is, there should not be an unbroken link between the 'fact reporting' and the 'data source', and I would argue too that the 'model' here is just as essential.
Links are cheap, and like, they're the entire basis of the internet!

What does it say about the credibility of an article, if you have one that links to a reputable scientific source, and one that just has a bunch of anecdotal interviews?

Especially in times when lives are at stake, we need to make sure that the facts are backed up by proper science.
If somehow you are using herd immunity as your strategy, well, at least people can review things to see if it actually works in this setting (tldr: it doesn't).
So please link back to a reputable source, don't make people like me suffer the pain of taking 10 minutes out of their lunch break to search for some preprint or journal article that clarifies the science.
At the very least, give people a nice rabbit hole to fall into.

Some people might just see the same information from various media outlets and assume that the 'herd' is right.
But really, what if they aren't?
Hence the need to link back to the original source.
We should be able to examine the assumptions being made, and rather than reinforcing herd behaviour, we should enable knowledgeable people to speak up on discrepancies, and correct them in time.

---

> [First they came](https://en.wikipedia.org/wiki/First_they_came_...) for the socialists, and I did not speak out—
>
> Then they came for the trade unionists, and I did not speak out—
>
> Then they came for the Jews, and I did not speak out—
>
> Then they came for me—and there was no one left to speak for me.
>
> <cite>[Martin Niemöller](https://en.wikipedia.org/wiki/Martin_Niem%C3%B6ller)</cite>

Next is on understanding exponentials, like really, be afraid of it.
It's also mixed in with a chronicle of my first quarter of the year 2020, so sit back and read on.

I flew to China on Sunday the 19th of January, and back then, I had the fortunate luck of purchasing an N95 mask before I went there.
No, not for the coronavirus, it was because I was transiting in Sydney and the [bushfires](https://en.wikipedia.org/wiki/2019-20_Australian_bushfire_season) was still a thing...

The mask was quite expensive, and I didn't find the need to use it inside Sydney airport, but I kept it and flew on to Shanghai.
The flight was delayed (I remember being on the tarmac for maybe 2 hours before we got to take off), and I arrived kinda late at night.
Fumbled through customs, and had a bit of a problem without wifi, trying to purchase duty free goods.
Thankgoodness I knew Chinese, got a SIM card (expensive lesson) and sorted things out.

My partner was there to greet me, and also her sisters (well, cousins), and I don't recall anyone much wearing a mask at the airport.
We went to their place by car, and I admired the night scenery, it's been 16 years since I last came to China, first time in Shanghai though.

The novel coronavirus (as it was called back then) was just starting to receive more attention on the news.
I went out the next day wearing a mask, though it was more for the air pollution...
My partner had kicked me off the subway a stop before her workplace's stop, so I navigated my way to the police station to register my details.
Ended up only needing to scan a QR code and fill in an online form.

Any other day now, I would have thought "Could have just stayed at home...", but it was nice exploring a bit of the city by myself.
The phone is an essential device.
Successfully used the local GPS app, bought a subway ticket home using Alipay (look, no cash!), and for lunch, my partner ordered a delivery for me which I only had to open the door for.

Like I knew how advanced China was already before I came, but feeling that level of convenience first hand, is awesome!
"I could really get used to this", I thought.

The next two days, 21 and 22 Jan, we went shopping for Chinese New Year stuff.
Already then, the novel coronavirus was getting serious attention.
The change was as sudden as can be, masks were sold out everywhere, pharmacies putting up signs so that you didn't even have to ask.
We kept ours on all the time, save when we were eating.
My N95 mask got its first use around then.

On 23rd Jan, [Wuhan went into lockdown](https://en.wikipedia.org/wiki/2020_Hubei_lockdowns).
Early in the morning, I was on a high speed train with my partner heading to a city about 500km Southeast from there.
Practically everyone was wearing a mask, and no one questioned it.
My partner's mom and uncle picked us and her sister (cousin) up, and we drove about an hour or so to their apartment.

That night, we went out to a big dinner at a restaurant.
My partner insisted that we wore masks on our way to and from there, and I didn't question it.
Lots of food (like really, loads!) were had, and so was alcohol, and smoking indoors (somethings have yet to change in parts of China), but overall, a very nice experience.

Chinese New Year's eve, 24th Jan, we went to her grandmother's place in the village.
Most of Hubei province was put into lockdown.
It seemed as though everyone in the country was talking of the novel coronavirus by then, news coming in in realtime on their phone apps.
We got to the village with no hiccups, had a nice reunion dinner, and so on.

Chinese New Year, 25th Jan, the restrictions started coming in hard and fast.
On our way to pick up my partner's dad a few hours' drive away, we were stopped by police at the highway toll, our temperatures taken, some questions asked about where we came from and where we're going.
You could sense the seriousness of the situation, limiting Chinese people's movements in China during Chinese New Year?
Not something you hear about in history books.
Me?
I was probably more nervous about meeting her dad.

In less than one week, the government had closed most public attractions and strongly discouraged households from meeting each other.
So I stayed at the village house, making dumplings, watching movies on an iPad with my partner, and really, just passing time.
The news seemed to be getting worse, and my parents in Malaysia started to worry.

On Tuesday 28th Jan, we went back to my partner's mom's city, where we stayed for another two nights.
Only went out once to the supermarket, masks are a must now, and so are gloves!
Hand sanitizer is starting to run short in some places, didn't even think about toilet paper (probably plenty, hoarding it wasn't a thing yet), otherwise they seem quite well stocked.
At home, we played cards, made more dumplings, and I got the question grilling from her dad (finally?)!

Took the high speed train back to Shanghai on 30 Jan, N90 mask check, disposable gloves check.
There weren't many passengers, as the national holiday was extended by a week.
We stayed at home, ate our instant noodles (fancy ones) and spent our last bit of quality time together before my flight.

31st Jan, evening.
We took the monorail to Shanghai Pudong airport, relatively few people on the streets.
The sky was clear that day, so much that you could make out some stars, guess air pollution really went down.
Temperatures were being taken before people could enter the airport.
It was a strange farewell.

I didn't really want to go, even with the virus and all that.
China outside of Wuhan still felt relatively safe, with hospitals being built in 10 days and all the measures in place.
Staying at home wasn't much of a big deal, with fast internet and delivery.
Besides, my partner was there, and it would have been nice to stay together.

Fast forward over February, where I was forced to stay in Malaysia for 2 weeks as countries restricted travel to those who were in China in the last 14 days.
I had 2 flight ticket changes, oh the drama.
Went through Singapore, (originally supposed to be in Brisbane, then Sydney, then...) Bali, and then Auckland, before arriving in Wellington.
I wasn't required to self isolate, so were the rules back then, as I was already 2 weeks outside of China.

The folks at my research centre knew about the Covid-19 news, but it still seemed like a distant thing for them.
"Oh yeah, it's just like the seasonal flu".
Life seemed to be fairly normal where I was, even as Covid-19 cases started popping up over Southeast Asia.
I knew trouble was coming, and rushed to get my paper ready for submission, while having to deal with my supervisor and his ideas about next steps in my thesis.

As more border restrictions were put in place, you could hear the university people lamenting the loss of their beloved Chinese international students.
Then sometime around late Feb/early March(?), South Korea, Italy and Iran become hotspots, and there were those cruise ship sagas...
The dialogue in the 'Western' world was still quite different, masks were practically shuned upon, and action was slow.

It only takes a week.
The world should have been prepared, but it wasn't.
Towards the end of March, more and more cases started to pop up in New Zealand, a faraway island in the corner of the world.
I could almost swear that in those early days, official case numbers were doubling every 2-2.5 days.
The exponential was coming in swiftly.

The panic buying started.
People scrambled to learn how to work from home.
Others like the restaurant I work at saw customer numbers drop to negligible amounts.
Either way, I knew what was to come was inevitable, I just hoped it would come sooner.

Lockdown, set for Wednesday 25 March 11.59pm.
I was in the office on Monday when it was announced, and to be honest, I didn't plan on coming in Tuesday anyway.
That evening, my restaurant boss invited me to go and pick up some veg from the restaurant, which was great as my Sunday market shopping was limited.
No way was I going to head out for a week at least, not until those mobs calm down.

Now it's just over a week into the Level 4 lockdown.
Looking back, I do feel fortunate that I got back to NZ in time, and though the tickets were expensive, they would be nothing compared to now.
Even luckier, I went out shopping on Tuesday and didn't have to wait in a queue at two different grocery stores (not telling you which)!

But I'm not going out for another two weeks, not even for 'exercise'.
Like, I don't see what's wrong with just staying at home.
Maybe that's just introvert me, but I've settled in quite nicely now.
I've seen what it's like in China, and I know it's a long game, considering that parts of Hubei province just exited their lockdown on 25 March 2020, about 2 months in total.

Yes I have the good fortune to be able to continue my research at home with a room to myself.
Yes I have a proper emergency fund to last me at least 3 months, which in reality could stretch out to 6 months or so since my stipend is still coming in.
Yes I have stocked up with a big 20kg bag of rice (bought prior to any suggestion of a lockdown), dried chickpeas, frozen veg and whatnot.

I don't want to list down every privilege I know I have.
What I do want to say though, is that while some things may not be under my control, the ones I can control are exercised.
Alone, I can't control herd behaviour, but I can avoid the herd, and not be a part of the herd.

It's possible to be prepared, both physically and mentally.
Stick to the science, rely on a bit more of technology, and stay safe.

Out there, it's a wild world.
Inside, is where you'll find bliss.
