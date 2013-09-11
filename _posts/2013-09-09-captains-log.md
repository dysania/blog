---
layout: post
title: "Captain's Log: 2013.09.09"
location: "Los Angeles, CA"
date: "Mon, Sep 09 2013 21:00:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: jz
---

{{ page.title }}
================

<img src="http://www.justsaypictures.com/images/almost-there-2hj5.jpg
" width="100%" />

+ I went solo tonight since Vyki had to take the night off
+ Sick with fever/cold! But must keep going...
+ Captain Kurt gave me some pair programming interview tips
+ Finally merged [`caching-support-for-preview`](https://github.com/dysania/onebox/pull/97) into master, 3 weeks after opening the PR
+ Created [`sanitize-url-for-preview`](https://github.com/dysania/onebox/pull/119) branch
  + We need to make sure oneboxes don't allow [cross-site scripting, aka XSS](http://en.wikipedia.org/wiki/Cross-site_scripting)
  + Added tests to `Engine` spec
    + Returns onebox wrapper
    + Doesn't allow XSS injection
  + Added tests to `Onebox` spec
    + No triple braces in Handlebars templates - this escapes values
    + No Javascript - `<script` tags or attributes like `onclick`, `onload`, etc.
  + Fixed Wikipedia onebox template to not use triple braces
  + Ready for Vyki to merge
+ We're now ready for 1.0.0 release! Now to do it together...



