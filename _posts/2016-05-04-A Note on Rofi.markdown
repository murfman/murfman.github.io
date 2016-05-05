---
layout: single
type: posts
read_time: true
author_profile: true
title:  "A Note About Rofi"
date:   2016-05-04 16:43:20 -0500
categories: update
---

This is a note more to myself than anything.

 So I was applying this setup on a Linux Mint system and ran into some issues particularly with getting rofi to display color configurations when including the -bg and -fg flags inline. For example:

{% highlight shell %}
rofi -show run -bw 4 -eh 1 -lines 8 -color-enabled -bg "#002b36" -fg "#00b1de" -opacity "80" -line-margin 4 -font "Inconsolata 15"
{% endhighlight %}

It turns out that the -color-enabled flag is not needed, and in fact breaks the damn thing in this instance. Removing it lets the -bg and -fg tags work perfectly.

On a separate, but not unrelated, note remember to load the new .Xresources file if you do change it to include rofi defaults.

{% highlight shell %}
xrdb -load ~/.Xresources
{% endhighlight %}
