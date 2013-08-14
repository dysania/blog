---
layout: post
title: "Captain's Log: 2013.08.13"
location: "Los Angeles, CA"
date: "Tue, Aug 13 2013 22:23:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ created `Matcher` class
  + TDD
  + `Engine` module to be included by oneboxes
  + refactor `preview`, move url matching functionality to `Matcher.oneboxed`
+ JZ added new oneboxes
  + [Qik](http://qik.com/)
  + [StackExchange](http://stackexchange.com/)
  + Captain Kurt helped add test for Qik video embedding and make spec DRYer
+ we don't know how to grab video embed code yet
  + still undecided on how to display videos in regards to autoplay
  + embed or linked thumbnail ?
+ learned about [Null Object](http://en.wikipedia.org/wiki/Null_Object_pattern)
+ learned how to autoclose issues with a commit message!
  + `git commit -m "Fixes #[issue number]"`
+ unable to merge `wikipedia-onebox` branch due to conflicts with master
  + learned how to deal with conflicts
    + `git pull --rebase origin master`
    + `fix conflicts`
    + `git add .`
    + `git rebase --continue`
    + `git push -f origin wikipedia-onebox`

+ How to make a good pull request via Robin and Jeff:
<blockquote class="twitter-tweet"><p>Now *this* is how you make a good pull request: <a href="https://t.co/WWKEI0OAok">https://t.co/WWKEI0OAok</a></p>&mdash; Robin Ward (@evil_trout) <a href="https://twitter.com/evil_trout/statuses/367442268258459649">August 14, 2013</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
<blockquote class="twitter-tweet"><p>Look at this pull request.. LOOK AT IT <a href="https://t.co/CzA91l6oQw">https://t.co/CzA91l6oQw</a></p>&mdash; Jeff Atwood (@codinghorror) <a href="https://twitter.com/codinghorror/statuses/367395684791508992">August 13, 2013</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

+ HOMEWORK:
  + refactor tests so more DRY
  + Read up on:
    + [VerbalExpressions](https://github.com/VerbalExpressions/RubyVerbalExpressions) for Ruby
    + `parse_open_graph`



