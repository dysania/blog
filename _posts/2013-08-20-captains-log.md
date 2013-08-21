---
layout: post
title: "Captain's Log: 2013.08.20"
location: "Los Angeles, CA"
date: "Tue, Aug 20 2013 22:27:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Started using Verbal Expressions for `Matcher` module
+ Refactored `Engine` module
  + Created `.===` method to determine if an engine matches a url
  + Created `.matches` method to take in verbal expression for engine
  + Learned more about ClassMethods, singleton methods, and `extend`/`include`
+ Edited `Matcher.oneboxed` to get array of engines and return appropriate onebox
  + array includes any Engines ending with "Onebox"
  + removed explicit regex url matching
+ Created `Engine` spec
+ Started copying regex used in discourse/discourse oneboxes for url matching into existing engines
  + Will convert to Verbal Expressions
+ HOMEWORK:
  + Mandatory watch last night's assigned video
  + Vyki:
    + Make sure there is an issue for every remaining onebox needed
    + Paste regex for url matching in each issue
    + Make sure milestone for each issue is 1.0.0
  + JZ:
    + Rewrite current regex to use verbal_expressions
    + Contact @vykster to merge request when they are all finished
  + If conscious, make more oneboxes.......
