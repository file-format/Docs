{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Kanaldefinitionsformat",
  "description" :"Erfahren Sie, was eine CDF-Datei und APIs sind, die CDF-Dateien erstellen und öffnen können.",
  "linktitle" :"CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Was ist eine CDF-Datei?

Eine Datei mit der Erweiterung .cdf ist ein XLM-basiertes Informationsverteilungsdateiformat, das verwendet wurde, um häufige Updates als "Kanäle" zu veröffentlichen. Die Informationen werden von jedem Webserver veröffentlicht und automatisch an Computer mit kompatiblen Empfangsprogrammen wie Webbrowsern geliefert. Benutzer abonnieren aktive Kanäle und bekommen geplante Updates auf ihren Desktop geliefert.
CDF-Dateien wurden früher in Verbindung mit den Microsoft-Technologien Active Channel, Active Desktop und Smart Offline Favorites verwendet.

## CDF-Dateiformat

CDF-Dateien werden als XML-Dateien gespeichert, bei denen es sich um ein generisches Webdateiformat für den Informationsaustausch handelt. Das CDF-Dateiformat ist jetzt ein altes Format und wurde nie weit verbreitet. Im Vergleich dazu war RSS von Netscape bekannter und weit verbreiteter.

### Beispiel für ein CDF-Dateiformat

Das Folgende ist ein allgemeines Beispiel für das CDF-Dateiformat.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://Domäne/Ordner/"
LASTMOD="1998-11-05T22:12"
PRECACHE="JA"
LEVEL="0">
<TITLE>Titel des Kanals</TITLE>
<ABSTRACT>Zusammenfassung der Inhalte des Kanals.</ABSTRACT>
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
<TITLE>Der Titel von Seite zwei</TITLE>
<ABSTRACT>Zusammenfassung des Inhalts von Seite Zwei.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Verweise

* [Kanaldefinitionsformat – von Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

