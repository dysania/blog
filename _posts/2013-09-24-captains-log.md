---
layout: post
title: "Captain's Log: 2013.09.24"
location: "Los Angeles, CA"
date: "Tue, Sep 24 2013 23:25:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Vyki finished up and merged `setting-up-hexpress` branch
+ JZ worked on issue [#61](https://github.com/dysania/onebox/issues/61)
  + We want to reduce the duplicated parts of each template by having a shared layout view
  + Created new branch [`adding-shared-layout-view`](https://github.com/dysania/onebox/pull/140)
  + Created new `Layout` class (which inherits from `Mustache`) to handle template rendering, instead of `Engine` module
  + Onebox engine templates will be rendered as partials within the default `_layout.handlebars`
+ Discussed how to implement [Imgur onebox](https://github.com/dysania/onebox/pull/107)
  + We'll need to make 2, one for albums and one for galleries
  + [@markijbema](https://github.com/markijbema) is back! He opened up some discussion regarding XSS issues we might not have addressed yet
+ Discussed how to implement exceptional onebox engines (Video, Audio, etc.)
  + They'll be similar to HTML/JSON/OpenGraph modules in that they will be included in other oneboxes (e.g. `include Video`)
+ Learned more about [Mustache](https://github.com/defunkt/mustache) and [Handlebars](http://handlebarsjs.com/)
+ Sent out invites for our [Rooftop Ruby](https://rooftop-ruby.eventbrite.com/) event on October 5 in Little Tokyo
  + If you're in LA and would like to attend, let us know and we'll send you an invite!
+ 84 STARS!
+ HOMEWORK: Keep on making oneboxes for v1.1.0...again


