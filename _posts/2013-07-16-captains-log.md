---
layout: post
title: "Captain's Log: 2013.07.16"
location: "Los Angeles, CA"
date: "Tue, Jul 16 2013 22:33:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

>+ Captain Kurt fixed JZ's expired version of Sublime Text 2
+ Vyki is still in the process of recreating her dev environment: installed Ruby, RVM, Sublime
+ Captain Kurt switched from Rails JSON to [MultiJSON](https://github.com/intridea/multi_json) for JSON parsing
+ Used RSpec to run discourse-oneboxer and fix specs on our own
	+ `bundle exec rake`: run all tests
	+ `rspec <file_with_error.rb:line>`: run specific test
+ Messed up git branches
	+ supposed to create new branches from master branch
	+ instead, created nested mess
	+ solution: git merged all nested branches into one
+ Fixed 9 tests, 23 failures to go
	+ replaced Rails methods 
		+ replaced `squish()` with `gsub()`
		+ changed `m.present?` to `m.to_a.any?` because it's more precise
		+ replaced `blank?` with `empty?`
		+ changed instances of `present?` to use `nil?` instead
	+ removed favicons from expected results
+ Conference/meetup talk
	+ Need to ask [Jen](https://twitter.com/jendiamond) if we can give quick talk at tomorrow's [Eastside/Westside Monthly Bash](http://www.meetup.com/Los-Angeles-Womens-Ruby-on-Rails-Group/events/124552602/) at [Oversee.net](http://oversee.net/) (all 3 of us will be in attendance)
	+ Might be interested in presenting at [GoGaRuCo 2013](http://gogaruco.com/) in September
+ HOMEWORK: fix all tests






