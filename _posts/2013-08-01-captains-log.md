---
layout: post
title: "Captain's Log: 2013.08.01"
location: "Los Angeles, CA"
date: "Thu, Aug 01 2013 23:00:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

>+ Skipped Ruby study group for this week, but will attend next week's [LA Ruby/Rails August meetup](http://www.meetup.com/laruby/events/129200762/)
+ Created fixtures for all the rest of the oneboxes
	+ Took up most of our session since oneboxer currently supports [30+ sites](https://github.com/dysania/discourse-oneboxer/tree/master/lib/discourse/oneboxer)
	+ Certain sites (i.e. Hulu, Google Play) kept making `curl` hang for some reason
	+ Now we'll focus on creating specs specific to each onebox
	+ Started to clean up fixtures but still need to finish
	+ According to [`whitelist.rb`](https://github.com/dysania/discourse-oneboxer/blob/master/lib/discourse/oneboxer/whitelist.rb) if a site supports [OpenGraph](http://ogp.me/) then it is already supported by oneboxer -- will have to keep that in mind when making tests
+ Captain Kurt's challenge: if we make the 1st failing test from yesterday (out of 2) pass, he'll get us pizza during the next session
	+ Used Nokogiri's [`inner_text()`](http://nokogiri.org/Nokogiri/XML/NodeSet.html#method-i-inner_text) method to get just text of extracted data, without HTML tags --> CHALLENGE COMPLETED
	+ Also made 2nd test pass technically...by commenting it out for now (bad test that we'll need to rewrite)
	+ Monday will be Pizza Day! Or hopefully perhaps something healthier
+ First tiny code review from mentor [Robin](https://twitter.com/evil_trout)
	+ Mostly positive, asked for reasoning behind using [`require_relative`](https://github.com/dysania/discourse-oneboxer/commit/45180d20d6dfb7be6f96b0e89707e66094fe7536) and [`add_onebox`](https://github.com/dysania/discourse-oneboxer/commit/deeb3df0b797665a99122f44650086bcb593cd4b) manually for each onebox instead of just including the whole onebox directory
	+ We replied that we figured it would be easier to understand and would reduce security risk
+ Planning on registering discourse-oneboxer gem to [RubyGems.org](http://rubygems.org) on Monday
	+ Captain Kurt joked that he would register it himself tomorrow without us (we don't meet on Fridays)
	+ We were not amused
	<img src="http://www.wall321.com/thumbnails/detail/20121107/usa%20freckles%20gymnast%20olympics%202012%20mckayla%20maroney%20not%20amused%20unimpressed%201920x1080%20wallpaper_www.wall321.com_1.jpg" width="80%" />
+ Worked on RGSoC introduction blog post
	+ Forked [summer-of-code](https://github.com/dysania/summer-of-code) repo, created new branch
	+ Converted approved rough draft to Markdown 
	+ Will submit pull request by Monday
+ Captain Kurt suggested creating Ruby wrapper in future for [Apsis](https://github.com/wilkie/apsis) game engine by [@wilkieii](https://twitter.com/wilkieii) 