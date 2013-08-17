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
  + Add latest version number excluding the last number `"<gemname>", "~>, x.x"`
+ Continued working on adding Open Graph support
  + switched from opengraph to [opengraph_parser](http://rubygems.org/gems/opengraph_parser)
+ Moved redundant code from oneboxes to engine module
  + use engine to open template for each onebox

``` ruby
def template_name
  self.class.name.split("::").last.downcase
end
```
>+ created new function in engine `read` to open url
  + re-factored tests to test new method
  + cleaned up onebox specs, used `let:` to handle repetitive tasks
+ created a few more merge conflicts while both editing gemspec
  + cleaned them up ourselves like we learned on tuesday


