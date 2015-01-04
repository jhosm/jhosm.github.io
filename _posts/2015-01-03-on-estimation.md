---
layout: post
title: On Estimations And The Need To Foretell The Future
comments: True
---

The desire to foretell the future is probably as ancient as the human race. We are still lousy at it. Yet, we need to do it all the time. When embarking on a project and, indeed, while it lasts, for instance. Here are some of my reflections on this devilish hard subject, with some [outside help](http://www.infoq.com/articles/software-development-effort-estimation).

---

Will I be rich? Will I be healthy? Will I find love? Shall I go to war? Should I make peace? Soothsayers, oracles, diviners.... even in our time, they are everywhere. It is said that many [powers-that-be do not make decisions before checking if the time is propitious](http://www.economist.com/news/obituary/21630948-joan-quigley-astrologer-reagans-died-october-21st-aged-87-presidents-stargazer). I was once told about a doctor that would see a soothsayer to know about her future health. I live in Lisbon, Portugal. I believe that there isn't a single windshield in this city that hasn't been graced with a flyer from "Professor Bambo", who can divine your future and cure all ills.

Why is that? Why do we have this urge to know our own future?

I once read a book by a philosoper (can't remember the name, but it must have been french) that engraved a thought in my mind: "The difference between humans and the rest of the animals is that we know there is a tomorrow". It's a powerfull thought. Without this crucial idea - there is a tomorrow - why would we be interested in anything besides finding food for the next few days (or winter, at the most)? Why would we care about the future? There would be no civilisation.

> "The difference between humans and the rest of the animals is that we know there is a tomorrow."

So... there is a future. We need to plan for it. Ok... but where shall we invest our time and resources? How do we know the grand plan (vision, mission, project, whatever) we have is worth it? There's lots of things to consider, but there's one question that we always have to answer: how long will it take? Another important characteristic of humans is that we know we're going to die. We can't wait forever.

Back to the main thread. How long will it take? ... That frightening question. "Dad, how long until we get there?" How I understand my parents now!

Do you see how I digress to run away from the answer? Almost 400 words before I start tackling it. But tackle it I must.

Let's start by narrowing it down to software projects. Sorry to disappoint you. You might have been expecting to get an all-encompassing answer. Were you?! Didn't you read the beginning of this rambling? We are trying to do it since we exist and we haven't succeeded yet! So bear with me. Software projects for now. And it won't be pretty.

Fortunately I have help besides my own experience to try to give some helpful nuggets of information. I recently read (again...) an excellent article by Magne Jørgensen titled ["What We Do and Don't Know about Software Development Effort Estimation"](http://www.infoq.com/articles/software-development-effort-estimation). It's a summary of research on the subject of estimation. Go read it if you have the time! If not, I'll give you a (not so) short summary, along with my ramblings. The article states that:

> "Overwhelming evidence documents a tendency toward cost and effort overruns in software projects. On average, this overrun seems to be around 30 percent. Furthermore, comparing the estimation accuracy of the 1980s with that reported in more recent surveys suggests that the estimation accuracy hasn’t changed much since then."

## Things we know

Magne lists a few things we know. Let's go over them one by one, as they are quite insightful.

__"There Is No “Best” Effort Estimation Model or Method"__. Several studies compare different approaches but, alas... they reach different conclusions. This resonates with my own experience. There are just to many inter-related variables. The team size, the project size, the team experience, the time the team has been working together, the business context, the stakeholders commitment... I could go on and on and on...

Magne says that this explains why "statistically advanced estimation models" are not much better than simple estimation models. Context is king. Even so, take a look at ["#NoEstimates Project Planning Using Monte Carlo Simulation"](http://www.infoq.com/articles/noestimates-monte-carlo) (and the comments).

__"Clients’ Focus on Low Price Is a Major Reason for Effort Overruns"__. I especially like this one, because it's so self-defeating. It's not that cost efficiency is a bad thing per se, it's a crucial aspect of running a business. But if we overdo it (e.g. bidding rounds), someone will suffer: the client or the supplier. Magne also mentions that in-house projects do not usually have this problem, but they can have the opposite: a bloated project. Yup... I've seen (and been in) both situations.

__"Minimum and Maximum Effort Intervals Are Too Narrow"__. [Three-point estimation](http://en.wikipedia.org/wiki/Three-point_estimation) is a popular technique: it's simple to grasp and intellectually appealing. We choose the minimum, most likely and maximum effort values, apply a simple formula and get a number. Research says that it's not completely bogus, but that it's only adequate when we find the minimum and maximum values based on historical data, not on expert judgement.

__"It’s Easy to Mislead Estimation Work and Hard to Recover from Being Misled"__. My favorite. I find that the mechanics are closely related to the client's focus on low price. Expert judgement (or the closest to it) is applied in every estimation method. The problem is that expert judgement is easily influenced. Quoting Magne:

> "Perhaps the strongest misleading happens when those responsible for the effort estimates, before or during the estimation work, are made aware of the budget, client expectations, time available, or other values that can act as so-called estimation anchors. (...) Expert judgment can also be misled when an estimation request includes loaded words, such as, “How much will this small and simple project cost?”"

The worst thing is that there is no reliable method to nullify this influence. If it were so easy as in those legal tv series where the judge simply orders: "the jury shall disregard what it has heard".

This kind of pressure, intentional or not, is present in almost every estimation request. Unfortunately, I do this more often than I'd like. It's good to be aware of it.

__"Relevant Historical Data and Checklists Improve Estimation Accuracy"__. (Your organization's) historical data and estimation checklists (contextualized to your organization) can help. For instance, developers easily forget that a project is not only about writing lines of code. Coding can be a surprising small part of the project. Do you account for all the meetings (e.g., in Scrum, Retrospectives, Demos, etc) you do? Is the problem domain well understood? Do you have dependencies with other teams? Do you have to provision new infrastructure? Performance/stress/load testing? How many environment do you have? Setting up the development environment? The list goes on.

Actually, this is something that I believe [OutSystems](www.outsystems.com) (my current employer)  can do extremely well. We have an internal tool that  really helps. We also do [reference class forecasting](http://arxiv.org/pdf/1302.3642.pdf), although I didn't knew it have a name until a few days ago. I have to read more of it. Hey, a [famous Nobel prize winner](http://en.wikipedia.org/wiki/Daniel_Kahneman) contributed to develop this concept!

__"Combining Independent Estimates Improves Estimation Accuracy"__. [Planning Poker](http://www.planningpoker.com/detail.html) works! I'm totally behind this one! I've been doing planning poker for years and it's much better than not doing it. I'm not saying it's perfect, but it's nice and simple. Don't forget, show your cards at the _same_ time.

__"Estimates Can Be Harmful"__. I also like this one a lot. Estimates influence later behaviour. No matter what we say about the uncertainty of an estimate, once we give it, both we and the person who requested it set an expectation. If the estimate is too low, lower quality is almost a given, with real consequences sooner or later. If the estimate is too high, [Parkinson’s law](http://en.wikipedia.org/wiki/Parkinson%27s_law) kicks in: "work expands so as to fill the time available for its completion" (that's why you always left your university's projects and exam's studies for the last minute...).

Defer estimates for the last _responsible_ moment. Give a range, not a single number.

## Things we don't know

Magne also talks about some of the things we don't know. They should all be pretty obvious, but it's good to see them backed by research.

__"How to Accurately Estimate the Effort of Mega - large, Complicated Software Projects"__. I guess we all know this by now, right? Don't feel sad for being a software engineer, always being told how civil engineering and architecture and all those other disciplines are so much better than we are at project planning. I don't believe they are.

The apartment block I live in is currently undergoing  simple (or so I thought) maintenance work that should have ended in September, having started in June or July. It's still ongoing. The [new Berlin airport](http://www.thelocal.de/20140108/berlin-airport-wont-open-this-year) is _very_ delayed. Hundreds of years of experience, but still major failures.

Generalisations can be useful, but are dangerous. Software engineering is not so bad. The rest is not so good.

It should be obvious by now that you should go agile. Real agile. More on that some other time.

__"How to Measure Software Size and Complexity for Accurate Estimation"__. I get the impression that many people put great faith in metrics regarding software size and complexity to estimate effort. Research indicates that none of them seem so be very useful, with the exception of some very specific contexts.

__"How to Measure and Predict Productivity"__. This is subject to hot debates, but it (again) seems that research confirms that we can't measure productivity. This shouldn't be too hard to believe in. Software projects are inherently a creative and exploratory activity. After all, if you're not doing anything new, why are you doing it? Shouldn't it be already automated and/or packaged as a product? If you're doing cookie-cutter projects always from scratch (the one sure way to really repeat work), your organization's lifespan will be shorter than most.

It's not like a factory that produces 1000 (almost identical) cars a day. No, every project explores new territory, in a unique context, so it's difficult to compare teams and projects.

Organisation's still try to do it, understandably. After all, we can't objectively measure productivity, but we all know that some persons/teams are much more productive than others. Top-notch team not only do things faster, they do things that others simply cannot do.

## The end

This has been one long post. I've more things to say about estimations and (agile) project management, but I'll leave it for other time.

## Small digression

About humans knowing there is a future, let me tell you a curious religious story. I'm not a religious person, although I'm surely influenced by Christian ethics and values. I'm a Portuguese so, like every Westerner, I just can't help it (and I think that's a _good_ thing). But I like to read about religion and how it influences our world view and life. If you're into it, grab a copy of ["Heirs to Forgotten Kingdoms: Journeys Into the Disappearing Religions of the Middle East"](http://www.amazon.com/exec/obidos/ASIN/0465030564/theconomists-20). At the very least, you'll know why we have seven days in a week and how Muslims were much more tolerant than Christians in the past.

I once read (I read a lot...) that suicide is a deadly sin if you're a Christian (not sure about other religions) because in the Middle Ages people had an awful temporal life: nasty, brutish and short, as Thomas Hobbes famously said. Given that the Church said that there would be a Heaven in the Afterlife, then some believers might see suicide as a quick way to get there.

_Thank you for listening. You're nice._
