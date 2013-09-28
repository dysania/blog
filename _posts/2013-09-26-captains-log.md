---
layout: post
title: "Captain's Log: 2013.09.26"
location: "Los Angeles, CA"
date: "Thu, Sep 26 2013 22:27:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: jz
---

{{ page.title }}
================
>+ Vyki's night off!
+ Finally finished and merged [`add-shared-layout-view`](https://github.com/dysania/onebox/pull/140) branch for [#61](https://github.com/dysania/onebox/issues/61)!
  + Triple curls allowed only for layout template
  + Updated all onebox engine templates so they don't include duplicated elements anymore
  + Refactored `View` class
  + Decided that all onebox engines should each have a template -- including Example
+ Learned that you don't need to always immediately act on an object upon initialization
  + The context: using `#to_html` on new `View` object within a method
  + Why: Might use up time/power on this action when it won't even be necessary, like if you timeout
+ Learned about [`#tap`](http://ruby-doc.org/core-2.0.0/Object.html#method-i-tap)
+ SO CLOSE to releasing v1.1.0...
+ HOMEWORK: Keep on making oneboxes for v1.1.0...again

