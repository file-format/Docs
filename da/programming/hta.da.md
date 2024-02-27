{
  "date": "2021-09-16",
  "keywords": [
"hta",
"fil",
"udvidelse",
"filformat",
"hta implementering",
"Programmeringsvejledning",
"hta eksempel",
"HTML-applikation",
"Hypertext Markup Language Application",
"HTA filer",
"Microsoft HTML-applikation"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "HTA - HTML-applikationsfiler",
  "description": "Lær om HTA filformat og API'er, der kan oprette og åbne HTA filer.",
  "linktitle": "HTA",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ht-daa"
}
},
  "lastmod": "2021-09-16"
}

## Hvad er en HTA fil?

HTMLA står for **Hypertext Markup Language Application** er et program, der er kompatibelt med Microsoft Windows. Kildekoden til dette program indeholder mere end ét scriptsprog såsom [HTML](/web/html/) og [JavaScript](/web/js/). Til brugergrænsefladen foretrækkes en HTML-applikation, mens der bruges ethvert andet scriptsprog for at opfylde kravet om programlogik.

En HTML-applikation er uafhængig af internetbrowserens sikkerhedsmodel og kører som et fuldt betroet program. Udvidelsen, der bruges til filer vedrørende disse applikationer, er HTA. Disse applikationer inkluderer funktioner i HTML sammen med egenskaberne for andre scriptsprog.


## Kort historie ##

The HTA was first introduced in 1999 by Microsoft along with the release of Internet Explorer 5. Det var kompatibelt med Internet Explorer og kunne derfor kun udføres på Windows-operativsystemet. Denne teknologi blev patenteret i 2003. HTA-filerne udføres på samme måde som alle andre .exe-filer. HTA-filerne er også kompatible med dagens opdaterede version af Windows 11.


## Teknisk specifikation ##

MTV'er har det samme format som enhver anden HTML-side består af, mens nogle attributter bruges til at kontrollere stilarter af grænser eller ikoner for programmer. Desuden fremføres argumenter for lanceringen af MTV. Disse applikationer kan udføres ved hjælp af et program ved navn mshta.exe. Den kan tilgås ved blot at dobbeltklikke på filen. Disse programmer kører automatisk sammen med Internet Explorer. Udover andre specifikationer er disse ikke uafhængige af Trident-motorbrowseren, men er uafhængige af Internet Explorer. Det betyder, at disse kan udføres uden brug af Internet Explorer.

Mærkerne bruges til at tilpasse udseendet af disse applikationer. Konverteringen fra Microsoft HTML-applikation til HTA-format er lettere, dvs. du behøver kun at ændre udvidelsen. Da vi ved, at disse applikationer har fuld tillid til, omfatter disse flere funktioner og fordele sammenlignet med simple HTML-filer. Teksteditorer kan bruges til at oprette HTA. Disse editorer kan erhverves af Microsoft eller enhver anden betroet kilde.


## HTA filformat eksempel ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Reference ##

* [HTA - af Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)




