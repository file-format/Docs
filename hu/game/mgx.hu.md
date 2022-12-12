{
  "date" : "2021-09-08",
  "keywords" :[ "mgx fájl", "mgx fájlformátum", "mi az mgx fájl", "fájl", "mgx példa", "mgx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tudjon meg többet az Age of Empires 2 Expansion Replay MGX fájlformátumáról és az MGX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Mi az MGX fájl?

Az .mgx kiterjesztésű fájl az Age of Empires II: The Conquerors játék rögzített fájlja, amely az Age of Empires II programon belül újrajátszható. A felhasználó által lejátszott kampány teljes felvételét tartalmazza. Az Age of Empires II programban betölthető és lejátszható. Az újrajátszás után a játék megmutatja az összes eseményt és forgatókönyvet, amelyet a felhasználó a kampányhoz tervezett és játszott.

## MGX fájlformátum - További információ

Az MGX fájl belső fájlformátumát kidolgozták, és részben hitelesített információként elérhető az [Age of Empires 2: The Conquerors – Savegame File Format Specification] (https://github.com/stefan-kolb/aoc-mgx-) oldalon. formátum). A specifikációk a következő szakaszokban ismertetik a részleteket.

### Struktúra definíciók

A GPX-fájlformátum szerkezetdefinícióiról úgy gondolják, hogy a [BinData Ruby Gem-deklarációkon] (https://github.com/dmendel/bindata/wiki) alapulnak, amelyek lehetőséget biztosítanak a strukturált bináris adatok olvasására és írására. Ez lehetővé teszi a programozó számára, hogy meghatározza a bináris adatok formátumát, amelyeket a BinData olvas és ír.

### MGX Messaging

Az MGX üzenetküldés kétféle üzeneten alapul.

* GAMESTART – a játék indítási parancsait határozza meg, és a mai napig nincs érvényesítve
* CHAT – a játékon belüli csevegési üzeneteket írja le. A játékosok és maga a játék (Gaia) is küldhet játékon belüli üzeneteket.

### JÁTÉKMŰVELETEK

Számos [GAMEPLAY-művelet] (https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) lett letöltve, és amelyek részletei elérhetők.

## Hivatkozások

* [Age of Empires 2: The Conquerors – Savegame fájlformátum specifikáció](https://github.com/stefan-kolb/aoc-mgx-format)

