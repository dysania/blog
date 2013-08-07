---
layout: post
title: "Captain's Log: 2013.08.06"
location: "Los Angeles, CA"
date: "Tue, Aug 06 2013 23:05:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================


>+ Major gem changes/cleanup in prep for 1.0 release
	+ Renamed gem from `discourse-oneboxer` to `onebox`
	+ Renamespaced `Discourse::Oneboxer` to `Onebox`
	+ Deleted all the files we didn't originally write
+ Note to selves
	+ Don't use `git rm .` unless you want to delete your entire directory
	+ Make sure you're in the correct Git branch ALWAYS
	+ Refresh your Sublime project once in a while...your files might not be missing after all. Don't panic!
	+ Captain Kurt - where's our pizza??
+ [First pull request from an outside contributor!](https://github.com/dysania/onebox/pull/28) Shout out to [Mark IJbema](https://github.com/markijbema)
+ It seems we have a bit of an audience
[<img src="{{ site.baseurl }}/images/onebox_audience.png" width="100%" style="margin:20px 0 20px 0;"/>](https://github.com/dysania/onebox)
+ HOMEWORK:
	+ Update remotes to point to the right repository
	+ Update [dysania/onebox README](https://github.com/dysania/onebox/blob/master/README.md)
		+ extra credit: provide example using onebox
	+ For all services (Coveralls, Travis, Code Climate) - update to point to right repository
	+ Update [`dysania/discourse`](https://github.com/dysania/discourse) from upstream
	+ Clean up branches
		+ `git branch --merged`: all branches merged w/ current branch
		+ `git branch -D [branch-name]`: delete local branch
	+ If there's time, do as many oneboxes as you can
	+ Read about semantic versioning - [semver.org](http://semver.org)
	+ Learn about bike shedding in programming context
	+ Introduce ourselves on meta.discourse