---
layout: post
title: "Captain's Log: 2013.08.12"
location: "Los Angeles, CA"
date: "Mon, Aug 12 2013 23:52:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

>+ Vyki merged another [pull request](https://github.com/dysania/onebox/pull/35) from [markijbema](https://github.com/markijbema) requiring [Rubocop](https://github.com/bbatsov/rubocop) gem
  + For consistent code style, according to [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide)
  + Default cop settings
  + Spacing corrections
+ [Sam](https://twitter.com/samsaffron) cc'd us on new thread on [Discourse Meta](http://meta.discourse.org/): ["Sometimes onebox hangs"](http://meta.discourse.org/t/sometimes-onebox-hangs/9010)
  + We'll need to address HTTP request issues (limits/timeouts) in our gem
+ LA Ruby/Rails August meetup recap
  + We voted [Jeff Casimir](https://twitter.com/j3) of [JumpstartLab](http://www.jumpstartlab.com/) as MVP presenter
+ Discussed possible topics for lightning talk at LA Women's Ruby/Rails Group August Monthly Bash next Thursday
  + Present onebox gem
  + [Semantic versioning](http://semver.org/)
  + [Rubocop](https://github.com/bbatsov/rubocop)
  + Ruby's unique [pessimistic operator](http://robots.thoughtbot.com/post/2508037841/rubys-pessimistic-operator)
+ JZ kicked herself for forgetting her laptop charger at home
+ Captain Kurt was sleep-deprived so we ended our session early
+ HOMEWORK:
  + Create 4 new oneboxes (2 each) based on Amazon and Example
  + Create new object that matches given URL to correct onebox class
    + This functionality is currently in `lib/onebox/preview` but should be separate since it'll get huge
    + Pair-program on this
    + TDD - commit spec first, then class
  + From last week - look at what `parse_open_graph` does
