---
layout: post
title:  "Firefox kontextmeny och direkt vänsterklick"
date:   2017-10-09 18:05:59 +0200
tags:
    - bspwm
    - firefox
    - css
categories: jekyll update
---

Under en tid har jag testat [Budgie](https://budgie-desktop.org/home/) i kombination med Gala från elementary OS. Det har fungerat utmärkt ända tills den senaste versionen utav GNOME kom in Arch stabila förråd. Att stänga ner program i fullskärm gjorde att systemet kraschade, ett [välkänt](https://bbs.archlinux.org/viewtopic.php?id=230619) problem. Jag försökte kompilera Gala gentemot nya Mutter men det ändrade ingenting. Jag behövde ett fungerande system och installerade bspwm igen, en klassiker för mig och en tiling manager jag känner mig bekväm med.

En sak jag märkte per omgående var att när jag använde Firefox och högerklickade någonstans registrerades först mitt högerklick, men också ett direkt vänsterklick. Hade jag precis besökt en sida och högerklickade någonstans gick jag alltså tillbaka (såvida jag inte höll knappen intryckt och förflyttade mig något) Högerklickade jag på en länk öppnades länken i en ny flik direkt och så vidare. Det kan vara farligt om jag exempelvis gör ett bankärende och sedan går tillbaka till föregående sida utan att det var min mening.

![](/images/firefox-wrong.png)

Med bspwm tillkom även ett par program som inte användes tillsammans med min gamla setup. Dunst, sxhkd och Compton är några exempel. Någon som använder Compton har haft [problemet](https://github.com/chjj/compton/issues/207), jag testade att stänga av Compton men det hjälpte inte. Jag gick även igenom inställningarna för bspwm samt sxhkd utan att komma vidare. Efter lite sökande hittade jag dock något som åtgärdade problemet för mig. Det Du vill göra är att skapa eller modifiera `userChrome.css` med följande:

{% highlight css %}
#contentAreaContextMenu{ margin: 10px 0 0 10px }
{% endhighlight %}

Spara, starta om Firefox och slutresultatet blir följande:

![](/images/firefox-right.png)

