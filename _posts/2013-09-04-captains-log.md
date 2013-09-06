---
layout: post
title: "Captain's Log: 2013.09.05"
location: "Los Angeles, CA"
date: "Wed, Sep 09 2013 23:35:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: dysania
---

{{ page.title }}
================
>+ Continued working on caching support
  + Continued refactoring `Preview` class
    + Refactored A LOT
    + Renamed `#record` to `#data` in `Engine` module
  + Added new specs in `spec_helper.rb`
    + Make sure oneboxes behave like engines

{% highlight ruby %}
shared_examples_for "engines" do
  it "should behave like an engine" do
    expect(described_class.private_instance_methods).to include(:data, :record, :raw)
  end

  it "should have implemented a data method" do
    expect { described_class.new(link).send(:data) }.not_to raise_error
  end
end
{% endhighlight %}

>+ In onebox specs, move fake web to global scope since our tests were using actual web pages instead of fixtures
+ Captain Kurt released v1.2.0 of his [Hexpress](https://github.com/krainboltgreene/hexpress) gem!
  + We made a new branch that requires it in onebox since we will be using that instead of Verbal Expressions to match urls
+ We realized we need to rename our onebox specs to end in `onebox_spec.rb` (instead of just `spec.rb`) to reflect the files they are testing
+ Vyki made her first [Tumblr](http://open-gov.tumblr.com/) today! [#opengov](https://twitter.com/search?q=%23opengov&src=typd)

+ HOMEWORK
  + Catch up on logs!
  + Read more about [accessors](http://www.rubyist.net/~slagell/ruby/accessors.html)
