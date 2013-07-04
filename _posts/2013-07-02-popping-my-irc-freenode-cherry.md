---
layout: post
title: "Popping my IRC Freenode Cherry"
location: "Los Angeles, CA"
date: "Tue, Jul 02 2013 15:39:00 -07:00"
image: headers/jesus_ami.jpg
color: 880706
author: jz
---

{{ page.title }}
================

Shout out to UForgotten of the IRC [#vagrant](http://www.vagrantup.com/) channel, who helped me **debug a problem on Freenode for the first time!**

Earlier today, I tried to run `vagrant up` again in my new Linux environment as per [Discourse as Your First Rails App](http://blog.discourse.org/2013/04/discourse-as-your-first-rails-app/), and luckily it didn't hang at the VM boot anymore. However, I kept getting this error:

{% highlight bash %}
[Default] Mounting NFS shared folders...
The following SSH command responded with a non-zero exit status.
Vagrant assumes that this means the command failed! 
{% endhighlight %}

I scrounged the Discourse docs for [NFS](http://docs-v1.vagrantup.com/v1/docs/nfs.html) errors and found the following in the [Discourse Vagrant Developer Guide](https://github.com/discourse/discourse/blob/master/docs/VAGRANT.md):

[<img src="{{ site.baseurl }}/images/discourse_nfs.png" width="100%" />]({{ site.baseurl }}/images/discourse_nfs.png)

Nope, not my errors. Google wasn't any real help either; Vagrant issues [#1659](https://github.com/mitchellh/vagrant/issues/1659), [#1694](https://github.com/mitchellh/vagrant/issues/1694), and [#1702](https://github.com/mitchellh/vagrant/issues/1702) mentioned similar errors but the solutions didn't work for me. Vyki and Kurtis weren't online to help out. [I was so totally (de)buggin'](https://www.youtube.com/watch?v=iuL2loyB1bk).

Frustrated after running `vagrant up` and `vagrant halt` over and over again with no success, I turned to the next best thing: irc.freenode.net.

I posted my problem on the #vagrant channel, and bam, UForgotten immediately responded. (The badass was actually troubleshooting for multiple IRC users at the same time.) He asked me some questions, and had me run some commands to get to the bottom of things. He thought at first it had to do with IP issues that he himself had run into recently with Vagrant, but that wasn't it. 

UForgotten eventually told me to send him my [Vagrantfile](https://github.com/discourse/discourse/blob/master/Vagrantfile) and [debugging log](http://docs.vagrantup.com/v2/debugging.html) after running this:

{% highlight bash %}
$ VAGRANT_LOG=debug vagrant up
{% endhighlight %}

I did so, and after some time, he informed me that the problem lay in this line of the log:

{% highlight bash %}
exportfs: /home/jzeta/Projects/rgsoc/discourse does not support NFS export
{% endhighlight %}

Wait a second.....I'd seen that before.......!

[<img src="{{ site.baseurl }}/images/discourse_nfs_holdup.png" width="100%" />]({{ site.baseurl }}/images/discourse_nfs_holdup.png)

**"The root Discourse directory cannot be on an ecryptfs mount or you will receive an error."** When I installed Ubuntu, I had opted to encrypt my home folder, which is where I had put Discourse. All I have to do is remove the encryption, and the Discourse environment should be able to run.

The answer had been right in front of me! Guess I just had to learn the hard way to always read the error log.

UForgotten was pretty patient with my noobiness, and said the reason why I couldn't use an encrypted folder was that NFS simply can't handle the decoding. Another IRC user, smerrill, also put in his 2 cents about how [NFS can't export symlinks](http://www.phase2technology.com/blog/vagrant-and-nfs/) either.

I thanked UForgotten for his help, and he replied, "De nada mang. Welcome to IRC. It's good karma, I need help once in a while so when I can I try to pay it forward." Cool.

Really glad my first foray into IRC Freenode went well! On to fixing the encryption thing tomorrow.

<blockquote class="twitter-tweet"><p>1st time getting help on irc freenode ---&gt; problem solved! thanks <a href="https://twitter.com/search?q=%23vagrant&amp;src=hash">#vagrant</a> channel <a href="https://twitter.com/RailsGirlsSoC">@RailsGirlsSoC</a></p>&mdash; jz (@jzeta) <a href="https://twitter.com/jzeta/statuses/352160070928306178">July 2, 2013</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>





