---
layout: post
title: Mobile Web & Early Web - Pretty similar, performance-wise
comments: True
---

Mobile is a revolution that is changing the entire world. It is also very interesting to realize how, in many performance-related ways, it's so similar to the early web. History does repeat itself, with some nuances.

---

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

As with the early web, I believe that the mobile status quo will also change with time. Fortunately, those early web lessons (more on that on another post) are there to be leveraged. Generally, we are always talking about distributed systems after all.

For those of you who will tell me that mobile and early web are not the same: they are not. I'm just saying that they have many important similarities, from a performance perspective. And they are totally different beasts from a business perspective. Mobile is an extension of yourself, so you have even lower tolerance for unresponsiveness. The desktop will never manage to be that.

"Pure" mobile web isn't there yet. But it will. The advantages are just to compelling (a theme for another post... someday... maybe). I firmly believe in that, as I believed that the Web would overtake Desktop apps. In the mean time, hybrid is the best option for many scenarios. My employer, OutSystems, has a nice [paper](https://www.outsystems.com/blog/2015/02/how-to-chose-the-best-mobile-architecture-infograph.html) on that. It's obviously (slightly) biased but it's very informative and easy to read.
