---
title: Bloggutdrag med hjälp av Liquid
layout: post
---

Udrag ur inlägg (excerpt) är populärt i bloggar. Tyvärr har Jekyll inte stöd för detta "out of the box". Lyckligtvis finns det flera plugins som råder bot på detta. En nackdel med plugins är att om du använder GitHub Pages så tillåts inte detta. En annan nackdel med automatiserade utdrag via Liquids truncate är att det ibland blir brutna meningar på väldigt olyckliga platser.

Genom att skriva följande liquidmagi i inläggsloopen kontrollerar man själv brytpunkten för inlägget.
{% highlight html %}
{% raw %}
{{ post.content | split: '<!-- more -->' | first }}
{% endraw %}
{% endhighlight %}

Skriv en helt vanlig HTML-kommentar med "more" som innehåll i ett inlägg på den plats där du önskar att sluta utdraget.
{% highlight html %}
<!-- more -->
{% endhighlight %}