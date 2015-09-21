---
layout: post
title: On Scaling Software Development - II
comments: True
---

On a [previous article](http://jhosm.github.io/2015/07/19/on-scaling/) on scaling software development, I highlighted four principles:

* Free flow of information
* Small, autonomous teams
* Small, autonomous services
* Standards on interactions, both for teams and for services

Part I discussed the free flow of information. On part II, let's discuss small, autonomous teams.

---

We already know that free flow of information is the lifeblood of a scalable and innovative organization. Actually, it's the lifeblood of a prosperous and free society, but I digress...

Coming back to the issue at hand, free flow of information is a necessary ingredient, but is not sufficient. There are other crucial ingredients.

### Why command and control is still popular

On a small scale, there simple isn't too much difference between centralized and decentralized decision making. But as you scale things start to get complicated. Nowadays, almost everyone wants (or says it wants) to free up the creativity of its people. But that's (a lot) easier to say than to do. There are many, many reasons for old style command-and-control to keep rearing its ugly head. Let me just mention a couple of them.

Humans need [certainty](http://lifehacker.com/this-graphic-explains-20-cognitive-biases-that-affect-y-1730901381). Not only managers or bosses... humans in general. They need to know what the [future will look like](http://jhosm.github.io/2015/01/03/on-estimation/). Command and control gives the _illusion_ of certainty. The top of the hierarchy has a vision and a plan to bring about that vision. Everyone just needs to act as planned and results will appear. No doubts on the way to get to the destination. Certainty.

Humans need comfort. Command and control is comfortable for everyone.  Managers don't have to worry about their team going in different directions, much less directions they don't like! But it's also comfortable for the _underlings_. "I'm just doing what I'm told to do". "Not my fault". "They must know best".

There are many other reasons, but I wanted to focus on these. By the way, why do _you_ think command and control is still so pervasive?

## Autonomous Teams

But the opposite, setting no rules and letting people without any kind of guidance can be even worse. You have to set the [right conditions](http://www.slideshare.net/iodboi/contiuously-deploying-culture-20-agile-sland).

What makes a team autonomous? There's more to it than meets the eye. Let's look at some conditions that I believe need to be in place. Again, not an exhaustive list, far from it, but important stuff.

### Team Size

Teams must be small. I find that between 5 and 6 people is usually best, but it really depends on context. Too small a team and it's difficult, but not impossible, to get anything done. Too large a team and you get a group of people who do not have much to say to each other. The tasks they're working on are too diverse. The effort to keep everyone in the loop grows exponentially (you know, the mythical man-month...). The effort to reach a consensus wears everyone down.

### Product Management

When a team has to make a product (software _is_ a product) decision, can they easily find the key stakeholders? How easy it is to reach a decision? Does the team clearly understands what is their area of responsibility and of others?

If a team does not know why it's doing what it's doing, then the team is not autonomous. If the team does not have a say on the things it builds, then it's not autonomous. If the team cannot easily discuss with all the stakeholders, then it's not autonomous. If the team does not know what it owns, then it's not autonomous.

### Product Architecture

How constrained is the team by the product's architecture? Teams don't usually work in green field projects, so their technical decisions are constrained by what's already there. We want to minimize those constraints as much as possible. Nowadays, this means moving away from monoliths towards microservices.

A team is not fully autonomous if it can never do what it thinks is the best technical solution for the problem at hand.

### Change with confidence

A team, or an individual team member, has to make many small decisions per day. These small decisions is where the rubber meets the road, where all those nice architectural diagrams are realized. So the team needs to be confident to make these small decisions and not back away from experimenting for fear of breaking things.

This means very, very tight feedback loops. You know... fast tests, continuous integration, all those cool things.

But what if the team needs to change something it's not comfortable with, something it doesn't own? In those cases, it's important to review those changes with the owner team. In a fast, probably asynchronous way: GitHub's pull requests are a great example to that end.

What other ingredients do you think are needed?
