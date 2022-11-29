{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Channel Definition Format",
  "description" :"Läs mer om vad en CDF-fil och API:er är som kan skapa och öppna CDF-filer.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Vad är CDF fil?

En fil med filtillägget .cdf är ett XLM-baserat informationsdistributionsfilformat som användes för att publicera frekventa uppdateringar som "kanaler". Informationen publiceras från valfri webbserver och levereras automatiskt till datorer med kompatibla mottagningsprogram såsom webbläsare. Användare prenumererar på aktiva kanaler och får schemalagda uppdateringar levererade till sina skrivbord.
CDF-filer användes tidigare tillsammans med Microsofts teknologier Active Channel, Active Desktop och Smart Offline Favorites.

## CDF filformat

CDF-filer sparas som XML-filer som är ett generiskt webbfilformat för utbyte av information. CDF-filformat är ett gammalt format nu och har aldrig antagits allmänt. I jämförelse med detta var Netscapes RSS mer känd och allmänt använd.

### Exempel på CDF-filformat

Följande är ett allmänt exempel på filformatet CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domän/mapp/"
LASTMOD="1998-11-05T22:12"
PRECACHE="JA"
LEVEL="0">
<TITLE>Kanalens titel</TITLE>
<ABSTRACT>Sammanfattning av kanalens innehåll.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="JA"
LEVEL="1">
<TITLE>Sida tvås titel</TITLE>
<ABSTRACT>Sammanfattning av sidan tvås innehåll.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referenser

* [Channel Definition Format - av Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

