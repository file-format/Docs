{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extension", "file", "format", "image", "Apple Icon Image", "macOS", "Apple", "Icon" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Apple Icon Image",
  "description":"További információ az ICNS fájlformátumról és az ICNS-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az ICNS fájl? ##

A macOS-programok által használt ikonformátumot ICNS-fájlnak nevezik. Lehetővé teszi az 1 bites és a 8 bites alfa sávokat, és egy vagy több képet ment, általában [PNG](/hu/image/png/) dokumentumokból. A program ikonja a macOS böngészőben és felületen ICNS-fájlok használatával jelenik meg.

A helytől függően ugyanannak a stílusikonnak több beállítása is lehet. Az ICNS formátum számos módosításon ment keresztül, és odáig fejlődött, hogy mára különféle kompatibilis formátumok alapjaként használható. Íme néhány további fontos szempont, amit tudnia kell:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource és Mac OS icons Resource néhány egyéb elnevezés.
* Az ikoninformációkhoz az erőforrás ágban található forrást használjuk.
* A legtöbb esetben egy fájl számos képet tartalmaz. Az 1612 pixeles négyzet és az 1024, 512, 256, 128, 48, 32 és 16 pixeles négyzetes képméretek támogatottak.


## ICNS fájlformátum ##

Az ICNS adatformátum egy vagy több kép kapszula, amely támogatja az 1 bites sávokat és számos képállapotot.
Az operációs rendszer át tudja méretezni az ikonképeket, hogy azok megfeleljenek a kívánt kijelzőméretnek. A nagyobb ikonképek általában [JPEG](/hu/image/jpeg/) 2000 vagy [PNG](/hu/image/png/) fájlként kerülnek mentésre. Tömörített és tömörítetlen ICNS-fájlok egyaránt lehetségesek.

A fejléc és a bináris ikonadatok alkotják az ICNS-fájl szerkezetét. A fejléc 8 bájtnyi adatot tartalmaz, amelyek közül négy a mágikus literál, négy pedig a fájl hossza. Az egyes ikonképek típusát és méretét az ikonadatok részben tároljuk, amit a bináris képadatok követnek. A kép mérete határozza meg a bináris rész méretét.

## Műszaki specifikáció ##

### Fejléc ###

|Eltolás|Méret|Célkitűzés
---|---|---|
|0|4|Magic literal, "icns"-nek kell lennie (0x69, 0x63, 0x6e, 0x73)
|4|4|Fájl hossza, bájtban, először msb


### Ikonadatok ###

|Eltolás|Méret|Célkitűzés
---|---|---|
|0|4|Ikon típusa
|4|4|Adatok hossza bájtban (beleértve a típust és a hosszt), msb először
|8|Változó|Ikonadatok

### Tömörítés ###

A pixeladatok bizonyos mértékig tömörítve vannak. A 32 bites ("is32", "il32", "ih32", "it32") és ARGB ("ic04", "ic05") pixeleket gyakran (csatornánként) a PackBits-hez hasonló módon tömörítik.

|Lead Value|Tail Bytes|Eredmény (tömörítetlen)
---|---|---|
|0 - 127|1 - 128|1 - 128 bájt
|128 - 255|1 bájt|3 - 130 példány

## Hivatkozási szám

* [ICNS – Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

