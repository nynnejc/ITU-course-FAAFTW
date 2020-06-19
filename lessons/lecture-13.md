# Web Performance

## Why

Web performance is vital for your website visitors to have a good experience, and can be considered a subset of web accessibility. Isn’t much accessible about a site you can’t access because of poor loading times, is there?

**Web performance can improve conversion rates**
A conversion rate is the rate at which site visitors perform a measured or desired action. For example, this might be making a purchase, reading an article, or subscribing to a newsletter. The action being measured as the conversion rate depends on the website's business goals.

**Make your site more Accessible**
To users with different internet speeds and devices, such as the lions’ share of users in developing countries.

**Reduce Carbon Footprint**
The Internet uses an enormous amount of electricity. This of course needs to be produced somewhere. In most countries, this means fossil fuels. This, in turn, means that the Internet’s carbon footprint has grown to the point where it may have eclipsed global air travel, and this makes the Internet the largest coal-fired machine on Earth.To paraphrase Smashing Magazine’s article on this: performance, user experience and sustainability are all neatly intertwined. The key metric for measuring the sustainability of a digital product is its energy usage. This includes the work done by the server, the client and the intermediary communications networks that transmit data between the two.


## Apollo 11 trip to the moon vs. JavaScript

A few years ago, an intern at NASA found the source code for the Apollo 11 mission and put it [on github!](https://github.com/chrislgarry/Apollo-11) To put things into perspective, about 1.7 megabyte of uncompressed code was used for on both the Lunar module and the command module, but there's a lot of overlap and 1.7 MB is set a bit high, because each of the modules have quite a lot of comments that are documentation, so it is significantly less than that. 

*Less than 1.7 MB software that landed people on the moon.*

The median mobile site ships 1.8 MG of uncompressed Javascript!

An incredible amount of JavaScript out there on the internet. JS it byte for byte the most expensive resource we have. With JS you pay a performance penalty at least 3 times, probably 4 times. 

## What

Part of good user experience is ensuring the content is quick to load and responsive to user interaction. This is known as *web performance*.

**Reducing overall load time:** How long does it take the files required to render the web site to download on to the user's computer? This tends to be affected by latency, how big your files are, how many files there are, and other factors besides. 
A general strategy is to make your files as small as possible, reduce the number of HTTP requests made as much as possible, and employ clever loading techniques (such as preload) to make files available sooner.

**Making the site usable as soon as possible:** This basically means loading your web site assets in a sensible order so that the user can start to actually use it really quickly. Any other assets can continue to load in the background while the user gets on with primary tasks, and sometimes we only load assets when they are actually needed (this is called lazy loading). The measurement of how long it takes the site to get to a usable start after it has started loading is called time to interactive.

**Performance measurements:** Web performance involves measuring the actual and perceived speeds of an application, optimizing where possible, and then monitoring the performance, to ensure that what you've optimized stays optimized. This involves a number of metrics (measurable indicators that can indicate success or failure) and tools to meaure those metrics, which we will discuss throughout this module.

**Smoothness and interactivity:** Does the application feel reliable and pleasurable to use? Is the scrolling smooth? Are buttons clickable? Are pop-ups quick to open up, and do they animate smoothly as they do so? There are a lot of best practices to consider in making apps feel smooth, for example using CSS animations rather than JavaScript for animation, and minimizing the number of repaints the UI requires due to changes in the DOM.

**Perceived performance:** How fast a website seems to the user has a greater impact on user experience than how fast the website actually is. How a user perceives your performance is as important, or perhaps more important, than any objective statistic, but it's subjective, and not as readily measurable. Perceived performance is user perspective, not a metric. Even if an operation is going to take a long time (because of latency or whatever), it is possible to keep the user engaged while they wait by showing a loading spinner, or a series of useful hints and tips (or jokes, or whatever else you think might be appropriate). Such an approach is much better than just showing nothing, which will make it feel like it is taking a lot longer and possibly lead to your users thinking it is broken and giving up.

## Measuring Performance

Measuring performance is important: you need metrics to see how your app compares to your competitors and to see how the upcoming release compares to your current and past releases. 

There is no single number or metric that works for all sites and all business goals. The metrics you choose to measure should be relevant to your users, site and business goals, measurable in a consistent manner, and, preferably to ensure internal support for web performance efforts, understandable to non-developers. 

Tools like [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) can measure a website’s performance. You can enter a URL and get a performance report in seconds. The report contains scores about how your website is performing, both for mobile and desktop. This is a good start for getting an idea about what you are already doing well and what could be improved.

[webpagetest.org](https://webpagetest.org/) is another example of a tool that automatically tests your site and returns lots of useful metrics.
Try running your favorite website now, on both webpagetest.org and PageSpeed Insights, and see what the scores are!

## Performance Terminology

**First Contentful Paint**
FCP measures how long it takes the browser to render the first piece of DOM content after a user navigates to your page. Images, non-white <canvas> elements, and SVGs on your page are considered DOM content; anything inside an iframe isn't included.

**Speed Index**
Speed Index measures how quickly content is visually displayed during page load. Lighthouse first captures a video of the page loading in the browser and computes the visual progression between frames. Lighthouse then uses the Speedline Node.js module to generate the Speed Index score.

**Largest Contentful Paint (LCP)**
The Largest Contentful Paint (LCP) metric reports the render time of the largest content element visible in the viewport.

**Time to Interactive**
TTI measures how long it takes a page to become fully interactive. A page is considered fully interactive when:
The page displays useful content, which is measured by the First Contentful Paint,
Event handlers are registered for most visible page elements, and
The page responds to user interactions within 50 milliseconds.

 
## Animation / Perceived Load Time

The perception of how fast your site loads and how responsive it feels to the user interaction is important; even more important that actual download time but difficult to quantify. There are areas of your site that you may not be able to make faster, but you can make it [feel faster even if the metrics can't be improved](https://developer.mozilla.org/en-US/docs/Learn/Performance/Perceived_performance
).

## Easy Wins

**Minimize initial load**
To improve perceived performance, minimize the original page load. 
First download everything you're going to actually show, but only the stuff you are actually using, then download the rest. If you're downloading all the assets in the end, the weight of all your assets hasn't improved -- in fact, you may need to add some code -- but because the download of non-immediately necessary assets are delayed in a manner that is not perceptible the the user, the user will feel like the download was faster. 
To minimize the assets required for initial load, separate interactive functionality from content so that required content  -- the text, styles, and images visible at initial load -- can be loaded first. 

**Delay, or lazy load, the rest of the assets**
Don't load images or scripts that aren’t used or visible on the initial page load. Either delay their load, loading them when the page becomes usable, or, loading them when they become necessary. Loading additional assets and resources after initial page load improves perceived performance. Loading essential data in initial requests and progressively loading features and data only as needed helps mitigate low bandwidth and lower spec hardware.
Additionally, you should optimize the assets you do load. Images and video should be served in the most optimal format, compressed, and in the correct size.

**Avoid font file delays**
Fonts can also harm user experience, especially if the fonts used need to be imported, and if the importing is not optimal.  Flicker of unstyled text and missing text both harm performance.
Make fallback fonts the same size and weight so that when fonts load the page change is less noticeable.

**Interactive elements are interactive**
Make sure visible interactive elements are always interactive and responsive. If input elements are visible, the user should be able to interact with them without a lag. Users feel that something is laggy when they take more than 50ms to react. They feel that a page is janky when content repaints slower than 16.67ms (or 60 frames per second) or repaints at uneven intervals.
Make things like type-ahead a progressive enhancement: use css to display input modal, JS to add typeahead/autocomplete as it is available
 
## Lazy Loading
One of the biggest improvements to most websites is lazy-loading images beneath-the-fold, rather than downloading them all on initial page load regardless of whether a visitor scrolls to see them or not. Many JavaScript libraries can implement this for you, such as lazysizes, and browser vendors are working on a native lazyload attribute that is currently in the experimental phase.
Lazy loading is a strategy to identify resources as non-blocking (non-critical) and load these only when needed. It's a way to shorten the length of the critical rendering path, which translates into reduced page load times.
Lazy loading can occur on different moments in the application, but it typically happens on some user interactions such as scrolling and navigation. 

```<img src="image.jpg" loading="lazy" alt="..." /> <iframe src="video-player.html" loading="lazy"></iframe>```

The loading attribute on an <img> element (or the loading attribute on an <iframe>) can be used to instruct the browser to defer loading of images/iframes that are off-screen until the user scrolls near them.
 
## Images
Media, namely images and video, account for over 70% of the bytes downloaded for the average website. In terms of download performance, eliminating media, and reducing file size is the low-hanging fruit. 

**Image Format**
The optimal file format typically depends on the character of the image.
The less colors an image has and the less photographic it is, the better it is to use the SVG format. This requires the source to be available as in a vector graphic format. Should such an image only exist as a bitmap, then PNG would be the fallback format to chose. Examples for these types of motifs are logos, illustrations, charts or icons (note: SVGs are far better than icon fonts!). Both formats support transparency.

**Serving the optimal size**
In image delivery the "one size fits all" approach will not yield the best results, meaning that for smaller screens you would want to serve images with smaller resolution and vis-versa for larger screens. On top of that you'd also want to serve higher resolution images to those devices that boast a high DPI screen (e.g. "Retina"). So apart from creating plenty of intermediate image variants you also need a way to serve the right file to the right browser. That's where you would need to upgrade your ```<picture>``` and ```<source>``` elements with media and/or sizes attributes.

**Controlling the priority (and ordering) of downloading images**
Getting the most important images in front of visitors sooner than the less important can deliver improved perceived performance.

The first thing to check is that your content images use ```<img>``` elements and your background images are defined in CSS with background-image — images referenced in ```<img>``` elements are assigned a higher loading priority than background images.

## Exercice

Use google's chrome performance plugin to make a performance audit of one of your favourite websites. Make sure you understand the score system.
Considering today's'  lecture on web performance, find one or more adjustments you can make to your project to make it perform better.


## Reading

- [Why Web Performance Matters](https://developers.google.com/web/fundamentals/performance/why-performance-matters)
- [MDN Web Performance Primer](https://developer.mozilla.org/en-US/docs/Learn/Performance)
- [Webpabetest](https://www.webpagetest.org/)
- [Google's Lighthouse](https://developers.google.com/web/tools/lighthouse)
- [Performant front-end architecture](https://www.debugbear.com/blog/performant-front-end-architecture)
- [Front-End Performance Checklist 2020](https://www.smashingmagazine.com/2020/01/front-end-performance-checklist-2020-pdf-pages/)
- [Performance Budgets, Pragmatically](https://csswizardry.com/2020/01/performance-budgets-pragmatically/)

