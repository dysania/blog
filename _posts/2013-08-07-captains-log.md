---
layout: post
title: "Captain's Log: 2013.08.07"
location: "Los Angeles, CA"
date: "Wed, Aug 07 2013 22:52:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

<img src="http://media.catmoji.com/cache/post/kbh/grumpy-cat_thumb.jpg" style="margin:auto;display:block;" />
>+ Started creating oneboxes solo based on Amazon and Example
  + Vyki made Wikipedia onebox and succeeded
  + JZ tried to make Flickr onebox but failed
    + Flickr images are generated w/ Javascript, so we can't use our usual way of parsing an HTML response
    + Discourse uses `parse_open_graph` function to access Flickr content
    + Realized we lacked functionality to onebox sites that support [Open Graph Protocol](http://ogp.me/)
    + Note to self: pick easier onebox to do first...
+ We need to put off gem release until we can support Open Graph Protocol sites :(
+ [Painted the bikeshed](http://bikeshed.com/) (try refreshing the page repeatedly...)
+ Attending [LA Ruby/Rails August meetup](http://www.meetup.com/laruby/events/129200762/) tomorrow
+ Got a text from [Jen](https://twitter.com/jendiamond) - we'll be presenting our onebox gem at LA Women's Ruby/Rails Group August Monthly Bash
+ HOMEWORK:
  + Look at what `parse_open_graph` function does
  + Self-assigned: listen to latest [Ruby Rogues #117](http://rubyrogues.com/117-rr-discourse-part-2-with-sam-saffron-and-robin-ward/) featuring mentors [Sam Saffron](https://twitter.com/samsaffron) and [Robin Ward](https://twitter.com/evil_trout)
  + Start creating oneboxes for sites that don't support OGP
  + Remove `html body` from Nokogiri CSS selectors in oneboxes - it's redundant. Use classes and ids instead of tags (if possible)
  + At some point, need to create a guide for making oneboxes
