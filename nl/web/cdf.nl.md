{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Kanaaldefinitieformaat",
  "description" :"Meer informatie over wat een CDF-bestand is en API's die CDF-bestanden kunnen maken en openen.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Wat is een CDF-bestand?

Een bestand met de extensie .cdf is een op XLM gebaseerd informatiedistributiebestandsformaat dat werd gebruikt om frequente updates als "kanalen" te publiceren. De informatie wordt gepubliceerd vanaf elke webserver en wordt automatisch geleverd aan computers met compatibele ontvangstprogramma's zoals webbrowsers. Gebruikers abonneren zich op actieve kanalen en krijgen geplande updates op hun desktop.
CDF-bestanden werden eerder gebruikt in combinatie met de Active Channel-, Active Desktop- en Smart Offline Favorites-technologieën van Microsoft.

## CDF-bestandsindeling

CDF-bestanden worden opgeslagen als XML-bestanden, een generiek webbestandsformaat voor het uitwisselen van informatie. Het CDF-bestandsformaat is nu een oud formaat en werd nooit algemeen aanvaard. In vergelijking hiermee was de RSS van Netscape bekender en werd deze veel gebruikt.

### Voorbeeld van CDF-bestandsindeling

Het volgende is een algemeen voorbeeld van het CDF-bestandsformaat.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domein/map/"
LASTMOD="1998-11-05T22:12"
PRECACHE="JA"
NIVEAU="0">
<TITLE>Titel van kanaal</TITLE>
<ABSTRACT>Synopsis van de inhoud van het kanaal.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="JA"
NIVEAU="1">
<TITLE>Titel van pagina twee</TITLE>
<ABSTRACT>Synopsis van de inhoud van Page Two.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referenties

* [Indeling kanaaldefinitie - door Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

