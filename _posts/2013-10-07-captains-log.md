---
layout: post
title: "Captain's Log: 2013.10.07"
location: "Los Angeles, CA"
date: "Mon, Oct 07 2013 22:30:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Finished GitHub Commit onebox (PR [#159](https://github.com/dysania/onebox/pull/159))
+ Finished Twitter onebox (PR [#161](https://github.com/dysania/onebox/pull/161))
  + Discourse uses Twitter API, which requires oAuth
  + But, we're making a gem, not an application
  + We'll use `HTML` module to parse instead to make it easier
  + Might run into problems with protected tweets later -- these should only output the tweet URL if the user is not allowed access to that URL
+ Created 2 new issues
  + We don't want protected tweets to be oneboxed ( [#162](https://github.com/dysania/onebox/issues/162))
  + Time display conversion for JSON oneboxes ( [#160](https://github.com/dysania/onebox/issues/160))
+ Google Hangout with Discourse mentors next Tuesday
+ Everybody's tired! Early turn-in
+ HOMEWORK
  + Keep on making oneboxes for v1.1.0...again
