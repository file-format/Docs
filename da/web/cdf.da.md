{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF - Channel Definition Format",
  "description": "Lær om, hvad en CDF-fil og API'er er, der kan oprette og åbne CDF-filer.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-daf"
}
},
  "lastmod": "2021-08-18"
}

## Hvad er CDF fil?

En fil med filtypenavnet .cdf er et XLM-baseret informationsdistributionsfilformat, der blev brugt til at udgive hyppige opdateringer som kanaler. Oplysningerne offentliggøres fra enhver webserver og leveres automatisk til computere med kompatible modtageprogrammer såsom webbrowsere. Brugere abonnerer på aktive kanaler og får planlagte opdateringer leveret til deres skrivebord.
CDF-filer blev tidligere brugt i forbindelse med Microsofts Active Channel, Active Desktop og Smart Offline Favorites-teknologier.

## CDF filformat

CDF-filer gemmes som XML-filer, der er et generisk webfilformat til udveksling af information. CDF-filformatet er et gammelt format nu og blev aldrig udbredt. I sammenligning med dette var Netscapes RSS mere berømt og meget brugt.

### Eksempel på CDF-filformat

Det følgende er et generisk eksempel på CDF-filformatet.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domæne/mappe/
LASTMOD=1998-11-05T22:12
PRECACHE=JA
LEVEL=0>
<TITLE>Kanalens titel</TITLE>
<ABSTRACT>Oversigt over kanalens indhold.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=JA
LEVEL=1>
<TITLE>Side tos titel</TITLE>
<ABSTRACT>Synopsis af side tos indhold.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## Referencer

* [Channel Definition Format - Af Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)


