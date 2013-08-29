---
layout: post
title: "Captain's Log: 2013.08.28"
location: "Los Angeles, CA"
date: "Wed, Aug 28 2013 22:35:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Continued working on caching support
  + Decided to use [moneta](https://github.com/minad/moneta) after all
    + Set `expire = true` in options
    + Created singleton `.defaults` to DRY code for initializing Moneta caches
  + Made edits based on Captain Kurt's comments
  + We're gonna need to fix `Preview` specs to check that cache behaves like a cache
    + Bad test right now - only checks that it's a kind of Hash
    + Need to test that it behaves like a cache system, with abilities to `#store`, `#fetch`, and `#key`
+ Discussed using default images for oneboxes missing usable images
  + Considering using [this process](http://prioritized.net/blog/gemify-assets-for-rails/) to help integrate with Rails
+ Vyki created Clikthrough onebox
  + NOT "CLICKTHROUGH"!
+ JZ made edits to oneboxes from last night based on Captain Kurt's comments on open pull requests
  + Use `Array#first` instead of `Array[0]` because more idiomatic
  + Make sure to indicate on pull requests if it depends on another one
+ Discussed more on regex, Verbal Expressions, and played with Rubular
  + We'll be using the regex matchers from Discourse to help guide us with our Verbal Expressions in our `matches` blocks
  + This will be important for security
+ Learned more on constants and how classes/modules are basically constants
  + You can actually do something like `Onebox = Module.new do ... end`
+ Captain Kurt recommended we look at [Hamster](https://github.com/harukizaemon/hamster)

+ HOMEWORK
  + Work on oneboxes
  + At some point, make edits to README branch - some instructions are already outdated
