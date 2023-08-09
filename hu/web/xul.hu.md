{
  "date" : "2021-05-24",
  "keywords" :["xul", "File", "Extension", "File Format", "File Extension", "XML User Interface Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML felhasználói felület nyelvi fájl",
  "description":"További információ a XUL fájlformátumról és az API-król, amelyek XUL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Mi az a XUL fájl?

A .xul kiterjesztésű fájl ([XUL](https://wiki.mozilla.org/XUL:Home_Page) az XML felhasználói felület nyelve) egy [XML](/hu/web/xml/) alapú jelölőnyelvi fájl felhasználói felületek létrehozása. A Mozilla fejlesztette ki a fejlesztők számára, hogy a weboldalak készítéséhez használt más jelölőnyelvekhez hasonló grafikus felhasználói felületelemeket hozzanak létre. Az XUL-t a Mozilla széles körben használta a Firefox böngészőjében, ahol a Mozilla kódbázist használta. Az XUL renderelés a
[Gecko motor](https://en.wikipedia.org/wiki/Gecko_(software)). A Firefox villái, például a Pale Moon, a Basilisk és a Waterfox továbbra is támogatják az XUL-bővítményeket. A XUL-fájlokat a MIME-típus azonosítja: application/vnd.mozilla.xul+xml.

## XUL fájlformátum

A XUL fájlok egyszerű szövegben, XML fájlformátum alapján vannak megírva, és a Gecko motor segítségével jelennek meg. A XUL-struktúra három fő része a következő:

* `Tartalom` - Ez magában foglalja az ablak deklarációit és a bennük lévő felhasználói felület elemeit.
* "Skin" - Minden stíluslapot, képet és egyéb témával kapcsolatos fájlt tartalmaz. Az ablak megjelenését a stíluslapok írják le.
* `Locale` – Az ablakon belül megjelenő szöveget a rendszer külön tárolja, és több nyelvi fájlkészletet is használhatnak a felhasználók.

### XUL példa

A következő példa három gombot hoz létre, amelyek függőleges irányban egymásra helyezkednek.

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

## Hivatkozások

* [XUL – a Wikipédia által](https://en.wikipedia.org/wiki/XUL)
* [XUL archivált dokumentáció – Mozilla által](https://wiki.mozilla.org/XUL:Home_Page)

