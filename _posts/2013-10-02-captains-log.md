---
layout: post
title: "Captain's Log: 2013.10.02"
location: "Los Angeles, CA"
date: "Wed, Oct 02 2013 22:28:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Discussed Affordable Healthcare Act and being able to handle high salaries
+ Broke GitHub onebox specs since they should have been failing
  + Using JSON responses with regular URLs, when actual HTTP responses are in HTML
  + No URL conversion yet
+ Added custom `#url` reader methods and `#matcher` methods to GitHub Pull Request and Gist oneboxes
  + Extracted pieces of URL using named captures
  + PR [#157](https://github.com/dysania/onebox/pull/157)
  + Fixed (issues [#137](https://github.com/dysania/onebox/issues/137) and [#144](https://github.com/dysania/onebox/issues/144))
  + Lots of regex!
+ Realized GitHub Commit oneboxes are using `HTML` module, should switch to `JSON` module and have same format as Pull Request and Gist (issue [#156](https://github.com/dysania/onebox/issues/156))
+ How to fix commit messages with git interactive rebase
  + `git rebase -i HEAD~<# of commits>`
+ Changed RSpec command line options
  + `--format documentation`
  + `--fail-fast` - stop on first failing test
  + `--backtrace`
+ 104 STARS!
+ HOMEWORK
  + Keep on making oneboxes for v1.1.0...again
