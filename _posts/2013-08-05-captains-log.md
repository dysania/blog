---
layout: post
title: "Captain's Log: 2013.08.05"
location: "Los Angeles, CA"
date: "Mon, Aug 05 2013 22:43:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

>+ Continued editing Preview, Example, and Amazon specs on `preview-refactor` branch
	+ edited Preview spec to use Example fixture and [fakeweb](http://rubygems.org/gems/fakeweb)
		+ we want the spec to not request a website, and to use our fixture
		+ we need to ask why is this important? Don't we want tests to fail once an actual website changes?
	+ created `response()` function in html spec helper for less repetitive code in specs
	+ used `let()` to do lazy assignments 
		+ ex: `let(:link) { "http://example.com" }`
	+ finished creating and passing all tests for Amazon
		+ First spec finished with least amount of input from Captain Kurt yet!
		+ JZ: write tests
		+ Vyki: make tests pass
		+ learned more about Nokogiri, used `.first["src"]` to get src attribute for product image

+ First [pull request](https://github.com/dysania/discourse-oneboxer/pull/26) from [Robin](https://twitter.com/evil_trout)
	+ tiny change to keep us up-to-date with discourse/discourse
+ oneboxer changes to discourse/discourse [being redirected our way](https://github.com/discourse/discourse/pull/1288)
+ New recommended resources
	+ [Bitcast.io](https://www.bitcast.io/) - Captain Kurt suggested we use it for learning by creating our own screencasts on top of watching existing screencasts
	+ [Rails 4 In Action](http://www.manning.com/bigg2/) - Book, check out the early access edition
+ HOMEWORK: Listen to more RubyRogues, checkout [Ruby Tapas](http://www.rubytapas.com/)

<blockquote class="twitter-tweet"><p>Meet <a href="https://twitter.com/jzeta">@jzeta</a> &amp; <a href="https://twitter.com/toastergrrl">@toastergrrl</a> from Team Dysania! They are developers by night AND can make balloon arches:<a href="http://t.co/6cdokfAiN7">http://t.co/6cdokfAiN7</a> <a href="https://twitter.com/search?q=%23teamoftheweek&amp;src=hash">#teamoftheweek</a></p>&mdash; Rails Girls SoC (@RailsGirlsSoC) <a href="https://twitter.com/RailsGirlsSoC/statuses/364315597707808768">August 5, 2013</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
