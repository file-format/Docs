{
  "date" : "2021-08-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ECE File - Escenic Dynamic Web Page File Format",
  "description":"További információ az ECE fájlformátumról és az API-król, amelyek ECE fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ECE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-04"
}

## Mi az ECE fájl?

Az ECE-fájl a tartalomkezelő platform, az **Escenic Content Engine (ECE)** által dinamikusan generált weboldal. Szerveroldali kódot tartalmaz, amelyet a webszerver dolgoz fel, és [HTML](/hu/web/html/) oldalként szolgál vissza a felhasználói böngészőnek. Az ECE fájlformátum nem túl népszerű, összehasonlítva más szerveroldali fájlformátumokkal, mint például az ASP és a PHP. Ezeket a fájlokat a rendszer belsőleg rendereli, és megjelenítési célból szolgálja ki a végfelhasználóknak.

## ECE fájlformátum

Az ECE fájlokat a rendszer nem menti lemezre, hanem kérésre közvetlenül a felhasználónak szolgáltatja. Ezeket HTML-vé alakítják, és visszaküldik a felhasználó böngészőjébe megjelenítés céljából. Az Escenic Content Engine-t aktívan használják hírcikk-oldalak közzétételére. A JEE és SQL technológián alapuló ECE szerver megbízható és méretezhető tárolót biztosít minden online tartalom számára.

A kliens böngészők a HTTP/REST API-n keresztül érhetik el az ECE szerverek tartalmát. A [HTML](/hu/web/html/) oldalak kiszolgálása mellett az ECE rendkívül hatékony munkafolyamatot biztosít a video-/audiotartalom kezeléséhez és közzétételéhez.

## Hivatkozások

* [Adobe Edge](https://en.wikipedia.org/wiki/Adobe_Edge_Animate)

