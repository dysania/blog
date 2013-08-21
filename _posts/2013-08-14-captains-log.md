---
layout: post
title: "Captain's Log: 2013.08.14"
location: "Los Angeles, CA"
date: "Wed, Aug 14 2013 23:00:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Dealt w/ a LOT of merge conflicts
  + We had pull requested a few onebox branches before we refactored
    + Qik
    + Wikipedia
    + StackExchange
  + Renamespaced oneboxes to `Engine` module instead of `Preview` class
+ Cleaned up local and remote branches in `dysania/onebox`
+ Started looking at VerbalExpressions
+ Learned about the difference between `include` and `extend` re: singleton class methods
+ For sites that support OpenGraph, we decided we'll be using the [opengraph](https://www.google.com/url?q=https%3A%2F%2Fgithub. com%2Fintridea%2Fopengraph&sa=D&sntz=1&usg=AFQjCNGJyQrwMaX1IFBEYInqmAPK3N6GIg) gem
+ [markijbema](https://github.com/markijbema) asked about why we created Matcher object ([issue #43](https://github.com/dysania/onebox/issues/43))
  + He thought it made sense that we keep url matching code close to onebox conversion code since it would define which urls we support
  + We created `Matcher` object because `Preview` should only have to worry about onebox conversion and not how to find the correct onebox
+ Discussed our lightning talk for next week
  + Semantic versioning
  + Ruby's pessimistic operator
  + Our experience so far extracting feature as a gem (the meetup's theme is gems)

+ HOMEWORK:
  + Add `require opengraph` in gemfile, commit in new branch for [issue #44](https://github.com/dysania/onebox/issues/44)
