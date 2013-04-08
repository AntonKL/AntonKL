---
title: Jekyll som bagare för bloggen
layout: post
---

Att välja plattform för min personliga sajt var inget lätt val. Bloggverktyg såsom WP kan vara smidiga med sin webbaserade hantering. Samtidigt är de otroligt överlastade för den enkla uppgift en simpel blogg har. En annan otrevlig faktor är den brist på kontroll som WYSIWYG ger. Som utvecklare var den en avgörande punkt att kunna arbeta med innehållet på ett sätt som jag var van vid. Det var även ett önskemål att slippa databaser och den extra komplexitet detta innebär.
<!-- more -->
Valet föll slutligen på det Rubybaserade verktyget Jekyll som kunde leverera flera starka fördelar:

*   Statiskt verkyg vilket ger möjlighet att driva sajten från AWS S3 eller GitHub Pages.
*   Aktiv utveckling och god dokumentation.
*   Öppen källkod.
*   Stödjer Markdown eller HTML för blogginlägg. Detta ger flexibiliteten från HTML kombinerat med hastigheten av Markdown för enkla textbaserade inlägg.
*   Använder Liquid för logiska satser.
*   Enkelt att implementera optimeringar.
*   God tillgång på plugins för allehanda uppgifter.

## Flödet i tre enkla steg:

1.  Ett nytt inlägg skapas i Markdown eller HTML. I början av dokumentet defineras META-taggar och titel för sidan med hjälp av YAML.
2.  Med hjälp av Jekyll bakas sajten ihop till färdiga statiska filer som redo att publiceras.
3.  Innehållet i _site kan publiceras via valfritt system till en server. FTP, Git eller [Dystatic](http://github.com/AlexanderEkdahl/dystatic "Dystatic").