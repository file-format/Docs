{
  "date" : "2021-05-24",
  "keywords" :["xul", "Fil", "Tillägg", "Filformat", "Filtillägg", "XML-användargränssnittsspråk"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML User Interface Language File",
  "description":"Läs mer om XUL-filformat och API:er som kan skapa och öppna XUL-filer.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Vad är en XUL fil?

En fil med filtillägget .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) står för XML User Interface Language) är en [XML](/sv/web/xml/)-baserad märkningsspråkfil för skapa användargränssnitt. Det utvecklades av Mozilla för utvecklare för att skapa grafiska användargränssnittselement som liknar andra märkningsspråk som används för att skapa webbsidor. XUL har använts flitigt av Mozilla i sin webbläsare Firefox där den använde Mozilla-kodbasen. XUL-rendering utförs med hjälp av
[Gecko-motor](https://en.wikipedia.org/wiki/Gecko_(software)). Firefox-gafflar som Pale Moon, Basilisk och Waterfox behåller stöd för XUL-tillägg. XUL-filer identifieras med MIME-typ: application/vnd.mozilla.xul+xml.

## XUL filformat

XUL-filer skrivs i vanlig text baserat på XML-filformat och renderas med Gecko-motorn. De tre huvuddelarna i en XUL-struktur är:

* `Innehåll` - Detta inkluderar deklarationerna för fönstret och användargränssnittselementen som finns i dem.
* `Skin` - Den innehåller alla stilmallar, bilder och andra temarelaterade filer. Utseendet på ett fönster beskrivs i stilmallarna.
* `Lokal` - Text som visas i ett fönster lagras separat och flera uppsättningar språkfiler kan användas av användare.

### XUL Exempel

Följande exempel skapar tre knappar som staplas ovanpå varandra i vertikal riktning.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referenser

* [XUL - av Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [XUL Archived Documentation - By Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

