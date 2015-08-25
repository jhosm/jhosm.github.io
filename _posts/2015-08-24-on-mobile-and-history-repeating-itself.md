---
layout: post
title: Mobile Web & Early Web - A Lot Of Similarities
comments: True
---

Mobile is a revolution that is changing the entire world. It is also very interesting to realize how, in many (software engineering) ways, it's so similar to the early web. History does repeat itself, with some nuances. Oh... and a long (but hopefully entertaining) story to begin with.

---

#### TL;DR;

Early Web:

* Browsers were at a rudimentary stage of evolution (in too many ways to count);
* If you wanted performance, you built rich client applications - Javascript was sloowww;
* If you wanted great UI, you built rich client applications;
* If you wanted access to physical devices, you built rich client applications;
* Network bandwidth was a scarce resource;
* Latency could kill you;
* Desktop hardware was much less powerful than nowadays;
* Continuous Delivery was science fiction.
* The desktop ecosystem was dominated by Microsoft;

Mobile:

* Mobile browsers are lacking;
* If you want great UI, you're told to build native apps;
* If you want access to sensors, you're told to build native apps;
* Network bandwidth is a scarce resource;
* Latency can kill you;
* Some smartphone hardware can kill you;
* Continuous Delivery is science fiction, if you build a native app.
* The mobile ecosystem is dominated by Apple and Google;

As with the early web, with mobile you:

* Have to minimize the number of requests you do to the server;
* Have to minimize the number of bytes you send and receive in each request;
* Have to cache as much as you possibly can (and you can cache a lot);
* Have to be really careful (and knowledgeable) in crafting Web UIs;

As with the early web, I believe that the mobile status quo will also change with time. Fortunately, those early web lessons are there to be leveraged. Generally, we are always talking about distributed systems after all.

For those of you who will tell me that mobile and early web are not the same: they are not. I'm just saying that they have many important similarities, from a software engineering perspective. And they are totally different beasts from a business perspective. Mobile is an extension of yourself. The desktop will never manage to be that.

#### For those who love a good story

A few (many?) years ago, I was part of a (small) team that was building a (small) web application. I was working at Banco BPI (a bank) at the time, and the application was to be used at the bank's branches. The application was not too complex: we were building a workflow to bring under control a process that involved a lot of paper going back and forth between the branches and a back-office department.

Technically, we were using a lot of Javascript and doing most of the processing on the browser. These were early days of the AJAX explosion and the Prototype library reigned supreme (jQuery and all the other gazillions frameworks didn't exist). Happy times, when I learned how interesting and powerful Javascript was. But I digress.

We were happy with our work and we deployed it to seven branches, for a pilot program... We started to get feedback from the field: "The application is soooo slow"! "It's unusable!". We couldn't believe it. The application wasn't super fast, agreed. But it wasn't unbearable or anything like it! Bah! Those insufferable end-users. Always putting the blame on IT!

Nonetheless, we decided to visit one of those branches. It's always good to see how users actually use your application. When I arrived at the branch, a really nice (and patient!) colleague took me to her desk, typed the application's URL and we waited... and waited, staring at a big, white, _blank_ screen... and waited. After about one minute, the page loaded. I was dismayed. What's happening here??

At the time, the bank (as most of the rest of the world) used only Internet Explorer. IE gave you (the developer) exactly ZERO help: it was a complete black-box. So I came back to the office very concerned (as expected) but also extremely curious. Troubleshooting is like detective work and I do love crime novels!

After some head scratching we got our breakthrough: the best that we could expect from branches was 128kbps networks, shared by the whole branch. That's right: 128kbps (that's kilobytes per second). Shared by all the people at the branch. Those were the best conditions. Some branches (as was the case of the one I visited) had even tighter bandwidth. Bandwidth was really expensive at the time. Why didn't we know this from the beginning? For several reasons, but that's another post (if ever).

Our next step was to check how much data we were sending down the pipe. We hadn't checked it before because... hey, it seemed fast enough in our machines and on the tester's machines. We all had nice network bandwidths.

It turned out that we were sending a couple of megabytes, IIRC. By the way, [HTTP Fiddler](https://en.wikipedia.org/wiki/Fiddler_\(software\)) was my best friend at the time. Amazing piece of software. But I digress... again.

So, a couple of megabytes. Oh, and we were sending that amount of data over many different HTTP requests. Remember that in those days, browsers would only do two requests simultaneously.

So we started to optimize and remove waste. We started by drastically reducing the amount of data sent over the wire, and the number of requests:

* We configured IIS to compress static (e.g.: images, javascript, html, css) files. We compressed dynamic files. The former forced us to trade CPU time (both in the server and the desktops) for request size.
* We configured IIS to tell the browsers to aggressively cache all the static files for a lengthy period (one month, I believe).
* We introduced some cache-busting techniques so that the browsers would retrieve updated files whenever needed.
* We had a lot of javascript code, spread over a lot of files. We merged all of them into one file and minified it.
* We had css spread over several files, so we also merged them.
* We removed from the requests all the data that was unused. We were reusing some services that were returning a lot more data than needed for our use cases.

Fortunately, we already had an automated build process in place (maybe that's another story) and that allowed us to make some of the optimizations without sacrificing readability. For instance, we were able to keep our Javascript code factored into different files.

Those optimizations helped us *a lot*. After an initial "prefetch", where we had to "load" the application (and cache all the files), subsequent requests, even after browser restarts, only had to get the needed data. The branches were now getting about the same performance as we were. But, as I said earlier, the application wasn't super fast in our machines.

We still weren't totally happy. It was a matter of pride to make it as fast and possible. So... now what? We were dumbfounded. The network wasn't an issue anymore. The server was handling the requests pretty fast. It had to be something in the browser. Well, we were doing a lot Javascript, including major updates to the DOM. But the browser was a black-box. We had no help to do any kind of performance profiling.

I was in love with Javascript by then, so I thought: how hard can it be to build a code profiler in Javascript to profile Javascript? Not to hard, it turned out. About 200 lines of code, IIRC, including whitespace, a lot of curly braces and a bare-bones UI. We wouldn't get precise measurements, as the profiling code had a noticeable performance impact - the Heisenberg principle, I guess ;) - but it would be enough to spot the... hotspots (pun intended).

We instrumented the code and we found two main culprits:

* String concatenation (one of the usual suspects...)
* Too many changes to the DOM

We built a StringBuilder, changed the way we... changed the DOM and... got the page loading in about 1 second! Success! Could we have made it even faster? Probably. But we had reached a point were it didn't really matter.

Would I have gone to all this trouble today? It depends, but in the case of that application, probably not. Why? Because technology have moved on and matured. Even without most of those optimizations, the application would probably be fast enough nowadays. Browsers provide us with incredibly powerful development tools. Broadband (and wi-fi) internet is extremely fast. Javascript engines have improved by leaps and bounds. Web apps provide a nicer user experience than most desktop applications, in my opinion.

Mobile web isn't there yet. But it will. The advantages are just to compelling (a theme for another post... someday... maybe).
