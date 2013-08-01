---
layout: post
title: "Captain's Log: 2013.07.31"
location: "Los Angeles, CA"
date: "Wed, Jul 31 2013 21:46:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================

>+ Still working on `preview-refactor` branch
+ TDD:
	+ JZ: making tests pass
	+ Vyki: created tests that failed
+ Added `amazon` spec
+ Created fixtures for `amazon` and `example`
+ Made `preview` and `amazon` specs pass
+ Learned how to get contents of url in bash using curl
	+ `curl --output spec/fixtures/amazon.response -L -X GET http://amzn.com/193609620X`
	+ how we will create fixtures for all oneboxes
+ Vyki bought [The Well-Grounded Rubyist](http://www.google.com/url?q=http%3A%2F%2Fwww.amazon.com%2Fgp%2Fproduct%2F1933988657%2Fref%3Doh_details_o00_s00_i03%3Fie%3DUTF8%26psc%3D1&sa=D&sntz=1&usg=AFQjCNEzcqRfz_hCoFeKTom7WuLvoKpPiw) from [Lili's](https://www.google.com/url?q=https%3A%2F%2Ftwitter.com%2Flkoponen&sa=D&sntz=1&usg=AFQjCNFJr2dNbYKMSlaaet5DZEAB1E2QHQ) recommendation
+ JZ didn't die from Day 2 of bike commuting and was reunited with her lost keys
+ Gave status update to our RGSoC supervisor [Benedikt](https://twitter.com/benediktdeicke)
+ Sent in our introduction blog post to RGSoC organizers for review -- to be published Monday!
+ HOMEWORK (Vyki): Clean up Amazon response (remove CSS and whitespace) 
+ HOMEWORK (JZ): Create fixture for `example`, pick another onebox to refactor and capture response for it