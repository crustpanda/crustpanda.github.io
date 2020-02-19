---
layout: post
title:  "Firefox, bspwm och högerklick (igen)"
date:   2020-02-19 22:38:00 +0200
tags:
    - bspwm
    - firefox
categories: jekyll update
---

Första inlägget på ett par år nu. Jag ändrade dock designen nyligen och jobbar lite i det dolda, som synes. Jag använder liksom [tidigare]({% post_url 2017-10-09-Firefox_context %}) bspwm samt Firefox och denna post kommer handla om problemet jag tidigare hade och som löstes med några rader CSS.


# Ny lösning på problemet

Skriv följande i Firefox URL-bar:
`about:config`

Sök sedan efter `ui.context_menus.after_mouseup` och ändra dess värde till `true` och starta om Firefox.

Glöm inte att ta bort CSS-lösningen. Det räcker med en lösning på detta problem. Igenom att kommentera den relevanta delen har du kvar koden om du av någon anledning skulle vilja använda den istället.

{% highlight css %}
/*#contentAreaContextMenu {
margin: 10px 0 0 5px 
}
*/
{% endhighlight %}


Förhoppningsvis ska det inte dröja lika många år innan mitt nästa inläggen dyker upp på bloggen.






