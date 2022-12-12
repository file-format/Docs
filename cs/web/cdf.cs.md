{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF – formát definice kanálu",
  "description" :"Zjistěte, co je soubor CDF a rozhraní API, která mohou vytvářet a otevírat soubory CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Co je soubor CDF?

Soubor s příponou .cdf je formát souboru distribuce informací založený na XLM, který se používal k publikování častých aktualizací jako „kanály“. Informace jsou publikovány z libovolného webového serveru a jsou automaticky dodávány do počítačů s kompatibilními přijímacími programy, jako jsou webové prohlížeče. Uživatelé se přihlásí k odběru aktivních kanálů a mají naplánované aktualizace doručovány na jejich plochu.
Soubory CDF byly dříve používány ve spojení s technologiemi Microsoft Active Channel, Active Desktop a Smart Offline Favorites.

## Formát souboru CDF

Soubory CDF se ukládají jako soubory XML, což je obecný formát webových souborů pro výměnu informací. Formát souboru CDF je nyní starý formát a nikdy nebyl široce přijat. Ve srovnání s tím bylo RSS Netscape známější a široce používané.

### Příklad formátu souboru CDF

Následuje obecný příklad formátu souboru CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://doména/složka/"
LASTMOD="1998-11-05T22:12"
PRECACHE="ANO"
LEVEL="0">
<TITLE>Název kanálu</TITLE>
<ABSTRACT>Synopse obsahu kanálu.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="ANO"
LEVEL="1">
<TITLE>Název druhé strany</TITLE>
<ABSTRACT>Synopse obsahu druhé strany.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Reference

* [Formát definice kanálu – podle Wikipedie](https://en.wikipedia.org/wiki/Channel_Definition_Format)

