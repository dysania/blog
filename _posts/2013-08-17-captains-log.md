---
layout: post
title: "Captain's Log: 2013.08.17"
location: "Los Angeles, CA"
date: "Sat, Aug 17 2013 17:01:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

<img src="{{ site.baseurl }}/images/library.jpg" width="100%" />

>+ 1st meeting during the weekend!
+ Chilled at the [Los Angeles Grand Central Library](http://www.lapl.org/branches/central-library), walked around DTLA a bit
+ Renamed all onebox engines and specs to end with `_onebox`/`Onebox`
  + We want to pass an array of all the oneboxes, but without including the `OpenGraph` module
  + We'll be searching for the onebox engines/specs based on their suffixes
  + Renamed throughout the project
+ Created `OpenGraph` module
  + Includes `Engine` module
  + To be used for sites that support Open Graph Protocol
    + It's standardized and easier to parse
    + Don't have to deal with OGP sites that generate content using Javascript (like Flickr)
    + Lots of supporting sites, so won't have to create as many explicit engines and specs
  + Learned how to namespace from root (ex. `::OpenGraph.new(@url)`)
+ Created Flickr engine and specs to start using `OpenGraph` module
+ Captain Kurt drafted a format for our presentation, to be called "Pulling a Gem Out of your App"
  + We'll highlight 5 lessons we've learned since starting work on onebox gem
+ HOMEWORK:
  + Read article from [Heart, Mind Code](http://www.heartmindcode.com/blog/2013/08/loyalty-and-layoffs/) by [David Brady](https://twitter.com/dbrady)
  + Keep working on presentation
