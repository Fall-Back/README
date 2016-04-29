![Fall-Back](fallback-logo-wide-lg.jpg)

[http://fall-back.github.io](http://fall-back.github.io)

Introduction
============

Fall-Back is a set of patterns, methodologies and a philosophy geared around providing a modern experience in modern browsers, but using hacks and a little JS as needed to provide an acceptable fallback experience for older browsers or browsers where CSS or JS isn't available (or disabled) and also taking into account accessibility issues. 

Basically, it's for Progressive Enhancement.

There will always be older browsers. The browsers we use today are tomorrow's older browsers. Auto-updates are a great thing, in my opinion, but you can't always guarantee a user doesn't get stuck on one version for some reason or another. Technology moves so fast it can be hard for users to keep up and even harder for companies, businesses or organisations. Don't get me wrong, I'm all for moving the web forward but sometimes it's just not acceptable for a page to look so broken. I'm fine with things not looking the same in all browsers. I'm fine with providing a simple universal stylesheet to older browsers. Heck, I'm even fine with not providing any stylesheet at all to some browsers if need be - I always make sure the HTML looks fine by itself - but what I'm not fine with is broken pages.

"It costs too much to maintain support", I hear. "It holds the web back if we don't give the user any reason to upgrade". I get those points, I really do. I just can't abide a broken page. Some users can't upgrade for some reason, some choose to use old browsers for some reason. Some choose to disable things like Cookies, JS, Images or even CSS, for some reason. It's their choice.

I come across the same problems all the time. Something breaks in an older browser and the page looks a mess. Tracking it down can be taxing and time consuming. Should I bother? Well let's look at the stats. Time and again I see older browsers cropping up on the stats. Numbers are low, I'll admit that, but for some reason, a small group of users has decided to stick with an older browser. And the page is broken. "It's too costly to fix", I hear again. Well, yes... But does it have to be?

What if we could build a site out of a set of discrete patterns we know will work independently or together, and work how we want them to where we want them to? Well, there are loads of frameworks and libraries that help with that, but I couldn't find one that added the extra layer I was looking for; the Fall-Back layer. Why can't there be a framework (or even just a set of patterns) that has been tested in older browsers and will provide them with something that's not broken. It doesn't have to try and emulate the main intended display - it just has to be acceptable. Just good enough.

So, I set about building and assembling Fall-Back. Each pattern is intended to be used independently as necessary, but also to work well together as a set. Using progressive enhancement techniques, I've tried to create some patterns that will give the user an acceptable experience whatever they're using. That's not to say you can't make it an exceptional experience for the majority of your users - that goes without saying - but by using these patterns from the start the small minority of users using older browsers is automatically catered for at no extra cost.

Tbc
