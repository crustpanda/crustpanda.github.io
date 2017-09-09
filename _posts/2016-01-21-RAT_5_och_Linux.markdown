---
layout: post
title:  "RAT 5 och Linux"
date:   2016-01-21 18:05:59 +0200
tags:
    - RAT5
    - xorg
    - Linux
categories: jekyll update
---
Jag har en RAT 5, till Linux behövs lite extra konfiguration för att allt ska funka som det ska.

Skapa filen `/etc/X11/xorg.conf.d/20-cyborgrat5.conf` med följande innehåll:

{% highlight text %}
Section "InputClass"
Identifier "Mouse Remap"
MatchProduct "Mad Catz Mad Catz R.A.T.5 Mouse"
MatchDevicePath "/dev/input/event*"
Option "AccelerationProfile" "1"
Option "ConstantDeceleration" "5"
Option "ButtonMapping" "1 2 3 4 5 6 7 8 9 10 11 12 0 0 0"
Option "ZAxisMapping" "4 5 6 7"
EndSection
{% endhighlight %}

Glöm inte att logga ut för att förändringarna ska appliceras. 