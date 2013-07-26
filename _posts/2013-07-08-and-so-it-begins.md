---
layout: post
title: "And So It Begins"
location: "Los Angeles, CA"
date: "Mon, Jul 08 2013 00:59:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: vyki
---

{{ page.title }}
================
Tonight was the first night all three of us ([Vyki](http://twitter.com/toastergrrl), [JZ](http://twitter.com/jzeta), and [Kurtis](https://twitter.com/krainboltgreene)) got to work in the same room together!  Though I'm still getting all of my [tools](http://railsgirlssummerofcode.org/tools/) installed and set up, and despite my kernel headers problem with VirtualBox, we dove right in.

We started off with lectures on [semantic versioning](http://en.wikipedia.org/wiki/Software_versioning#Semantic_versioning) and best practices for Ruby gems. We then officially forked [Discourse](https://github.com/discourse/discourse) to our [GitHub](https://github.com/dysania). 

In 3 short hours we managed to:
>+ learn about [oneboxing](http://meta.discourse.org/t/what-is-a-onebox/4546)
+ create a [discourse-oneboxer](https://github.com/dysania/discourse-oneboxer) repo for the gem we're building
+ generate a new gem using Bundler
+ start pulling in oneboxer files from the Discourse lib to discourse-oneboxer
+ start properly namespacing the files in discourse-oneboxer

Now off to finish our homework! Mine is to finish the namespacing in discourse-oneboxer, and JZ's is to finish transfering all the oneboxer files to discourse-oneboxer.






