{
  "date" : "2021-02-26",
  "keywords" :[ "SXC", "file", "extension", "file format", "Sun XML Calc", "Spreadsheet" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az SXC fájlformátumról és az API-król, amelyek SXC fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"SXC fájlformátum",
  "linktitle" : "SXC",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-02-26"
}

## Mi az SXC fájl? ##

Az SXC (Sun XML Calc) fájlformátum az OpenOffice.org nevű irodai programcsomaghoz tartozik. Ez a formátum általában a felhasználók táblázatkezelési igényeit elégíti ki, mivel ez egy XML alapú táblázatkezelő fájlformátum. Az SXC formátum a képleteket, függvényeket, makrókat és diagramokat támogatja a DataPilot mellett, ami hihetetlen funkció, mert automatikusan személyre szabja és összefoglalja a nyers importált adatokat. Az ezzel a szoftverrel létrehozott fájlok .sxc kiterjesztéssel kerülnek mentésre.


## SXC fájlformátum ##

A .sxc kiterjesztésű fájlok a Microsoft Excel programcsomaggal nyithatók meg, amely egy Microsoft Office programcsomag táblázatkezelő szoftvere. Vannak más szoftverek is, amelyek .sxc kiterjesztésű fájlokat nyithatnak meg, például Libre Office, StarOffice stb.

Ennek a formátumnak a tartalomtípusai a következők:

* application/vnd.sun.xml.calc
* application/vnd.sun.xml.calc.template

## Fájlkompatibilitás ##

Az SXC fájlok kompatibilisek az Apache Open Office calc programmal, és az adatok exportálhatók Microsoft Excel fájlba és más formátumokba is.

## Fájlkezelés ##

Az ImportMatrix és ExportMatrix parancsok képesek olvasni és írni az SXC fájlt. Ha a forrás egy SXC-fájl, és a cél is egy SXC-fájl, akkor a **f** Sun XML Calc-táblázatfájlnak minősül. A mátrix importálása és exportálása egyaránt támogatja ezt a formátumot, amelyet a rendszer automatikusan észlel, ha a formátum nincs megadva, és a fájlnév .sxc-re végződik.

Az SXC fájl megnyitásához egy megfelelő programot kell társítani a fájlhoz. Amikor egy .sxc kiterjesztésű fájlt kell megnyitni, győződjön meg arról, hogy hibamentes és nem sérült. A fájl bármely hibája könnyen kezelhető a felhasználó által, és ez a legtöbb esetben nem igényel technikai támogatást.


## Referenciák ##

* [StarOffice – a Wikipedia által](https://en.wikipedia.org/wiki/StarOffice)

