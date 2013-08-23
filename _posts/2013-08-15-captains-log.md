---
layout: post
title: "Captain's Log: 2013.08.15"
location: "Los Angeles, CA"
date: "Thu, Aug 15 2013 22:23:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Pizza! Sodapop! courtesy of Captain Kurt, our prize for making all of our tests pass on [8/1/2013](http://dysania.github.io/blog/2013/08/01/captains-log.html)
+ Added pessimistic version numbers for all of the gems in gemspec
  + Find current version number with `gem list -r <gemname>`
  + Add latest version number excluding the last decimal number: <br />`spec.add_runtime_dependency "<gemname>", "~>, x.x"`
+ Continued working on adding Open Graph support
  + Switched from opengraph to [opengraph_parser](http://rubygems.org/gems/opengraph_parser)
  + opengraph's Nokogiri version dependency [hasn't been updated in a while](https://github.com/intridea/opengraph/blob/master/opengraph.gemspec), so it breaks our code
  + opengraph_parser has [bad version dependencies generally](https://github.com/huyha85/opengraph_parser/blob/master/opengraph_parser.gemspec), but would still rather use that
+ Moved duplicated code from oneboxes to new `Engine` module
  + All oneboxes include `Engine` --> share methods
  + Onebox engines now only need to define their own `extracted_data()` function
  + Handlebars templates must follow name pattern

            {% highlight ruby %}
            def template_name
              self.class.name.split("::").last.downcase
            end{% endhighlight %}

>+ Created new function `read()` in `Engine` to open url
  + Will eventually use eithr Nokogiri or opengraph_parser depending on website
  + Refactored Engine spec
  + Cleaned up onebox specs, used `let:` to handle repetitive tasks
+ Created a few more merge conflicts while we were both editing gemspec
  + Cleaned them up ourselves like we learned on Tuesday

