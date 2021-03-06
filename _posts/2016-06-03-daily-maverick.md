---
layout: page
title:
---

## Statistics

* Google's PageSpeedInsight: [46 / 100 mobile, 54 / 100 desktop](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fwww.dailymaverick.co.za%2F)
* Webaim's WAVE: [7 errors / 627 alerts](http://wave.webaim.org/report#/thedailymaverick.co.za)
* WebPageTest on 3G: [SpeedIndex of 12,487](http://www.webpagetest.org/result/160601_AX_111H/)

## Review

The Daily Maverick is, in its own words, "a unique blend of news, information, analysis and opinion delivered from our newsroom in Johannesburg, South Africa". Their website unfortunately has a number of performance issues. These can be summarised as:

- large page size;
- high number of HTTP requests;
- external scripts;
- minimal caching;
- CSS and JS not minified;
- images not compressed.

These mean a cost to visitors in terms of time (the page loads slowly) and money (a lot of data is needed to load the page).

Total page size for the home page is 4.4MB. **The biggest factor affecting page size is JavaScript that weighs in at 2.7MB**. A large percentage of these come from third party domains again increasing page load time: **these could be evaluated as to whether they could be removed**. Are they necessary or do they add value? For example, sharing scripts from third party services like Addthis add significant JS size, requests, and round trips to an external server. Considering that very few people engage with social sharing buttons (see [What Percent of Page Views Share on Social Media?](http://www.lukew.com/ff/entry.asp?1852)) these can either be removed or replaced with simpler versions (see [Ridiculously Responsive Social Sharing Buttons](http://kurtnoble.com/labs/rrssb/)).

**The home page currently has 247 requests: that is a lot**. 174 of them are images. While image size is generally small this still amounts to over 1MB of images and many requests. **The design could be re-evaluated in this area**. For example, does every story need to have an image attached to it? In many cases text will be sufficient to convey meaning.

**A number of scripts are loaded at the top of the page**, which blocks rendering of the page. **These can be moved to the bottom to minimise render blocking**.

Where possible, CSS and JS files should be concatenated to minimise requests. Cacheable resources like CSS files, JS files and images should be cached to save network requests. CSS and JS files can be minified to save download time and images can be compressed to save file size.

**Making the above improvements will greatly improve load times and reduce data costs.**

---

[Steve Barnett](https://naga.co.za/) ([@maxbarners](https://twitter.com/maxbarners)) and [Justin Slack](http://justinslack.com/) ([@justin_r_slack](https://twitter.com/justin_r_slack))

[CTFEDs](http://ctfeds.org/) Organising Team
