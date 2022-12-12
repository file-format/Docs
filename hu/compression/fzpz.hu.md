{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ fájlformátum - Fritzing részfájl",
  "description":"További információ arról, hogy mi az FZPZ fájl és az API-k, amelyek FZPZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Mi az FZPZ fájl?

Az FZPZ fájl a **Fritzing** áramköri prototípus- és tervezőalkalmazással létrehozott elektronikus áramkör-tervezésben használt alkatrész/alkatrész. Ez egy tömörített archívum, amely egy [FZP](/hu/cad/fzp/) fájlt és négy [SVG](/hu/image/svg/) képet tartalmaz, amelyek leírják a Fritzing teljes részét. E fájlok használatának előnye, hogy a felhasználók megoszthatják FZPZ fájljaikat mindegyikkel az újrafelhasználhatóság szempontjából. Az FZPZ-alkatrészek megosztása segít az áramköri alkatrészek integrálásában a nagyobb PCB-tervek gyors létrehozásához.

## FZPZ fájlformátum - További információ

Az FZPZ fájlokat a rendszer tömörített [ZIP](/hu/compression/zip/) archívumként menti a lemezre. A kiterjesztést átnevezheti .fzpz-ről .zip-re, és bármilyen szabványos kitömörítő segédprogrammal, például WinZIP-pel kibonthatja a fájlokat az archívumból.

### FZPZ fájlszerkezeti információ

Amint már említettük, az FZPZ fájl olyan archív fájl, amely többszörös fájlt tartalmaz a nyomtatott áramköri lapon használt alkatrész ábrázolására. Az FZPZ a következő fájlokat tartalmazza:

* "Négy SVG-fájl" - amelyek az alkatrész kenyértábláját, kapcsolási rajzát, PCB-jét és ikonképeit képviselik
* `FZP fájl` - XML fájl, amely információkat tartalmaz az alkatrész tulajdonságairól, csatlakozóiról és buszairól

A fájlok elnevezése általában a következő.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Hivatkozások ##

* [Új alkatrészek fzpz kiterjesztéssel](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

