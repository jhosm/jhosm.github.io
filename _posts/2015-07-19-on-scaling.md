---
layout: post
title: On Scaling Software Development - I
comments: True
---

Scaling software is hard. Really hard. Scaling organizations is even harder. Oh! Those pesky humans! Always with their own opinions about what is wrong and what is right. Common sense is like DNA: everyone has it, everyone's unique. At the same time, we're social beings as no other. That's what allows us to be bigger than ourselves. So how to keep the spark that allowed an organization to have to think about scaling?

---

For an organization to scale effectively, it must adhere to a basic set of principles. They can be sliced and diced in many different ways, but the fundamental premise is:

> Free flow of information between autonomous organisms, be it an individual or a team.

_Autonomous_: having the power or right to govern itself. _Organism_: a system with many parts that depend on each other and work together.

Let's split this basic premise into four distinct principles:

* Free flow of information
* Small, autonomous - within their area of responsibility - teams
* Small, autonomous services
* Standards on interactions, both for teams and for services

Let's start with flow of information and deal with the rest in later articles (hopefully...).

## Free Flow of Information

Humans must communicate if they want to work towards a common goal. No flow of information, no social being. No social being, no great works. Every small barrier to the free flow of information lowers our potential to do great things!

Can we identify some barriers? Let's try:

* Different desks, rooms, building floors, buildings, time zones
* Rules, sometimes informal, that state what can and cannot be said
* Lots of new people continuously joining the organization
* Bad communication tools

When the organization is small, communication is almost an afterthought. Everyone is so close to each other that information just flows. When the organization is small the most effective mean of communication, face-to-face, is the norm. The organization's knowledge is also small enough to fit in one's head, or small enough for everyone to know someone (in small organizations, usually a friend) who knows what's needed.

Once you start to grow, those barriers start to creep in subtle ways:

* It starts to become difficult to find someone who can explain you why some piece of information (e.g.: a snippet of code) is the way it is;
* You start to see group dynamics forming;
* Some people start to shy away from asking for help, because "I don't want to bother those guys" (another way of saying "I don't know them well enough so I don't feel comfortable in coming to them");
* History becomes a very important part of explaining why, but history is nowhere to be found except on some people's heads.
* You don't have a map to help navigate the existing information (everyone had the map in their minds)

What happened? Face-to-face communication broke down. It's a combinatorial explosion problem, famously stated in the "Mythical Man-Month" book. If the organization's geographically distributed, face-to-face as the main means of communication is simply not an option. But even if you're not spread out over multiple offices and timezones, once you reach a certain size face-to-face is still important. But it's not nearly enough.

We have to use different communication tools. Those tools have a very strong impact on the continued free flow of information. Those tools should be human-centered and support the free flow of information.

#### Location-independent communication

Put all teams, no matter where they are on an equal footing. Talking with someone in the same desk as me should be more or less the same experience as talking with someone in another floor or another building. Sure, it will never be the same thing. But it should be as close as possible, at least on a work context.

Standardizing on location-independent solutions for inter-teams communication is key to bring all the people close to each other, no matter where they are.

#### Knowledge Findability

People must easily find other people who have the knowledge they're seeking with ease. The most important thing is to keep people talking to each other. And if other people can follow along and also acquire that knowledge, that's the sweet spot!

Of course, there's also a lot of information stored outside people's brains: documents, videos, images, among others. Keeping all this knowledge always organized in a way that makes sense for all is almost hopeless. Excellent search capabilities are the best solution to find documents. So spend less time worrying about organization and more about having great search tools.

Anyway, people must always be at the center of communication, not documents. Documents exist to support people's conversations. Documents must not replace people. Documents do not think. Documents do not talk to people. Documents do not create new stuff. People working together create new stuff.

#### Push essential information, pull specifics

If we want to keep people talking to each other, then we must ensure the information they need is pushed to where they talk. Don't force them to jump from app to app to gather info. Keep everything in one place: communication and information (it's all information, really). Answering these answers should be equally simple for everyone:

* Has my build succeeded?
* Is anyone committing to my branch?
* What are the current milestones for the next release?
* Hey, even other stuff might be helpful...Are there any strikes tomorrow that might affect any early morning meetings?

On the other hand, we all know that information overload can be as debilitating as lack of information. So keep less important information out of people's sights, but easily findable when needed.

#### Level the playing field for introverts and extroverts, newbies and old-timers

People have different personalities. Some are more extroverted, some more introverted. Some are old-timers (in every possible sense), some are newbies (in every possible sense). All have something valuable to add. Face-to-face can be intimidating for some people. Chat rooms can really help. Maybe I just want to lurk and learn by listening to the conversations happening across the organization. Maybe I'll want to dip my toes in the water when I feel ready, without having to interrupt someone.

Again, we want to make it easy to for people to talk to each other, no matter their personality traits.

#### Security and confidentiality

A word about security and confidentiality. In an ideal world, information would flow completely free. We all know that isn't possible, some information must be kept secret in some form. To avoid people constraining themselves, we should have some simple, but clear guidance of what constitutes a "company secret", what is public and what isn't.
