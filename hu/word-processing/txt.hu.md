{
  "date" : "2019-10-11",
  "keywords" :[ "txt fájl", "txt fájl formátum", "mi az a txt fájl", "fájl", "txt példa", "txt fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TXT - szöveges dokumentumfájl",
  "description":"További információ a TXT fájlformátumról és az API-król, amelyek TXT fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a TXT fájl?

A .TXT kiterjesztésű fájl olyan szöveges dokumentumot jelent, amely egyszerű szöveget tartalmaz sorok formájában. A szöveges dokumentum bekezdéseit a kocsivisszaadások felismerik, és a fájltartalom jobb elrendezésére használják. A szabványos szöveges dokumentum bármely szövegszerkesztőben vagy szövegszerkesztő alkalmazásban megnyitható különböző operációs rendszereken. Az ilyen fájlokban található összes szöveg ember által olvasható formátumban van, és karakterek sorozata ábrázolja.

A szöveges fájlok nagy mennyiségű adatot tárolhatnak, mivel a tartalom méretét illetően nincs korlátozás. Az ilyen nagy fájlokat megnyitó szövegszerkesztőknek azonban okosnak kell lenniük ezek betöltéséhez és megjelenítéséhez. Szinte minden operációs rendszerhez tartozik szövegszerkesztő, amely lehetővé teszi szöveges fájlok létrehozását és szerkesztését. Például a Windows operációs rendszerhez Jegyzettömb és Wordpad tartozik erre a célra. Hasonlóképpen, a MacOS-ban is megtalálható a TextEdit a szöveges dokumentumok létrehozásához és szerkesztéséhez. Vannak azonban más ingyenes szövegszerkesztők is elérhetők az interneten, amelyek lehetővé teszik a szöveges dokumentumokkal való együttműködést, mint például a Notepad++, amely sokkal fejlettebb a funkcionalitás szempontjából.

## Fájlformátum specifikációi ##

A szöveges fájlformátumnak nincsenek speciális fájlformátum-specifikációi. A szöveges fájlok "szöveges/sima" MIME típusúak, és alig vagy egyáltalán nem formáznak. Ez lehetővé teszi a szövegszerkesztők számára az ilyen fájlok megnyitását minden egyéb követelmény nélkül. A szövegfájlok alapértelmezett karakterkészlete az ASCII, amely szöveges fájlok tartalmának létrehozására és megjelenítésére szolgál. A karakterek kódolása ASCII-karakterkészlettel történik, de ez korlátozza az olyan karakterek használatát, mint például a font jel, a dollár és az eurójel, amelyeket nem lehet ASCII-karakterkészlettel ábrázolni. Így a szöveges fájlok Unicode formátumban is menthetők, a leggyakrabban az UTF-8.

### Windows szöveges fájlformátum ###

A Windows operációs rendszer szövegfájljai több sorból állnak, ahol minden sor karaktersorozatból áll. Minden felhasználó által feltételezett sor két karakter kombinációjával van definiálva, azaz kocsivissza (CR) és Line Feed (LF). A Windows szöveges fájlok ANSI, OEM, Unicode vagy UTF-8 kódolásúak lehetnek. Az UTF-16 kódolás segít olyan szöveges fájlba menteni az információkat, amelyek megjelenítéséhez két bájt szükséges. Az ilyen fájlok általában bájtsorrend-jellel (BOM) kezdődnek, amely közli a fájltartalom végét. Meg kell jegyezni, hogy a Windows operációs rendszer más alkalmazásai szöveges fájlformátumban tárolhatnak információkat, de eltérő fájlkiterjesztésekkel, hogy az alkalmazásspecifikus szöveget ábrázolják. Például a programozási nyelvek általában szöveges fájlba mentik a kódot, de saját kiterjesztéssel.

### Unix szöveges fájlformátum ###

Minden ilyen rendszer a szöveges fájlt olyan fájlként kezeli, amelynek karakterei nulla vagy több sorba vannak rendezve. Minden sor nulla vagy több nem újsor karakterből és egy befejező újsor karakterből áll, általában LF.

## Referenciák ##

* [TXT fájlformátum](https://en.wikipedia.org/wiki/Text_file)

