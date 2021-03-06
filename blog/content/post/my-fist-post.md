+++
author = "Vivek Rao"
tags = [
  "hugo",
  "aws",
  "s3",
]
categories = [
  "cloud",
  "aws",
]
draft = false
date = "2017-01-13T16:52:37-05:00"
title = "Standing on the shoulders of giants"
description = "My first post about standing up this blog"

+++

*“For everything, there is a first time.” - Spock*

I have thought about creating my own website several times over the last 13 years but never really got around to doing it. Back in 2001 or 2002 during engineering college, a bunch of my friends and I created and hosted a website on [GeoCities](https://en.wikipedia.org/wiki/Yahoo!_GeoCities "GeoCities") sharing our source code and project details for the greater good. Once we landed jobs out of college, we gradually forgot about it. I remember back in 2009, a few years after I had moved to the United States, reading that Yahoo was shutting GeoCities down and thinking what a wasted opportunity it was for Yahoo.

<!--more-->

A large part of my reluctance to building my own website was that I would have to figure out a way to build it from scratch, host it, maintain it and figure out a way to track visitors, basic analytics etc. While that would have been an interesting challenge, it would have consumed a good chunk of my time out of work - time I wasn't prepared to spend after gruelling 14 hour work days.

Fast forward and it is early 2017. I decide over the MLK day long weekend that I want to finally build my own website. My time is still limited, albeit not with 14 hour workdays but with time I **want** to spend with my kids and my wife. But this time, things are different. Paraphrasing Isaac Newton, this time I am standing on the shoulder of giants and can see further than ever before. I figure that I can probably pull this off over a long weekend, working a couple of nights after the kids are in bed.

I figure that I would need a domain name, a DNS provider - both possible using [Route 53](https://aws.amazon.com/route53/ "Route 53"). I remember from [AWS Solutions Architect](https://aws.amazon.com/certification/certified-solutions-architect-associate/ "AWSSA") course that I can host static websites on the cheap using [Amazon S3](https://aws.amazon.com/s3/ "S3"). I would also need a static website engine, either [Jekyll](https://jekyllrb.com/ "Jekyll") or [Hugo](https://gohugo.io/ "Hugo") that can build static pages from simple text or [markdown](https://en.wikipedia.org/wiki/Markdown "Markdown") files using predefined themes. That's it and I would be good to go as far as getting the site up and running.

It took me a few minutes and a credit card to buy my domain name - vivekrrao.com. I spent a little over 2 hours in deciding which static website engine I wanted to use (went with Hugo because of simpler installation and faster build speed), the theme I liked the best ([Phlat](http://themes.gohugo.io/hugo-phlat-theme/ "Phlat")) and getting it all setup on my laptop.

I followed the step by step documentation [here](http://docs.aws.amazon.com/gettingstarted/latest/swh/website-hosting-intro.html "Static Website Hosting") on setting up my S3 buckets, bucket policies to enable website hosting. I was able to setup my Route 53 hosted zones and point the record set to my S3 website end points for both http and www. All in about an hour and a half.

Excluding the time it took for me to write this post, I was mostly up and running in under 5 hours, spread across a few days. I most likely will pay a dollar or two if not pennies to host this site every month. I wonder if this would have been possible 10 years ago.

Of course, there is a lot of opportunity to do more. For one, I want to fully automate the build and deploy process, tests, spell check and all. I want to implement SSL and a global CDN such as [CloudFront](https://aws.amazon.com/cloudfront/ "CloudFront") so I can deliver content faster while saving more money. I would like to add basic analytics to determine hits, visitors etc but all that for another day.

And this is just the tip of the iceberg. To me, the lesson is that the cloud lowers the barrier for entry for an individual like me who doesn't want to spend a lot of time or money building the infrastructure necessary to create a personal blog. I can spend more time thinking of what to blog rather than building the blog itself. That's tremendous ROI which would not have been possible just 10 years ago.  
