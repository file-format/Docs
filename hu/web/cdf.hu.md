{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF – csatornadefiníciós formátum",
  "description" :"További információ arról, hogy mi az a CDF-fájl és az API-k, amelyek CDF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Mi az a CDF fájl?

A .cdf kiterjesztésű fájl egy XLM-alapú információterjesztési fájlformátum, amelyet a gyakori frissítések "csatornaként" való közzétételére használtak. Az információkat bármely webszerverről közzéteszik, és automatikusan eljuttatják kompatibilis fogadó programokkal, például webböngészőkkel rendelkező számítógépekre. A felhasználók feliratkoznak az aktív csatornákra, és az ütemezett frissítéseket az asztalukra szállítják.
A CDF fájlokat korábban a Microsoft Active Channel, Active Desktop és Smart Offline Favorites technológiáival együtt használták.

## CDF fájl formátum

A CDF-fájlok XML-fájlként kerülnek mentésre, amely egy általános webes fájlformátum az információcseréhez. A CDF fájlformátum egy régi formátum, amelyet soha nem alkalmaztak széles körben. Ehhez képest a Netscape RSS-je híresebb és szélesebb körben használt.

### Példa CDF fájlformátumra

A következő egy általános példa a CDF fájlformátumra.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domain/mappa/"
LASTMOD="1998-11-05T22:12"
PRECACHE="IGEN"
LEVEL="0">
<TITLE>Csatorna címe</TITLE>
<ABSTRACT>A csatorna tartalmának áttekintése.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="IGEN"
LEVEL="1">
<TITLE>A második oldal címe</TITLE>
<ABSTRACT>A második oldal tartalmának összefoglalása.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Hivatkozások

* [Csatornadefiníciós formátum – Wikipédia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

