---
layout: post
title: "Goodbye Screen, My Old Friend"
location: "Anna Maria Island, FL"
image: headers/jesus_ami.jpg
color: 880706
---

{{ page.title }}
================

Around four years ago when joining a new firm, like many devs out there I had to spend most of a day setting up my new machine. It was then that I read a post about this tool, [GNU Screen][]. It's a [terminal multiplexer][], but of course you already knew that. Well, during the days, weeks, and months that followed, Screen and I became good friends. Eventually, I even got Screen to perform [new tricks][]. But, after four years, I'm saying goodbye.

[GNU Screen]: http://www.gnu.org/software/screen/ "Gnu Screen"
[terminal multiplexer]: http://en.wikipedia.org/wiki/Terminal_multiplexer "Terminal Multiplexer"
[new tricks]: http://old.evanmeagher.net/2010/12/patching-screen-with-vertical-split-in-os "I patched it for vertical splits"

This past month I've been using [tmux][], another multiplexer that's fast gaining popularity. To be honest, at first I wasn't convinced. It was like Screen, but with added complication (Obviously I forgot the many hours I've spent tweaking my .screenrc file). But very quickly, tmux has grown on me. It's easily configured and comes with [vertical split][] and a status line out of the box. Probably the feature I like most is its predefined layouts which conveniently for me, include the layout I would always initially construct in Screen.

[tmux]: http://en.wikipedia.org/wiki/Tmux "tmux is awesome"
[vertical split]: http://fungi.yuggoth.org/vsp4s/ "Yes, I know Screen has this now - apparently"

## Sessions, Windows, & Panes

tmux works in a world of sessions, windows, & panes that are managed by the single **server**. When a tmux **client** connects to the server, a *session* is created that contains a single *window*. The window can be divided up into rectangular *panes*, each one of them a [pseudo terminal][]. It's also possible to have multiple sessions that each contain multiple windows, all under a single tmux server. 

[pseudo terminal]: http://en.wikipedia.org/wiki/Pseudo_terminal "What is a pseudo terminal?"

Usefully, a tmux client can be detached from the server, whilst the session is persisted and continues to run in the background. The session can then be reattached at some later point. A good use case for this would be to keep a long running process alive or returning to a development environment that's ready to rock.

The next steps show how I got started with tmux. Please let me know if something doesn't work for you. Better still, improve [my config][folder].

## Installation (OSX)

{% highlight bash %}
$ brew install tmux
$ tmux -V
# tmux 1.8
{% endhighlight %}

## Configuration

My up to date tmux configuration can be found within the relevant [folder][] of [my dotfiles][] (tmux uses the dotfile `.tmux.conf`). There's little value in going over lots of configuration when [tmux's man page][] covers it all. Right now, these are a few of the settings I found useful when I initially made the switch from Screen.

[folder]: https://github.com/MozMorris/dotfiles/tree/master/tmux "tmux topic folder"
[my dotfiles]: https://github.com/MozMorris/dotfiles "These are my dotfiles"
[tmux's man page]: http://www.openbsd.org/cgi-bin/man.cgi?query=tmux&sektion=1 "tmux's man page"

I tried using tmux's default prefix key mapping `ctrl-b` for a couple of days but it didn't stick. So I binded the prefix to `ctrl-a`, replicating the behaviour of Screen.

{% highlight bash %}
# ~/.tmux.conf

# Remap prefix key to Ctrl-a
unbind-key C-b
set -g prefix C-a
{% endhighlight %}

Binding `ctrl-a` to the tmux prefix key breaks "jump to start of line". Fix it (kind of) - hitting `a` again after the tmux prefix jumps to start of line:

{% highlight bash %}
# ~/.tmux.conf

# Fix jump to end of line
bind-key a send-prefix
{% endhighlight %}

Bind vertical split to `|`. Again, I've used Screen's binding. To me this makes a lot of sense as tmux uses `"` for horizontal split, placing the two split keys next to each other.

{% highlight bash %}
# ~/.tmux.conf

# Remap vertical split
unbind-key %
bind-key | split-window -h
{% endhighlight %}